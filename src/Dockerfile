FROM node:21-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080

USER daniel

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 CMD [ "curl", "-f", "http://localhost:3000/health" ]

CMD ["node", "server.js"]


# docker build -f Dockerfile -t danielucb/projeto-caotico:v4 .
# docker run -dti --name projeto-caotico -p 8080:8080 danielucb/projeto-caotico:v4