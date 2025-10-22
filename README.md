# wazo-calld-queue

Plugin Wazo pour la gestion des files d'attente (queues) via l'API calld et la publication des stats temps réels de files d'attente.

## Description

Ce plugin ajoute des fonctionnalités de contrôle des files d'attente à wazo-calld et publie les événements vers le websocket Wazo. Il permet également de gérer les stats temps réels de files d'attente depuis wazo-call-logd.

## Fonctionnalités

- **Gestion des files d'attente** : Liste, consultation et contrôle des queues
- **Statistiques temps réel** : Consultation des stats live des files d'attente
- **Statut des agents** : Visualisation du statut de tous les agents
- **Interception d'appels** : Possibilité d'intercepter des appels en queue
- **Logs des files d'attente** : Publication des événements de queue via websocket

## Installation

```bash
wazo-plugind-cli -c "install git https://github.com/mwolff44/wazo-calld-queue"
```

## Configuration requise

- Wazo version 25.02 ou supérieure

## Utilisation

Une fois installé, les endpoints sont disponibles dans l'API calld de votre Wazo :
- Consultez la documentation API : `http://votre_wazo/api` (section calld)

### Endpoints principaux

- `GET /queues` - Liste toutes les files d'attente
- `GET /queues/{queue_name}` - Détails d'une file d'attente
- `PUT /queues/{queue_name}/add_member` - Ajouter un membre
- `PUT /queues/{queue_name}/remove_member` - Retirer un membre
- `PUT /queues/{queue_name}/pause_member` - Mettre en pause un membre
- `GET /queues/{queue_name}/livestats` - Statistiques temps réel
- `GET /queues/agents_status` - Statut de tous les agents
- `POST /queues/{queue_name}/intercept` - Intercepter un appel

## Auteurs

- Sylvain Boily
- Mathias WOLFF

## Licence

Voir le fichier LICENSE pour plus de détails.

## Support

Pour toute question ou problème, ouvrez une issue sur [GitHub](https://github.com/mwolff44/wazo-calld-queue).
