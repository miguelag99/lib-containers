FROM nvcr.io/nvidia/pytorch:22.11-py3

RUN useradd -rm -d /home/user -s /bin/bash -g root -G sudo -u 1000 user
RUN echo "user:container"| chpasswd
WORKDIR /home/user/workspace

ENTRYPOINT /bin/bash