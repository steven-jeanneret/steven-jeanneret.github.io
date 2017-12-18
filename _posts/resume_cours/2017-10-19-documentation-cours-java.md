---
layout: post
title:  "Documentation pour le cours de Java"
date:   2017-10-19 21:34:00 +0200
category: résumé
---

- [Git](#git)
	- [Push](#push)
- [Convention](#convention)
- [Raccourci clavier](#raccourci-clavier)
- [Commentaire Java doc](#commentaire-java-doc)
- [Utilitaires](#utilitaires)
- [Théorie](#th%C3%A9orie)
- [Container](#container)
	- [Tableau](#tableau)
		- [Initialisation](#initialisation)
		- [Affichage](#affichage)
		- [Tableau 2 dimensions](#tableau-2-dimensions)
			- [Déclaration d'un tableau 2D](#d%C3%A9claration-dun-tableau-2d)
				- [Tableau rectangulaire simple](#tableau-rectangulaire-simple)
				- [Tailles des lignes différentes](#tailles-des-lignes-diff%C3%A9rentes)
	- [Liste](#liste)
		- [LinkedList](#linkedlist)
		- [ArrayList](#arraylist)
			- [Affichage](#affichage)
	- [Set](#set)
	- [Map, Dictionnaire](#map-dictionnaire)
		- [TreeMap](#treemap)
		- [HashMap](#hashmap)
			- [Insertion](#insertion)
			- [Affichage](#affichage)
- [Wrapper](#wrapper)
- [Itérateur](#it%C3%A9rateur)
- [Enum](#enum)
- [Classe incontournable](#classe-incontournable)
	- [Arrays](#arrays)
	- [Math](#math)
	- [Random](#random)
- [Canevas](#canevas)
- [Importer un jar dans le Workspace](#importer-un-jar-dans-le-workspace)
- [Assertion](#assertion)
- [Test unitaire](#test-unitaire)
	- [Test unitaire du workspace](#test-unitaire-du-workspace)
- [Try Catch](#try-catch)
- [Bonnes pratiques](#bonnes-pratiques)
	- [TODO et FIXME](#todo-et-fixme)
	- [Regénération du projet et test unitaire](#reg%C3%A9n%C3%A9ration-du-projet-et-test-unitaire)
- [Outils de monitoring](#outils-de-monitoring)
- [Programmation Orientée Objet](#programmation-orient%C3%A9e-objet)
	- [Constructeur](#constructeur)
	- [Constructeur par recopie](#constructeur-par-recopie)
	- [Méthode](#m%C3%A9thode)
	- [Attributs](#attributs)
	- [Stringbuilder](#stringbuilder)
	- [Tostring](#tostring)
	- [Classe inaltérable](#classe-inalt%C3%A9rable)
- [Accès aux attributs](#acc%C3%A8s-aux-attributs)
- [Static](#static)
- [Surcharge des opérateurs](#surcharge-des-op%C3%A9rateurs)
- [Réecriture](#r%C3%A9ecriture)
	- [Run](#run)
	- [Iterable](#iterable)
	- [equals](#equals)
	- [Clone](#clone)
- [hashcode](#hashcode)
	- [Héritage de la classe Object](#h%C3%A9ritage-de-la-classe-object)
- [Object](#object)
- [A trier!](#a-trier)
- [Déploiement suite](#d%C3%A9ploiement-suite)
- [Creer un jar](#creer-un-jar)

# Git
```bash
git clone ssh://java@157.26.83.27/home/java/git/WCoursJava.git
```

## Push
Sélectionner le projet du cours java 
Raccourci commit dans eclipse (à droite de +)
**CTRL + A** clic droit ajouter à l'index (tant que il y a qqch)
Sélectionner le projet Push (à gauche de +)

# Convention
small **camelCase** pour les variables
Big **CamelCase** pour les classes

# Raccourci clavier
**ctrl + 7**  commente la/les lignes
**ctrl + F11** lance le dernier programme
**ctrl + shift + f** formate le code pour la convention White Smith
**ctrl + shift + o** organise et purge les include
**ctrl + shift + s** Sauvegarde tout et compile
**alt + shift + r** Refactor 

# Commentaire Java doc
Commentaire java doc ```/**``` -> enter
Pour le voir : *Window -> ShowView -> JavaDoc*

# Utilitaires
*clic droit -> refactor -> rename* permet de changer le nom de l'objet dans tous le fichiers
*double clic* sur un onglet pour le plein écran.
kitebase *clic droit -> create -> new class*
```java
int nbLance = Integer.MAX_VALUE/100;
```
*Permet d'obtenir un nombre sans dépasser la valeur max du type!*

.toString() //automatique pour un affichage

syserr -> System.err.println("Erreur"); //Permet d'envoyer un message d'erreurs (rouge)

sysexit -> System.exit(-1); //Permet d'arrêter le code

# Théorie
Package : c'est un dossier qui permet l'unicité
Tous les objets sont créer avec **new** donc ils sont sur le tas,
Les pointeurs sont sur la pile,
**Pas de delete!**

**Static** on peut utiliser la méthode sans passer par un objet :
```java
ClasseNom.methode();
```

Java même type que C++ sauf les unsigned !

**JRE** Java Run Time
**JAR** Java Archive
**JDK** Java Developpement Kit

**Interface** liste de méthodes publiques non-statiques non-implémentés

Exemple d'interface : 
* List
* Set
* Runnable
* Iterable


# Container
## Tableau
### Initialisation
```java
int[] tab = { 1, 2, 3 }; //Méthode rapide pour créer un tableau
double[] tab = new double[] { 1, 2, 3 };
double[] tab = new double[3]; //Si on connait pas les valeurs
int size = tab.length; //Taille du tableau
```

### Affichage
```java
for(int i = 0; i < tab.length; i++) {
	System.out.println(tab[i]);
}

for(double valeur:tab) {
	System.out.println(valeur);
}

System.out.println(Arrays.toString(tab));
```
[La classe Arrays](#classe-incontournable)

### Tableau 2 dimensions
N'existe pas en informatique (mémoire linéaire), tableau 1D dans un tableau 1D
#### Déclaration d'un tableau 2D
##### Tableau rectangulaire simple
```java
double[][] tab2D = new double[n][m];
```
##### Tailles des lignes différentes
```java
double[][] tabExtern = new double[n][];
for(int i = 0; i < n; i++) {
	double[] tabLigne = new double[m];
	tabExtern[i] = tabLigne;
}
```

## Liste
### LinkedList
rapide pour ajouter ou supprimer des éléments
```java
List<Double> name = new LinkedList<Double>();
``` 

### ArrayList
rapide pour parcourir les éléments
```java
List<Double> name = new ArrayList<Double>();
```

ArrayList on peut spécifier la taille pour gagner en performance mais pas nécessaire!
```
List<Integer> list = Arrays.asList(1, 2, 3); //permet de créer rapidement une liste en 1 ligne
List<Double> name = new ArrayList<Double>(n);
```

> En déclarant une variable de type List plutôt que de type ArrayList
> On peut facilement passer de ArrayList à LinkedList

```java
list.add(value);
list.remove(value);
int nbElem = list.size();
```

#### Affichage

La plus pratique pour un affichage personnalisé :
```java
for(double element:list)
{
	System.out.println(element);
}
```

La plus rapide :
```java
System.out.println(list)
```

## Set
> Un set ne peut contenir qu'une fois la même valeur.

```java
Set<Double> set = new TreeSet<Double>();
set.add(Math.PI);

{//v1
	for(Double element:set) {
		System.out.println(element);
	}
}
{//v3
	System.out.println(set);
}
```

## Map, Dictionnaire
> Système de clé valeur

### TreeMap
```java
Map<String, Integer> name = new TreeMap<String, Integer>();
```
On peut trier par clé, l'ordre est conservé

### HashMap
```java
Map<String, Integer> name = new HashMap<String, Integer>(n);
```
Plus rapide mais l'ordre est incertain

n facultatif, sert d'optimisation

#### Insertion
```java
map.put("Personne" + i, i);
```

#### Affichage
Set<Entry<String, Integer>> set = map.entrySet();
for(Entry<String, Integer> entry:set) {
	{
		String clef = entry.getKey();
		Integer valeur = entry.getValue();
		System.out.println(clef + " = " + valeur);
	}
	{
		System.out.println(entry); //Version plus courte
	}
}

*Entry<T1,T2>*

> Peut on inverser Clé <=> valeur ?
>
> Non on ne peut garantir l'unicité des valeurs

# Wrapper

> Un wrapper est une classe qui encapsule le type

**Type** | **Wrapper**
--- | ---
double | Double
long | Long
float | Float
int | Integer
char | Character

# Itérateur
> Peut servir au parcours d'une liste

```java
Iterator<Double> it = list.iterator();
while(it.hasNext()) {
	double element = it.next(); //unboxing automatique Double->double
	System.out.println(element);
}
```

Conversion de wrapper avec les itérateurs
```java
double y = ity.next().doubleValue();
Double y = ity.next();
double y = ity.next(); //Le compilateur fait la conversion objet -> type simple
```

# Enum
<span style="color:red">à vérifier</span>

Un enum type est une donnée spécial qui permet de définir une variable à certaines valeurs spécifiés.

```java
public enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY,
    THURSDAY, FRIDAY, SATURDAY 
}

Day d1 = Day.MONDAY;
```

# Classe incontournable
## Arrays
Permet par exemple de convertir un tableau en string
```java
System.out.println(Arrays.toString(tab));
Arrays.sort(tab);
```

## Math
Exemple d'arrondi supérieur
```java
Math.ceil(nbLancees / (double)nbSimulations)
```
atan2 permet de faire im/re sans ce soucier que re peut être = 0

## Random
Exemple de nombre aléatoire entre 1 et size
```java
Random r = new Random(); 
int value = r.nextInt(size) + 1;
```

# Canevas
Les canevas servent à générer un bout de code.
> mot clés => ctrl + espace

Canevas | utilisation
--- | ---
cmain | code de base d'un main
cmpu | ?
cmpr | ? 
cjunit | pour les tests unitaires
csa | canevas static attributs
ci | canevas is
cs | canevas static

# Importer un jar dans le Workspace
> Copier le jar dans workspace -> PDeploy -> Deploy -> ext

Puis dans la vue Package 
> sélectionner PCoursJava -> Configure Build Path -> Add Library or Jars(chemin relatif) or External Jars (chemin absolu pas utilisé)

# Assertion
Utile pour le debug permet de localiser une erreur pour le développeur!
Une assertion est une condition *true / false*, si elle est fausse, cause l'arrêt du programme.
Importer de org.junit.Assert
A mettre partout dans le code ou nécessaire

Ici on s'assure que les 2 listes ai la même taille.
```java
Assert.assertTrue(list1.size()==list2.size());
```

# Test unitaire
Dans les tests unitaires on prend des valeurs différentes de 1 et 0, ainsi que des mêmes chiffres.

> Un assert par fonction test.

Utiliser le canevas cjunit dans une nouvelle classe.
Le @Test permet de définir que la fonction qui suit est un test.
Ici on vérifie que le résultat espéré est bien le résultats obtenu.
```java
@Test
public void testLineaire1() {
	int a = 12;
	int b = 24;
	double xEmpirique = Lineaire.solve(a, b);
	double xTheorique = -2;
	Assert.assertTrue(xEmpirique == xTheorique);
}
```
> Clic droit => Run AS JUnit Test

## Test unitaire du workspace
<span style="color:red">à compléter</span>
Pour exécuter tous les tests unitaires du workspace :
> Dans les options de build ouvrir RunConfigurations
Création d'un junit pour tous le workspace : fléche verte de compilation -> RunConfigurations -> New JUnit -> TestAll (ou autre nom) -> Run all tests... -> PCoursJava -> Run

# Try Catch
Sélection du bloc clic droit surround with -> try/catch

```java
try {
	String[] tab = bloc.split("=");
	double value = Double.valueOf(tab[1]);

	mapABCValeurs.put(tab[0], value);
}
catch (NumberFormatException e) {
	System.err.println("Mode d'emploi");
	System.exit(-1); // 0 normal, -1 anormal
}
```

# Bonnes pratiques
<span style="color:red"> Vérifier le code</span>
Ne **jamais** modifier les valeurs passées en paramètres, copier(cloner) puis trier.

> Si le code est général et réutilisable on fait une bibliothèque pour pouvoir la réutiliser et la partager.

## TODO et FIXME
```java
//TODO commentaire permettant de revenir rapidement
//FIXME commentaire permettant de revenir rapidement
```

## Regénération du projet et test unitaire
Supprimer les fichiers compilé :

On supprime le ch dans bin

Regeneration des fichiers compilé

Project -> clean -> nettoyer tous

Lancer les tests unitaires de tous le projet

# Outils de monitoring 
jvisualvm (Raccourci bureau)
On voit les machines virtuelles java qui sont entrain de tourner. (faire un long sleep pour qu'elle reste allumer).
On peut voir voit les propriétés.
On va la récupérer depuis le code java : 
```java
String name = System.getProperty("user.name");
```

# Programmation Orientée Objet
Structure est un container multi types

## Constructeur
Construit les données

## Constructeur par recopie
On appel le constructeur principal depuis le constructeur secondaire.
```java
A(int m) {
	this.m = m;
}

A(A src) {
	this(A.m());
}
```

L'appel d'un constructeur principal depuis un constructeur secondaire, doit se faire à la 1ère ligne.
L'astuce est de faire une méthode static pour copier le tableau. 

> Si la méthode n'est pas static on ne peux l'appeler avant d'avoir créer l'objet or on veut l'appeler avant la construction!

Pour un type simple on copie la valeur pas le pointeur donc pas de new dans le constructeur par copie.

## Méthode
Modifie les données

## Attributs
Contienne les données
* Input
* Tools
* Output

On commence par créer les attributs 
puis clic droit sources -> generate constructor using Fields
clic droit sources -> generate tostring

## Stringbuilder
Permet de construire une string
on tapes : marque : " + this.brand ...

on le séléectionnes et quick fix -> extract Use stringbuilder

## Tostring
Source generate to string

## Classe inaltérable 
Classe dont les données ne sont pas modifiées via des setters.
> String est une classe inaltérable

```java
String str = "Pirelli"; //Créer l'objet pirelli
str = "Continental"; //Créer un nouvel objet Continental
```
Quand on modifie un string, il crée un nouvel objet, on ne modifie pas l'ancien!

# Accès aux attributs
On peut accèder aux attributs private depuis une classe, les getters servent uniquement à l'extérieur de la classe.


# Static 
Si on utilise pas this (attribut) dans la méthode c'est qu'elle doit être static.

# Surcharge des opérateurs
> En java, il n'y a pas de surcharge des opérateurs!

c3 = c1 + c2 devient :
c3 = c1.add(c2);

```java
public Complexe add(Complexe z2)
	{
	return new Complexe(this.x + z2.x, this.y + z2.y);
	}
```

# Réecriture
... changer le nom
## Run
implements Runnable //a la suite de la déclaration de la classe 
```java
public class Lineaire implements Runnable
```

Ensuite on peut générer le run en restant sur l'erreur du nom de classe
```java
@Override
public void run() {
	x = -b/a;
}
```

## Iterable
```java
for(Type var:Iterable<T>)
```
> Iterable est l'objet qu'on veut parcourir
Pour une classe, il faudra implémenter Iterable.

```java
public class Garage implements Iterable<Car>

...

@Override
public Iterator<Car> iterator(); {
	return listCars.iterator();
}
```

## equals
equals ctrl + space permet de récrire equals
```java
@Override
public boolean equals(Object obj)
	{
	if (obj instanceof Complexe)
		{
		return this.isEquals((Complexe)obj);
		}
	else
		{
		return false;
		}
	}
```

## Clone
clo -> clone
```java
public Complexe cloneOf()
		{
		return new Complexe(this);
		}

@Override
protected Complexe clone() throws CloneNotSupportedException
	{
	return this.cloneOf();
	}
```

2 objets égaux doivent avoir le même hashcode.
Ce n'est pas parce 2 objets ont le même hashcode qu'ils sont égaux.
# hashcode
```java
@Override
public int hashCode()
	{
	return 1;
	}
```
return 1 if is equals

## Héritage de la classe Object
Toutes les classes hérites de Object 
# Object 
+ toString()
+ equals()
+ close()
+ hashcode()






# A trier!

Garbage collector

Java tous est références

# Déploiement suite
Dans eclipse on exécute des fichiers .class
Pour le déploiement on veut faire des packages donc on prend nos fichiers .class on les transforme en .jar (via .zip)

On mets tous dans Deploy
copier/coller soft -> java -> jre dans workspace...../...../Deploy/
On ajoute le nom qualitfié de la classe
On édite run.cmd  pour savoir quel fichier on va exécuter -> ch.hear.cours................UseQuadratiqueClavier
Et on décommente :
```bash
rem set JRE_PATH=./jre/bin
rem set PATH=%JRE_PATH%;%PATH%
```

Création du jar
On zip ch de bin avec l'algorithme zip et on renomme l'extension .zip en .jar
On place ce .jar dans deploy

On copie le folder deploy dans la machine virtuel

On lance le run



# Creer un jar
Dans bin on zip .ch en paramètre et on spécifie standard (pas optimisé)
On spécifie CoursJava.jar
On le mets dans pDeploy/Deploy
On édite le script run pour ajouter le chemin complet : ch.hearc.cours.kitbase.quadratique.UseQuadratiqueArgs a=1 b=-3 c=2
Cehmin du programme et paramètres