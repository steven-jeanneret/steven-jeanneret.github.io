---
layout: post
title:  "Résumé réseau"
date:   2017-12-05 10:22:00 +0200
category: réseau
---

- [Introduction](#introduction)
	- [Compression de l'information](#compression-de-linformation)
- [Théorie de l'information](#th%C3%A9orie-de-linformation)
	- [Codage](#codage)
		- [Formes de codages](#formes-de-codages)
	- [Sources](#sources)
	- [Conversion A/D](#conversion-ad)
	- [Quantité de décision et débit](#quantit%C3%A9-de-d%C3%A9cision-et-d%C3%A9bit)
	- [Quantité d'information](#quantit%C3%A9-dinformation)
	- [Entropie](#entropie)
	- [Redondance](#redondance)
	- [Compression sans perte](#compression-sans-perte)
		- [Problèmes](#probl%C3%A8mes)
	- [Compression avec perte](#compression-avec-perte)
		- [Algorithmes](#algorithmes)
- [Les limites des canaux](#les-limites-des-canaux)
	- [Rapel logarithmes](#rapel-logarithmes)
	- [Etats électriques](#etats-%C3%A9lectriques)
	- [Débit de décision et débit de moment](#d%C3%A9bit-de-d%C3%A9cision-et-d%C3%A9bit-de-moment)
		- [Bande passante](#bande-passante)
		- [Débit de décision d'un canal parfait](#d%C3%A9bit-de-d%C3%A9cision-dun-canal-parfait)
		- [Débit de décision d'un canal physique](#d%C3%A9bit-de-d%C3%A9cision-dun-canal-physique)
		- [Rapport entre signal sur bruit](#rapport-entre-signal-sur-bruit)
- [Traitement des erreurs](#traitement-des-erreurs)
	- [Protection contre les erreurs de transmission](#protection-contre-les-erreurs-de-transmission)
	- [Hamming](#hamming)
	- [Condition pour la détection et la correction d'erreur](#condition-pour-la-d%C3%A9tection-et-la-correction-derreur)
	- [Détection d'erreur](#d%C3%A9tection-derreur)
		- [Parité](#parit%C3%A9)
		- [CRC](#crc)
			- [CRC par tranche](#crc-par-tranche)
- [Questions diverses](#questions-diverses)
	- [Rendement](#rendement)
		- [Rendements ldle RQ](#rendements-ldle-rq)
		- [Rendement Continuous RQ selective repeat](#rendement-continuous-rq-selective-repeat)
		- [Rendement Continuous RQ go-back-N](#rendement-continuous-rq-go-back-n)

# Introduction
## Compression de l'information
* Une suite de symboles codés sur 8 bits et produits aléatoirement.

> Chaque symbole prend 8 bits, aucune compression possible si purement aléaotire.

* Une suite formée d'un symbole toujours identique.

> On remarque qu'aucune information n'est transmise. On peut donc ne pas coder le symbole.

* Une suite formée de symboles alternant entre 0 et 1

> On remarque qu'aucune information n'est transmise. On peut donc ne pas coder le symbole.

* Une suite aléatoire dans l'ensemble [A-Z0-5]

> On peut coder sur 5 bits $$2^{5}=32 symboles$$




# Théorie de l'information
## Codage
Le codage représente un alphabet donné sous forme de bits en vue d'être transmis par la couche physique.
La forme de codage détermine l'efficacité et la résistance aux erreurs de transmission.

### Formes de codages
* Le codage de source à pour but de réduire la redondance, algorithme de compression/décompression, avec ou sans perte.
* Le codage de voie à pour but de protéger les données contre les perturbations, ajout de redondance pour détecter voir corriger les erreurs de transmission.

## Sources
Une **source d'information discrète** est un système capable de générer un flux d'information selon une loi statistique donnée, possède un alphabet fini.
Si la probabilité d'apparition d'un symbole dépend des symboles apparus jusque là on parle de **source de Markov** sinon de **source sans mémoire**
Les langues naturelles sont des source de Markov, après un *a* il y a plus de chance qu'un *n* apparaisse plutôt qu'un *e*.

## Conversion A/D
La première phase, l'échantillonnage prélève $$2f_{max}$$ échantillons/seconde. Le théorème de Nyquist dit que 8000 échantillons par seonde suffisent pour une fréquence entre 0 et 4 kHz (assuré par un filtre passe bas).
La deuxième phase, est la quantification, G.711 définit une quantification à 256 niveau (8 bits) (escalier qui approche les valeurs échantillonnées.
La troisième phase, le choix de la représentation binaire. Différent avantage selon le besoin.
Si l'échantillonnage de Nyquist est respecté, seule l'étape de quantification perd de l'information.2

## Quantité de décision et débit
Si on a n symboles à différencier, la quantité de décision vaut :
$$ D = [log_{2}(n)] bits$$
Ce chiffre ne tiens pas compte de la répartition des symboles.

Si on choisi un nombre de bits variables 
$$ D = l_{m}$$ représente la longueur moyenne des symboles en bits.

Le débit bianire peut être vu comme la dérivé de D par rapport au temps t.

## Quantité d'information
Les symboles apparaissant le plus souvent seront encodés sur le moins de bits possible.

$$ P_{i} est = \frac{nb apparition}{nb total apparition} $$

$$H_{i}=-log_{2}P_{i}$$

## Entropie
L'entropie est la quantité moyenne :

$$H=-\sum P_{i}*log_{2}(P_{i})$$

## Redondance
On pourra au mieux avoir une taille égale à l'entropie.
La redondance est le potentiel de compression de la source :

$$R = D - H$$

On tente d'élimier cette redondance en utilisant un codage le plus efficace possible.

## Compression sans perte
Plusieurs options s'offrent ici :

* Considérer la répartition statistique de chaque symbole, compression entropique classique (la seule sans mémoire)
	* Code de Shannon-Fano
		* Classe les symboles par probabilité descendante
		* On divise les symboles en deux sous-ensemble le plus égaux possible (nombre de redondance)
		* On attribue 0 à un groupe et 1 à l'autre
		* Puis on répète l'étape
	* Code de Huffman
		* On classe les symboles par probabilité descendante
		* On concatène les 2 derniers symboles et on somme leur fréquence d'apparition
		* Retrie le tableau et on regroupe de symbole jusqu'à ce qu'il n'y ai plus que 2 élèments
		* On construit un arbre et on attribut 0 à une branche et 1 à l'autre branche et on descend jusqu'au symbole
* Considérer que les données changent lentement, compression différentielle
* Considérer que certains symboles peuvent se répeter (Run Length Encoding)
* Considérer la répartition de sous-chaînes ou sous-textes (Lempel-Ziv)

### Problèmes
Les techniques différentielles peuvent propager les erreurs.

La répartition statistique nécessite l'échange des tables.

## Compression avec perte
A la décompression, toutes les données ne sont pas restituées. Perte irréversible.

Les fichiers multimédia tels que sons, images et vidéos peuvent avoir un ratio perte de données gain de place assez bon.

### Algorithmes
* Prédictif, définit un signal par rapport au passé ainsi qu'une variation du signal correspond bien à la musique
* Transformatifs, basés sur des constatations liés au sens humains. Résolution d'image basse lors d'un mouvement rapide, fréquence inaudible en musique.

# Les limites des canaux
## Rapel logarithmes
$$ log_{a}(x)=\frac{log_{b}(x)}{log_{b}(a)} $$

## Etats électriques
Il faut coder l'information de façon adaptée au support de transmission.
Pour un support de transmission électrique on peut :

* Utiliser 2 tensions une pour le 0 et une pour le 1
* Utiliser 4 tensions pour faire des paire de bits (00,01,10,11)
* Utilisation de $$2^{n}$$ pour transmettre n état du canal
* Utilisation de la modulation d'une porteuse

Sur fibre optique on peut représenter la valeur 1 par la présence de lumière.

## Débit de décision et débit de moment
Le débit de décision est donné en bits par seconde (bps), c'est le nombre de bits par état
Le débit de moment est donnée en Baud, la fréquence de changement d'état du canal. 

$$D = log_{2}(m)*M$$

D est le débit de décision (bps)

M est le débit de moment (Baud)

m est le nombre d'états

### Bande passante
$$M_{max} = 2B$$

B est la largeur de bande du canal (Hz)

### Débit de décision d'un canal parfait

$$D_{max}=C=M*log_{2}(m)$$

C est la vitesse de transmission maximale (bps)
Le débit n'est pas atteignable en pratique.

### Débit de décision d'un canal physique
Les canaux physique sont bruités :

$$D_{max}=C=B*log_{2}(1+\frac{S}{N})$$

S est la puissance du signal (Watt)
N est la puissance du bruit (Watt)

### Rapport entre signal sur bruit
Le rapport entre les puissances du signal et du bruit est indiqué en dB : 

$$\eta=SNR_{dB}=10log_{10}\frac{S}{N}$$




# Traitement des erreurs
La couche physique n'est pas fiable, les bits peuvent êtres modifiées au cours de la transmission.

La détection et/ou correction se fait dans la couche de liaison ou la couche de transport.

* Codage de source, suppression de la redondance par compression
* Codage de voie, ajout de redondance pour détection/correction d'erreurs.

## Protection contre les erreurs de transmission
* Ajout de redondance permettant de reconstruire l'information originale correcte. Permet de corriger un nombre limité d'erreurs et elle augmente les coûts de communication.
* Ajout de redondance permettant de détecter les erreurs sans pouvoir les corriger, retransmission nécessaire, plus léger.

## Hamming
La distance entre 2 mots code est obtenu en faisant un XOR entre les 2 mots code, on trouve le nombre de bits changeant et ça nous donne la distance. (si deux bits varie il y a une distance de 2)

## Condition pour la détection et la correction d'erreur
Si entre n'importe quel mots code valide il faut au moins 2 perturabations, on peut détecter une erreur.

Pour la correction il faut que 2 mots codes erronée (d'un bit) ne puisse être identique.

$$D_{Hamming}(N)\geq(E+1)$$ pour détecter E erreurs simples

$$D_{Hamming}(N)\geq(2E+1)$$ pour corriger E erreurs simples

N est l'ensemble des mots codes valides.

## Détection d'erreur
### Parité
Un mot de code de 7 bits sera transformé en un mot de code de 8 bits, ce 8ème bit vaut 1 s'il y a un nombre impair de bits, sinon il vaut 0. S'il y a une erreur de transmission on peut la détecter mais sans la corriger.
Pour corriger l'erreur il faudrait utiliser la parité double (horizontale et verticale).

### CRC
> Pour les trames de grande longueur avec possibilité d'erreurs en rafales

On ajoute *N* zéros derrière le message *M*, ou *N* = nombre de bit du diviseur *D* - 1 on obtiens *G*.

On divise *G* (avec des xor), Quand on descend un nombre à la fois, on note 1 si on descend 2 nombres à la fois on note 0. On obtiens un reste *R*.

On envoi le message *M* suivis de *R* (représenté sous *N* bits!) qui forme *O*.

On reçois *O* qu'on divise par *D*.

Si on obtiens 0, il n'y a pas eu d'erreur sinon il y a des erreurs.

#### CRC par tranche
Calcul du CRC par tranches de *n* nouveaux bits à chaque fois en partant du CRC précèdant.

symbole|signification
-----|-----
*c*|Anciens bits de redondance déjà calculés
*d*|Nouveaux bits de redondance à trouver
*r*|Nombre de bits du reste
*n*|Nombre de nouveaux bits de la tranche
*m*|Nombre de bits déjà pris en compte dans le message
*ab*|Juxtaposition des *m* et des *n*
*g*|Générateur, diviseur de r+1 bits
*/*|Reste de la division
*+*|Ou exclusif

# Questions diverses

DSLAM (multiplexeur des flux ADSL sur ATM) permet de transmettre sur différents canaux sur le même câbles physiques.

Backhaul toutes technologies qui se situent entre l'abonné et le réseau central.

Mode infrastructure : présence d'un AP, on peut atteindre de plus grande distance, possibilité d'étendre le réseau avec plusieurs AP.

Abaisser le MTU en PPPoE car présence d'entêtes de transport Ethernet supplémentaires qui limite la tailles des données disponibles pour les couches supérieures dont IP.

## Rendement

$$ P_{f}=1-(1-P)^{N} $$

P est le taux d'erreur de la ligne.

N est la taille du paquet (taille du messages si < taille max)

$$ a=\frac{T_{P}}{T_{ix}} $$

a est le rendement du protocole.

$$ T_{p} $$ est le temps de propagation

$$ T_{ix} $$ est le temps de propagation du message, obtenu par $$ T_{ix}=\frac{N}{D} $$

D est le débit en bits par seconde

### Rendements ldle RQ

* $$ U=\frac{1-P_{f}}{1+2a} $$

### Rendement Continuous RQ selective repeat

* $$ k<1+2a $$
	
	$$ U=\frac{k(1-P_{f})}{1+2a} $$

* $$ k\geq1+2a $$
	
	$$ U=1-P_{f} $$

### Rendement Continuous RQ go-back-N

* $$ k<1+2a $$
	
	$$ U=\frac{k(1-P_{f})}{(1+2a)(1+P_{f}(k-1))} $$

* $$ k\geq1+2a $$
	
	$$ U=\frac{1-P_{f}}{1+P_{f}(k-1)} $$