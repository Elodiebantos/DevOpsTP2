#Image de Postgre
FROM postgres

#Copie du script
COPY words.sql /docker-entrypoint-initdb.d/

#Autorisation de la connexion 
ENV POSTGRES_HOST_AUTH_METHOD=trust