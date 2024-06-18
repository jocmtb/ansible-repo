# import the last base image from respository
FROM ubuntu:20.04
# Proxy 
ARG PROXY=""
# change of variable to avoid configuration questions
ENV DEBIAN_FRONTEND=noninteractive
# expose the port 8019 for ansible container
EXPOSE 8019
# change to root directory
RUN apt-get update && apt install -y lsb-core && \
apt-get install -y software-properties-common && \
apt-get install -y python3-pip
# update to the lastest code
RUN pip install ansible && ansible-galaxy collection install cisco.aci
#CMD
CMD tail -f /dev/null