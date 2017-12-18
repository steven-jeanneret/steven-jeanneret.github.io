---
layout: post
title:  "Resumé algorithme"
date:   2017-11-16 21:22:00 +0200
category: résumé
---

- [Shell sort](#shell-sort)
	- [Pour les passages :](#pour-les-passages)
	- [La fonction sortArrayStep](#la-fonction-sortarraystep)
- [Heap sort](#heap-sort)
	- [Maximier](#maximier)
	- [Tri croissant](#tri-croissant)
- [Quick sort](#quick-sort)
- [Merge sort](#merge-sort)

# Types de tri
 - tri interne
	- s'effectue uniquement sur la mémoire principale nombre de donnée limitée
 - tri externe
	- utilise du stockage comme un disque dur (limite 1/2 taille du HDD)

# Tri bulle
* Fait remonter les petites valeurs en échangeant 2 valeurs l'un à coté de l'autre
* Parcours le tableau en inversant 2 valeurs (côtes à côtes) si la 1ère est plus grande
* On répète cette opération sur le tableau.
* O(n^2) stable
* Idéal pour détecter si un tableau est trié
* Tri caillou
	* Fait descendre les grosses valeurs
* Tri shaker
	* Combine le tri caillou et le tri bulle

# Tri extraction
* On cherche la plus petite valeur et on la mais devant
* On parcours le tableau pour trouver la plus petite valeur et on l'échange avec celle de gauche, on répète cela en décalant l'indice de gauche.
* O(n^2) pas stable
* Ne détecte pas si un tableau déjà trié

# Tri insertion
* On insère les éléments dans une partie déjà trié du tableau
* On regarde les éléments des indices  i et i+1 et quand la valeur est entre 2 on insère
* O(n^2) stable
* Pour un tableau partiellement trié

# Tri par base
* On tri en premier les unités puis les dizaines puis les centaines etc... (10 files => correspond à l'unité utilisée)
* o(n) stable
* Efficace en temps mais pas en mémoire

# Shell sort
Consiste à faire un tri par insertion avec des pas pour dégager les grandes valeurs en fin de tableau et les petites valeurs en début.
On réduit la taille des pas jusqu'à avoir un pas de 1 (insertion sort).

## Pour les pas 
```cpp
int h = 1;
while(h<size) {
	h = 3*h+1;
}
h = (h-1)/3;
clock_start = getTime();
while(h > 3) {
	h = (h - 1) / 3;
	sortArrayStep(tab, size, h);
}
sortArrayStep(tab, size, 1);
```

## La fonction sortArrayStep
```cpp
for (int i = 0; i < step; ++i) {
    for (int k = i + step; k < size; k += step) {
		int j = k - step;
		int curr = tab[k];
		while (j >= i && tab[j] > curr) {
			tab[j+step] = tab[j];
			j -= step;
			assignments++;
		}
		tab[j+step] = curr;
		assignments++;
	}
}
```

# Heap sort
> Tri par tas en français

On peut trouver les enfants d'un noeud grâce aux formules :

Pour le premier enfant : 2 * i + 1

Pour le deuxième enfant : 2 * i + 2

Pour trouver le dernier parents : size/2 - 1

## Maximier
Un maximier est un arbre ou les enfants ont une valeur inférieur à leur père.
Pour rendre un arbre maximier on parcours dans l'ordre inverse depuis le derniers parents, et on compare avec les enfants on montant la plus grande valeurs, si on a effectué un changement on rappel la fonction pour le noeud changé afin de vérifier, s'il y a un enfant plus grand que la nouvelle valeur montée.

```cpp
void build_heap_max(int* tab, int size) {
	int last_parent = size / 2 - 1;
	for (int i=last_parent; i>=0; i--) {
		heapify_max_rec(tab, size, i);
	}
}

void heapify_max_rec(int* tab, int size, int parent)
{
	int left = parent * 2 + 1;
	int right = parent * 2 + 2;
	int maxi = parent;
	
	if (left < size && tab[left] > tab[parent]) {
		maxi = left;
	}
	if (right < size && tab[right] > tab[maxi]) {
		maxi = right;
	}
	if (maxi != parent) {
		swap(tab, maxi, parent);
		heapify_max_rec(tab, size, maxi);
	} else {
		return;
	}
}
```

## Tri croissant
On sait que les enfants sont plus petit que le parent. Ainsi le maximum est la première valeur.
On commence par échanger la première valeur avec la dernière valeur non triée (size qu'on décremente au fur et à mesure). Ensuite on rend l'arbre à nouveau maximier pour que la 2ème plus grande valeur se trouve en haut.

```cpp
for (int i=size-1; i>0; i--) {
	swap(tab, 0, i);
	heapify_max_rec(tab, i, 0);
}
```

# Quick sort

Le principe du Quick sort consiste à choisir un pivot, ici nous prendrons toujours la première case (d'indice 0). Ensuite on compare les élèments du tableaux avec le pivot et on rangera tous ce qui est plus petit que le pivot dans les case 1 à x et tous ce qui est plus grand dans les cases x à size - 1. Puis on inverse le pivot et la dernière valeur échangé (à l'indice x).

Finalement on recommence la procédure avec 2 sous tableaux, l'un de 0 à x et l'autre de (x + 1) à (size - 1.) 

```cpp
void quick_sort(int* tab, int size, int n) {
	int last;
	if(size>2) {
		last = prep_quick_sort(tab,size);
	}
	
	if(size>3) {
		quick_sort(tab,last,n);
		quick_sort(tab+last+1,size-last,n);
	}
}

int prep_quick_sort(int* tab, int size) {
	int start = 1;
	int end = size-1;
	while(end > start) {
		while(tab[0] >= tab[start] && end > start) {
			start++;
		}
		while(tab[0] <= tab[end] && end > start) {
			end--;
		}
		swap(tab,start,end);
	}
	swap(tab,0,start-1);
	return start - 1;
}
```

# Merge sort
Ce tri consiste à décomposer le tableau en sous tableau jusqu'à avoir des tableaux de 2 élèments. Ensuite on va assembler ces sous tableaux en mettant les valeurs dans l'ordre dans un nouveau tableau, une fois dans l'ordre on remet ces valeurs dans le premier tableau.

```cpp
void merge_sort(int* a, int size) {
	if (size < 2) return;
	int h = size / 2;
	merge_sort(a, h);
	merge_sort(a+h, size-h);
	merge1(a, h, size);
}

void merge1(int* a, int middle, int size) {
	int c[size];
	merge2(a, middle, a + middle, size-middle, c);
	for (int i=0; i<size; i++) {
		a[i] = c[i];
	}
}

void merge2(int* tab1, int size1, int* tab2, int size2,int* tabRes) {
	int i = 0;
	int j = 0;
	while(i+j < size1 + size2) {
		if(tab1[i] < tab2[j] && i < size1 || j >= size2) {
			tabRes[i+j] = tab1[i];
			++i;
		} else {
			tabRes[i+j] = tab2[j];
			++j;
		}
	}
}

```