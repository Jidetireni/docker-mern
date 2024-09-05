FROM node:18.9.1-bullseye-slim

WORKDIR /app

COPY package.json .

RUN --mount=type=cache,target=/app/.npm  \
    npm set cache /app/.npm && \
    npm install --only=production

USER node

COPY --chown=node:node . .

EXPOSE 5050

CMD [ "npm", "start" ]