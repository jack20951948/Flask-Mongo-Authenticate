## A Flask Authentication Boilerplate.

#### _Blueprints + React + Typescript + MongoDB_

_spawned from_ [_Luke Peters work here_](https://github.com/LukePeters/flask-mongo-api-boilerplate)

#### _Setup:_

```
# clone:
git clone https://github.com/Jesssullivan/Flask-Mongo-Authenticate/ && cd Flask-Mongo-Authenticate

(Git Bash)
# venv:
python3 -m venv .venv
source .venv/Scripts/activate
pip install -r requirements.txt

# node:
npm install

# permiss:
sudo chmod +x setup run

# configure (default values are provided too):
./setup

# have at it:
./run
```

---

### _Structure:_

```console
├── api
  ├── main
    ├── auth
      └── token authentication methods
    ├── config
      └── the ./setup script populates a new config.cfg file for Flask,
          using the ##FIELDS## provided in config.cfg.sample
    ├── tools
      └── utilities for date/time, expression matching, the like
    └── user
      └── models.py defines the User() class
      └── routes.py implements User() methods api/routes as a blueprint
          (registered at /user/)
├── public
  └── all hot reloading and whatnot is done from react-scripts at index.html
└── src
  └── insert client-side source here, hack away  xD
      the thinking is one deal with compiling & serving production code elsewhere
```

---

_Notes:_

- Only tested on Ubuntu with GNU utilities, YMMV
- On Mac, please use GNU `sed`, see `./setup` for details

```
# MongoDB & gnu sed for Mac:
brew install gnu-sed
brew tap mongodb/brew
brew install mongodb-community@4.4
```
