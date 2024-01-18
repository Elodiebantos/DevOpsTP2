# Utilisez une image Debian/Ubuntu comme base
FROM debian:latest

# Mise à jour des paquets et installation de Java, Maven
RUN apt-get update && \
    apt-get install -y \
    default-jre \
    maven \
    && rm -rf /var/lib/apt/lists/*

# Copiez les fichiers de l'application dans le conteneur
COPY . /app

# Définissez le répertoire de travail
WORKDIR /app/

# Compilation de l'application avec Maven
RUN mvn verify

# Commande par défaut pour lancer le serveur
CMD ["java", "-Xmx8m", "-Xms8m", "-jar", "target/words.jar"]

# Exposez le port sur lequel le serveur écoute
EXPOSE 8080
