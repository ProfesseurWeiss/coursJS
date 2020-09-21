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
