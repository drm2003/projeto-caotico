FROM cgr.dev/chainguard/node

ENV NODE_ENV=production

WORKDIR /app

COPY --chown=node:node package*.json ./

RUN npm install --omit-dev

COPY --chown=node:node . .

EXPOSE 8080

CMD ["server.js"]


# docker build -f Dockerfile -t danielucb/projeto-caotico:v4 .
# docker run -dti --name projeto-caotico -p 8080:8080 danielucb/projeto-caotico:v4