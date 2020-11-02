 requires Microsoft Visual C++ Redistributable
py -m venv chatbotenv python==3.7.6
.\chatbotenv\Scripts\activate
pip install ujson==2.0.3
pip install tensorflow==2.1.0
pip install rasa==1.10.0
rasa init

Deploying to local server
socketio:
 user_message_evt: user_uttered
 bot_message_evt: bot_uttered
 session_persistence: true

rasa run --cors "+" --debug #running chatbot
rasa run -m models --enable-api --cors "*" --debug  
#running chatbot along with enabling api

#speech recog module
pip install PyAudio-0.2.11-cp37-cp37m-win_amd64.whl

#google translator
pip install gtts
sudo apt-get install mpg321

rasa run -m  models --endpoints endpoints.yml --port 5002 --credentials credentials.yml
rasa run actions

pip install yamllint
pip install rasa-core-sdk
python -m rasa_core_sdk.endpoint --actions action