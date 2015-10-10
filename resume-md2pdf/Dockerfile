# use the ubuntu base image provided by official repo
FROM ubuntu:latest
MAINTAINER Steve Zhang "stevzhg@gmail.com"

# prepare work directory
WORKDIR /resume

# install requirement
RUN apt-get update
RUN apt-get -y install git wget python-pip python-dev

RUN wget http://download.gna.org/wkhtmltopdf/0.12/0.12.2.1/wkhtmltox-0.12.2.1_linux-trusty-amd64.deb \
    && dpkg -i wkhtmltox-0.12.2.1_linux-trusty-amd64.deb \
    && apt-get -y install -f \
    && rm wkhtmltox-0.12.2.1_linux-trusty-amd64.deb

# install md2pdf
RUN pip install git+git://github.com/hit9/md2pdf.git@master