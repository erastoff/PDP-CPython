#docker build -t python27-ubuntu:22.04_r1 .
#docker run -ti --rm python27-ubuntu:22.04_r1

FROM centos:7

RUN yum clean all && \
    yum install -y \
    git \
    make \
    gcc-c++ \
    vim \
    ssh

RUN git clone https://github.com/python/cpython.git

WORKDIR /cpython

RUN git checkout 2.7

RUN ./configure --with-pydebug --prefix=/tmp/python

RUN make -j2

