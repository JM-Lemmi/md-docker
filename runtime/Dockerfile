FROM python

RUN apt-get update && apt-get install ffmpeg -y
RUN pip3 install moodle-dl

WORKDIR /srv/md

CMD moodle-dl --path /srv/md