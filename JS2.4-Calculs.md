CALCUL, OPERATEUR et INCREMENTATION
===================================

La notion d'expression
----------------------

Une **expression** est un morceau de code qui produit une valeur. On
crée une expression en combinant des variables, des valeurs et des
opérateurs. Toute expression produit une valeur et correspond à un
certain type. Le calcul de la valeur d'une expression s'appelle
**l'évaluation**. Lors de l'évaluation d'une expression, les variables
sont remplacées par leur valeur.

``` js
// 3 est une expression dont la valeur est le nombre 3
const c = 3;
// c est une expression dont la valeur est celle de c (ici 3)
let d = c;
// (d + 1) est une expression. Sa valeur est celle de d augmentée de 1 (ici 4)
d = d + 1; // d contient la valeur 4
console.log(d); // Affiche 4
```

Une expression peut comporter des parenthèses qui modifient la priorité
des opérations lors de l'évaluation. En l'absence de parenthèses, la
priorité des opérateurs est la même qu'en mathématiques.

``` js
let e = 3 + 2 * 4; // e contient la valeur 11
e = (3 + 2) * 4; // e contient la valeur 20
```

Le langage JavaScript permet d'inclure des expressions dans une chaîne
de caractères lorsque cette chaîne est délimitée par une paire d'accents
graves seuls ou *backticks* (\`). Une telle chaîne est appelée un
*template literal* ou littéral de gabarit. A l'intérieur, les
expressions sont indiquées par la syntaxe `${expression}`.

On utilise souvent cette possibilité pour créer des chaînes intégrant
des valeurs de variables.

``` js
const pays = "France";
console.log(`J'habite en ${pays}`); // Affiche "J'habite en France"
const x = 3;
const y = 7;
console.log(`${x} + ${y} = ${x + y}`); // Affiche "3 + 7 = 10"
```

Incrémenter une variable de type nombre
---------------------------------------

Il est également possible d'augmenter ou de diminuer la valeur d'un
nombre avec les opérateurs `+=` et `++`. Ce dernier est appelé opérateur
d'**incrémentation**, car il permet d'incrémenter (augmenter de 1) la
valeur d'une variable.

Dans l'exemple suivant, les lignes 2 et 3 permettent chacune d'augmenter
la valeur de la variable `b` de 1.

``` js
let b = 0; // b contient la valeur 0
b += 1; // b contient la valeur 1
b++; // b contient la valeur 2
console.log(b); // Affiche 2
```
