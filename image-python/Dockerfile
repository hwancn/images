FROM python:3.11-slim-bullseye
COPY sources.list /etc/apt/sources.list
COPY pydistutils.cfg /root/.pydistutils.cfg
COPY pip.conf /root/.pip/pip.conf
RUN apt-get update  \
    && apt-get install -y \
        python3-dev \
        gcc \
        libc-dev \
        make \
        cmake \
        g++ \
        gfortran \
        curl \
        wget \
        vim \
        iputils-ping \
        dnsutils \
        traceroute  \
    && pip install --upgrade pip  \
    && ln -snf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo "Asia/Shanghai" > /etc/timezone
