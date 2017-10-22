---
layout: post
title:  "Documentation pour le cours de Java"
date:   2017-10-19 21:34:00 +0200
category: java
---
# Git
```bash
git clone ssh://java@157.26.83.27/home/java/git/WCoursJava.git
```
Password : ***h2o2017***

## 2 ème semaine
créer java2
cloner dans java2
travailler dans java2

## 3 ème semaine
créer java3
cloner dans java3
travailler dans java3


## Au projecteur
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

*Entry<T1,T2>*

> Peut on inverser Clé <=> valeur ?
>
> Non on ne peut garantir l'unicité des valeurs



## Wrapper

> Un wrapper est une classe qui encapsule le type

**Type** | **Wrapper**
--- | ---
double | double
long | Long
float | Float
int | Integer
char | Character

## Itérateur
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


## Enum
<span style="color:red">à vérifier</span>

Un enum type est une donnée spécial qui permet de définir une variable à certaines valeurs spécifiés.

```java
public enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY,
    THURSDAY, FRIDAY, SATURDAY 
}

Day d1 = Day.MONDAY;
```

## Classe incontournable
La classe **Arrays** permet de convertir un tableau en string
System.out.println(Arrays.toString(tab));
String





# A trier!


Garbage collector
Java tous est références

#Ajouter bout de codes pour chaque container et tous!

#Canevas
cmain
cmpu
cmpr
cjunit

# Test unitaire
JUnit Test Case //Framework
Télécharger les Jar => les copier dans workspace -> PDeploy -> Deploy -> ext
Créer une classe avec le canevas cjunit
Les @Test définisse que c'est un test JUnit

On mets une ou plusieurs assertions puis clic droit => run as -> JUnit Test

Création d'un junit pour tous le workspace : fléche verte de compilation -> RunConfigurations -> New JUnit -> TestAll (ou autre nom) -> Run all tests... -> PCoursJava -> Run

# Assertion
Importer de org.junit.Assert
Utile pour le debug permet de trouver l'erreur pour le développeur!
A mettre partout dans le code ou nécessaire
# Jar dans le Workspace
Copier les jar dans workspace -> PDeploy -> Deploy -> ext
Puis dans Package sélectionner PCoursJava -> Configure Build Path -> Add Library or Jars(chemin relatif) or External Jars (chemin absolu pas utilisé)

# Try Catch
sélection du bloc clic droit surround with -> try/catch

syserr -> System.err.println("Erreur"); //Permet d'envoyer un message d'erreurs (rouge)

sysexit -> System.exit(-1); //Permet d'arrêter le code

# Creer un jar
Dans bin on zip .ch en paramètre et on spécifie standard (pas optimisé)
On spécifie CoursJava.jar
On le mets dans pDeploy/Deploy
On édite le script run pour ajouter le chemin complet : ch.hearc.cours.kitbase.quadratique.UseQuadratiqueArgs a=1 b=-3 c=2
Cehmin du programme et paramètres