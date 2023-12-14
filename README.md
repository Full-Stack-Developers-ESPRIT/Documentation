# Documentation du projet Microservice : TerrainSpot app


## Aperçu du projet
L'application TerrainSpot vise à fournir un système complet de réservation et de gestion de terrains. Le projet utilise une architecture microservices pour garantir la flexibilité, la scalabilité et la résilience du système. Les utilisateurs pourront rechercher et réserver des terrains, rechercher des produits et passer des commandes, tandis que les administrateurs pourront gérer efficacement les informations sur les différents éléments.

## Objectifs
Les objectifs clés du projet TerrainSpot sont les suivants :

Automatiser le processus de réservation de terrain : L'application permettra aux utilisateurs de réserver des terrains de manière fluide et automatisée.

Fournir des informations en temps réel sur les événements et les produits : Les utilisateurs pourront accéder aux informations les plus récentes concernant les événements à venir et les produits disponibles.

Assurer une gestion efficace des réservations et des commandes : Les administrateurs disposeront d'outils puissants pour gérer les réservations et les commandes, ce qui facilitera la gestion globale de l'application.

## Architecture de TerrainSpotApp
L'application TerrainSpot est basée sur une architecture microservices, ce qui signifie qu'elle est divisée en plusieurs services indépendants, cohérents et spécialisés. Chaque service est responsable d'une fonctionnalité spécifique du système et communique avec les autres services via un bus de services.

Les principaux services implémentés dans l'application TerrainSpot sont :

## Service Eureka :
Il s'agit d'un service de découverte de microservices qui permet l'enregistrement et la résolution des adresses IP et des ports des différents services.

## Service Terrain :
Gère les fonctionnalités liées aux terrains, y compris la création, la mise à jour et la suppression de terrains. Il offre également des requêtes pour récupérer des informations sur les terrains.

## Service Evenement : 
Gère les fonctionnalités liées aux événements, notamment la création, la mise à jour et la suppression d'événements. Il fournit également des requêtes pour récupérer des informations sur les événements.

## 
Service Reservation : Gère les fonctionnalités de réservation, y compris la création, la mise à jour et la suppression de réservations. Il offre également des requêtes pour récupérer des informations sur les réservations.

## Service Produit : 
Gère les fonctionnalités liées aux produits, y compris la création, la mise à jour et la suppression de produits. Il fournit également des requêtes pour récupérer des informations sur les produits.

## Service Commande :
Gère les fonctionnalités liées aux commandes, y compris la création, la mise à jour et la suppression de commandes. Il offre également des requêtes pour récupérer des informations sur les commandes.

## Service Reclamation :
Gère les fonctionnalités de réclamation, y compris la création, la mise à jour et la suppression de réclamations. Il offre également des requêtes pour récupérer des informations sur les réclamations.

Chaque service communique avec les autres services via un bus de services, ce qui facilite l'échange de données entre les différents composants du système.

## Spécifications des services
Chaque service dispose de spécifications détaillées pour les opérations qu'il prend en charge, les modèles de données utilisés et les événements émis. Voici un aperçu des spécifications des services principaux :

## Service Terrain
Le service Terrain gère les fonctionnalités liées aux terrains.

## Opérations
CreateTerrain : Crée un nouveau terrain.
UpdateTerrain : Met à jour les informations d'un terrain existant.
DeleteTerrain : Supprime un terrain existant.
getTerrainById : Récupère les informations d'un terrain en fonction de son ID.
getAllTerrains : Récupère toutes les informations des terrains.
getTerrainByNom : Récupère les terrains en fonction de leur nom.
getTerrainByType : Récupère les terrains en fonction de leur type.
####Modèles de données

## Terrain
ID : Identifiant unique du terrain
Nom : Nom du terrain
Type : Type de terrain (football, tennis, basket, etc.)
Adresse : Adresse du terrain
Capacité : Capacité maximale du terrain
Prix : Prix de la réservation du terrain
Disponibilité : Indique si le terrain est disponible ou non
## Événements émis
TerrainCreated : Émis lorsqu'un nouveau terrain est créé.
TerrainUpdated : Émis lorsqu'un terrain existant est mis à jour.
TerrainDeleted : Émis lorsqu'un terrain est supprimé.
Service Evenement
Le service Evenement gère les fonctionnalités liées aux événements.

## Opérations
CreateEvenement : Crée un nouvel événement.
UpdateEvenement : Met à jour les informations d'un événement existant.
DeleteEvenement : Supprime un événement existant.
getEvenementById : Récupère les informations d'un événement en fonction de son ID.
getAllEvenements : Récupère toutes les informations des événements.
getEvenementsByTerrain : Récupère les événements associés à un terrain spécifique.
Modèles de données
## Evenement
ID : Identifiant unique de l'événement
Nom : Nom de l'événement
TerrainID : ID du terrain associé à l'événement
Date : Date de l'événement
HeureDebut : Heure de début de l'événement
HeureFin : Heure de fin de l'événement
Description : Description de l'événement
## Événements émis
EvenementCreated : Émis lorsqu'un nouvel événement est créé.
EvenementUpdated : Émis lorsqu'un événement existant est mis à jour.
EvenementDeleted : Émis lorsqu'un événement est supprimé.
## Service Reservation
Le service Reservation gère les fonctionnalités de réservation.

## Opérations
CreateReservation : Crée une nouvelle réservation.
UpdateReservation : Met à jour les informations d'une réservation existante.
DeleteReservation : Supprime une réservation existante.
getReservationById : Récupère les informations d'une réservation en fonction de son ID.
getAllReservations : Récupère toutes les informations des réservations.
getReservationsByUser : Récupère les réservations associées à un utilisateur spécifique.
getReservationsByTerrain : Récupère les réservations associées à un terrain spécifique.
Modèles de données
## Reservation
ID : Identifiant unique de la réservation
UserID : ID de l'utilisateur effectuant la réservation
TerrainID : ID du terrain réservé
Date : Date de la réservation
HeureDebut : Heure de début de la réservation
HeureFin : Heure de fin de la réservation
Statut : Statut de la réservation (confirmée, en attente, annulée, etc.)
## Événements émis
ReservationCreated : Émis lorsqu'une nouvelle réservation est créée.
ReservationUpdated : Émis lorsqu'une réservation existante est mise à jour.
ReservationDeleted : Émis lorsqu'une réservation est supprimée.
Service Produit
Le service Produit gère les fonctionnalités liées aux produits.

## Opérations
CreateProduit : Crée un nouveau produit.
UpdateProduit : Met à jour les informations d'un produit existant.
DeleteProduit : Supprime un produit existant.
getProduitById : Récupère les informations d'un produit en fonction de son ID.
getAllProduits : Récupère toutes les informations des produits.
Modèles de données
## Produit
ID : Identifiant unique du produit
Nom : Nom du produit
Description : Description du produit
Prix : Prix du produit
## Événements émis
ProduitCreated : Émis lorsqu'un nouveau produit est créé.
ProduitUpdated : Émis lorsqu'un produit existant est mis à jour.

## Service Eureka

Le service Eureka est responsable de la découverte des microservices et de la gestion de leur enregistrement et de leur résolution d'adresses IP et de ports.

## Opérations
RegisterService : Enregistre un service auprès du serveur Eureka.
DeregisterService : Désenregistre un service auprès du serveur Eureka.
Heartbeat : Signale au serveur Eureka que le service est toujours actif.
Modèles de données
ServiceInstance
InstanceID : Identifiant unique de l'instance du service
ServiceName : Nom du service
IPAddress : Adresse IP de l'instance du service
Port : Port de l'instance du service
Événements émis
ServiceRegistered : Émis lorsqu'un service s'enregistre auprès du serveur Eureka.
ServiceDeregistered : Émis lorsqu'un service se désenregistre du serveur Eureka.

## API Gateway

L'API Gateway est un composant essentiel de l'architecture microservices. Il agit comme un point d'entrée unique pour les clients et dirige les requêtes vers les services appropriés. Il fournit également des fonctionnalités telles que l'authentification, l'autorisation et la gestion des versions d'API.

## Fonctionnalités
Routage des requêtes : L'API Gateway reçoit les requêtes des clients et les achemine vers les services appropriés en fonction de l'URL ou d'autres critères de routage.
Gestion des versions d'API : L'API Gateway permet de gérer différentes versions d'API et de diriger les clients vers la version appropriée.
Authentification et autorisation : L'API Gateway peut gérer l'authentification des utilisateurs et l'autorisation des requêtes en utilisant des mécanismes tels que JWT (JSON Web Tokens) ou OAuth.
Caching : L'API Gateway peut mettre en cache les réponses des services pour améliorer les performances et réduire la charge sur les services.
Limitation du débit : L'API Gateway peut limiter le débit des requêtes vers les services afin de prévenir les abus ou les surcharges.
Journalisation et surveillance : L'API Gateway peut enregistrer les journaux et les métriques liés aux requêtes et aux services, ce qui facilite la surveillance et le débogage.

## Keycloak

Keycloak est une solution open source de gestion des identités et des accès (IAM) qui permet d'ajouter des fonctionnalités d'authentification et d'autorisation sécurisées à une application. Il offre des fonctionnalités telles que l'authentification unique (SSO), la gestion des utilisateurs, les rôles et les autorisations, la connexion sociale, etc.

## Fonctionnalités
Authentification : Keycloak prend en charge plusieurs méthodes d'authentification, notamment l'authentification par nom d'utilisateur/mot de passe, la connexion sociale (Google, Facebook, etc.), les certificats, etc.
Autorisation et gestion des rôles : Keycloak permet de définir des rôles et des autorisations pour contrôler l'accès aux fonctionnalités de l'application.
Authentification unique (SSO) : Keycloak permet aux utilisateurs de se connecter une seule fois pour accéder à plusieurs applications protégées par Keycloak sans avoir à ressaisir leurs identifiants.
Flux de travail de récupération de mot de passe : Keycloak fournit des fonctionnalités pour la récupération de mot de passe, notamment la réinitialisation du mot de passe par e-mail ou par des questions de sécurité.
Intégration avec des protocoles standard : Keycloak prend en charge des protocoles standard tels que OAuth 2.0 et OpenID Connect, ce qui facilite l'intégration avec d'autres services et applications.
Console d'administration : Keycloak offre une console d'administration conviviale pour gérer les utilisateurs, les rôles, les clients d'application, etc.
L'intégration de Keycloak dans l'architecture de l'application TerrainSpot permettra de sécuriser l'accès aux services, d'authentifier les utilisateurs et de gérer les autorisations en fonction des rôles et des permissions définis.

##  Conclusion

Ce projet illustre une architecture microservices robuste et évolutive en utilisant Spring Boot pour le développement, Eureka pour la découverte de services, et une combinaison de Docker et Kubernetes pour l'orchestration des containers.

