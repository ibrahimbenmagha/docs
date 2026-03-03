---
title: Webhooks
description: Recevez des mises à jour en temps réel sur les messages, les contacts, les conversations et les tickets.
icon: i-lucide-webhook
---

Les webhooks vous permettent de recevoir des notifications `POST` en temps réel directement sur votre serveur lorsqu'un événement spécifique se produit dans Digishare.

## 1. Configuration

::steps
### Définir l'URL du Webhook
Configurez l'URL de votre endpoint dans les paramètres de votre application Digishare.

### Écouter les événements
Votre serveur doit être prêt à recevoir des requêtes `POST` avec un payload JSON.

### Accuser réception
Votre endpoint **doit** répondre avec un code HTTP `200 OK` pour confirmer la réception.
::

::warning
Si votre serveur ne répond pas avec un `200 OK`, Digishare tentera de renvoyer la notification selon une politique de retry avant de désactiver temporairement le webhook.
::


::tip
Pour les mises à jour (`updated`), le payload inclut un objet `changes` montrant uniquement les champs modifiés et leurs nouvelles valeurs.
::
