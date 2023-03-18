FROM node:16-alpine
RUN mkdir /opt/app
COPY example-frontend/ /opt/app/
WORKDIR /opt/app
RUN npm install
ENV REACT_APP_BACKEND_URL=http://localhost:8000 
RUN npm run build
RUN npm install -g serve
CMD ["serve", "-s", "-l", "5000", "build"]
#ENTRYPOINT [ "/bin/sh" ]