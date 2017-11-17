FROM python:3.5

RUN mkdir /root/.pip/ \
 && echo '[global]' >> /root/.pip/pip.conf \
 && echo 'index-url = https://pypi.douban.com/simple' >> /root/.pip/pip.conf

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install --no-cache-dir -r requirements.txt

ONBUILD COPY . /usr/src/app
