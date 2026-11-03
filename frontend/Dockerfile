FROM node:20-alpine

WORKDIR /app

# Copia i descrittori delle dipendenze per sfruttare il caching dei layer
COPY package*.json ./

RUN npm install

# Copia il resto dell'applicazione
COPY . .

EXPOSE 4200

# --host 0.0.0.0 consente al browser su Windows di accedere al container
CMD ["npm", "start"]
