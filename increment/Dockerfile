#docker build -t python27-ubuntu:22.04_r1 .
#docker run -ti --rm python27-ubuntu:22.04_r1

FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y \
    git \
    make \
    gcc \
    g++ \
    vim \
    ssh \
    python2.7 \
    python2.7-dev

WORKDIR /opt
RUN git clone https://github.com/python/cpython.git
WORKDIR /opt/cpython
RUN git checkout 2.7
RUN ./configure --with-pydebug --prefix=/tmp/python
RUN make -j2
RUN make install

# CMD ["/tmp/python/bin/python"]

