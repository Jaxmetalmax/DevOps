FROM node:16.13.1-bullseye-slim
ENV NODE_ENV=production
WORKDIR /usr/src/app
COPY ["package.json", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY --chown=node:node . .
EXPOSE 3000
USER node
CMD ["npm", "start"]
