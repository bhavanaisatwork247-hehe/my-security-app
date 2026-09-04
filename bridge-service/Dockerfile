FROM node:18-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./
RUN npm install --production || npm init -y && npm install express axios

# Copy application source code
COPY . .

EXPOSE 3000

CMD ["node", "index.js"]