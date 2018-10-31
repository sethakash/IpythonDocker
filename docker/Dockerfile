FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y python3
RUN apt-get install -y python3-pip
RUN pip3 install --upgrade pip
RUN pip3 install jupyter

EXPOSE 8888
RUN jupyter notebook --generate-config
COPY .jupyter /root/.jupyter
CMD jupyter notebook --ip 0.0.0.0 --no-browser --allow-root --notebook-dir='/home'
