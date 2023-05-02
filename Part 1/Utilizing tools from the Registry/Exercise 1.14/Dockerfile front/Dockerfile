FROM node:16.20.0-slim

WORKDIR /usr/src/app

COPY . .

ENV REACT_APP_BACKEND_URL http://192.168.56.11:8080


RUN npm install
RUN npm run build
RUN npm install -g serve

EXPOSE 5000

CMD ["serve", "-s", "-l" ,"5000", "build"]