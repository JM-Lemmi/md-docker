FROM python
#python:latest is debian based

RUN apt-get update && apt-get install ffmpeg -y
RUN pip3 install moodle-dl

WORKDIR /config

CMD moodle-dl -i