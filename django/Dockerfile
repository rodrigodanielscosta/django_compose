# pull official base image
FROM python:3.8.0-alpine

# create directory for the app user
RUN mkdir -p /home/django

# create the appropriate directories
ENV HOME=/home/django
#ENV APP_HOME=/home/django/web
#RUN mkdir $HOME
RUN mkdir $HOME/staticfiles
RUN mkdir $HOME/mediafiles
WORKDIR $HOME

# install dependencies

COPY requirements.txt .
RUN pip install --upgrade pip
#WORKDIR $HOME
RUN pip install -r requirements.txt

# copy project
COPY . $APP_HOME


# chown all the files to the app user
#RUN chown -R app:app $APP_HOME

# change to the app user
#USER app
