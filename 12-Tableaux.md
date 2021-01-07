Les tableaux
============

Introduction : le rôle des tableaux
-----------------------------------

Imaginez que vous souhaitiez informatiser la liste de tous les films que
vous avez vus récemment. Une première solution serait de créer une
variable par film, comme dans l'exemple suivant.

``` js
const film1 = "Le loup de Wall Street";
const film2 = "Vice-Versa";
const film3 = "Babysitting";
// ...
```

Si vous êtes cinéphile, vous risquez rapidement de vous retrouver avec
un grand nombre de variables dans votre programme. Pire, toutes ces
variables sont entièrement indépendantes. Il n'existe aucun moyen pour,
par exemple, afficher la liste complète des films ou rechercher un titre
dans la liste.

On pourrait stocker tous les titres dans une unique chaîne de
caractères, en choisissant un caractère pour délimiter les titres.

``` js
const films = "Le loup de Wall Street - Vice-Versa - Babysitting - ...";
```

Cette chaîne risque de devenir exagérément longue, et que faire si le
caractère délimiteur est également présent dans le titre d'un film,
comme c'est le cas ici ?

Il faudrait trouver une solution pour mémoriser ensemble plusieurs
éléments sans devoir les nommer individuellement. Cette solution existe
: ce sont les tableaux.

Un **tableau** est un type de donnée qui permet de stocker un ensemble
d'éléments. Découvrons comment utiliser les tableaux en JavaScript.

Manipulation des tableaux en JavaScript
---------------------------------------

En JavaScript, un tableau est un objet disposant de propriétés
particulières.

### Créer un tableau

Voici comment créer notre liste de films sous la forme d'un tableau.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
```

On crée un tableau à l'aide d'une paire de crochets `[]`. Tout ce qui se
trouve entre les crochets correspond au contenu du tableau. Les
différents éléments stockés sont séparés par des virgules.

Avec JavaScript, on peut stocker dans un tableau des éléments de
différents types, comme dans l'exemple ci-dessous.

``` js
const tableau = ["Bonjour", 7, { message: "Coucou maman" }, true];
```

> Puisqu'un tableau est destiné à contenir plusieurs éléments, une bonne
> pratique consiste à donner aux variables tableaux des noms exprimant
> le pluriel, comme par exemple `films`, `tabFilms` ou encore
> `lesFilms`.

### Obtenir la taille d'un tableau

Le nombre d'éléments stockés dans un tableau est appelé sa **taille**.
Voici comment l'obtenir.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
console.log(films.length); // 3
```

La taille d'un tableau s'obtient en lui appliquant la propriété
`length`. Bien entendu, cette propriété renvoie 0 dans le cas d'un
tableau vide (sans aucun élément).

``` js
const tableauVide = []; // Création d'un tableau vide
console.log(tableauVide.length); // 0
```

### Accéder à un élément d'un tableau

Chaque élément présent dans un tableau est identifié par un numéro,
appelé son **indice** (index en anglais). On peut représenter
graphiquement un tableau comme un ensemble de cases, chacune stockant
une valeur spécifique et associée à un indice. Voici comment on pourrait
représenter le tableau `films`.

![Représentation du tableau](images/chapter07-01.png)

L'accès à un élément s'effectue en plaçant cet indice entre crochets,
comme dans l'exemple ci-dessous.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];

console.log(films[0]); // "Le loup de Wall Street"
console.log(films[1]); // "Vice-Versa"
console.log(films[2]); // "Babysitting"
```

> L'indice du premier élément d'un tableau est 0 et non 1 comme on
> aurait pu s'y attendre. Le plus grand indice utilisable est donc égal
> à la taille du tableau - 1.

Utiliser un indice invalide pour accéder à un élément d'un tableau
JavaScript renvoie la valeur spéciale `undefined`.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];

console.log(films[3]); // undefined : le dernier indice valide est 2
```

Dans d'autres langages, cela provoque une erreur : à éviter !

Parcourir un tableau
--------------------

Il existe plusieurs solutions pour parcourir un tableau élément par
élément.

La première consiste à utiliser la boucle `for` que vous connaissez
déjà. L'exemple ci-dessous permet d'afficher la liste des films présents
dans le tableau.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];

for (let i = 0; i < films.length; i++) {
  console.log(films[i]);
}
```

Avec la boucle `for`, on fait varier l'indice du tableau de 0 (indice du
premier élément) à *taille du tableau - 1* (indice du dernier) pour
accéder aux éléments les uns après les autres.

Une autre solution consiste à utiliser la méthode `forEach()` sur le
tableau. Celle-ci permet d'appliquer une fonction sur chaque élément du
tableau. Voici l'exemple précédent réécrit avec forEach().

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
films.forEach(film => {
  console.log(film);
});
```

Lors de l'exécution, chaque élément du tableau est successivement passé
en paramètre à la fonction anonyme associée à la méthode `forEach()`.

> Attention à bien écrire `forEach()` avec un E majuscule, et à
> distinguer le tableau (ici `films`) de l'élément passé à la fonction
> (ici `film`). On voit ici l'intérêt de nommer les variables tableaux
> au pluriel.

Une troisième solution pour parcourir un tableau est d'utiliser la
boucle `for-of`, introduite récemment dans le langage. Elle a l'avantage
de ne pas nécessiter la gestion d'un compteur de boucle.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];

for (const film of films) {
  console.log(film);
}
```

Modifier le contenu d'un tableau
--------------------------------

### Ajouter un élément dans un tableau

Inutile de nier : vous avez craqué et regardé Les Bronzés pour la 7ème
fois.

![Jean-Claude, pense à ta licence !](images/chapter07-02.jpeg)

Ajoutons ce film à notre liste.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
films.push("Les Bronzés"); // Ajoute le film à la fin du tableau
console.log(films[3]); // "Les Bronzés"
```

L'ajout d'un nouvel élément dans un tableau se fait avec la méthode
`push()`. Elle prend en paramètre l'élément à insérer, qui est ajouté à
la fin du tableau.

Une autre méthode, `unshift()`, permet d'ajouter l'élément au début du
tableau.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
films.unshift("Les Bronzés"); // Ajoute le film au début du tableau
console.log(films[0]); // "Les Bronzés"
```

### Supprimer un élément d'un tableau

On peut supprimer le dernier élément d'un tableau grâce à la méthode
`pop()`.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
films.pop(); // Supprime le dernier élément
console.log(films.length); // 2
console.log(films[2]); // undefined
```

Une autre méthode de suppression, `splice()`, permet de supprimer
plusieurs éléments d'un coup. Son premier paramètre est l'indice à
partir duquel supprimer, et le second est le nombre d'éléments à
supprimer.

``` js
const films = ["Le loup de Wall Street", "Vice-Versa", "Babysitting"];
films.splice(0, 1); // Supprime 1 element à partir de l'indice 0
console.log(films.length); // 2
console.log(films[0]); // "Vice-Versa"
console.log(films[1]); // "Babysitting"
```
