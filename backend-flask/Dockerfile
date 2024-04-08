FROM python:3.10-slim-buster

# Inside Container
# make a new folder inside container 
WORKDIR /backend-flask

# Outside Container -> Inside Container
# This contains the libraries want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container
# Install the python Librraries used for the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# means everything in the current directory
# first Period . -/backend-flask (Outside Container)
# Second Period . -/backend-flask (Outside Container)
COPY . .

# Set Environment Variable (Env Vars)
# Inside Container and will remain set when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# Python3 -m flask run --host=0.0.0.0 --port=4567
CMD ["python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
