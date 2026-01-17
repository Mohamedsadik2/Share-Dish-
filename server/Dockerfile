# server/Dockerfile
FROM node:20-alpine

WORKDIR /app
ENV NODE_ENV=production

# Install deps first (better caching)
COPY package*.json ./
RUN npm ci --omit=dev

# Copy source
COPY . .

# Your server runs on 5000
EXPOSE 5000

# In Docker we run node (not nodemon)
CMD ["node", "app-working.js"]
