#https://github.com/aajanki/yle-dl/blob/master/OS-install-instructions.md
FROM debian:bullseye
RUN apt-get update && apt-get upgrade -y
RUN apt-get install wget ffmpeg python3-dev python3-setuptools \
    python3-pip python3-requests python3-lxml -y \
    && apt-get purge -y && rm -rf /var/lib/apt/lists/*
RUN mkdir /opt/dl
#COPY download.sh /opt/dl
# Save source
COPY Dockerfile /opt/dl
#RUN mkdir /opt/app
WORKDIR /opt/dl
RUN useradd -m yle
RUN chown yle .
USER yle
RUN pip3 install --user --upgrade yle-dl
RUN export PATH=$PATH:$HOME/.local/bin
#RUN git clone https://github.com/aajanki/yle-dl.git
#RUN cd yle-dl
#RUN pip3 install --user .
#ENTRYPOINT [ "./download.sh" ]
ENTRYPOINT ["/home/yle/.local/bin/yle-dl"]