---
title: 'Conventions de codage F #'
description: 'Découvrez les recommandations générales et idiomes lors de l’écriture de code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: f3d16f735ddc1901aeaa5ebb39e2fa2b70a3d836
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="f-coding-conventions"></a>Conventions de codage F #

Les conventions suivantes sont formulées d’une expérience d’utilisation de grande taille) (F # codebases. Le [cinq principes du bon code F #](index.md#five-principles-of-good-f-code) constituent la base de chaque recommandation. Elles sont liées à la [règles de conception du composant F #](component-design-guidelines.md), mais s’appliquent à n’importe quel code F #, pas seulement les composants tels que les bibliothèques.

## <a name="organizing-code"></a>Organisation du code

Fonctionnalités de deux méthodes principales pour organiser le code F # : les modules et les espaces de noms. Ceux-ci sont similaires, mais que vous n’ont pas les différences suivantes :

* Espaces de noms sont compilés en tant qu’espaces de noms .NET. Les modules sont compilés en tant que classes statiques.
* Espaces de noms sont toujours de niveau supérieur. Modules peuvent être imbriqués dans d’autres modules et de niveau supérieur.
* Espaces de noms peut s’étendre sur plusieurs fichiers. Les modules ne peuvent pas.
* Modules peuvent être décorées avec `[<RequireQualifiedAccess>]` et `[<AutoOpen>]`.

Les instructions suivantes vous aideront à utiliser pour organiser votre code.

### <a name="prefer-namespaces-at-the-top-level"></a>Préférez des espaces de noms au niveau supérieur

Pour tout code utilisable publiquement, espaces de noms sont préférentiels aux modules au niveau supérieur. Car ils sont compilés en tant qu’espaces de noms .NET, elles sont utilisable à partir de c# sans problème.

```fsharp
// Good!
namespace MyCode

type MyClass() =
    ...
```

À l’aide d’un module de niveau supérieur peuvent ne pas apparaît différent lorsqu’elle est appelée uniquement à partir de F #, mais les consommateurs de c#, les appelants peuvent être surpris par devoir qualifier `MyClass` avec la `MyCode` module.

```fsharp
// Bad!
module MyCode

type MyClass() =
    ...
```

### <a name="carefully-apply-autoopen"></a>Avec soin s’appliquent `[<AutoOpen>]`

Le `[<AutoOpen>]` construction peut pollue pas l’étendue de ce qui est disponible pour les appelants, et la réponse à quelque chose la provenance est « magique ». Cela n’est généralement pas une bonne chose. Une exception à cette règle est la bibliothèque principale F # lui-même (même si cela est également un peu controversé).

Toutefois, il est pratique si vous disposez des fonctionnalités d’assistance pour une API publique que vous souhaitez organiser séparément à partir de cette API publique.

```fsharp
module MyAPI =
    [<AutoOpen>]
    module private Helpers =
        let helper1 x y z =
            ...


    let myFunction1 x =
        let y = ...
        let z = ...

        helper1 x y z
```

Cela vous permet de détails de l’implémentation distincte correctement à partir de l’API publique d’une fonction sans avoir à qualifier complètement un programme d’assistance à chaque fois que vous l’appelez.

En outre, exposer des méthodes d’extension et les générateurs d’expressions au niveau de l’espace de noms peut être parfaitement exprimée avec `[<AutoOpen>]`.

### <a name="use-requirequalifiedaccess-whenever-names-could-conflict-or-you-feel-it-helps-with-readability"></a>Utilisez `[<RequireQualifiedAccess>]` chaque fois que les noms peuvent être en conflit ou si vous pensez qu’il facilite la lisibilité

Ajout de la `[<RequireQualifiedAccess>]` attribut à un module indique que le module ne peut-être pas être ouvertes et des références aux éléments du module doivent explicite qualifié accès. Par exemple, le `Microsoft.FSharp.Collections.List` module a cet attribut.

Cela est utile lorsque les valeurs dans le module et les fonctions ont des noms qui sont susceptibles d’entrer en conflit avec les noms dans d’autres modules. Nécessitant un accès complet peut considérablement améliorer la facilité de maintenance à long terme et evolvability d’une bibliothèque.

```fsharp
[<RequireQualifiedAccess>]
module StringTokenization =
    let parse s = ...

...

let s = getAString()
let parsed = StringTokenization.parse s // Must qualify to use 'parse'
```

### <a name="sort-open-statements-topologically"></a>Tri `open` instructions topologiquement

En F #, l’ordre des déclarations est important, notamment avec `open` instructions. Contrairement à c#, où l’effet de `using` et `using static` est indépendante de l’ordre de ces instructions dans un fichier.

En F #, éléments ouverts dans une étendue peuvent occulter autres déjà présent. Cela signifie que la réorganisation `open` instructions Impossible de modifier la signification du code. Par conséquent, toute arbitraire de tri de tous les `open` instructions (par exemple, dans l’ordre alphanumérique) n’est généralement pas recommandé, moins vous générez un comportement différent que vous pouvez vous attendre.

Au lieu de cela, nous vous recommandons de les trier [topologiquement](https://en.wikipedia.org/wiki/Topological_sorting); autrement dit, la commande votre `open` dans l’ordre dans lequel les instructions _couches_ de votre système sont définis. Effectuant alphanumérique de tri au sein des différentes couches topologiques peut également être considéré comme.

Par exemple, voici le tri topologique pour le fichier F # du compilateur service public API :

```fsharp
namespace Microsoft.FSharp.Compiler.SourceCodeServices

open System
open System.Collections.Generic
open System.Collections.Concurrent
open System.Diagnostics
open System.IO
open System.Reflection
open System.Text

open Microsoft.FSharp.Compiler
open Microsoft.FSharp.Compiler.AbstractIL
open Microsoft.FSharp.Compiler.AbstractIL.Diagnostics
open Microsoft.FSharp.Compiler.AbstractIL.IL
open Microsoft.FSharp.Compiler.AbstractIL.ILBinaryReader
open Microsoft.FSharp.Compiler.AbstractIL.Internal
open Microsoft.FSharp.Compiler.AbstractIL.Internal.Library

open Microsoft.FSharp.Compiler.AccessibilityLogic
open Microsoft.FSharp.Compiler.Ast
open Microsoft.FSharp.Compiler.CompileOps
open Microsoft.FSharp.Compiler.CompileOptions
open Microsoft.FSharp.Compiler.Driver
open Microsoft.FSharp.Compiler.ErrorLogger
open Microsoft.FSharp.Compiler.Infos
open Microsoft.FSharp.Compiler.InfoReader
open Microsoft.FSharp.Compiler.Lexhelp
open Microsoft.FSharp.Compiler.Layout
open Microsoft.FSharp.Compiler.Lib
open Microsoft.FSharp.Compiler.NameResolution
open Microsoft.FSharp.Compiler.PrettyNaming
open Microsoft.FSharp.Compiler.Parser
open Microsoft.FSharp.Compiler.Range
open Microsoft.FSharp.Compiler.Tast
open Microsoft.FSharp.Compiler.Tastops
open Microsoft.FSharp.Compiler.TcGlobals
open Microsoft.FSharp.Compiler.TypeChecker
open Microsoft.FSharp.Compiler.SourceCodeServices.SymbolHelpers

open Internal.Utilities
open Internal.Utilities.Collections
```

Notez qu’un saut de ligne sépare les couches topologiques, avec chaque couche qui est triée par ordre alphabétique par la suite. Cela organise correctement code sans accidentellement clichés instantanés de valeurs.

## <a name="use-classes-to-contain-values-that-have-side-effects"></a>Utiliser les classes pour contenir des valeurs qui ont des effets secondaires

Il existe plusieurs fois lorsque l’initialisation d’une valeur peut avoir des effets secondaires, tels que l’instanciation d’un contexte pour une base de données ou d’autres ressources à distance. Il est tentant d’initialiser des éléments dans un module et l’utiliser dans les fonctions suivantes :

```fsharp
// This is bad!
module MyApi =
    let dep1 = File.ReadAllText "/Users/{your name}/connectionstring.txt"
    let dep2 = Environment.GetEnvironmentVariable "DEP_2"

    let private r = Random()
    let dep3() = r.Next() // Problematic if multiple threads use this

    let function1 arg = doStuffWith dep1 dep2 dep3 arg
    let function2 arg = doSutffWith dep1 dep2 dep3 arg
```

Il s’agit généralement déconseillé pour les raisons suivantes :

Tout d’abord, configuration de l’application est placée dans le code de base avec `dep1` et `dep2`. Il est difficile à maintenir dans codebases supérieure.

Ensuite, initialisées de manière statique des données ne doivent pas inclure de valeurs qui ne sont pas thread-safe si votre composant lui-même utilise plusieurs threads. Cela est enfreinte clairement par `dep3`.

Enfin, l’initialisation du module compile dans un constructeur statique pour l’unité de compilation entier. Si une erreur se produit dans l’initialisation de valeurs de liées à let dans ce module, il se manifeste sous un `TypeInitializationException` qui est ensuite mis en cache pour toute la durée de vie de l’application. Cela peut être difficile à diagnostiquer. Il existe généralement une exception interne que vous pouvez essayer d’analyser, mais s’il n’est pas, il n’existe aucun indiquant la cause racine.

Juste utiliser à la place, une classe simple pour contenir les dépendances :

```fsharp
type MyParametricApi(dep1, dep2, dep3) =
    member __.Function1 arg1 = doStuffWith dep1 dep2 dep3 arg1
    member __.Function2 arg2 = doStuffWith dep1 dep2 dep3 arg2
```

Cela permet les opérations suivantes :

1. En exécutant un push de n’importe quel état dépendant en dehors de l’API elle-même.
2. Configuration peut maintenant être effectuée en dehors de l’API.
3. Erreurs dans l’initialisation de valeurs dépendantes ne sont pas susceptibles de se manifester par un `TypeInitializationException`.
4. L’API est désormais plus facile à tester.

## <a name="error-management"></a>Gestion des erreurs

Gestion des erreurs dans les grands systèmes est un défi subtils et complexe, et il n’existe aucune silver puces vous être assuré de vos systèmes à tolérance de pannes et se comportent correctement. Les instructions suivantes doivent proposer une aide pour la navigation dans cet espace difficile.

### <a name="represent-error-cases-and-illegal-state-in-types-intrinsic-to-your-domain"></a>Représentent les cas d’erreur et d’état non conforme dans les types intrinsèques à votre domaine

Avec [les Unions discriminées](../language-reference/discriminated-unions.md), F # vous donne la possibilité pour représenter l’état du programme défectueux dans votre système de type. Par exemple :

```fsharp
type MoneyWithdrawalResult =
    | Success of amount:decimal
    | InsufficientFunds of balance:decimal
    | CardExpired of DateTime
    | UndisclosedFailure
```

Dans ce cas, il existe des manières connus retrait de l’argent d’un compte bancaire peut échouer. Chaque cas d’erreur est représenté dans le type et peuvent donc être traitées en toute sécurité l’ensemble du programme.

```fsharp
let handleWithdrawal amount =
    let w = withdrawMoney amount
    match w with
    | Success am -> printfn "Successfully withdrew %f" am
    | InsufficientFunds balance -> printfn "Failed: balance is %f" balance
    | CardExpired expiredDate -> printfn "Failed: card expired on %O" expiredDate
    | UndisclosedFailure -> printfn "Failed: unknown"
```

En règle générale, si vous pouvez modéliser les différentes façons dont il se pouvez **échouer** dans votre domaine, puis gestion du code d’erreur n’est plus traité en tant que quelque chose que vous devez gérer avec en plus des flux de programme régulière. Il est simplement une partie du flux normal du programme et pas considéré comme **exceptionnelles**. Il existe deux grands avantages à cela :

1. Il est plus facile à gérer votre domaine que les modifications apportées au fil du temps.
2. Cas d’erreur sont plus faciles à des tests unitaires.

### <a name="use-exceptions-when-errors-cannot-be-represented-with-types"></a>Utiliser des exceptions lorsque les erreurs ne peut pas être représentés avec les types

Toutes les erreurs peuvent être représentés dans un domaine de problème. Ces types d’erreurs sont *exceptionnelles* par nature, donc la possibilité de déclencher et intercepter les exceptions en F #.

Tout d’abord, il est recommandé de lire le [les règles de conception Exception](../../standard/design-guidelines/exceptions.md). Ceux-ci sont également applicables à F #.

Les constructions principales disponibles en F # pour les besoins de déclenchement d’exceptions doivent être considérées dans l’ordre de préférence suivant :

| Fonction | Syntaxe | Objectif |
|----------|--------|---------|
| `nullArg` | `nullArg "argumentName"` | Déclenche un `System.ArgumentNullException` avec le nom de l’argument spécifié. |
| `invalidArg` | `invalidArg "argumentName" "message"` | Déclenche un `System.ArgumentException` avec un nom d’argument spécifié et le message. |
| `invalidOp` | `invalidOp "message"` | Déclenche un `System.InvalidOperationException` avec le message spécifié. |
|`raise`| `raise (ExceptionType("message"))` | Mécanisme à usage général pour lever des exceptions. |
| `failwith` | `failwith "message"` | Déclenche un `System.Exception` avec le message spécifié. |
| `failwithf` | `failwithf "format string" argForFormatString` | Déclenche un `System.Exception` avec un message déterminé par la chaîne de format et de ses entrées. |

Utilisez `nullArg`, `invalidArg` et `invalidOp` comme mécanisme de lever `ArgumentNullException`, `ArgumentException` et `InvalidOperationException` quand cela est approprié.

Le `failwith` et `failwithf` fonctions doivent être évitées en règle générale, car elles déclenchent la base de `Exception` de type, pas une exception spécifique. Comme pour le [règles de conception d’Exception](../../standard/design-guidelines/exceptions.md), vous souhaitez lever d’exceptions plus spécifiques dès que possible.

### <a name="using-exception-handling-syntax"></a>À l’aide de la syntaxe de gestion des exceptions

F # prend en charge les modèles d’exception via la `try...with` syntaxe :

```fsharp
try
    tryGetFileContents()
with
| :? System.IO.FileNotFoundException as e -> // Do something with it here
| :? System.Security.SecurityException as e -> // Do something with it here
```

Rapprochement des fonctionnalités à effectuer en cas d’une exception avec les critères spéciaux peut être un peu difficile si vous souhaitez conserver le code de nettoyage. Une telle pour gérer cette situation consiste à utiliser [modèles actifs](../language-reference/active-patterns.md) comme un moyen de la fonctionnalité de groupe se rapportant à un cas d’erreur avec une exception lui-même. Par exemple, vous pouvez consommer une API qui, lorsqu’il lève une exception, inclut des informations précieuses dans les métadonnées d’exception. Désencapsulage d’une valeur utile dans le corps de l’exception capturée à l’intérieur du modèle actif et en retournant que la valeur peut être utile dans certaines situations.

### <a name="do-not-use-monadic-error-handling-to-replace-exceptions"></a>N’utilisez pas monadic gestion des erreurs pour remplacer des exceptions

Les exceptions sont considérées comme quelque peu interdits dans la programmation fonctionnelle. En effet, les exceptions violent pureté, afin de prendre en compte fonctionnel non-tout à fait en toute sécurité. Toutefois, il ignore la réalité d’où le code doit s’exécuter et ce runtime erreurs peuvent se produire. En règle générale, écrire du code sur l’hypothèse que la plupart des éléments sont total, afin de minimiser les surprises désagréables ni pure.

Il est important de considérer les principaux atouts/aspects suivants des Exceptions en ce qui concerne leur pertinence et de pertinence dans le runtime .NET et l’écosystème de la gestion interlangage dans son ensemble :

1. Elles contiennent des informations de diagnostic détaillées, ce qui est très utiles lors du débogage d’un problème.
2. Ils sont bien compris par le runtime et d’autres langages .NET.
3. Elles permettent une réduction significative réutilisable lors de la comparaison avec le code sort de sa méthode pour *éviter* exceptions en implémentant un sous-ensemble de leur sémantique sur une base ad hoc.

Cet troisième point est essentiel. Pour les opérations complexes non triviale, utiliser des exceptions peut limiter dans le traitement des structures, comme suit :

```fsharp
Result<Result<MyType, string>, string list>
```

Ce qui peut entraîner facilement fragile code telles que les critères spéciaux sur les erreurs de « stringly typée » :

```fsharp
let result = doStuff()
match result with
| Ok r -> ...
| Error e ->
    if e.Contains "Error string 1" then ...
    elif e.Contains "Error string 2" then ...
    else ... // Who knows?
```

En outre, il peut être tentant d’absorber toute exception dans la volonté de disposer d’une fonction « simple » qui retourne un type « agréable » :

```fsharp
// This is bad!
let tryReadAllText (path : string) =
    try System.IO.File.ReadAllText path |> Some
    with _ -> None
```

Malheureusement, `tryReadAllText` peut lever des exceptions de nombreuses en fonction de la multitude d’éléments peuvent se produire sur un système de fichiers, et ce code annule immédiatement toutes les informations concernant ce qui peut en fait être va pas dans votre environnement. Si vous remplacez ce code avec un type de résultat, vous êtes à l’analyse « stringly typée » une erreur :

```fsharp
// This is bad!
let tryReadAllText (path : string) =
    try System.IO.File.ReadAllText path |> Ok
    with e -> Error e.Message

let r = tryReadAllText "path-to-file"
match r with
| Ok text -> ...
| Error e ->
    if e.Contains "uh oh, here we go again..." then ...
    else ...
```

Et en plaçant l’objet exception lui-même dans le `Error` constructeur simplement vous oblige à gérer correctement le type d’exception sur le site d’appel, plutôt que dans la fonction. Cette opération efficacement crée les exceptions vérifiées, qui sont notoirement unfun à traiter comme un appelant d’une API.

Une bonne approche pour les exemples ci-dessus est d’intercepter *spécifique* exceptions et retournent une valeur significative dans le contexte de cette exception. Si vous modifiez le `tryReadAllText` fonctionnent comme suit, `None` a plus de sens :

```fsharp
let tryReadAllTextIfPresent (path : string) =
    try System.IO.File.ReadAllText path |> Some
    with :? FileNotFoundException -> None
```

Au lieu de fonctionner comme un tout, cette fonction maintenant correctement gère le cas lorsqu’un fichier n’a été trouvé et affecter ce sens à un retour. Cette valeur de retour peut mapper à ce cas d’erreur lors de pas en ignorant toutes les informations contextuelles ou forcer des appelants pour y faire face à un incident ne peut pas s’appliquer à ce stade dans le code.

Types tels que `Result<'Success, 'Error>` appropriées pour les opérations de base où ils ne sont pas imbriqués, et facultatif types F # sont parfaites pour représenter lorsqu’un élément a un retour *quelque chose* ou *rien*. Ils ne sont pas un remplacement pour les exceptions, cependant et ne doivent pas servir lors d’une tentative pour remplacer les exceptions. Au lieu de cela, ils doivent être appliqués judicieusement à des aspects spécifiques d’adresse de l’exception et la stratégie de gestion des erreurs de façons ciblé.

## <a name="partial-application-and-point-free-programming"></a>Application partielle et exempt de point de programmation

F # prend en charge application partielle et par conséquent, différentes façons de programme dans un style exempt de point. Ceci peut être avantageux de réutilisation du code dans un module ou l’implémentation d’un objet, mais il n’est généralement pas quelque chose pour exposer publiquement. En général, exempt de point de programmation n’est pas une raison dans et de lui-même et peut ajouter un frein COGNITIF pour les personnes qui ne sont pas immergés dans le style.

### <a name="do-not-use-partial-application-and-currying-in-public-apis"></a>N’utilisez pas l’application partielle et curryfication dans les API publiques

Avec peu d’exception, l’utilisation de l’application partielle dans les API publiques permettre prêter à confusion pour les consommateurs. En règle générale, `let`-valeurs liées dans le code F # sont **valeurs**, et non **des valeurs de fonction**. Mélange de valeurs et les valeurs de fonction peut entraîner l’enregistrement d’un petit nombre de lignes de code en échange d’un peu de surcharge COGNITIF, surtout si combinées avec des opérateurs tels que `>>` pour composer des fonctions.

### <a name="consider-the-tooling-implications-for-point-free-programming"></a>Tenez compte des conséquences des outils pour la programmation de libérer de point

Fonctions curryfiées étiquette pas leurs arguments. Cela a des implications des outils. Prenez en compte les deux fonctions suivantes :

```fsharp
let func name age =
    printfn "My name is %s and I am %d years old!" name age

let funcWithApplication =
    printfn "My name is %s and I am %d years old!"
```

Les deux sont des fonctions valides, mais `funcWithApplication` est une fonction curryfiée. Lorsque vous pointez sur leurs types dans un éditeur, vous voyez ceci :

```fsharp
val func : name:string -> age:int -> unit

val funcWithApplication : (string -> int -> unit)
```

Sur le site d’appel, les info-bulles dans des outils tels que Visual Studio ne vous donnera des informations significatives à ce que le `string` et `int` représentent les types d’entrée.

Si vous rencontrez exempt de point de code comme `funcWithApplication` qui est consommable publiquement, il est recommandé de procéder à une expansion de η complète pour que les outils peuvent réponde à des noms explicites pour les arguments.

En outre, le débogage du code sans aucun point de peut être difficile, voire impossible. Outils de débogage s’appuient sur les valeurs liées aux noms (par exemple, `let` liaisons) afin que vous pouvez inspecter l’exécution au milieu de valeurs intermédiaires. Lorsque votre code n’a aucune valeur à inspecter, il n’est rien à déboguer. Dans le futur, outils de débogage peut évoluer pour synthétiser ces valeurs basées sur les chemins d’accès précédemment exécutées, mais il n’est pas judicieux de couvrir vos meilleurs résultats sur *potentiels* fonctionnalités de débogage.

### <a name="consider-partial-application-as-a-technique-to-reduce-internal-boilerplate"></a>Considérez une application partielle comme une technique afin de réduire le code réutilisable interne

Contrairement au point précédent, application partielle est un outil merveilleux pour réduire le code réutilisable à l’intérieur d’une application ou les détails plus approfondis internes d’une API. Il peut être utile pour l’implémentation des API plus complexe, où réutilisable est souvent difficiles à gérer de tests unitaires. Par exemple, le code suivant montre comment vous pouvez accomplir les infrastructures plus factices affichent sans prendre une dépendance externe sur une telle infrastructure et avoir à apprendre un connexes ad hoc API.

Par exemple, considérez la topographie de solution suivants :

```
MySolution.sln
|_/ImplementationLogic.fsproj
|_/ImplementationLogic.Tests.fsproj
|_/API.fsproj
```

`ImplementationLogic.fsproj` peut exposer du code tel que :

```fsharp
module Transactions =
    let doTransaction txnContext txnType balance =
        ...

type Transactor(ctx, currentBalance) =
    member __.ExecuteTransaction(txnType) =
        Transactions.doTransaction ctx txtType currentBalance
        ...
```

Tests unitaires `Transactions.doTransaction` dans `ImplementationLogic.Tests.fspoj` est simple :

```fsharp
namespace TransactionsTestingUtil

open Transactions

module TransactionsTestable =
    let getTestableTransactionRoutine mockContext = Transactions.doTransaction mockContext
```

Application partiellement `doTransaction` avec un contexte factices objet vous permet d’appeler la fonction dans tous vos tests unitaires sans avoir à construire un contexte factices chaque fois :

```fsharp
namespace TransactionTests

open Xunit
open TransactionTypes
open TransactionsTestingUtil
open TransactionsTestingUtil.TransactionsTestable

let testableContext =
    { new ITransactionContext with
        member __.TheFirstMember() = ...
        member __.TheSecondMember() = ... }

let transactionRoutine = getTestableTransactionRoutine testableContext

[<Fact>]
let ``Test withdrawal transaction with 0.0 for balance``() =
    let expected = ...
    let actual = transactionRoutine TransactionType.Withdraw 0.0
    Assert.Equal(expected, actual)
```

Cette technique ne doit pas être appliquée globalement à votre code base entière, mais il s’agit d’un bon moyen de réduire le code réutilisable pour développer des mécanismes complexes et les mécanismes internes de tests unitaires.

## <a name="access-control"></a>Contrôle d'accès

F # dispose de plusieurs options pour [le contrôle d’accès](../language-reference/access-control.md), hérité de ce qui est disponible dans le runtime .NET. Celles-ci ne sont pas utilisables uniquement pour les types - vous pouvez les utiliser pour les fonctions de trop.

* Préférez non -`public` types et membres jusqu'à ce que vous avez besoin pour être utilisable publiquement. Cela réduit également les deux consommateurs à
* Essayez de conserver toutes les fonctionnalités d’assistance `private`.
* Envisagez d’utiliser `[<AutoOpen>]` sur un module privé de fonctions d’assistance s’ils sont nombreux.

## <a name="type-inference-and-generics"></a>L’inférence de type et les génériques

L’inférence de type peut vous permettre d’économiser de la saisie d’une grande quantité de code réutilisable. Et généralisation automatique dans le compilateur F # peut vous aider à écrire plus de code générique avec quasiment aucun effort supplémentaire de votre part. Toutefois, ces fonctionnalités ne sont pas universellement correcte.

* Envisagez d’étiqueter les noms des arguments avec des types explicites dans les API publiques et n’utilisez pas l’inférence de type pour cela.

    La raison en est que **vous** doit se trouver dans le contrôle de la forme de votre API, et non par le compilateur. Bien que le compilateur peut effectuer une tâche convient à déduire les types pour vous, il est possible d’avoir la forme de la modification de l’API si elle s’appuie sur les éléments internes ont été modifiés de types. Il peut s’agir de ce que vous souhaitez, mais certainement causera une modification avec rupture API qui ont pour traiter les consommateurs en aval. En revanche, si vous ne contrôliez explicitement la forme de votre API publique, vous pouvez contrôler ces modifications avec rupture. En termes DDD, cela peut être représenté comme une couche de lutte contre la corruption.

* Donnez un nom significatif à vos arguments génériques.

    Sauf si vous écrivez du code réellement générique qui n’est pas spécifique à un domaine particulier, un nom significatif peut aider d’autres programmeurs comprendre le domaine, dans qu'ils travaillent. Par exemple, un paramètre de type nommé `'Document` dans le contexte de l’interaction avec un document de base de données plus clairement que les types de document générique peuvent être acceptées par la fonction ou le membre que vous utilisez.

* Envisagez de nommer les paramètres de type générique avec PascalCase.

    Il s’agit de la manière générale pour effectuer des opérations dans .NET, il est recommandé d’utiliser PascalCase plutôt que snake_case ou camelCase.

Enfin, la généralisation automatique n’est pas toujours un boon pour les personnes qui sont nouveaux pour F # ou un code base volumineux. Charge COGNITIF est à l’aide des composants qui sont génériques. En outre, si automatiquement généralisée de fonctions ne sont pas utilisées avec différents types d’entrée (permettent uniquement s’ils sont destinés à être utilisé en tant que tel), il n’existe aucun avantage réel pour les cours générique à ce stade dans le temps. Toujours prendre en compte si le code que vous écrivez bénéficieront réellement d’être générique.

## <a name="performance"></a>Performances

Valeurs de F # sont immuables par défaut, ce qui vous permet d’éviter certaines classes de bogues (en particulier les impliquant d’accès concurrentiel et parallélisme). Toutefois, dans certains cas, afin d’optimiser l’efficacité d’optimale (ou même raisonnable) de la durée d’exécution ou des allocations de mémoire, une plage de travail peut mieux être implémentée à l’aide de mutation sur place de l’état. Cela est possible dans une base opt-in avec F # avec le `mutable` (mot clé).

Toutefois, l’utilisation du `mutable` en F # peuvent avoir l’impression ne correspond pas à la pureté fonctionnelle. Il s’agit bien, si vous ajustez les attentes de pureté [référentielle transparence](https://en.wikipedia.org/wiki/Referential_transparency). Transparence référentielle - pas à la pureté - est l’objectif final lors de l’écriture de fonctions F #. Cela vous permet d’écrire une interface fonctionnelle sur une implémentation mutation pour le code critique de performances.

### <a name="wrap-mutable-code-in-immutable-interfaces"></a>Encapsuler le code mutable dans les interfaces immuables

Transparence référentielle comme objectif, il est essentiel d’écrire du code qui n’expose pas l’underbelly mutable des fonctions critiques pour les performances. Par exemple, le code suivant implémente la `Array.contains` fonction dans la bibliothèque principale F # :

```fsharp
[<CompiledName("Contains")>]
let inline contains value (array:'T[]) =
    checkNonNull "array" array
    let mutable state = false
    let mutable i = 0
    while not state && i < array.Length do
        state <- value = array.[i]
        i <- i + 1
    state
```

Appel de cette fonction plusieurs fois ne modifie pas le tableau sous-jacent, et il vous oblige à conserver un état mutable dans sa consommation. Il est référentielle transparent, même si presque chaque ligne de code utilise la mutation.

### <a name="consider-encapsulating-mutable-data-in-classes"></a>Envisagez d’encapsuler des données mutables dans les classes

L’exemple précédent a utilisé une seule fonction pour encapsuler des opérations à l’aide de données mutables. Cela n’est pas toujours suffisant pour les jeux de données plus complexes. Tenez compte des ensembles de fonctions suivants :

```fsharp
open System.Collections.Generic

let addToClosureTable (key, value) (t: Dictionary<_,_>) =
    if not (t.ContainsKey(key)) then
        t.Add(key, value)
    else
        t.[key] <- value

let closureTableCount (t: Dictionary<_,_>) = t.Count

let closureTableContains (key, value) (t: Dictionary<_, HashSet<_>>) =
    match t.TryGetValue(key) with
    | (true, v) -> v.Equals(value)
    | (false, _) -> false
```

Ce code est performant, mais elle présente la structure de données basée sur une mutation que les appelants sont responsables de la maintenance. Cela peut être encapsulée à l’intérieur d’une classe sans membres sous-jacentes qui peuvent changer :

```fsharp
open System.Collections.Generic

/// The results of computing the LALR(1) closure of an LR(0) kernel
type Closure1Table() =
    let t = Dictionary<Item0, HashSet<TerminalIndex>>()

    member __.Add(key, value) =
        if not (t.ContainsKey(key)) then
            t.Add(key, value)
        else
            t.[key] <- value

    member __.Count = t.Count

    member __.Contains(key, value) =
        match t.TryGetValue(key) with
        | (true, v) -> v.Equals(value)
        | (false, _) -> false
```

`Closure1Table` encapsule la structure sous-jacente de données basées sur une mutation, ne pas forcer l’appelants pour conserver la structure de données sous-jacente. Les classes sont un excellent moyen d’encapsuler des données et des routines qui sont basés sur une mutation sans exposer les détails aux appelants.

### <a name="prefer-let-mutable-to-reference-cells"></a>Préférez `let mutable` aux cellules de référence

Cellules de référence sont un moyen pour représenter la référence à une valeur plutôt que la valeur elle-même. Bien qu’ils peuvent être utilisés pour le code critique pour les performances, ils sont généralement pas recommandés. Prenons l'exemple suivant :

```fsharp
let kernels =
    let acc = ref Set.empty

    processWorkList startKernels (fun kernel ->
        if not ((!acc).Contains(kernel)) then
            acc := (!acc).Add(kernel)
        ...)

    !acc |> Seq.toList
```

L’utilisation d’une cellule de référence est maintenant « pollue « tout le code suivant à la suppression de la référence et re-référencer les données sous-jacentes. Envisagez plutôt `let mutable`:

```fsharp
let kernels =
    let mutable acc = Set.empty

    processWorkList startKernels (fun kernel ->
        if not (acc.Contains(kernel)) then
            acc <- acc.Add(kernel)
        ...)

    acc |> Seq.toList
```

Le point de mutation au milieu de l’expression lambda unique, à l’exception de tout autre code qui touche `acc` faire d’une manière qui est identique à l’utilisation d’un vecteur normal `let`-immuable valeur limite. Cela rend plus facile de modifier au fil du temps.

## <a name="object-programming"></a>Objet de programmation

F # est prise en charge complète pour les objets et concepts de (OO) et orienté objet. Bien que de nombreux concepts OO sont puissantes et utiles, tous les sont idéaux pour une utilisation. Les listes suivantes offrent des conseils sur les catégories de fonctionnalités OO à un niveau élevé.

**Envisagez d’utiliser ces fonctionnalités dans de nombreuses situations :**

* Notation par points (`x.Length`)
* Membres d’instance
* Constructeurs implicites
* Membres static
* Notation d’indexeur (`arr.[x]`)
* Arguments nommés et facultatifs
* Interfaces et implémentations d’interface

**Ne pas atteindre tout d’abord pour ces fonctionnalités, mais judicieusement appliquent les lorsqu’ils se trouvent pratiques résoudre un problème :**

* Surcharge de méthode
* Données mutables encapsulées
* Opérateurs sur les types
* Propriétés automatiques
* Implémentation de `IDisposable` et `IEnumerable`
* Extensions de type
* Événements
* Structs
* Délégués
* Enums

**Généralement éviter ces fonctionnalités, sauf si vous devez les utiliser :**

* Hiérarchies d’héritage de type et l’héritage d’implémentation
* Les valeurs NULL et `Unchecked.defaultof<_>`

### <a name="prefer-composition-over-inheritance"></a>Préférer composition d’héritage

[Composition de l’héritage](https://en.wikipedia.org/wiki/Composition_over_inheritance) est un idiome de longue date bon code F # peut respecter. Le principe fondamental est que vous ne devez pas exposer une classe de base et forcer les appelants à hériter de cette classe pour obtenir les fonctionnalités de base.

### <a name="use-object-expressions-to-implement-interfaces-if-you-dont-need-a-class"></a>Utiliser des expressions d’objet pour implémenter les interfaces si vous n’avez pas besoin d’une classe

[Expressions d’objet](../language-reference/object-expressions.md) vous permettent d’implémenter des interfaces à la volée, liaison de l’interface implémentée à une valeur sans avoir à le faire à l’intérieur d’une classe. Ceci est pratique, surtout si vous _uniquement_ doivent implémenter l’interface et n’ont pas besoin d’une classe complète.

Par exemple, voici le code qui est exécuté dans [Ionide](http://ionide.io/) pour fournir une action de correction du code si vous avez ajouté un symbole que vous n’avez pas une `open` instruction pour :

```fsharp
    let private createProvider () =
        { new CodeActionProvider with
            member this.provideCodeActions(doc, range, context, ct) =
                let diagnostics = context.diagnostics
                let diagnostic = diagnostics |> Seq.tryFind (fun d -> d.message.Contains "Unused open statement")
                let res =
                    match diagnostic with
                    | None -> [||]
                    | Some d ->
                        let line = doc.lineAt d.range.start.line
                        let cmd = createEmpty<Command>
                        cmd.title <- "Remove unused open"
                        cmd.command <- "fsharp.unusedOpenFix"
                        cmd.arguments <- Some ([| doc |> unbox; line.range |> unbox; |] |> ResizeArray)
                        [|cmd |]
                res
                |> ResizeArray
                |> U2.Case1
        }
```

Car il n’est pas nécessaire pour une classe lors de l’interaction avec l’API de Code Visual Studio, les Expressions d’objet sont un outil idéal pour cela. Ils sont également utiles pour les tests unitaires, lorsque vous souhaitez une interface avec les routines de test de stub de manière ad hoc.

## <a name="type-abbreviations"></a>Abréviations de types

[Abréviations de types](../language-reference/type-abbreviations.md) sont un moyen pratique pour attribuer une étiquette à un autre type, par exemple une signature de fonction ou un type plus complexe. Par exemple, l’alias suivant attribue une étiquette à ce qui est nécessaire pour définir un calcul avec [CNTK](https://www.microsoft.com/cognitive-toolkit/), une profondeur d’apprentissage :

```fsharp
open CNTK

// DeviceDescriptor, Variable, and Function all come from CNTK
type Computation = DeviceDescriptor -> Variable -> Function
```

Le `Computation` nom est un moyen pratique pour désigner n’importe quelle fonction qui correspond à la signature, il s’agit d’alias. À l’aide des abréviations de Type, comme cela est pratique et autorise le code plus concise.

### <a name="avoid-using-type-abbreviations-to-represent-your-domain"></a>Évitez d’utiliser les abréviations de Type pour représenter votre domaine

Bien que les abréviations de Type sont pratiques pour donner un nom à des signatures de fonction, elles peuvent être ambigües lors de l’abréviation d’autres types. Prenez en compte cette abréviation :

```fsharp
// Does not actually abstract integers.
type BufferSize = int
```

Cela peut prêter à confusion de plusieurs façons :

* `BufferSize` n’est pas une abstraction ; Il est simplement un autre nom d’un entier.
* Si `BufferSize` est exposé dans une API publique, il peut facilement être mal interprétée pour signifier plus que `int`. En général, les types de domaine ont plusieurs attributs leur et ne sont pas des types primitifs comme `int`. Cette abréviation viole cette hypothèse.
* La casse de `BufferSize` (PascalCase) implique que ce type conserve plus de données.
* Cet alias n’offre pas de souci de clarté accrue par rapport à fournir un argument nommé d’une fonction.
* L’abréviation n’apparaîtra pas dans IL compilé ; Il s’agit simplement d’un entier, et cet alias est une construction de la compilation.

```fsharp
module Networking =
    ...
    let send data (bufferSize: int) =
        ...
```

En résumé, le piège avec les abréviations de Type est qu’ils sont **pas** abstractions sur les types qu’ils sont l’abréviation. Dans l’exemple précédent, `BufferSize` est simplement un `int` en arrière-plan, avec des données supplémentaires, ni les avantages du système de type en dehors de ce que `int` a déjà.
