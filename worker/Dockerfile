# Première étape : compilation

# On utilise une image Maven
FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder

# On définit le dossier de travail
WORKDIR /app

# On copie les fichiers nécessaires
COPY pom.xml .

# On installe les dépendances
RUN mvn dependency:resolve

# On compile
COPY src ./src
RUN mvn package

# Deuxième étape : exécution

# On utilise une image eclipse-temurin
FROM eclipse-temurin:21-jre-alpine

# On définit le dossier de travail
WORKDIR /app

# On récupère la compilation JAR de l'étape 1
COPY --from=builder /app/target/worker-jar-with-dependencies.jar .

# On lance l'application
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]