### Travail à réaliser

#### 1. **Dockerfile**

Voici ce que votre maître de stage a analysé et vous demande de mettre en place :

- **Base de l’image** :FROM node:18-alpine 
- **Répertoire de travail** : WORKDIR /app
- **Téléchargement de l'application** : 
    - RUN apk  add --no-cache git
    - RUN git clone https://github.com/toptal/haste-server
- **Installation des dépendances** :
    - RUN npm install
- **Personnalisation** :
  - COPY config.json /app
  - COPY index.html /static
- **Port d'écoute** : "port": 8085, (modifier dans config.json)
- **Commande de lancement** : Run npm start 

#### 2. lancement de l'application
docker build -t node:18-alpine . 

Vous devez maintenant :

- Lire et comprendre chaque instruction du Dockerfile.
- Vérifier que l'application se lance correctement via le navigateur sur [http://localhost:8085](http://localhost:8085).
- Contrôler les personnalisations suivantes :
  - **Votre nom** :  style="padding: 10px; text-align: center; color: #ccc; font-family: sans-serif;">Axelle</span></a>

  - **Suppression du logo Twitter**
  - **Port d’écoute** : "port": 8085, (config.json)
  - **Clé d’accès** : "keyLength": 5, (config.json)
  - **Taille maximale d’un paste (d'un message)** :"maxLength": 10, (config.json)


