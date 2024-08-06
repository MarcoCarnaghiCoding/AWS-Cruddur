FROM python:3.10-slim-buster

#Inside the container
# make a new folder inside the container
WORKDIR /backend-flask

# Outside de container --> inside the container
# this contains the libraries want to install to run the app
COPY requirements.txt requirements.txt

# Outside de container --> inside the container
# Install the python libraries used for the app
RUN pip3 install -r requirements.txt

# Outside de container --> inside the container
# . means everything in the current directory
# first period . - /backend-flash (outside container)
# second period . - /backend-flash (inside container)
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
# CMD command
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]