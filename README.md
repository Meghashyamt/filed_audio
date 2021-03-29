# filed_audio

tup the system

Setup codebase

clone the code in a directory

 git clone https://github.com/meghashyamt/filed_audio.git
go in the directory cd filed_audio_file_server

install all project requirements, use command python -m pipenv install -r requirements.txt

go in pipenv virtualenv by python -m pipenv shell

set up flask env variable, run commands

export FLASK_APP=main.py
export FLASK_ENV=developement
create database

in postgresql create database "audioserver" and grant permission to user, in postgresql shell run command .

1. create db audioserver;
2. GRANT ALL PRIVILEGES ON DATABASE audioserver to "prashant"; # my username
create the table in audioserver database

in .env file add the data as below

# example
# DATABASE_URL="postgresql://prashant:rana@localhost:5432/audioserver"
DATABASE_URL="postgresql://<username>:<password>@<server host>:<port>/<database name>
SECRET_KEY="this-is-a-sample-secret-key"
FLASK_ENV="development"
SQLALCHEMY_TRACK_MODIFICATIONS=True
lets do migrations, run following commands

flask db init
flask db migrate
flask db upgrade
this will create a migration folder, and create table in the database

run app, activate envrionment pipenv shell and run the command to run server flask run

check if server is running, in browser go to localhost:5000/, you will get server is running msg.
