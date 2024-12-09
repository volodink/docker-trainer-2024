# FROM  ubuntu:24.04
# RUN apt-get update && \
#     apt-get upgrade -y && \
#     apt-get install -y build-essential && \
#     rm -rf /var/lib/apt/lists/*
# WORKDIR /workdir
# COPY . .
# RUN make
# ENTRYPOINT [ "./bin/prog" ]

FROM  ubuntu:24.04
# FROM danger89/cmake:latest
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y build-essential cmake && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /workdir
COPY . .
RUN cmake -S . -B build && \
    cmake --build build
ENTRYPOINT [ "./build/prog" ]

