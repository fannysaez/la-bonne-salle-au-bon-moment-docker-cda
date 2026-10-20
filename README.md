# la-bonne-salle-au-bon-moment-docker-cda

Orchestration Docker (frontend + backend + MongoDB) pour le projet "La Bonne Salle au Bon Moment".

## Prérequis

- Docker et Docker Compose installés
- Git

## Installation

Cloner les 3 repos dans le même dossier parent :

```bash
git clone git@github.com:fannysaez/la-bonne-salle-au-bon-moment-docker-cda.git
cd la-bonne-salle-au-bon-moment-docker-cda
git clone git@github.com:fannysaez/la-bonne-salle-au-bon-moment-frontend-cda.git
git clone git@github.com:fannysaez/la-bonne-salle-au-bon-moment-backend-cda.git
```

Créer le fichier `.env` dans `la-bonne-salle-au-bon-moment-backend-cda/` :

```env
PORT=3000
MONGO_URI=mongodb://mongo:27017/la-bonne-salle-au-bon-moment
JWT_SECRET=<ta_valeur_secrete>
```


## Lancer le projet

```bash
docker compose up
```

- Frontend : http://localhost:5173
- Backend : http://localhost:3000
- Documentation API : http://localhost:3000/api-docs

## Arrêter le projet

```bash
docker compose down
```

Les données MongoDB sont conservées dans le volume `docker-react_mongo_data`.