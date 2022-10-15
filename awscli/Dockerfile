FROM alpine:latest
LABEL maintainer "Kamalesh Giri <nerdlaunda@gmail.com>"


RUN apk update && apk add \
	ca-certificates \
	groff \
	nano \
	python3 \
	jq \
	py-pip \
  	&& pip install pip --upgrade \
  	&& pip install awscli \
	&& rm -rf /var/cache/apk/* 

VOLUME /root/.aws

WORKDIR "/data"

# Autorun aws
ENTRYPOINT ["aws"]