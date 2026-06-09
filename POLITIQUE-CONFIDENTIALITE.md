# Politique de Confidentialité — Orgamama

> Version 1.1 — en vigueur à compter du 9 juin 2026

---

## 1. Qui sommes-nous ?

L'application Orgamama est éditée par **GARIGUETTES SAS**, immatriculée au RCS de Nancy sous le numéro 948 717 681, dont le siège est 4 rue Piroux, 54000 Nancy.

SIRET : 948 717 681 000 19

Contact protection des données : contact@gariguettes.fr

---

## 2. Notre philosophie : local-first

Orgamama a été conçue avec un principe structurant : **tes données de santé ne quittent jamais ton téléphone.**

Concrètement, toutes les informations sensibles que tu saisis dans l'app — ta date prévue d'accouchement, tes check-ins quotidiens, tes notes, ton historique de rendez-vous médicaux, ton projet de naissance — sont **stockées localement et chiffrées sur ton appareil**. Ces données ne transitent pas par nos serveurs et ne sont pas accessibles par l'éditeur.

Ce choix est à la fois une conviction (ta grossesse, c'est ton histoire) et un parti pris technique assumé.

---

## 3. Quelles données traitons-nous, et pour quoi ?

### 3.1 Données stockées uniquement sur ton appareil (jamais transmises)

| Donnée | Finalité |
|---|---|
| Date prévue d'accouchement (DPA) | Calcul de la semaine de grossesse, personnalisation de l'app |
| Prénom | Personnalisation de l'interface |
| Âge, situation professionnelle, nb d'enfants | Personnalisation des démarches admin et des contenus |
| Check-ins quotidiens (humeur, symptômes) | Suggestions personnalisées, historique bien-être |
| Notes, RDV médicaux, statut des démarches | Suivi personnel |
| Contenu du projet de naissance, valises, dossier maternité | Outils personnels |

**Base légale** : exécution du contrat / intérêt légitime (fonctionnement de l'app).
**Durée** : tant que l'app est installée sur l'appareil. La désinstallation supprime définitivement ces données.

### 3.2 Données transmises à des services tiers

Orgamama n'utilise pas de compte utilisateur. Le strict minimum non-santé susceptible de transiter est :

| Donnée | Destinataire | Finalité | Base légale |
|---|---|---|---|
| Identifiant opaque anonyme (généré par le store) | RevenueCat | Gestion de l'abonnement premium | Exécution du contrat |
| Statut d'abonnement | RevenueCat | Débloquer les fonctionnalités premium | Exécution du contrat |
| Jeton de notification push, identifiant appareil | OneSignal | Envoi de notifications push (rappels démarches, conseils hebdo) | Consentement |
| Tags de segmentation : semaine de grossesse, trimestre, statut premium, nombre de check-ins, jours depuis dernier check-in, premier enfant (oui/non), consentements notifs | OneSignal | Personnalisation et ciblage des notifications push | Consentement |

Les tags envoyés à OneSignal sont **pseudonymisés** : ils sont associés à un identifiant technique d'appareil, sans lien avec ton identité (pas de nom, pas d'email). Tu peux désactiver les notifications à tout moment depuis les réglages de l'app ou de ton téléphone, ce qui stoppe l'envoi de tags.

Nous ne collectons pas ton adresse email, ton nom, ni aucune donnée permettant de t'identifier directement.

### 3.3 Assistant IA (Maïa) — traitement éphémère

Lorsque tu utilises l'assistant conversationnel Maïa, le contexte de ta requête (semaine de grossesse, check-in du jour si tu l'as partagé, et ta question) est **transmis éphémèrement à notre infrastructure IA** pour générer la réponse.

Le traitement suit le chemin suivant : ton appareil → notre serveur relais hébergé sur Google Cloud Platform (pas de stockage) → API Anthropic (Claude) qui génère la réponse.

Ce traitement est :
- **Éphémère** : notre serveur relais ne stocke aucune donnée. Anthropic peut conserver les échanges API jusqu'à 30 jours pour des finalités de sécurité et de lutte contre les abus, puis les supprime automatiquement. Anthropic n'utilise pas ces échanges pour entraîner ses modèles.
- **Anonymisé** : les requêtes sont associées à un identifiant opaque sans lien avec ton identité.
- **Sécurisé** : les échanges transitent via HTTPS de bout en bout.

**Base légale** : exécution du contrat.

Cette exception à la règle local-first est documentée ici et mentionnée dans l'app lors de la première utilisation de l'assistant.

---

### 3.4 Notifications push locales

Orgamama programme des notifications locales sur ton appareil (rappels de démarches, conseils de la semaine, suggestions d'outils). Ces notifications sont **générées et planifiées entièrement sur ton téléphone** — aucune donnée ne transite vers un serveur pour cette fonctionnalité.

---

## 4. Cookies et traceurs

L'Application mobile n'utilise pas de cookies.

La version web peut utiliser des cookies techniques strictement nécessaires au fonctionnement du service. Aucun cookie publicitaire ou de tracking tiers n'est déposé.

---

## 5. Sous-traitants et transferts de données

Nous faisons appel aux sous-traitants suivants pour les traitements décrits en §3.2 et §3.3 :

| Sous-traitant | Rôle | Localisation |
|---|---|---|
| **RevenueCat** | Gestion des abonnements in-app | États-Unis (garanties SCCs) |
| **Anthropic** (Claude) | Traitement des requêtes assistant IA Maïa | États-Unis (garanties SCCs) |
| **Google Cloud Platform** | Hébergement du serveur relais IA (Cloud Functions) | UE (europe-west1) ou États-Unis |
| **OneSignal** | Service de notifications push et segmentation | États-Unis (garanties SCCs) |
| **Apple / Google** | Distribution et facturation via les stores | États-Unis |

En cas de transfert hors UE, des garanties appropriées (clauses contractuelles types) sont en place.

---

## 6. Sécurité

Les données stockées localement sur ton appareil sont chiffrées. Les transmissions vers nos serveurs utilisent le protocole HTTPS (TLS 1.2 minimum). Les accès aux systèmes internes sont contrôlés et journalisés.

En cas de perte ou de vol de ton appareil, tes données de santé sont protégées par le chiffrement local. Nous t'encourageons à utiliser le code PIN ou la protection biométrique de ton appareil.

---

## 7. Tes droits (RGPD)

Conformément au Règlement Général sur la Protection des Données (RGPD) et à la loi Informatique et Libertés, tu disposes des droits suivants sur les données nous concernant (§3.2 et §3.3) :

- **Droit d'accès** : obtenir une copie des données que nous détenons sur toi.
- **Droit de rectification** : corriger des données inexactes.
- **Droit à l'effacement** (« droit à l'oubli ») : demander la suppression de tes données.
- **Droit à la portabilité** : recevoir tes données dans un format structuré.
- **Droit d'opposition** : t'opposer à certains traitements.
- **Droit à la limitation** : demander la limitation du traitement.

**Pour exercer ces droits** : envoie un email à contact@gariguettes.fr en indiquant ton identifiant opaque d'appareil (disponible dans les réglages de l'app sous « Mon identifiant »).

Concernant les données stockées localement sur ton appareil, l'exercice de tes droits s'effectue directement depuis l'app (suppression des données via les réglages, désinstallation de l'app).

**Délai de réponse** : nous répondrons dans un délai maximum de 30 jours.

En cas de difficulté, tu peux également introduire une réclamation auprès de la **CNIL** :
Commission Nationale de l'Informatique et des Libertés
3 place de Fontenoy — TSA 80715 — 75334 Paris Cedex 07
[www.cnil.fr](https://www.cnil.fr)

---

## 8. Données des mineures

Orgamama est destinée aux personnes majeures (18 ans et plus). Nous ne collectons pas sciemment de données concernant des mineures.

---

## 9. Modifications de cette politique

En cas de modification significative de cette politique, tu seras informée par une notification in-app. La date de mise à jour est indiquée en haut de ce document. Nous t'encourageons à la consulter régulièrement.

---

## 10. Contact

Pour toute question relative à la protection de tes données :

**GARIGUETTES SAS**
4 rue Piroux, 54000 Nancy
Email : contact@gariguettes.fr

---

*Politique de confidentialité Orgamama — GARIGUETTES SAS — Version 1.1*
