FROM  ubuntu:24.04

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y build-essential cmake && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /workdir
COPY . .
RUN cmake -S . -B build && \
    cmake --build build

ENTRYPOINT [ "./build/prog" ]
