# docker-drachtio-nodejs

A Dockerfile for a base nodejs image.

## Usage

Create a Dockerfile in your nodejs application directory with the following content:

```bash
FROM drachtio/nodejs

WORKDIR /app
ADD package.json /app/
RUN npm install
ADD . /app

CMD []
ENTRYPOINT ["/nodejs/bin/npm", "start"]
```

Run the following command in your app directory:

```bash
$ docker build -t my/app .
```