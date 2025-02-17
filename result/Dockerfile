# On utilise une image légère de Node.js
FROM node:18-alpine

# On définit le dossier de travail
WORKDIR /app

# On copie les fichiers nécessaires
COPY package*.json ./

# On installe les dépendances
RUN npm install

# Copie de local vers container
COPY . .

# On expose le port 80
EXPOSE 80

# On lance l'application
CMD ["npm", "start"]