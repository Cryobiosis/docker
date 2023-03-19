FROM node:16-alpine
RUN mkdir /opt/app
#COPY kurssitiedot /opt/app/
RUN apk --no-cache add subversion
# Git can't download subfolder, so using subversion
#RUN git clone https://github.com/Cryobiosis/fullstack/tree/master/osa2/kurssitiedot /opt/app/
RUN svn checkout https://github.com/Cryobiosis/fullstack/trunk/osa2/kurssitiedot /opt/app/
# TODO: Remove apk cache, and git
WORKDIR /opt/app
RUN npm install
RUN npm run build
RUN npm install -g serve
EXPOSE 5000
CMD ["serve", "-s", "-l", "5000", "build"]
