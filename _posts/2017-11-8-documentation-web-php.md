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
$mots[0] = strtoupper($mots[0]); //Mets le premier mots en majuscule
echo(pow($num)); //Carré de la fonction
```
# Tableau
```php
$tab = array(1,2,3); //Tableau classique
//Tableau associatif ou dictionnaire
$dico = array("num1" => 1, "num2" => 2, "num3" => 3);
foreach ($dico as $key => $value) {
	print($key . " => " . $value . "\n");
}
```
# Fonction
```php
function perso($s) {
	print_r($s);
}
```