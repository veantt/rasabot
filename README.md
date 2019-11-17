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

curl -XPOST localhost:5002/parse -d '{"q":"I am looking for Chinese food"}

curl -XPOST http://localhost:5002/webhooks/myio/webhook \
-d '{"sender": "user1", "message": "hello"}' \
-H "Content-type: application/json"
