FROM ubuntu:16.04

WORKDIR /tools

RUN apt-get update
RUN apt-get install -y libldns-dev git build-essential

RUN git clone https://github.com/blechschmidt/massdns.git
RUN cd massdns && make
RUN mv massdns/bin/massdns /bin/massdns

RUN git clone https://github.com/BonJarber/fresh-resolvers.git

ENTRYPOINT ["/bin/bash"]
