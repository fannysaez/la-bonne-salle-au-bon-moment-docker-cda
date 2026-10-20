# la-bonne-salle-au-bon-moment-docker-cda

Orchestration Docker (frontend + backend + MongoDB) pour le projet "La Bonne Salle au Bon Moment".

---

## Aperçu

| Frontend | Backend (API) |
|---|---|
| <img src="screenshots/Frontend.png" width="400"> | <img src="screenshots/Backend-API.png" width="400"> |

---

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

```bash
PORT=3000
MONGO_URI=mongodb://mongo:27017/la-bonne-salle-au-bon-moment
JWT_SECRET=<ta_valeur_secrete>
```

## Lancer le projet

```bash
docker compose up
```

- Frontend : http://localhost:5173
- Backend : http://localhost:3000 (API préfixée en `/api`, ex: `/api/users`)
- Documentation API : http://localhost:3000/api-docs

---
## Arrêter le projet

Pause rapide (conteneurs gardés, redémarrage instantané) :
```bash
docker compose stop
```

Arrêt complet (conteneurs supprimés, données conservées) :
```bash
docker compose down
```

---
Les données MongoDB sont conservées dans le volume `docker-react_mongo_data`.