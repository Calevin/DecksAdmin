# === Development Stage ===
FROM node:22-alpine AS dev
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install
# Code is mounted via volumes for hot reload, but we copy it anyway
COPY . .
EXPOSE 5173
# Run vite dev server
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]

# === Build Stage ===
FROM node:22-alpine AS build
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build

# === Production Stage ===
FROM nginx:alpine AS prod
# Copy built files from the build stage
COPY --from=build /app/dist /usr/share/nginx/html
# Copy custom Nginx proxy configuration if needed (will do default fallback)
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
