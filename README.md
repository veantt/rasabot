# rasabot
Test Rasa bot

# Getting started
Activate the virtual environment:

$ cd project/rasabot/
$ source venv/bin/activate

Verify Python environment
$ python --version
$ pip --version

Init training
$ rasa init --no-prompt

NLU training data
$ cat data/nlu.md

Train a Model
$ rasa train

Talk
$ rasa shell
$ rasa shell --debug

Start server
https://rasa.com/docs/rasa/user-guide/running-the-server/

$ rasa run -m models --enable-api --log-file out.log -p 5002
Starting Rasa server on http://localhost:5002

Specific endpoints
$ rasa run -m models --enable-api --log-file out.log -p 5002 --endpoints endpoints.yml

Start server + Fix No 'Access-Control-Allow-Origin'
$ rasa run -m models --enable-api --log-file out.log -p 5002 --cors "*"
$ rasa run -m models --enable-api --log-file out.log -p 5002 --cors "*" --debug



webhook

curl -XPOST localhost:5005/webhooks/rest/webhook -d '{"sender":"Me","message":"how are you?"}'

curl -XPOST localhost:5005/webhooks/rest/webhook \
-d '{"sender":"Me","message":"how are you?"}' \
-H "Content-type: application/json"
