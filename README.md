# website
This is my own website by flask  
You can have a look [here](http://honmaple.com)

## flask-flatpages
This version I use flask-flatpages to open the md file and read the contents of file

## config/__init__.py
    #__init__.py
    def load_config():
        try:
            from .development import DevelopmentConfig
            return DevelopmentConfig
        except ImportError as e:
            from .default import Config
            return Config

## config/development.py
    class DevelopmentConfig(object):
        DEBUG
        SECRET_KEY
        SECURITY_PASSWORD_SALT

        FLATPAGES_AUTO_RELOAD = True
        FLATPAGES_EXTENSION = '.md'

        MAIL_SERVER
        MAIL_PORT
        MAIL_USE_TLS
        MAIL_USE_SSL
        MAIL_USERNAME
        MAIL_PASSWORD
        MAIL_DEFAULT_SENDER

        RECAPTCHA_PUBLIC_KEY
        RECAPTCHA_PRIVATE_KEY
        SQLALCHEMY_TRACK_MODIFICATIONS
        SQLALCHEMY_BINDS

## if you want to use
    gunicorn run:app -c gunicorn.conf 

