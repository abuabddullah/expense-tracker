FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --omit=dev

# npm আর লাগবে না, ওর ভেতরের vulnerable tar মুছে ফেলি
RUN rm -rf /usr/local/lib/node_modules/npm /usr/local/bin/npm /usr/local/bin/npx

COPY src ./src

EXPOSE 5000

CMD ["node", "src/server.js"]
