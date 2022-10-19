# Use a Python base image in version 3.8
FROM python:3.8

LABEL maintainer="Nafiseh Namazypour"

COPY ./project/techtrends /app
WORKDIR /app


#Install packages defined in the requirements.txt file
RUN pip install -r requirements.txt

#Ensure that the database is initialized with the pre-defined posts in the init_db.py file
RUN python init_db.py

# Expose the application port 3111
EXPOSE 3111

# command to run on container start
CMD [ "python", "app.py" ]
