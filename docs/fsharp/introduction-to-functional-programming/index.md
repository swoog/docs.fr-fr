---
title: Introduction à la programmation fonctionnelle en F#
description: Découvrez les principes fondamentaux de la programmation fonctionnelle dans F#.
ms.date: 10/29/2018
ms.openlocfilehash: 84022e58c0f17b9e9875402c653c31e494e940da
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772786"
---
# <a name="introduction-to-functional-programming-in-f"></a>Introduction à la programmation fonctionnelle en F\#

Programmation fonctionnelle est un style de programmation qui met l’accent sur l’utilisation de fonctions et données immuables. Programmation fonctionnelle typée est lors de la programmation fonctionnelle est combinée avec des types statiques, telles que F#. En règle générale, les concepts suivants sont mis en évidence dans la programmation fonctionnelle :

* Fonctions en tant que les constructions principales que vous utilisez
* Expressions au lieu d’instructions
* Valeurs immuables sur les variables
* Programmation déclarative sur la programmation impérative

Tout au long de cette série, vous allez découvrir les concepts et modèles de programmation fonctionnelle à l’aide de F#. Tout au long du processus, vous découvrirez certaines F# trop.

## <a name="terminology"></a>Terminologie

Programmation fonctionnelle, telles que d’autres paradigmes de programmation est fourni avec un vocabulaire dont vous aurez besoin par la suite pour en savoir plus. Voici certains termes courants, vous verrez tout le temps :

* **Fonction** -une fonction est une construction qui produit une sortie en fonction d’une entrée. Plus formellement, il _mappe_ un élément à partir d’une valeur à un autre ensemble. Cette formalisme est capturée dans la concret dans bien des égards, surtout lorsque vous utilisez des fonctions qui opèrent sur des collections de données. Il est le meilleur parti des concept de base (et important) dans la programmation fonctionnelle. 
* **Expression** -une expression est une construction dans le code qui génère une valeur. Dans F#, cette valeur doit être liée ou explicitement ignorée. Une expression peut être simplement remplacée par un appel de fonction.
* **Pureté** -pureté est une propriété d’une fonction telle que sa valeur de retour est toujours le même pour les mêmes arguments, et que son évaluation n’a aucun effet secondaire. Une fonction pure dépend entièrement de ses arguments.
* **Transparence référentielle** -transparence référentielle est une propriété des expressions telles qu’elles puissent être remplacées sans affecter le comportement d’un programme avec leur sortie.
* **Immuabilité** -signifie d’immuabilité qu’une valeur ne peut pas être modifié sur place. Ceci est le contraire des variables qui peuvent changer en place.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent ces concepts fondamentaux.

### <a name="functions"></a>Fonctions

Les plus courantes et fondamentale de programmation fonctionnelle est la fonction. Voici une fonction simple qui ajoute 1 à un entier :

```fsharp
let addOne x = x + 1
```

Sa signature de type est la suivante :

```fsharp
val addOne: x:int -> int
```

La signature peut être lu comme, «`addOne` accepte un `int` nommé `x` et produira un `int`». Plus formellement, `addOne` est _mappage_ une valeur de l’ensemble d’entiers à l’ensemble d’entiers. Le `->` jeton désigne ce mappage. Dans F#, vous pouvez généralement consulter la signature de fonction pour obtenir une idée de ce qu’il fait.

Par conséquent, pourquoi est-la signature important ? Dans la programmation fonctionnelle typée, l’implémentation d’une fonction est souvent moins importante que la signature de type réel ! Le fait que `addOne` ajoute la valeur 1 à un entier est intéressante lors de l’exécution, mais lorsque vous construisez un programme, le fait qu’il accepte et retourne un `int` est ce qui indique comment vous allez utiliser réellement cette fonction. En outre, une fois que vous utilisez cette fonction correctement (par rapport à sa signature de type), diagnostiquer des problèmes est possible uniquement dans le corps de la `addOne` (fonction). Il s’agit de l’idée derrière la programmation fonctionnelle typée.

### <a name="expressions"></a>Expressions

Les expressions sont des constructions qui donnent comme résultat une valeur. Contrairement aux instructions qui effectuent une action, les expressions peuvent être considérées d’effectuer une action qui renvoie une valeur. Les expressions sont presque toujours utilisées en faveur des instructions dans la programmation fonctionnelle.

Considérez la fonction précédente, `addOne`. Le corps de `addOne` est une expression :

```fsharp
// 'x + 1' is an expression!
let addOne x = x + 1
```

Il est le résultat de cette expression qui définit le type de résultat de la `addOne` (fonction). Par exemple, l’expression de cette fonction peut être changée pour être un type différent, comme un `string`:

```fsharp
let addOne x = x.ToString() + "1"
```

La signature de la fonction est désormais :

```fsharp
val addOne: x:'a -> string
```

Depuis n’importe quel type dans F# peut avoir `ToString()` appelé dessus, le type de `x` soit devenue générique (appelé [généralisation automatique](../language-reference/generics/automatic-generalization.md)), et le type résultant est un `string`.

Les expressions ne sont pas simplement les corps des fonctions. Vous pouvez avoir des expressions qui produisent une valeur que vous utilisez un autre emplacement. Un commun un est `if`:

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result
```

Le `if` expression produit une valeur appelée `result`. Notez que vous pourriez omettre `result` entièrement, ce qui le `if` le corps d’expression de la `addOneIfOdd` (fonction). Le point clé à retenir sur les expressions est qu’elles produisent une valeur.

Il existe un type spécial, `unit`, qui est utilisé lorsqu’il n’y a rien à retourner. Par exemple, considérez cette fonction simple :

```fsharp
let printString (str: string) =
    printfn "String is: %s" str
```

La signature se présente comme suit :

```fsharp
val printString: str:string -> unit
```

Le `unit` type indique qu’il n’existe aucune valeur réelle retournée. Cela est utile lorsque vous avez une routine qui doit « fonctionnent-elles » bien ne qu’aucune valeur de retour à la suite de ce travail.

Cela se démarque de la programmation impérative, où l’équivalent `if` construction est une instruction, et produire des valeurs est souvent effectuée avec des variables de mutation. Par exemple, dans C#, le code peut être écrit comme suit :

```csharp
bool IsOdd(int x) => x % 2 != 0;

int AddOneIfOdd(int input)
{
    var result = input;

    if (IsOdd(input))
    {
        result = input + 1;
    }

    return result;
}
```

Il est important de souligner que C# et d’autres langages de style C ne prennent pas en charge la [expression ternaire](../../csharp/language-reference/operators/conditional-operator.md), ce qui permet la programmation basée sur une expression conditionnelle.

Dans la programmation fonctionnelle, il est rare de muter les valeurs avec des instructions. Bien que certains langages fonctionnels prennent en charge les instructions et une mutation, il n’est pas courant d’utiliser ces concepts dans la programmation fonctionnelle.

### <a name="pure-functions"></a>Fonctions pures

Comme mentionnées précédemment, pures fonctions sont les fonctions qui :

* Évaluez toujours la même valeur pour la même entrée.
* N’ont aucun effet secondaire.

Il est utile de considérer les fonctions mathématiques dans ce contexte. En mathématique, les fonctions dépendent uniquement de leurs arguments et n’ont pas d’effets secondaires. Dans la fonction mathématique `f(x) = x + 1`, la valeur de `f(x)` dépend uniquement de la valeur de `x`. Dans la programmation fonctionnelle, les fonctions pures sont la même façon.

Lorsque vous écrivez une fonction pure, la fonction doit dépendre uniquement de ses arguments et pas effectuer toute action qui entraîne un effet secondaire.

Voici un exemple d’une fonction non pure, car elle dépend d’état global et mutable :

```fsharp
let mutable value = 1

let addOneToValue x = x + value
```

Le `addOneToValue` fonction est clairement impure, étant donné que `value` peut être changé à tout moment pour avoir une valeur différente de 1. Ce modèle de selon une valeur globale doit être évitée dans la programmation fonctionnelle.

Voici un autre exemple d’une fonction non pure, car elle effectue un effet secondaire :

```fsharp
let addOneToValue x = 
    printfn "x is %d" x
    x + 1
```

Bien que cette fonction ne repose pas sur une valeur globale, il écrit la valeur de `x` à la sortie du programme. Bien qu’il n’a rien de choquant dans cette opération, cela signifie que la fonction n’est pas pure. Si une autre partie de votre programme dépend de l’élément externe au programme, telles que la mémoire tampon de sortie, puis en appelant cette fonction peut affecter à cette autre partie de votre programme.

Suppression de la `printfn` instruction rend la fonction pure :

```fsharp
let addOneToValue x = x + 1
```

Bien que cette fonction n’est pas fondamentalement _mieux_ que la version précédente avec la `printfn` instruction, cela ne garantit que cette fonction n’est retournent une valeur. Appel de n’importe quel nombre de fois où cette fonction produit le même résultat : il génère simplement une valeur. La prévisibilité donnée par la pureté est quelque chose pour que s’efforcent de nombreux programmeurs fonctionnels.

### <a name="immutability"></a>Immuabilité

Enfin, un des concepts plus fondamentaux de la programmation fonctionnelle typée consiste immuabilité. Dans F#, toutes les valeurs sont immuables par défaut. Cela signifie qu’ils ne peut pas être muter sur place, sauf si vous les marquez comme mutables.

Dans la pratique, travailler avec des valeurs immuables signifie que vous remplacez votre approche de programmation, « Je dois modifier quelque chose » à « j’ai besoin produire une nouvelle valeur ».

Par exemple, ajout de 1 à une valeur signifie produisant une nouvelle valeur, ne pas de mutation existant :

```fsharp
let value = 1
let secondValue = value + 1
```

Dans F#, le code suivant effectue **pas** muter le `value` fonction ; au lieu de cela, il effectue une vérification de l’égalité :

```fsharp
let value = 1
value = value + 1 // Produces a 'bool' value!
```

Certains langages de programmation fonctionnelles ne gèrent pas mutation. Dans F#, il est pris en charge, mais il n’est pas le comportement par défaut pour les valeurs.

Ce concept s’étend même jusqu'à proposer des structures de données. Dans la programmation fonctionnelle, les structures de données immuables telles que les jeux (et bien plus encore) ait une implémentation différente que vous pouvez initialement prévu. Conceptuellement, un tel ajout d’un élément à un ensemble ne modifie pas le jeu, il génère un _nouveau_ définie avec la valeur ajoutée. En coulisses, souvent cela par une structure de données différente qui permet de suivre efficacement une valeur pour que la représentation appropriée des données peut être donnée en conséquence.

Ce style de l’utilisation de valeurs et les structures de données est cruciale, car il vous permet de traiter toute opération qui modifie quelque chose comme s’il crée une nouvelle version de ceci force. Cela permet à des éléments comme l’égalité et d’infériorité être cohérents dans vos programmes.

## <a name="next-steps"></a>Étapes suivantes

La section suivante couvre soigneusement les fonctions, exploration de différentes façons, vous pouvez les utiliser dans la programmation fonctionnelle.

[Fonctions de première classe](first-class-functions.md) explore les fonctions profondément, montrant comment vous pouvez les utiliser dans différents contextes.

## <a name="further-reading"></a>Informations supplémentaires

Le [penser fonctionnellement](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) série est également une excellente ressource pour en savoir plus sur la programmation fonctionnelle avec F#. Il couvre les notions de base de la programmation fonctionnelle de façon pragmatique et facile à lire, à l’aide de F# fonctionnalités pour illustrer les concepts.
