Interactions avec l'utilisateur
===============================

Saisie et affichage à l'écran
-----------------------------

Maintenant que nous savons utiliser des variables, nous pouvons écrire
des programmes qui échangent des informations avec l'utilisateur.

``` js
const prenom = prompt("Entrez votre prénom :");
alert(`Bonjour, ${prenom}`);
```

A l'exécution, une première boîte de dialogue apparaît pour demander la
saisie du prénom.

![Résultat de l'exécution](images/08-01.png)

Cette boîte est le résultat de l'exécution de l'instruction JavaScript
`prompt("Entrez votre prénom :")`.

Après saisie du prénom, une seconde boîte affiche un "bonjour"
personnalisé.

![Résultat de l'exécution](images/08-02.png)

La valeur saisie dans la première boîte de dialogue a été stockée dans
une variable de type chaîne nommée `prenom`. Ensuite, l'instruction
JavaScript `alert()` a déclenché l'affichage de la seconde boîte,
contenant le message d'accueil.

Affichage dans la console
-------------------------

Nous avons vu dans le précédent chapitre que l'instruction JavaScript
`console.log()` permettait d'afficher une information.

I&gt; On désigne par "console" une zone d'informations textuelles.
L'instruction `console.log()` ne fait pas à proprement parler partie de
la spécification du langage JavaScript. Cependant, la très grande
majorité des environnements JavaScript, et notamment les navigateurs
web, disposent d'une console dans laquelle il est possible d'afficher
des informations.

On peut donc utiliser soit `console.log()`, soit `alert()` pour afficher
des informations à l'utilisateur. Contrairement à `alert()`,
`console.log()` ne bloque pas l'exécution du programme, ce qui en fait
souvent un meilleur choix.

Il est possible d'utiliser `console.log()` pour afficher plusieurs
valeurs simultanément, en les séparant par des virgules.

``` js
const temp1 = 36.9;
const temp2 = 37.6;
const temp3 = 37.1;
console.log(temp1, temp2, temp3); // Affiche "36.9 37.6 37.1"
```

Saisie d'un nombre
------------------

Quel que soit le texte saisi, l'instruction `prompt()` renvoie toujours
une valeur de type chaîne. Il faudra penser à convertir cette valeur
avec l'instruction `Number()` si vous souhaitez ensuite la comparer à
d'autres nombres ou l'utiliser dans des expressions mathématiques.

``` js
const saisie = prompt("Entrez un nombre : "); // saisie est de type chaîne
const nb = Number(saisie); // nb est de type nombre
```

Il est possible de combiner les deux opérations (saisie et conversion)
en une seule ligne de code, pour un résultat identique :

``` js
const nb = Number(prompt("Entrez un nombre : ")); // nb est de type nombre
```

Ici, le résultat de la saisie utilisateur est directement converti en
une valeur de type nombre par l'instruction `Number()` et affecté à la
variable `nb`.
