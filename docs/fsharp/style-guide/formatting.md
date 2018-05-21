---
title: 'Les instructions de mise en forme de code F #'
description: 'Découvrez les instructions de mise en forme du code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 1433b6891a6a0ddcdc082c141365ae54fa40c27b
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
---
# <a name="f-code-formatting-guidelines"></a>Les instructions de mise en forme de code F #

Cet article propose des recommandations pour la mise en forme votre code afin que votre code F # est :

* Généralement affichées comme plus lisibles
* Est conformément aux conventions appliquées par les outils dans Visual Studio et autres éditeurs de mise en forme
* Similaire à un autre code en ligne

Ces instructions sont basées sur [un guide complet sur les Conventions de mise en forme F #](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) par [Anh-fumier Phan](https://github.com/dungpa).

## <a name="general-rules-for-indentation"></a>Règles générales pour la mise en retrait

F # utilise un espace blanc significatif par défaut. Les instructions suivantes sont destinées à fournir des conseils sur la manière de jongler avec des défis que cela peut imposer.

### <a name="using-spaces"></a>L’utilisation des espaces

Lors de la mise en retrait est requise, vous devez utiliser des espaces, tabulations pas. Au moins un espace est requis. Votre organisation peut créer des normes de codage pour spécifier le nombre d’espaces à utiliser pour la mise en retrait ; deux, trois ou quatre espaces de mise en retrait à chaque niveau de mise en retrait est typique.

**Nous vous recommandons 4 espaces par mise en retrait.**

Ceci dit, la mise en retrait des programmes est une question subjective. Variations sont OK, mais la première règle, vous devez suivre est *la cohérence de la mise en retrait*. Choisissez un style de mise en retrait de généralement accepté et utiliser systématiquement dans l’ensemble de votre code base.

## <a name="formatting-discriminated-union-declarations"></a>Mise en forme discriminée déclarations d’union

Mettre en retrait `|` dans la définition de type par 4 espaces :

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

Instancié Unions discriminées réparties sur plusieurs lignes doit fournir des données qu’ils contiennent une nouvelle étendue avec mise en retrait :

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

La parenthèse fermante peut également être sur une nouvelle ligne :

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-tuples"></a>Mise en forme des tuples

Une instanciation de tuple doit être entre parenthèses et les virgules de délimitation dans doivent être suivis par un espace, par exemple : `(1, 2)`, `(x, y, z)`.

Une exception couramment acceptée est d’omettre les parenthèses dans les critères spéciaux de tuples :

```fsharp
let (x, y) = z // Destructuring

match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-records"></a>Mise en forme des enregistrements

Enregistrements courts peuvent être écrites dans une seule ligne :

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

Les enregistrements qui sont plus longs doivent utiliser les nouvelles lignes pour les étiquettes :

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

Placer le jeton d’ouverture sur la même ligne et le jeton de fermeture sur une nouvelle ligne est également correct :

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

Les mêmes règles s’appliquent pour les éléments de liste et tableau.

## <a name="formatting-lists-and-arrays"></a>Mise en forme de listes et des tableaux

Écrire `x :: l` avec les espaces autour de le `::` (opérateur) (`::` est un opérateur infixe, par conséquent, entouré par des espaces) et `[1; 2; 3]` (`;` est un délimiteur, par conséquent, suivi d’un espace).

Utilisez toujours au moins un espace entre les deux opérateurs accolade de type distincts. Par exemple, laissez un espace entre un `[` et un `{`.

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

Listes et aux tableaux réparties sur plusieurs lignes respecte une règle similaire comme enregistrements :

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a>Mise en forme if expressions

Mise en retrait des éléments conditionnels varie selon les tailles des expressions qui les composent. Si `cond`, `e1` et `e2` sont petites, il vous suffit de les écrire sur une seule ligne :

```fsharp
if cond then e1 else e2
```

Si `e1` et `cond` sont petits, mais `e2` est importante :

```fsharp
if cond then e1
else
    e2
```

Si `e1` et `cond` sont volumineux et `e2` est petite :

```fsharp
if cond then
    e1
else e2
```

Si toutes les expressions sont volumineuses :

```fsharp
if cond then
    e1
else
    e2
```

Plusieurs conditions avec `elif` et `else` sont mises en retrait à la même portée que la `if`:

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a>Constructions de correspondance de modèle

Utilisez un `|` pour chaque clause d’une correspondance avec aucune mise en retrait. Si l’expression est courte, vous pouvez utiliser une seule ligne.

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"

// OK
match l with [] -> false | _ :: _ -> true
```

Si l’expression à droite de la flèche de mise en correspondance est trop grande, déplacez-le vers la ligne suivante, la mise en retrait d’une seule étape à partir de la `match` / `|`.

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

Filtre de correspondance de fonctions anonymes, en commençant par `function`, doit généralement pas mettre en retrait trop loin. Par exemple, il est correct de mise en retrait d’une étendue comme suit :

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

Mise en correspondance dans les fonctions définies par `let` ou `let rec` doit être mis en retrait 4 espaces après le démarrage de `let`, même si `function` mot clé est utilisé :

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

Nous vous déconseillons d’alignement des flèches.

## <a name="formatting-trywith-expressions"></a>Essayez de mise en forme / avec des expressions

Mise en correspondance sur le type d’exception doit être mis en retrait au même niveau que `with`.

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a>Application de paramètre de fonction de mise en forme

En règle générale, la plupart des applications de paramètre de fonction sont effectuée sur la même ligne.

Si vous souhaitez appliquer des paramètres à une fonction sur une nouvelle ligne, les mettre en retrait une étendue.

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

Arguments de fonction anonyme peuvent être sur la ligne suivante ou avec un non résolu `fun` sur la ligne de l’argument :

```fsharp
// OK
let printListWithOffset a list1 =
    List.iter (fun elem ->
        printfn "%d" (a + elem)) list1

// OK, but prefer previous
let printListWithOffset a list1 =
    List.iter (
        fun elem ->
            printfn "%d" (a + elem)) list1
```

### <a name="formatting-infix-operators"></a>Opérateurs infix mise en forme

Opérateurs distincts par des espaces. Exceptions évidentes à cette règle sont les `!` et `.` opérateurs.

Les expressions infix sont OK l’alignement sur la même colonne :

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a>Opérateurs de pipeline de mise en forme

Pipeline `|>` opérateurs doivent figurer sous les ils opèrent sur des expressions.

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a>Mise en forme de modules

Code dans un module local doit être mis en retrait par rapport au module, mais le code dans un module de niveau supérieur ne doit pas être mis en retrait. Les éléments Namespace n’ont pas à être mis en retrait.

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a>Mise en forme d’expressions d’objet et des interfaces

Expressions d’objet et les interfaces doivent être alignées dans la même façon avec `member` en cours de mise en retrait après 4 espaces.

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-whitespace-in-expressions"></a>Mise en forme des espaces blancs dans les expressions

Évitez l’espace superflu dans les expressions F #.

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

Arguments nommés doivent avoir également pas espace entourant le `=`:

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```

## <a name="formatting-blank-lines"></a>Mise en forme des lignes vides

* Distinct niveau supérieur (fonction) et la classe définitions avec deux lignes vides.
* Les définitions de méthode à l’intérieur d’une classe sont séparées par une ligne vide.
* Lignes vierges supplémentaires peuvent servir (avec parcimonie) pour séparer les groupes de fonctions connexes. Lignes vides peuvent être omises entre un ensemble de commandes associées à une ligne (par exemple, un ensemble d’implémentations fictives).
* Utiliser avec parcimonie lignes vides dans les fonctions, pour indiquer les sections logiques.

## <a name="formatting-comments"></a>Mise en forme de commentaires

Préférez généralement plusieurs commentaires double barre oblique sur les commentaires en bloc style ML.

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    Generally avoid these kinds of comments.
*)
```

Commentaires incorporés doivent mettre en majuscule la première lettre.

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a>Conventions d'attribution d'un nom

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a>Utilisez camelCase pour les fonctions et les valeurs de limite de classe, expression-modèle liées et

Il est courant et acceptée style F # à utiliser camelCase pour tous les noms lié en tant que variables locales ou dans les correspondances de modèle et les définitions de fonction.

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

Fonctions liées au localement dans les classes doivent également utiliser camelCase.

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a>Utilisez camelCase pour les fonctions et les valeurs liées au module internes et privés

Utilisez camelCase pour des valeurs liées au module privées, notamment les suivantes :

* Les fonctions ad hoc dans les scripts

* Valeurs constituant l’implémentation interne de type ou module

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a>Utilisez camelCase pour les paramètres

Tous les paramètres doivent utiliser camelCase conformément aux conventions d’affectation de noms de .NET.

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a>Utiliser PascalCase pour les modules

Tous les modules (niveau supérieur, internes, privés, imbriquées) doivent utiliser PascalCase.

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a>Utilisez PascalCase pour les étiquettes, les membres et les déclarations de type

Classes, interfaces, structures, énumérations, délégués, les enregistrements et les unions discriminées doivent être nommées avec PascalCase. Les membres dans les types et les étiquettes pour les enregistrements et les unions discriminées doivent également utiliser PascalCase.

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a>Utilisez PascalCase pour les constructions intrinsèques pour .NET

Espaces de noms, exceptions, événements et le projet /`.dll` noms doivent également utiliser PascalCase. N’est pas seulement cela rend la consommation à partir d’autres langages .NET semble plus naturel aux consommateurs, il est également cohérent avec les conventions d’affectation de noms .NET que vous êtes susceptible de rencontrer.

### <a name="avoid-underscores-in-names"></a>Éviter les traits de soulignement dans les noms

Historiquement, certaines bibliothèques F # ont utilisé des traits de soulignement dans les noms. Toutefois, cela est n’est plus largement accepté, car il est en conflit avec les conventions d’affectation de noms .NET. Ceci dit, certains programmeurs F # utilisent des traits de soulignement importante, en partie pour des raisons historiques, et la tolérance de panne et de respect est important. Toutefois, sachez que le style est souvent disliked par d’autres personnes ont la possibilité d’utiliser.

Certaines exceptions inclut l’interopérabilité avec des composants natifs, où des traits de soulignement sont très courantes.

### <a name="use-standard-f-operators"></a>Utilisez les opérateurs standard F #

Les opérateurs suivants sont définis dans la bibliothèque standard) (F # et doivent être utilisées au lieu de définir des équivalents. L’utilisation de ces opérateurs est recommandée car il a tendance à rendre le code plus lisible et idiomatique. Les développeurs avec un arrière-plan dans OCaml ou autre langage de programmation fonctionnelle peuvent être habitués à différents langages. La liste suivante résume les opérateurs F # recommandées.

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Throwing away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a>Utilisez la syntaxe de préfixe des génériques (`Foo<T>`), plutôt que la syntaxe de suffixe (`T Foo`)

F # hérite à la fois le style de ML suffixée des noms de types génériques (par exemple, `int list`), ainsi que le préfixe style .NET (par exemple, `list<int>`). Préférez le style de .NET, à l’exception des quatre types spécifiques :

1. Pour F # les listes, utilisez la forme suffixée : `int list` plutôt que `list<int>`.
2. Pour les Options F #, utilisez la forme suffixée : `int option` plutôt que `option<int>`.
3. Pour les tableaux F #, utilisez le nom syntaxique `int[]` plutôt que `int array` ou `array<int>`.
4. Pour les cellules de référence, utilisez `int ref` plutôt que `ref<int>` ou `Ref<int>`.

Pour tous les autres types, utilisez le format de préfixe.
