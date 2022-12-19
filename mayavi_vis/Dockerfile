FROM python:3.8

RUN useradd -rm -d /home/robesafe -s /bin/bash -g root -G sudo -u 1000 robesafe
RUN echo "robesafe:container"| chpasswd


RUN apt-get update
RUN apt-get install -y libgl1-mesa-glx mesa-utils libglapi-mesa
# RUN apt-get install python3
RUN python -m pip install --upgrade pip

RUN apt-get install python3-vtk7 -y

RUN mkdir /home/robesafe/.cache
COPY requirements.txt /home/robesafe/.cache
RUN pip install -r /home/robesafe/.cache/requirements.txt

WORKDIR /home/robesafe
USER robesafe

ENTRYPOINT /bin/bash
