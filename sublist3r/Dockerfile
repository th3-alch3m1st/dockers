FROM debian:jessie

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python-requests git python-dnspython
WORKDIR /tools
RUN git clone https://github.com/aboul3la/Sublist3r.git

ENTRYPOINT ["/usr/bin/python", "/tools/Sublist3r/sublist3r.py"]
