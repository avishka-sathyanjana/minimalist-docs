FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
COPY tsconfig.json ./
COPY src ./src

RUN npm install
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]

# docker run 
# --env DATABASE_URL='mongodb+srv://admin:admin@minimalist-doc.udrln.mongodb.net/?retryWrites=true&w=majority&appName=minimalist-doc' 
# --env CLIENT_ORIGIN='http://minimalist.doc.v0.s3-website-us-east-1.amazonaws.com' -p 80:3000 --name=minimalist-docs-container