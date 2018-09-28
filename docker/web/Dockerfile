FROM python:latest

# Ensure that Python outputs everything that's printed inside
# the application rather than buffering it.
ENV PYTHONUNBUFFERED 1


# Creation of the workdir
RUN mkdir /project

WORKDIR /project

# Add requirements.txt file to container
ADD requirements.txt /project/

# Install requirements
RUN pip install --upgrade pip
RUN pip install -r /project/requirements.txt

# Add the current directory(the web folder) to Docker container
ADD . /project/
