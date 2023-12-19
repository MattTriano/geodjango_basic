FROM python:3.11.7

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update \
    && apt-get install -y binutils libproj-dev gdal-bin libgdal-dev python3-gdal

ENV GDAL_LIBRARY_PATH /usr/lib/libgdal.so

RUN mkdir /usr/src/app
WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r requirements.txt

COPY . /usr/src/app/

