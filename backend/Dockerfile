# Utiliser une image OpenJDK légère
FROM openjdk:17-jdk-slim

# Définir un volume pour conserver les fichiers temporaires ou logs si nécessaire
VOLUME /tmp

# Définir une variable d'environnement pour le JAR
ARG JAR_FILE=target/Backend-0.0.3-SNAPSHOT.jar

# Copier le fichier JAR dans le conteneur
COPY ${JAR_FILE} app.jar

# Exposer le port 8083 pour l’application
EXPOSE 8083

# Démarrer l’application Spring Boot
ENTRYPOINT ["java", "-jar", "/app.jar"]
