FROM node:16 as node
RUN apt-get update && apt-get -y install default-jre
RUN apt -y install default-jre
RUN apt install openjdk-11-jre-headless
COPY server/lib /build/server/lib
COPY server/xtext-server /build/server/xtext-server
COPY node_modules /build/node_modules
COPY server/webpack.config.js /build/server/
WORKDIR /build/server
EXPOSE 3000
ENTRYPOINT ["node","lib/server.js"]
