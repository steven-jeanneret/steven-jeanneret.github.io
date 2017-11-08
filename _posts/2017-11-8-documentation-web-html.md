---
layout: post
title:  "Documentation HTML"
date:   2017-11-08 15:34:00 +0200
category: dev-web
---
# Fichier HTML de base
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Titre apparaissant dans l'onglet</title>
	</head>
	<body>
		<h1>Premier titre</h1>
	</body>
</html>
```
# Commentaire
```html
<!-- ceci est un commentaire -->
```

# Eléments

## Titre
```html
<h1>Titre de niveau 1</h1>
<h2>Titre de niveau 2</h2>
<h3>Titre de niveau 3</h3>
<h4>Titre de niveau 4</h4>
<h5>Titre de niveau 5</h5>
<h6>Titre de niveau 6</h6>
```

## Paragraphe
```html
<p>Paragraphe</p>
<p>Retour auto à la ligne entre 2 paragraphes</p>
```

## Lien
```html
<a href="link.html">Mon lien</a>
```

## Image
```html
<img src="img/picture.jpg" alt="Texte" />
<!-- alt s'affiche à la place de l'image en cas d'erreur -->
```

## Listes
```html
<ul>
	<li>Premier item</li>
</ul>
<ol>
	<li>Premier item numeroté</li>
</ol>
<dl>
	<dt>Mot</dt><dd>Définition</dd>
</dl>
```



## Divers

### Bar horizontal
```html
<hr />
```
### Retour à la ligne
```html
<br />
```
### Indice et exposant
```html
f<sub>i</sub>(x)=x<sup>e</sup>
```



# Formulaire
```html
<form method="post" action="redirect.php">
	<p>
		<label for="name">Nom :</label>
		<input type="text" id="nom" />
	</p>
	<p>
		<label for="password">Mot de passe</label>
		<input type="password" id="password" />
	</p>
	<p>
		<label>Couleur :
			<input type="radio" id="chkbox1" value="rouge" name="color">
			<label for="rouge">Rouge</label>
			<input type="radio" id="chkbox2" value="bleu" name="color" checked="checked">
			<label for="bleu">Bleu</label>
		</label>
	</p>
	<p>
		<select name="city" >
			<option value="Neuchâtel">Neuchâtel</option>
			<option selected="selected" value="Montreux">Montreux</option>
		</select>
	</p>
	<p>
		<input type="submit" value="Envoyer"/>
		<input type="reset"  name=".reset" />
	</p>
</form>
```

# Tableau
```html
<table>
	<tr>
		<th>Titre 1</th>
		<th>Titre 2</th>
	</tr>
	<tr>
		<td>Elem 1</td>
		<td>Elem 2</td>
	</tr>
	<tr>
		<td rowspan="2" colspan="2">2 colonnes + 2 lignes</td>
	</tr>
</table>
```