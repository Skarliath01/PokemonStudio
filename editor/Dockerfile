# editor/Dockerfile

FROM node:20-alpine

# Définir le dossier de travail
WORKDIR /app

# Copie uniquement package.json et lock pour cache Docker
COPY package.json package-lock.json ./

# Installation des dépendances
RUN npm install

# Copie du reste du code
COPY . .

# Variables d’environnement utiles pour WSL2
ENV CHOKIDAR_USEPOLLING=true
ENV HOST=0.0.0.0

# Exposer le port de dev React
EXPOSE 3000

# Lancer le serveur React en mode développement
CMD ["npm", "start"]
