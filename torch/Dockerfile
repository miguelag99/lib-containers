FROM nvcr.io/nvidia/pytorch:22.11-py3

RUN useradd -rm -d /home/robesafe -s /bin/bash -g root -G sudo -u 1000 robesafe
RUN echo "robesafe:container"| chpasswd
USER robesafe

RUN python -m pip install --upgrade pip

RUN mkdir /home/robesafe/.cache
COPY requirements.txt /home/robesafe/.cache
RUN pip install -r /home/robesafe/.cache/requirements.txt

WORKDIR /home/robesafe

ENTRYPOINT /bin/bash
