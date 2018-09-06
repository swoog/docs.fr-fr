---
title: 'Les instructions de mise en forme de code F #'
description: 'Découvrez les instructions de mise en forme de code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 9c6e80509e9a5654e6514674d38c02e2a6b44e37
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734640"
---
# <a name="f-code-formatting-guidelines"></a>Les instructions de mise en forme de code F #

Cet article propose des instructions pour savoir comment mettre en forme votre code afin que votre code F # est :

* Généralement considérée comme plus lisibles
* Est conformément aux conventions appliquées par la mise en forme des outils dans Visual Studio et autres éditeurs
* Similaire à un autre code en ligne

Ces instructions sont basées sur [un guide complet sur les Conventions de mise en forme F #](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) par [Anh-Dung Phan](https://github.com/dungpa).

## <a name="general-rules-for-indentation"></a>Règles générales pour la mise en retrait

F # utilise des espaces blancs significatifs par défaut. Les instructions suivantes sont destinées à fournir des conseils quant à jongler avec des défis que cela peut imposer.

### <a name="using-spaces"></a>L’utilisation des espaces

Lors de la mise en retrait est requise, vous devez utiliser des espaces, tabulations pas. Au moins un espace est requis. Votre organisation peut créer des normes de codage pour spécifier le nombre d’espaces à utiliser pour la mise en retrait ; deux, trois ou quatre espaces de mise en retrait à chaque niveau de mise en retrait est typique.

**Nous vous recommandons 4 espaces par mise en retrait.**

Ceci dit, la mise en retrait de programmes est très subjective. Variations sont OK, mais la première règle, vous devez suivre est *la cohérence de la mise en retrait*. Choisir un style généralement accepté de mise en retrait et l’utiliser systématiquement tout au long de votre base de code.

## <a name="formatting-blank-lines"></a>Mise en forme des lignes vides

* Distinct niveau supérieur (fonction) et classe les définitions avec deux lignes vides.
* Les définitions de méthode à l’intérieur d’une classe sont séparées par une ligne vierge.
* Lignes vierges supplémentaires peuvent servir (avec parcimonie) pour séparer les groupes de fonctions associées. Peuvent être omis des lignes vides entre un ensemble de commandes associées à une ligne (par exemple, un ensemble d’implémentations factices).
* Utiliser avec parcimonie, des lignes vides dans les fonctions, pour indiquer les sections logiques.

## <a name="formatting-comments"></a>Mise en forme de commentaires

Préférez généralement plusieurs commentaires double barre oblique sur les commentaires de bloc de style de ML.

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

Les commentaires incorporés doivent mettre en majuscule la première lettre.

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a>Conventions d'attribution d'un nom

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a>Utilisent une casse mixte pour les fonctions et les valeurs de limite de classe, expression-liées aux et modèle

Il est courant et acceptés F # style à utiliser une casse mixte pour tous les noms liée en tant que variables locales ou dans les correspondances de modèle et les définitions de fonction.

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

Fonctions liées à localement dans les classes doivent également utiliser une casse mixte.

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a>Utilisent une casse mixte pour les fonctions publiques liées à un module

Quand une fonction liée au module fait partie d’une API publique, il doit utiliser une casse mixte :

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a>Utilisent une casse mixte pour les fonctions et les valeurs de module dépendant internes et privés

Utilisez la casse mixte pour les valeurs liée aux module privées, y compris les éléments suivants :

* Fonctions ad hoc dans les scripts

* Valeurs constituant l’implémentation interne d’un module ou un type

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a>Utilisez la casse mixte pour les paramètres

Tous les paramètres doivent utiliser une casse mixte conformément aux conventions d’affectation de noms .NET.

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a>Utiliser la casse Pascal pour les modules

Tous les modules (niveau supérieur, internes, privés, imbriquées) doivent utiliser la casse Pascal.

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a>Utilisez la casse Pascal pour les déclarations de type, les membres et les étiquettes

Classes, interfaces, structures, énumérations, délégués, les enregistrements et les unions discriminées doivent être nommées avec la casse Pascal. Membres au sein des types et des étiquettes pour les enregistrements et les unions discriminées doivent également utiliser la casse Pascal.

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

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a>Utilisez la casse Pascal pour les constructions intrinsèques pour .NET

Espaces de noms, exceptions, événements et projet /`.dll` noms doivent également utiliser la casse Pascal. Non seulement est-ce que la consommation à partir d’autres langages .NET sembler plus naturelle pour les consommateurs, il est également cohérente avec les conventions d’affectation de noms .NET que vous êtes susceptible de rencontrer.

### <a name="avoid-underscores-in-names"></a>Éviter les traits de soulignement dans les noms

Historiquement, certaines bibliothèques F # ont utilisé des traits de soulignement dans les noms. Toutefois, cela est n’est plus largement acceptée, en partie parce qu’il est en conflit avec les conventions d’affectation de noms .NET. Ceci dit, certains programmeurs F # utilisent des traits de soulignement fortement, en partie pour des raisons historiques, et la tolérance de panne et le respect est important. Toutefois, n’oubliez pas que le style n’est souvent pas satisfaisant par d’autres personnes qui ont la possibilité d’utiliser.

Certaines exceptions inclut l’interopérabilité avec les composants natifs, où des traits de soulignement sont très courantes.

### <a name="use-standard-f-operators"></a>Utilisez les opérateurs standard F #

Les opérateurs suivants sont définis dans la bibliothèque standard F # et doivent être utilisés au lieu de définir des équivalents. L’utilisation de ces opérateurs est recommandée car elle a tendance à rendre le code plus lisible et idiomatique. Les développeurs avec un arrière-plan dans OCaml ou autre langage de programmation fonctionnel peut-être habitués à différents idiomes. La liste suivante récapitule les opérateurs F # recommandées.

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
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

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a>Utiliser la syntaxe du préfixe pour les génériques (`Foo<T>`) plutôt que de la syntaxe de suffixe (`T Foo`)

F # hérite à la fois le style de ML suffixe de nommage des types génériques (par exemple, `int list`), ainsi que le préfixe de style .NET (par exemple, `list<int>`). Préférer le style de .NET, à l’exception des quatre types spécifiques :

1. Pour les listes F #, utilisez la forme suffixée : `int list` plutôt que `list<int>`.
2. Pour les Options F #, utilisez la forme suffixée : `int option` plutôt que `option<int>`.
3. Pour les tableaux F #, utilisez le nom syntaxique `int[]` plutôt que `int array` ou `array<int>`.
4. Pour les cellules de référence, utilisez `int ref` plutôt que `ref<int>` ou `Ref<int>`.

Pour tous les autres types, utilisez la forme de préfixe.

## <a name="formatting-tuples"></a>Mise en forme de tuples

Une instanciation de tuple doit être entre parenthèses, et les virgules de délimitation dans doivent être suivies par un espace, par exemple : `(1, 2)`, `(x, y, z)`.

Il est généralement admis pour omettre les parenthèses dans les critères spéciaux de tuples :

```fsharp
let (x, y) = z // Destructuring
let x, y = z // OK

// OK
match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-discriminated-union-declarations"></a>Mise en forme discriminée des déclarations d’union

Mettre en retrait `|` dans la définition de type par des 4 espaces :

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

## <a name="formatting-discriminated-unions"></a>Mise en forme des unions discriminées

Instancié Unions discriminées qui réparties sur plusieurs lignes doit fournir des données qu’il contient une nouvelle étendue avec la mise en retrait :

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

## <a name="formatting-record-declarations"></a>Mise en forme de déclarations d’enregistrement

Mettre en retrait `{` dans le type de définition par 4 espaces et démarrer la liste de champs sur la même ligne :

```fsharp
// OK
type PostalAddress =
    { Address : string
      City : string
      Zip : string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City

// Not OK
type PostalAddress =
  { Address : string
    City : string
    Zip : string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
    
// Unusual in F#
type PostalAddress =
    { 
        Address : string
        City : string
        Zip : string
    }
```

Le fait de placer le jeton d’ouverture sur la même ligne et le jeton de fermeture sur une nouvelle ligne consiste également, mais n’oubliez pas que vous devez utiliser le [syntaxe détaillée](../language-reference/verbose-syntax.md) pour définir les membres (le `with` mot clé) :

```fsharp
//  OK, but verbose syntax required
type PostalAddress = { 
    Address : string
    City : string
    Zip : string
} with
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
```

## <a name="formatting-records"></a>Mise en forme d’enregistrements

Enregistrements courts peuvent être écrite sur une seule ligne :

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

Les enregistrements qui sont plus longs doivent utiliser les nouvelles lignes pour les étiquettes :

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

Le fait de placer le jeton d’ouverture sur la même ligne et le jeton de fermeture sur une nouvelle ligne est également correcte :

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

## <a name="formatting-lists-and-arrays"></a>Mise en forme des listes et des tableaux

Écrire `x :: l` avec des espaces autour de la `::` opérateur (`::` est un opérateur infixe, par conséquent, entouré d’espaces) et `[1; 2; 3]` (`;` est un délimiteur, par conséquent, suivi d’un espace).

Utilisez toujours au moins un espace entre les deux opérateurs distincts de type accolade. Par exemple, laissez un espace entre un `[` et un `{`.

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

Listes et des tableaux réparties sur plusieurs lignes suivent une règle similaire comme enregistrements :

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

Mise en retrait des instructions conditionnelles varie selon les tailles des expressions qui les composent. Si `cond`, `e1` et `e2` sont courtes, il vous suffit de les écrire sur une seule ligne :

```fsharp
if cond then e1 else e2
```

Si `cond`, `e1` ou `e2` sont plus de temps, mais pas plusieurs lignes :

```fsharp
if cond
then e1
else e2
```

Si une des expressions est multiligne :

```fsharp
if cond then
    e1
else
    e2
```

Plusieurs instructions conditionnelles avec `elif` et `else` sont mises en retrait dans la même étendue en tant que le `if`:

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a>Constructions de correspondance de modèle

Utilisez un `|` pour chaque clause d’une correspondance avec aucune mise en retrait. Si l’expression est courte, vous pouvez envisager d’utiliser une seule ligne si chaque sous-expression est également simple.

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
```

Si l’expression à droite de la flèche de critères spéciaux est trop volumineuse, déplacez-le vers la ligne suivante, mis en retrait d’une seule étape à partir de la `match` / `|`.

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

Filtre de correspondance de fonctions anonymes, en commençant par `function`, doit généralement pas mettre en retrait trop loin. Par exemple, il est bien de mise en retrait d’une étendue comme suit :

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

Critères spéciaux dans les fonctions définies par `let` ou `let rec` doit être mis en retrait 4 espaces après le démarrage de `let`, même si `function` mot clé est utilisé :

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

Nous vous déconseillons d’alignement des flèches.

## <a name="formatting-trywith-expressions"></a>Mise en forme try / with expressions

Critères spéciaux sur le type d’exception doit être mis en retrait au même niveau que `with`.

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

## <a name="formatting-function-parameter-application"></a>Mise en forme d’application de paramètre de fonction

En règle générale, la plupart des applications de paramètre de fonction sont effectuée sur la même ligne.

Si vous souhaitez appliquer des paramètres à une fonction sur une nouvelle ligne, mettre en retrait les par une étendue.

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

Les mêmes règles s’appliquent pour les expressions lambda en tant qu’arguments de fonction. Si le corps d’une expression lambda, le corps peut avoir une autre ligne, la mise en retrait par une étendue

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

Toutefois, si le corps d’une expression lambda est plusieurs lignes, envisagez factorisant dans une fonction distincte plutôt que d’avoir une construction multiligne appliquée en tant qu’un seul argument à une fonction.

### <a name="formatting-infix-operators"></a>Opérateurs infixes mise en forme

Opérateurs distincts par des espaces. Exceptions évident à cette règle sont les `!` et `.` opérateurs.

Expressions de correspondance des infixes sont OK pour l’alignement sur la même colonne :

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a>Mise en forme des opérateurs de pipeline

Pipeline `|>` opérateurs doivent figurer sous elles opèrent selon des expressions.

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

### <a name="formatting-white-space-in-expressions"></a>Mise en forme des espaces blancs dans les expressions

Évitez les espaces superflus dans les expressions F #.

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
