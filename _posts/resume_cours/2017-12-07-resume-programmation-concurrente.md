---
layout: post
title:  "Résumé programmation concurrente"
date:   2017-12-18 20:22:00 +0200
category: résumé
---

- [Paradigmes programmation](#paradigmes-programmation)
- [Les problèmes de la concurrence](#les-probl%C3%A8mes-de-la-concurrence)
- [Thread](#thread)
	- [Méthode du boss](#m%C3%A9thode-du-boss)
	- [Méthode de Peer to Peer](#m%C3%A9thode-de-peer-to-peer)
	- [Méthode du pipeline](#m%C3%A9thode-du-pipeline)
- [Création d'un thread](#cr%C3%A9ation-dun-thread)
- [Jointure d'un thread](#jointure-dun-thread)
- [Rendre le processeur](#rendre-le-processeur)

# Definition
* Programme **séquentiel** exécute les instructions les unes après les autres.
* Programme **concurrent** exécute plusieurs tâches à la fois, le temps de calcul est **partagé** entre les threads.
* Programme **parallèle** Sur plusieurs coeurs, les tâches se déroulent réelement en même temps.
	* Sur un seul coeur, .

S'il y a concurrence, plusieurs actions se déroulent en même temps. le programme devient alors non-déterministe (on ne connait pas l'ordre d'exécution).




























# Paradigmes programmation
* Séquentielle, le programme comporte un seul thread
* Concurrente, 2 ou plusieurs threads coopérent
Plusieurs thread s'exécutent en même temps
	* Application multi-contexte
	* Application parallèle
	* Application distribuée
* Temps réel, la notion de temps est très importante
Doit délivrer des résultats exacts dans des délais imposés

# Les problèmes de la concurrence
* Partage des ressources
* Difficulté à synchroniser les tâches
* Difficulté de prévoir le moment de l'exécution
* Difficulté de reproduire des séquences identiques

# Thread
* Un processus peut contenir plusieurs threads
* Un thread est un processus léger

## Méthode du boss
Un thread principal crée les autres threads et leur assigne une tâche
## Méthode de Peer to Peer
Statut des threads égals
Le thread pair crée les threads mais ne délègue pas de responsabilités
## Méthode du pipeline
Les threads sont l'un derrières l'autres

# Création d'un thread
arg n'est pas obligatoire
```c
pthread_t thread;
pthread_create(&thread, NULL, func, arg)

```

# Jointure d'un thread
Attend la fin du thread t
status n'est pas obligatoire
```c
int * status
if(pthread_join(t,(void **)&status) != 0) {
	printf("%d",*status);
}
```

# Rendre le processeur
Met le thread à la fin de la file d'attente des threads (0 = success)

```c
#include <sched.h>

int sched_yield();
```
