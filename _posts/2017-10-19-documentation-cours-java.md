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
double | double
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
```

## Math
Exemple d'arrondi supérieur
```java
Math.ceil(nbLancees / (double)nbSimulations)
```

## Random
Exemple de nombre aléatoire entre 1 et size
```java
Random r = new Random(); 
int value = r.nextInt(size) + 1;
```

## String

# Canevas
Les canevas servent à générer un bout de code.
> mot clés => ctrl + espace

Canevas | utilisation
--- | ---
cmain | code de base d'un main
cmpu | ?
cmpr | ? 
cjunit | pour les tests unitaires

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
[Importer le jar](#importer-un-jar-dans-le-workspace)

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




# A trier!
Garbage collector
Java tous est références



# Creer un jar
Dans bin on zip .ch en paramètre et on spécifie standard (pas optimisé)
On spécifie CoursJava.jar
On le mets dans pDeploy/Deploy
On édite le script run pour ajouter le chemin complet : ch.hearc.cours.kitbase.quadratique.UseQuadratiqueArgs a=1 b=-3 c=2
Cehmin du programme et paramètres