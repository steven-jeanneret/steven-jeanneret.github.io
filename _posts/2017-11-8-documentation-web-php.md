---
layout: post
title:  "Documentation PHP"
date:   2017-11-08 17:22:00 +0200
category: dev-web
---
# Balise PHP
```php
<?php
	echo ("<h1>Test</h1>")
?>
```
# Fonction utile
```php
$mots = explode(' ', $chaines); //Sépare les mots
$mots[0] = strtoupper($mots[0]); /*Mets le premier mots en majuscule*/
echo(pow($num)); //Carré de la fonction
echo htmlentities($ch); /*Convert character who have an entity in HTML*/
echo(rand(start,stop)); //Génère un random entre start et stop
echo date("H:i:s"); //Affiche l'heure
```
## Math
```php
echo(sin($x));
echo(cos($x));
```
# Tableau
```php
$tab = array(1,2,3); //Tableau classique
//Tableau associatif ou dictionnaire
$dico = array("num1" => 1, "num2" => 2, "num3" => 3);
foreach ($dico as $key => $value) {
	print($key . " => " . $value . "\n");
}
$tab = array_combine(tab1,tab2); //Combine 2 tableaux
if(in_array($val, $tab)) { /*Vérifie si la valeur se trouve dans le tableau*/
	print("is in tab");
}
if (array_key_exists($abo, $tab)) {/*Vérifie si la clé existe dans le tableau*/
echo(array_keys($tab)); //Retourne les clés du tableau
sort($tab); //Trie le tableau
```
# Fonction
```php
function perso($s) {
	print_r($s);
}
```
# Boucles
## For
```php
for ($i=0; $i < sizeof($tab); $i++) { 
	echo($tab[$i]);
}
```
## Foreach + range
```php
foreach (range(1,10) as $v) {
	print($v);
}
$tab=range(0, 63); //Create tab from 0 to 62
```
## Switch
```php
switch($var) {
	case "val1" :
		echo("val1");
		break;
	default:
		echo("not in tab");
}
```
#Variable global
```php
$a = 3;

function test() {
	echo $a; //ne marche pas
	global $a; //Import de la variable global
	echo $a; //Marche
}
```
# Importer un fichier php
```php
require "file.php";
```	

# Redirection
```php
header("Location: http://example.com/myOtherPage.php");
```

# Connexion à MYSQL avec PDO
```php
$PARAM = array(
	'host' => 'localhost',
	'port' => '3306',
	'dbname' => 'simple',
	'user' => 'root',
	'pwd' => 'pass1234'
);

$pdo = new PDO('mysql:host=' . $PARAM['host'] . 
	';port=' . $PARAM['port'] . ';dbname=' . 
	$PARAM['dbname'] , $PARAM['user'] , $PARAM['pwd']);
$result = $pdo->prepare("select * from personne");
$result->execute();
$result->setFetchMode(PDO::FETCH_OBJ);
while ($ligne = $result->fetch()) {
	print($ligne->nom . " : " . $ligne->email);
	print("<br />");
}
```

# Session
```php
session_start(); //Avant toute sortie!
if(isset($_SESSION['produits'])) {
	$produits = $_SESSION['produits']; //Get session var
} else {
	$_SESSION['produits'] = $produits; //Fix session var
}
echo($_SERVER['PHP_SELF']); //Show the URL
```
