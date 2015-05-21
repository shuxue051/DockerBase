FROM centos:centos7
MAINTAINER robin "robin@gmail.com"

RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install python-pip; yum clean all
RUN yun -y install git gcc python libevent-dev python-dev

RUN pip install argparse

RUN pip install flask
RUN pip install paramiko
RUN pip install werkzeug
RUN pip install jinja2
RUN pip install ecdsa
RUN pip install gevent
RUN pip install gevent-websocket
RUN pip install zdaemon


RUN git clone https://github.com/aluzzardi/wssh.git

EXPOSE 5000

CMD ["wsshd "]
