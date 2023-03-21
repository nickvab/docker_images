FROM ubuntu:20.04
LABEL maintainer="nickvab@gmail.com"
ENV TZ=Europe/Minsk
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt update && apt upgrade -yqq
RUN apt install -yqq iputils-ping mc vim curl wget git telnet netcat \
    && apt-get purge --auto-remove -yqq \
	&& apt-get clean \
	&& rm -rf \
	    /var/lib/apt/lists/* \
	    /tmp/* \
	    /var/tmp/* \
	    /usr/share/man \
	    /usr/share/doc \
	    /usr/share/doc-base
