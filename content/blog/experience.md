---
external: false
title: "Expérimentation - Sécuriser une application Laravel"
description: "Retour d'Expérience sur le Projet Laravel : Sécurité et Apprentissage"
date: 2024-01-27
---

## Retour d'Expérience sur le Projet Laravel : Sécurité et Apprentissage

### Introduction

Dans le cadre d'un cours de développement sécurisé, nous avons entrepris la réalisation d'un projet Laravel riche en enseignements. Ce projet, axé sur la sécurité, comprenait plusieurs composantes clés : un système d'authentification, un gestionnaire de fichiers partagé, un chat, et une page administrateur. Voici un aperçu de notre parcours, des défis rencontrés et des solutions implémentées.

### Mise en Place du Projet

Le projet a été lancé via GitHub Codespaces et Docker en local. Cette approche flexible nous a permis de travailler efficacement dans différents environnements, tout en maîtrisant les outils de développement modernes. Les étapes de lancement et la configuration post-lancement ont été cruciales pour assurer une base solide pour notre application.

### Sécurité au Cœur du Projet

La sécurité était notre priorité absolue. Nous avons intégré plusieurs mesures pour protéger notre application :

* **Protection CSRF** : Utilisation du tag @csrf dans tous les formulaires pour prévenir les attaques Cross-Site Request Forgery.
* **Gestion des Rôles et Autorisations** : Mise en place de policies et middleware pour un contrôle d'accès fin.
* **Sécurisation des Fichiers** : Stockage des fichiers dans un dossier privé pour éviter l'accès direct depuis le web.
* **Journalisation des Actions** : Enregistrement des actions significatives pour faciliter le suivi et l'analyse en cas d'incident.
* **Authentification Robuste** : Implémentation de Laravel Breeze pour une gestion sécurisée de l'authentification.
* **Interaction Sécurisée avec la Base de Données** : Utilisation de l'ORM Eloquent pour prévenir les injections SQL.
* **Content Security Policy (CSP)** : Configuration d'une politique CSP stricte pour réduire les risques d'attaques basées sur l'injection de code.

### Identification des Faiblesses Logicielles Potentielles

Nous avons identifié des axes d'amélioration pour renforcer la sécurité de notre projet :

* **Utilisation d'un Stockage Cloud (AWS)** : Pour une sécurité et une fiabilité accrues.
* **Intégration d'un Antivirus** : Pour scanner les fichiers téléchargés à la recherche de malwares.
* **Passage en Mode Production** : Nécessaire pour optimiser la performance et la sécurité.

### Défis et Solutions

Un des plus grands défis a été la validation de l'identité de l'administrateur pour des actions sensibles. Nous avons dû intégrer un champ de mot de passe dans le formulaire de changement de rôle pour sécuriser ces actions, une solution efficace mais limitée en termes de versatilité.
Technologies et Librairies Utilisées

Le projet a été construit sur Laravel 10.10, avec PHP 8.3 comme langage de programmation. Nous avons également utilisé des outils et bibliothèques tels que Guzzle, Laravel Tinker, et Spatie Laravel CSP pour divers aspects du développement.

### Conclusion

Ce projet Laravel a été une expérience enrichissante, nous permettant d'appliquer des concepts de sécurité web et de développement sécurisé dans un cadre pratique. Nous avons appris l'importance de la sécurité à chaque étape du développement et avons acquis une expérience précieuse dans l'utilisation de Laravel et de ses diverses fonctionnalités de sécurité. Ce projet a non seulement renforcé nos compétences techniques, mais a également souligné l'importance de la sécurité dans le développement d'applications web modernes.