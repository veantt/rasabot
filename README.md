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

Starts a server with your trained model
$ rasa run

Generates a visual representation of your stories
$ rasa visualize
 

Start server
https://rasa.com/docs/rasa/user-guide/running-the-server/

# Start server + Fix No 'Access-Control-Allow-Origin'
$ rasa run -m models --enable-api --log-file out.log -p 5002 --cors "*"
$ rasa run -m models --enable-api --log-file out.log -p 5002 --cors "*" --debug

Staging server
Prod$ rasa run -m models --enable-api --log-file out.log -p 5002 --cors "http://206.189.46.29"

$ rasa run -m models --enable-api --log-file out.log -p 5002
Starting Rasa server on http://localhost:5002

Specific endpoints
$ rasa run -m models --enable-api --log-file out.log -p 5002 --endpoints endpoints.yml





## webhook

curl -XPOST localhost:5002/webhooks/rest/webhook -d '{"sender":"Me","message":"how are you?"}'

curl -XPOST localhost:5002/webhooks/rest/webhook \
-d '{"sender":"Me","message":"how are you?"}' \
-H "Content-type: application/json"

curl -XPOST localhost:5002/webhooks/rest/webhook -d '{"sender":"Me","message":"/i_want_more_game_hcl_info"}'

curl -XPOST http://206.189.37.110:5002/webhooks/rest/webhook -d '{"sender":"Me","message":"/i_want_more_game_hcl_info"}'

curl -XPOST 206.189.37.110:5002/webhooks/rest/webhook -d '{"sender":"Me","message":"how are you?"}'

## Front-end
https://rasa.com/docs/rasa/user-guide/connectors/your-own-website/
https://github.com/botfront/rasa-webchat
