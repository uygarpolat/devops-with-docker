FROM ubuntu

WORKDIR /myapp

RUN apt update && apt install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt install -y nodejs

COPY . .

ENV REACT_APP_BACKEND_URL=http://127.0.0.1:8080/

RUN npm install

RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]