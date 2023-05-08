FROM ubuntu:20.04
ENV LANG en_US.utf8
ENV MICRO_SERVICE=/usr/src/app

RUN mkdir -p $MICRO_SERVICE

WORKDIR $MICRO_SERVICE

COPY . .

RUN apt-get -o Acquire::Check-Valid-Until=false -o Acquire::Check-Date=false>
     apt install python -y &&\
     apt install python3-pip -y


RUN pip3 install -U pipenv
RUN pipenv install django
RUN pipenv --python 3
RUN pipenv shell
