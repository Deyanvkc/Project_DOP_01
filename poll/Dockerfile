# On utilise une image officielle de Python
FROM python:3.9-slim

# On définit le dossier de travail
WORKDIR /app

# On copie les fichiers de l'application
COPY . /app

# On installe les dépendances
RUN pip install -r requirements.txt

# Copie de local vers container
COPY . .

# On expose le port 80
EXPOSE 80

# On lance l'application
CMD ["python", "app.py"]