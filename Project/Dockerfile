FROM ubuntu:latest

WORKDIR /project

COPY . /project

RUN apt-get update && apt-get install -y python3 python3-pip

RUN pip3 install -r requirements.txt

RUN useradd -ms /bin/bash jupyter

USER jupyter

EXPOSE 5000

ENTRYPOINT [ "jupyter", "notebook", "--ip=*"]