---
layout: post
title:  "Resumé application web"
date:   2017-12-11 8:22:00 +0200
category: dev-web
---



# Objectif
modèle général de développement d'applications Web
environnement de développement et outils de debugging (console web surtout)
caractéristiques et méthodes de développement adaptées
évolution et état en 2017
le fonctionnement d'HTTP
méthodes de base (GET, POST)
méthodes avancées (p.ex. REST: PUT, DELETE)
les URLs
modèle client-serveur, PULL et PUSH
format des échanges (entêtes et contenu, types MIME, etc)
modèles de conception
le modèle 3-tier de conception et de déploiement (y.c. notion de répartition de charge et load-balancing DNS)
MVC
le PHP
concepts de base (embarqué HTML, portée, typage dynamique, structures de données, tableaux, particularités comme comparaison classique et comparaison typée triple égal, interpolation de chaînes)
structuration par fichiers d'include
les problèmes de sécurité (cross-scripting, injection) et la protection avec htmlentities() et/ou urlencode()
les éléments avancés du langage: fonctions de deuxièmes ordre (fonctions anonymes, fonctions dans des fonctions, portée, callback, passage par référence, valeurs par défaut de paramètres de fonction), internationalisation et localisation)
contrôle des entêtes (buts, moyens, comment)
HTML
critères de choix du standard
HTML5 vs XHTML
principes (markup, document, élément, attributs et imbrication, structure de base et validateur)
entités
séparation sémantique (HTML5) vs présentation (CSS)
auto-correction par le navigateur et risques
notion de doctype (savoir par coeur uniquement celui du HTML5)
tableaux, listes, emphase, entités, images, liens, (image-map)
éléments de type bloc et inline
caractéristiques spécifiques d'XHTML
HTML5
principes et changements
lien avec Javascript, CSS et APIs
quelques éléments sémantiques cf la vidéo niveau 1 CodeSchool
HTML et PHP
affichage simple, échappement et validation
comment valider l'HTML produit (par URL ou sinon par wget/curl)
jeux de caractères
les formulaires
critères post ou get
structure
attributs, valeurs par défaut
labels (2 méthodes)
encodage et script de traitement
paramètres multivalués en PHP
validation par tableau
échappements
type "hidden"
envoi d'un fichier (encodage multipart)
OO en PHP
classes, méthodes, constructeurs, héritage
attributs et qualificateurs (public, protected, private)
variables et méthodes de classe
exceptions
sérialisation (persistance)
pas de surcharge réelle en PHP
quelques éléments sur les fonctions magiques
CRUD
SGBD en PHP avec MySQL
3 méthodes
interfaçage textuel spécifique mysqli_XXX et ses dangers
interfaçage par binding (placeholders ?), générique avec PDO en OO, exceptions activées
vaguement ORM avec PDO FETCH_CLASS
type du backend MyISAM ou InnoDB, cohérence des jeux de caractères
validation et échappement
phpmyadmin et outil mysql (bases)
approche mono et multi-script
configuration séparée
le contexte (traitement des paramètres de formulaires, sessions et cookies)
approche MVC
concepts et qui fait quoi
modèle, vue, contrôleur
routeur et routage
génération, traitement et validations de formulaires
on ne vous demandera pas de réécrire notre mini-framework, mais d'être capable de l'utiliser selon le modèle MVC
la sécurité
flot général de validation et d'échappement d'une application PHP/HTML/MySQL/JS/...
validation (y.c. par expression régulière)
échappements de divers types (htmlentities(), urlencode(), mysqli_escape_string())
symptôme d'un mauvais flot: doubles échappements, échappements dans les données de la DB, nécessité de faire stripslashes() sur les paramètres POST ou GET, etc.