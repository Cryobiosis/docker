FROM node:16-alpine
RUN mkdir /opt/app
COPY example-frontend/ /opt/app/
WORKDIR /opt/app
RUN npm install
RUN npm run build
RUN npm install -g serve
CMD ["serve", "-s", "-l", "5000", "build"]
#ENTRYPOINT [ "/bin/sh" ]
