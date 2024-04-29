FROM node:21-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]


# docker build -f Dockerfile -t danielucb/projeto-caotico:v4 .
# docker run -dti --name projeto-caotico -p 8080:8080 danielucb/projeto-caotico:v4