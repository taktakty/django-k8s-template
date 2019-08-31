FROM python:3.7-alpine

RUN \
  apk add --no-cache \
  dumb-init \
	gcc \
	linux-headers \
	musl-dev \
	libffi-dev \
  libc-dev \
  mariadb-client \
  mariadb-dev \
	make

WORKDIR /usr/src/app

COPY . ./
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

EXPOSE 8000
CMD ["sh","init.sh"]
