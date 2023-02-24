FROM python:3.10-slim-buster

# inside container 
# make a new folder inside container 
WORKDIR /backend-flask

# Outside container -> inside container 
# this contains the librairies you want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container 
# Install the python librairies used for the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container 
# . means everthing in the current directory 
# fisrt period . /backend-flask (outside container)
# second period . / backedn-flask (inside container) 
COPY . .

# Set Env variables 
# Will remain ser inside container when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD (COMMAND)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]