TYPES et VALEURS !
==================

Une **valeur** est un morceau d'information utilisé dans un programme
informatique. Les valeurs existent sous différentes formes, appelées des
types.

Le **type** d'une valeur détermine son rôle et les opérations qui lui
sont applicables.

Chaque langage informatique dispose d'une panoplie de types qui lui est
propre. Nous allons étudier deux des principaux types disponibles en
JavaScript.

### Le type nombre

Une valeur de type **nombre** (*number*) représente une valeur
numérique, autrement dit une quantité. Comme en mathématiques, on
distingue les valeurs entières (ou entiers) 0, 1, 2, 3... et les valeurs
réelles (ou réels) auxquelles on ajoute des chiffres après la virgule
pour plus de précision.

I&gt; La virgule s'exprime en informatique sous la forme d'un point :
`3.14` et non `3,14` !

Les nombres servent essentiellement à compter. Nous pouvons appliquer à
des valeurs de type nombre les mêmes opérations qu'en mathématiques. Ces
opérations produisent un résultat lui aussi de type nombre. Les
principales opérations applicables sont rassemblées dans le tableau
suivant.

| Opérateur | Rôle           |
|-----------|----------------|
| `+`       | Addition       |
| `-`       | Soustraction   |
| `*`       | Multiplication |
| `/`       | Division       |

### Le type chaîne

Une valeur de type **chaîne de caractères** (en abrégé chaîne, ou
*string*) représente un texte. Ces valeurs sont délimitées par une paire
de guillemets doubles : `"Ceci est une chaîne"`.

I&gt; Il est également possible de délimiter une chaîne de caractères
avec une paire de guillemets simples : `'Ceci est aussi une chaîne'`.
Par convention, nous emploierons les guillemets doubles dans tous les
exemples de code de ce cours. L'important est d'être cohérent : utilisez
l'une ou l'autre notation, mais ne mélangez pas les deux.

E&gt; Il ne faut surtout pas oublier de "fermer" une chaîne : simples ou
doubles, les guillemets vont toujours par deux !

Pour inclure dans une chaîne certains caractères spéciaux, on utilise le
caractère `\` (prononcé "antislash" ou "backslash" en anglais) qui donne
un sens particulier au caractère suivant. Par exemple, `\n` permet
d'ajouter un retour à la ligne dans une chaîne :
`"Ceci est une chaîne\nSur plusieurs lignes"`.

On ne peut pas additionner ou supprimer des valeurs de type chaîne comme
on peut le faire avec des nombres. En revanche, l'opérateur `+` peut
être appliqué à deux valeurs de type chaîne. Son résultat est la
jointure de ces deux chaînes, appelée **concaténation**. Par exemple,
`"Bon"+"jour"` produit le résultat `"Bonjour"`.

Conversions de types
--------------------

L'évaluation d'une expression peut entraîner des conversions de type.
Ces conversions sont dites **implicites** : elles sont faites
automatiquement, sans intervention du programmeur. Par exemple,
l'utilisation de l'opérateur `+` entre une valeur de type chaîne et une
valeur de type nombre provoque la concaténation des deux valeurs dans un
résultat de type chaîne.

``` js
const f = 100;
// Affiche "La variable f contient la valeur 100"
console.log("La variable f contient la valeur " + f);
```

Le langage JavaScript est extrêmement tolérant au niveau des conversions
de type. Cependant, il se peut qu'aucune conversion ne soit possible. En
cas d'échec de la conversion d'un nombre, la valeur du résultat est
`NaN` (*Not a Number*).

``` js
const g = "cinq" * 2;
console.log(g); // Affiche NaN
```

Il arrive parfois que l'on souhaite forcer la conversion d'une valeur
dans un autre type. On parle alors de conversion **explicite**. Pour
cela, JavaScript dispose des instructions `Number()` et `String()` qui
convertissent respectivement en un nombre et une chaîne la valeur placée
entre parenthèses.

``` js
const h = "5";
console.log(h + 1); // Concaténation : affiche la chaîne "51"
const i = Number("5");
console.log(i + 1); // Addition numérique : affiche le nombre 6
```
