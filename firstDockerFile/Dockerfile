FROM xenial

MAINTAINER <TaeHoon> <<th2v@uxfac.com>>

ENV PATH /usr/local/bin:$PATH
ENV LANG C.UTF-8

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:jonathonf/python-3.6
RUN apt-get update
RUN apt-get install -y python3.6

RUN rm /usr/bin/python3
RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.5 1
RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 2

RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 1

RUN apt-get install -y python3-setuptools
RUN easy_install3 pip

RUN pip install django
