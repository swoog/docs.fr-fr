---
title: F#instructions de conception de composant
description: Découvrez les instructions pour l’écriture F# composants destinée à la consommation par les autres appelants.
ms.date: 05/14/2018
ms.openlocfilehash: c61e4cd9098388b356c71c325d66c760fa866cf0
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55066023"
---
# <a name="f-component-design-guidelines"></a>F#instructions de conception de composant

Ce document est un ensemble de règles de conception de composant pour F# de programmation, selon le F# les instructions de conception de composant, v14, Microsoft Research, et [une autre version](https://fsharp.org/specs/component-design-guidelines/) à l’origine organisé et géré par le F# Software Foundation.

Ce document suppose que vous êtes familiarisé avec F# de programmation. Plusieurs grâce à la F# Communauté pour obtenir des commentaires utiles sur différentes versions de ce guide et leurs contributions.

## <a name="overview"></a>Vue d'ensemble

Ce document présente certains des problèmes liés à F# conception de composant et de codage. Un composant peut signifier que les éléments suivants :

* Une couche dans votre F# projet qui a des consommateurs externes dans ce projet.
* Une bibliothèque destinée à la consommation par F# code entre les limites de l’assembly.
* Une bibliothèque destinée à la consommation par n’importe quel langage .NET entre les limites de l’assembly.
* Une bibliothèque prévue pour une distribution via un dépôt de packages, tels que [NuGet](https://nuget.org).

Suivent des techniques décrites dans cet article le [cinq principes bonne F# code](index.md#five-principles-of-good-f-code)et par conséquent utiliser à la fois fonctionnels et de l’objet de programmation comme il convient.

Quelle que soit la méthodologie, le Concepteur de composant et de bibliothèque est confronté à un nombre de problèmes pratiques et prosaïques lorsque vous tentez de créer une API qui n’est plus facilement utilisable par les développeurs. Consciencieux application de la [directives de conception de bibliothèque .NET](../../standard/design-guidelines/index.md) sera vous diriger vers la création d’un ensemble cohérent d’API qui sont agréables à utiliser.

## <a name="general-guidelines"></a>Indications générales

Il existe quelques instructions universelles qui s’appliquent à F# bibliothèques, quel que soit le public concerné par la bibliothèque.

### <a name="learn-the-net-library-design-guidelines"></a>Découvrez les instructions de conception de bibliothèque .NET

Quel que soit le type de F# codage vous effectuez, il est intéressant d’avoir une connaissance pratique de la [directives de conception de bibliothèque .NET](../../standard/design-guidelines/index.md). La plupart des autres F# et les programmeurs .NET seront connaissance de ces instructions et attendre le code .NET pour y conforment.

Les règles de conception de bibliothèque .NET fournissent des recommandations générales concernant d’affectation de noms, la conception des classes et interfaces, conception de membres (propriétés, méthodes, événements, etc.) et bien plus encore et sont utile premier point de référence pour un large éventail de guide de conception.

### <a name="add-xml-documentation-comments-to-your-code"></a>Ajouter des commentaires de documentation XML à votre code

Documentation XML sur les API publiques vous assurer que les utilisateurs peuvent obtenir excellent Intellisense et les Infosrapides lors de la bibliothèque à l’aide de ces types et membres et activer génération de documentation de fichiers. Consultez le [Documentation XML](../language-reference/xml-documentation.md) sur différentes balises xml qui peuvent être utilisées pour le balisage supplémentaire dans les commentaires de xmldoc.

```fsharp
/// A class for representing (x,y) coordinates
type Point =

    /// Computes the distance between this point and another
    member DistanceTo: otherPoint:Point -> float
```

Vous pouvez utiliser des commentaires XML forme abrégée (`/// comment`), ou des commentaires XML standards (`///<summary>comment</summary>`).

### <a name="consider-using-explicit-signature-files-fsi-for-stable-library-and-component-apis"></a>Envisagez d’utiliser des fichiers explicite de signature (.fsi) pour la bibliothèque stable et API de composant

À l’aide de fichiers de signatures explicite dans un F# bibliothèque fournit un résumé succinct des API publique, ce qui les deux permet de se pour assurer que vous connaissez le public complet surface de votre bibliothèque fournit une séparation nette entre la documentation publique et interne détails d’implémentation. Notez que les fichiers de signature ajoutent friction à l’évolution de l’API publique, en demandant des modifications doit être faite dans l’implémentation et la signature des fichiers. Par conséquent, les fichiers de signature doivent généralement uniquement être introduites lorsqu’une API deviennent solidification et est censée ne plus changer de manière significative.

### <a name="always-follow-best-practices-for-using-strings-in-net"></a>Suivez toujours les meilleures pratiques pour l’utilisation de chaînes dans .NET

Suivez [meilleures pratiques pour l’utilisation de chaînes dans .NET](../../standard/base-types/best-practices-strings.md) conseils. En particulier, l’état toujours explicitement *intention culturelle* dans la conversion et la comparaison de chaînes (le cas échéant).

## <a name="guidelines-for-f-facing-libraries"></a>Instructions pour F#-accessible sur les bibliothèques

Cette section présente des recommandations pour le développement publique F#-accessible sur les bibliothèques ; Autrement dit, les bibliothèques exposant les API publiques qui sont destinés à être consommés par F# les développeurs. Il existe une variété de recommandations sur la conception de la bibliothèque s’applique spécifiquement à F#. En l’absence des recommandations spécifiques qui suivent, les règles de conception de bibliothèque .NET sont les instructions de secours.

### <a name="naming-conventions"></a>Conventions d'attribution d'un nom

#### <a name="use-net-naming-and-capitalization-conventions"></a>Utiliser les conventions d’affectation de noms et de mise en majuscules de .NET

Le tableau suivant respecte les conventions d’affectation de noms et de mise en majuscules de .NET. Petite ajouts pour inclure également les F# construit.

| Construction | Case | Élément | Exemples | Notes |
|-----------|------|------|----------|-------|
| Types concrets | PascalCase | Nom / adjectif | La liste, Double, complexe | Types concrets sont des structs, des classes, des énumérations, des délégués, des enregistrements et des unions. Bien que les noms de types sont traditionnellement en minuscules dans OCaml, F# a adopté le schéma d’affectation de noms .NET pour les types.
| DLL           | PascalCase |                 | Fabrikam.Core.dll |  |
| Balises Union     | PascalCase | Nom | Certains, ajouter, réussite | N’utilisez pas de préfixe dans les API publiques. Si vous le souhaitez utiliser un préfixe lorsque internes, tels que `type Teams = TAlpha | TBeta | TDelta.` |
| Événement          | PascalCase | Verbe | ValueChanged / ValueChanging |  |
| Exceptions     | PascalCase |      | WebException | Nom doit se terminer avec « Exception ». |
| Champ          | PascalCase | Nom | CurrentName  | |
| Types interface |  PascalCase | Nom / adjectif | IDisposable | Nom doit commencer par « I ». |
| Méthode |  PascalCase |  Verbe | ToString | |
| Espace de noms | PascalCase | | Microsoft.FSharp.Core | En général utiliser `<Organization>.<Technology>[.<Subnamespace>]`, toutefois supprimer l’organisation si la technologie est indépendante de l’organisation. |
| Paramètres | camelCase | Nom |  typeName, transform, range | |
| laisser les valeurs (internes) | une casse mixte ou la casse Pascal | Nom / verbe |  getValue, myTable |
| laisser les valeurs (externe) | une casse mixte ou la casse Pascal | Nom/verbe  | List.map, Dates.Today | Let lié aux valeurs sont souvent publique si l'on suit les modèles de conception fonctionnelle traditionnel. Toutefois, généralement utiliser la casse Pascal lors de l’identificateur peut être utilisé à partir d’autres langages .NET. |
| Propriété  | PascalCase  | Nom / adjectif  | IsEndOfFile, BackColor  | Propriétés booléennes généralement l’utilisation est et peut et doit être positive, comme dans IsEndOfFile, IsNotEndOfFile pas.

#### <a name="avoid-abbreviations"></a>Éviter les abréviations

Les règles de .NET déconseillons l’utilisation des abréviations (par exemple, « utiliser `OnButtonClick` plutôt que `OnBtnClick`»). Abréviations courantes, telles que `Async` pour « Asynchrone », sont tolérées. Cette recommandation est parfois ignorée pour la programmation fonctionnelle ; par exemple, `List.iter` utilise une abréviation pour « parcourir ». Pour cette raison, à l’aide des abréviations a tendance à être tolérée à un degré supérieur dans F#- au -F# de programmation, mais doit toujours en général être évitées dans la conception du composant public.

#### <a name="avoid-casing-name-collisions"></a>Éviter les collisions de noms de mise en majuscules

Les règles de .NET dire que casse seul ne peut pas être utilisée pour lever l’ambiguïté des collisions de noms, dans la mesure où certaines langues du client (par exemple, Visual Basic) respectent la casse.

#### <a name="use-acronyms-where-appropriate"></a>Utiliser des acronymes approprié

Acronymes tel que XML ne sont pas des abréviations et sont couramment utilisés dans les bibliothèques .NET dans le formulaire en minuscule (Xml). Uniquement les acronymes bien connus, largement reconnues doivent être utilisés.

#### <a name="use-pascalcase-for-generic-parameter-names"></a>Utilisez la casse Pascal pour les noms de paramètre générique

Utilisez la casse Pascal pour les noms de paramètre générique dans les API publiques, y compris pour F#-accessible sur les bibliothèques. En particulier, utilisez des noms comme `T`, `U`, `T1`, `T2` pour les paramètres génériques arbitraires, et lorsque des noms spécifiques sont justifiées, puis pour F#-bibliothèques exposés utilisent des noms tels que `Key`, `Value`, `Arg` (mais pas par exemple, `TKey`).

#### <a name="use-either-pascalcase-or-camelcase-for-public-functions-and-values-in-f-modules"></a>Utilisez la casse Pascal ou la casse mixte pour les fonctions publiques et les valeurs de F# modules

une casse mixte est utilisée pour les fonctions publiques qui sont conçues pour être utilisés non qualifié (par exemple, `invalidArg`) et pour les fonctions de collection standard « » (par exemple, List.map). Dans ces deux cas, les noms de fonction fonctionnant un peu comme mots clés du langage.

### <a name="object-type-and-module-design"></a>Conception de Type, l’objet et le Module

#### <a name="use-namespaces-or-modules-to-contain-your-types-and-modules"></a>Utilisez des espaces de noms ou des modules pour contenir vos types et les modules

Chaque F# fichier dans un composant doit commencer par une déclaration d’espace de noms ou une déclaration de module.

```fsharp
namespace Fabrikam.BasicOperationsAndTypes

type ObjectType1() =
    ...

type ObjectType2() =
     ...

module CommonOperations =
    ...
```

ou

```fsharp
module Fabrikam.BasicOperationsAndTypes

type ObjectType1() =
    ...

type ObjectType2() =
    ...

module CommonOperations =
    ...
```

Les différences entre l’utilisation des modules et des espaces de noms pour organiser le code au niveau supérieur sont les suivantes :

* Espaces de noms peut s’étendre sur plusieurs fichiers
* Espaces de noms ne peut pas contenir F# fonctions, sauf si ces derniers sont dans un module interne
* Le code de n’importe quel module donné doit être contenu dans un seul fichier
* Modules de niveau supérieur peuvent contenir F# fonctions sans avoir besoin d’un module interne

Le choix entre un espace de noms de niveau supérieur ou un module a une incidence sur la forme compilée du code et par conséquent affecteront la vue à partir d’autres langages .NET devrait votre API être consommée en dehors de F# code.

#### <a name="use-methods-and-properties-for-operations-intrinsic-to-object-types"></a>Utiliser les méthodes et propriétés pour les opérations intrinsèques aux types d’objets

Lorsque vous travaillez avec des objets, il est préférable pour vous assurer que les fonctionnalité consommable est implémentée en tant que les méthodes et propriétés sur ce type.

```fsharp
type HardwareDevice() =

    member this.ID = ...

    member this.SupportedProtocols = ...

type HashTable<'Key,'Value>(comparer: IEqualityComparer<'Key>) =

    member this.Add(key, value) = ...

    member this.ContainsKey(key) = ...

    member this.ContainsValue(value) = ...
```

La majeure partie des fonctionnalités pour un membre donné ne doive pas nécessairement implémentée dans ce membre, mais la partie consommable de cette fonctionnalité doit être.

#### <a name="use-classes-to-encapsulate-mutable-state"></a>Utiliser des classes pour encapsuler un état mutable

Dans F#, cela ne doit être effectuée où qu’état n’est pas déjà encapsulé par une autre construction de langage, par exemple une fermeture, une expression de séquence ou un calcul asynchrone.

```fsharp
type Counter() =
    // let-bound values are private in classes.
    let mutable count = 0

    member this.Next() =
        count <- count + 1
        count
```

#### <a name="use-interfaces-to-group-related-operations"></a>Utiliser des interfaces pour regrouper des opérations associées

Utiliser des types d’interface pour représenter un ensemble d’opérations. Cette option est préférable aux autres options, telles que des tuples de fonctions ou des enregistrements de fonctions.

```fsharp
type Serializer =
    abstract Serialize<'T>: preserveRefEq: bool -> value: 'T -> string
    abstract Deserialize<'T>: preserveRefEq: bool -> pickle: string -> 'T
```

De préférence à :

```fsharp
type Serializer<'T> = {
    Serialize: bool -> 'T -> string
    Deserialize: bool -> string -> 'T
}
```

Les interfaces sont des concepts de première classe dans .NET, qui vous permettent d’obtenir les Functors normalement vous donnera. En outre, elles peuvent servir pour encoder les types existentiels dans votre programme, qui ne peut pas des enregistrements de fonctions.

#### <a name="use-a-module-to-group-functions-which-act-on-collections"></a>Utiliser un module à des fonctions de groupe qui agissent sur des collections

Lorsque vous définissez un type de collection, envisagez de fournir un ensemble standard d’opérations telles que `CollectionType.map` et `CollectionType.iter`) pour les nouveaux types de collection.

```fsharp
module CollectionType =
    let map f c =
        ...
    let iter f c =
        ...
```

Si vous incluez un de ces modules, suivez les conventions d’affectation de noms des fonctions trouvées dans FSharp.Core.

#### <a name="use-a-module-to-group-functions-for-common-canonical-functions-especially-in-math-and-dsl-libraries"></a>Utiliser un module à des fonctions de groupe pour les fonctions canoniques courants, en particulier dans les mathématiques et les bibliothèques DSL

Par exemple, `Microsoft.FSharp.Core.Operators` est une collection automatiquement ouverte de fonctions de niveau supérieur (comme `abs` et `sin`) fourni par FSharp.Core.dll.

De même, une bibliothèque de statistiques peut inclure un module avec des fonctions `erf` et `erfc`, où ce module est conçu pour être ouverte explicitement ou automatiquement.

#### <a name="consider-using-requirequalifiedaccess-and-carefully-apply-autoopen-attributes"></a>Envisagez d’utiliser des RequireQualifiedAccess et appliquez soigneusement les attributs de AutoOpen

Ajout de la `[<RequireQualifiedAccess>]` attribut à un module indique que le module ne peut-être pas être ouverts et des références aux éléments du module doivent explicite qualifié d’accès. Par exemple, le `Microsoft.FSharp.Collections.List` module a cet attribut.

Cela est utile lorsque les valeurs dans le module et les fonctions ont des noms qui sont susceptibles d’entrer en conflit avec les noms dans d’autres modules. Nécessitant un accès complet peut augmenter considérablement la facilité de maintenance à long terme et aspects d’une bibliothèque.

Ajout de la `[<AutoOpen>]` attribut à un module signifie que le module s’ouvre quand l’espace de noms conteneur est ouvert. Le `[<AutoOpen>]` attribut peut également être appliqué à un assembly pour indiquer un module qui s’ouvre automatiquement quand l’assembly est référencé.

Par exemple, une bibliothèque de statistiques **MathsHeaven.Statistics** peut contenir un `module MathsHeaven.Statistics.Operators` contenant des fonctions `erf` et `erfc`. Il est raisonnable de marquer ce module en tant que `[<AutoOpen>]`. Cela signifie que `open MathsHeaven.Statistics` également ouvrir ce module et afficher les noms `erf` et `erfc` dans l’étendue. Utiliser une autre bonne `[<AutoOpen>]` est pour les modules contenant les méthodes d’extension.

Abusez de `[<AutoOpen>]` aboutissent à des espaces de noms polluée et l’attribut doit être utilisée avec précaution. Pour les bibliothèques spécifiques dans des domaines spécifiques, une utilisation judicieuse de `[<AutoOpen>]` peut entraîner une meilleure convivialité.

#### <a name="consider-defining-operator-members-on-classes-where-using-well-known-operators-is-appropriate"></a>Envisagez de définir des membres de l’opérateur sur les classes où à l’aide des opérateurs bien connus est approprié

Parfois, les classes sont utilisées pour modéliser des mathématiques constructions telles que les vecteurs. Quand le domaine en cours de modélisation possède des opérateurs bien connus, il est utile de les définir en tant que membres intrinsèques à la classe.

```fsharp
type Vector(x: float) =

    member v.X = x

    static member (*) (vector: Vector, scalar: float) = Vector(vector.X * scalar)

    static member (+) (vector1: Vector, vector2: Vector) = Vector(vector1.X + vector2.X)

let v = Vector(5.0)

let u = v * 10.0
```

Ce guide correspond aux conseils généraux de .NET pour ces types. Toutefois, il peut être plus important dans F# codage car cela permet à ces types à utiliser conjointement avec F# fonctions et méthodes avec des contraintes de membre, telles que List.sumBy.

#### <a name="consider-using-compiledname-to-provide-a-net-friendly-name-for-other-net-language-consumers"></a>Envisagez d’utiliser CompiledName pour fournir une. Nom NET conviviale pour les autres consommateurs de langage .NET

Parfois, vous pouvez souhaiter donnez un nom dans un style pour les F# consommateurs (tel qu’un membre statique en minuscules afin qu’il apparaisse comme s’il s’agissait d’une fonction liée au module), mais ont un style différent pour le nom lorsqu’il est compilé dans un assembly. Vous pouvez utiliser la `[<CompiledName>]` attribut pour fournir un style différent pour non F# code utilisant l’assembly.

```fsharp
type Vector(x:float, y:float) =

    member v.X = x
    member v.Y = y

    [<CompiledName("Create")>]
    static member create x y = Vector (x, y)

let v = Vector.create 5.0 3.0
```

À l’aide de `[<CompiledName>]`, vous pouvez utiliser les conventions de nommage .NET pour non F# consommateurs de l’assembly.

#### <a name="use-method-overloading-for-member-functions-if-doing-so-provides-a-simpler-api"></a>Utilisez la surcharge de méthode pour les fonctions de membre, si cela vous permet une API plus simple

La surcharge de méthode est un outil puissant permettant de simplifier une API qui devra peut-être effectuer une fonctionnalité similaire, mais avec des options ou des arguments.

```fsharp
type Logger() =

    member this.Log(message) =
        ...
    member this.Log(message, retryPolicy) =
        ...
```

Dans F#, il est plus courant de surcharge sur le nombre d’arguments plutôt que des types d’arguments.

#### <a name="hide-the-representations-of-record-and-union-types-if-the-design-of-these-types-is-likely-to-evolve"></a>Masquer les représentations sous forme d’enregistrement et de types union si la conception de ces types est susceptible d’évoluer

Éviter de révéler des représentations concrètes des objets. Par exemple, la représentation concrète de <xref:System.DateTime> valeurs n’est pas révélée par l’API externe, public de la conception de la bibliothèque .NET. Au moment de l’exécution, le Common Language Runtime sait l’implémentation validée qui sera utilisée tout au long de l’exécution. Toutefois, code compilé ne lui-même récupère les dépendances sur la représentation concrète.

#### <a name="avoid-the-use-of-implementation-inheritance-for-extensibility"></a>Évitez d’utiliser l’héritage d’implémentation pour l’extensibilité

Dans F#, mise en œuvre l’héritage est rarement utilisé. En outre, les hiérarchies d’héritage sont souvent complexes et difficiles à modifier à l’arrivée de nouvelles exigences. Implémentation de l’héritage existe toujours dans F# pour la compatibilité et les rares cas où il est la meilleure solution à un problème, mais les autres techniques doivent être recherchées dans votre F# programmes lors de la conception pour le polymorphisme, par exemple d’interface mise en œuvre.

### <a name="function-and-member-signatures"></a>Signatures de fonction et de membre

#### <a name="use-tuples-for-return-values-when-returning-a-small-number-of-multiple-unrelated-values"></a>Utiliser des tuples pour les valeurs de retour lors du retour d’un petit nombre de plusieurs valeurs non liées

Voici un bon exemple d’utilisation d’un tuple dans un type de retour :

```fsharp
val divrem: BigInteger -> BigInteger -> BigInteger * BigInteger
```

Pour retourner des types contenant de nombreux composants, ou où les composants sont associés à une seule entité identifiable, envisagez d’utiliser un type nommé au lieu d’un tuple.

#### <a name="use-asynct-for-async-programming-at-f-api-boundaries"></a>Utilisez `Async<T>` pour la programmation à async F# limites des API

S’il existe une opération synchrone correspondante nommée `Operation` qui retourne un `T`, puis l’opération asynchrone doit être nommée `AsyncOperation` si elle retourne `Async<T>` ou `OperationAsync` si elle retourne `Task<T>`. Pour les types .NET couramment utilisés qui exposent des méthodes Begin/End, envisagez d’utiliser `Async.FromBeginEnd` pour écrire des méthodes d’extension comme une façade pour fournir le F# modèle de programmation asynchrone pour les API .NET.

```fsharp
type SomeType =
    member this.Compute(x:int): int =
        ...
    member this.AsyncCompute(x:int): Async<int> =
        ...

type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        ...
```

### <a name="exceptions"></a>Exceptions

Consultez [gestion des erreurs](conventions.md#error-management) pour en savoir plus sur l’utilisation appropriée des exceptions, les résultats et les options.

### <a name="extension-members"></a>Membres d’extension

#### <a name="carefully-apply-f-extension-members-in-f-to-f-components"></a>Appliquez soigneusement F# membres d’extension dans F#- au -F# composants

F#membres d’extension doivent généralement être utilisées uniquement pour les opérations qui se trouvent dans la clôture d’opérations intrinsèques associées à un type dans la majorité de ses modes d’utilisation. Une utilisation courante consiste à fournir des API qui sont plus idiomatiques F# pour différents types de .NET :

```fsharp
type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        Async.FromBeginEnd(this.BeginReceive, this.EndReceive)

type System.Collections.Generic.IDictionary<'Key,'Value> with
    member this.TryGet key =
        let ok, v = this.TryGetValue key
        if ok then Some v else None
```

### <a name="union-types"></a>Types d’union

#### <a name="use-discriminated-unions-instead-of-class-hierarchies-for-tree-structured-data"></a>Utiliser les unions discriminées au lieu de hiérarchies de classes pour les données structurées en arborescence

Structures en arborescence sont définis de manière récursive. C’est délicat avec l’héritage, mais il est élégant avec des Unions discriminées.

```fsharp
type BST<'T> =
    | Empty
    | Node of 'T * BST<'T> * BST<'T>
```

Représentant les données sous forme d’arborescence avec des Unions discriminées vous permet également de bénéficier d’exhaustivité dans les critères spéciaux.

#### <a name="use-requirequalifiedaccess-on-union-types-whose-case-names-are-not-sufficiently-unique"></a>Utilisez `[<RequireQualifiedAccess>]` sur les types d’union dont les noms cas ne sont pas suffisamment uniques

Vous pouvez vous retrouver dans un domaine où le même nom est le meilleur nom pour des choses différentes, telles que des cas d’Union discriminée. Vous pouvez utiliser `[<RequireQualifiedAccess>]` pour lever l’ambiguïté des noms d’incidents afin d’éviter de déclencher des erreurs à confusion en raison d’une occultation dépendantes de l’ordre des `open` instructions

#### <a name="hide-the-representations-of-discriminated-unions-for-binary-compatible-apis-if-the-design-of-these-types-is-likely-to-evolve"></a>Masquer les représentations sous forme d’unions discriminées pour les API compatible binaire si la conception de ces types est susceptible d’évoluer

Types d’unions s’appuient sur F# correspondance des formulaires pour un modèle de programmation concis. Comme mentionné précédemment, vous devez éviter de révéler les représentations sous forme de données concrètes si la conception de ces types est susceptible d’évoluer.

Par exemple, la représentation sous forme d’une union discriminée peut être masquée à l’aide d’une déclaration privée ou interne, ou à l’aide d’un fichier de signature.

```fsharp
type Union =
    private
    | CaseA of int
    | CaseB of string
```

Si vous affichez les unions discriminées sans discrimination, il peut s’avérer difficile de version de votre bibliothèque sans casser le code de l’utilisateur. Envisagez plutôt de révéler un ou plusieurs modèles actifs pour autoriser des critères spéciaux sur les valeurs de votre type.

Modèles actifs fournissent une autre méthode pour fournir F# consommateurs disposant de critères spéciaux tout en évitant l’exposition F# directement les Types d’Union.

### <a name="inline-functions-and-member-constraints"></a>Les fonctions inline et les contraintes de membre

#### <a name="define-generic-numeric-algorithms-using-inline-functions-with-implied-member-constraints-and-statically-resolved-generic-types"></a>Définir les algorithmes numériques génériques à l’aide des fonctions inline avec les contraintes de membre implicite et les types génériques résolus statiquement

Contraintes de membre arithmétique et F# contraintes de comparaison sont une norme pour F# de programmation. Considérons par exemple le code suivant :

```fsharp
let inline highestCommonFactor a b =
    let rec loop a b =
        if a = LanguagePrimitives.GenericZero<_> then b
        elif a < b then loop a (b - a)
        else loop (a - b) b
    loop a b
```

Le type de cette fonction est comme suit :

```fsharp
val inline highestCommonFactor : ^T -> ^T -> ^T
                when ^T : (static member Zero : ^T)
                and ^T : (static member ( - ) : ^T * ^T -> ^T)
                and ^T : equality
                and ^T : comparison
```

Il s’agit d’une fonction appropriée pour une API publique dans une bibliothèque mathématique.

#### <a name="avoid-using-member-constraints-to-simulate-type-classes-and-duck-typing"></a>Évitez d’utiliser des contraintes de membre pour simuler des classes de type et canard en tapant

Il est possible de simuler à l’aide de « canard en tapant » F# les contraintes de membre. Toutefois, les membres qui rendent utilisent ce grand pas en utiliser dans F#- au -F# conceptions de bibliothèque. Il s’agit, car les conceptions de bibliothèque en fonction des contraintes implicites inconnus ou non standards ont tendance à provoquer le code utilisateur à devenir rigide et liée au modèle un framework particulier.

En outre, il est probable que le temps de compilation très longue peut entraîner une utilisation intensive de contraintes de membre de cette manière.

### <a name="operator-definitions"></a>Définitions d’opérateur

#### <a name="avoid-defining-custom-symbolic-operators"></a>Évitez de définir des opérateurs symboliques personnalisés

Opérateurs personnalisés sont essentielles dans certaines situations et des appareils de notation très utiles au sein d’un large corps de code d’implémentation. Pour les nouveaux utilisateurs d’une bibliothèque, fonctions nommées sont souvent plus faciles à utiliser. En outre, les opérateurs symboliques personnalisés peuvent être difficiles de document, et rend difficile plus à rechercher de l’aide sur les opérateurs, en raison des limitations existantes dans l’IDE et recherche des moteurs.

Par conséquent, il est préférable de publier vos fonctionnalités en tant que fonctions nommées et les membres et exposer en outre les opérateurs pour cette fonctionnalité uniquement si les notation avantages l’emportent sur la documentation et les cognitive coût engendré par les.

### <a name="units-of-measure"></a>Unités de mesure

#### <a name="carefully-use-units-of-measure-for-added-type-safety-in-f-code"></a>Avec soin les unités de mesure de la sécurité de type ajouté dans F# code

Information de type supplémentaire pour les unités de mesure est effacée lorsqu’ils sont affichés par d’autres langages .NET. N’oubliez pas que la réflexion, des outils et composants .NET verra types sans unités. Par exemple, C# consommateurs verrez `float` plutôt que `float<kg>`.

### <a name="type-abbreviations"></a>Abréviations de types

#### <a name="carefully-use-type-abbreviations-to-simplify-f-code"></a>Utiliser avec précaution les abréviations de type pour simplifier F# code

Réflexion, des outils et composants .NET ne verront pas les noms abrégés pour les types. Intensive des abréviations de type peut également afficher un domaine plus complexe qu’il est en fait, ce qui peut perturber de consommateurs.

#### <a name="avoid-type-abbreviations-for-public-types-whose-members-and-properties-should-be-intrinsically-different-to-those-available-on-the-type-being-abbreviated"></a>Éviter les abréviations de type pour les types publics dont les membres et les propriétés doivent être intrinsèquement différents de ceux disponibles sur le type en cours abrégé

Dans ce cas, le type en cours abrégé révèle trop d’informations sur la représentation du type réel qui est défini. Au lieu de cela, envisagez d’encapsuler l’abréviation dans un type de classe ou une union discriminée cas unique (ou, lorsque les performances sont essentielles, envisagez d’utiliser un type struct pour encapsuler l’abréviation).

Par exemple, il est tentant de définir un mappage multi comme un cas spécial d’un F# la carte, par exemple :

```fsharp
type MultiMap<'Key,'Value> = Map<'Key,'Value list>
```

Toutefois, les opérations logiques-notation par points sur ce type ne sont pas le même que les opérations sur une carte – par exemple, il est raisonnable que l’opérateur de recherche sont mappés. la liste vide si la clé n’est pas dans le dictionnaire, au lieu de lever une exception de retour [clé].

## <a name="guidelines-for-libraries-for-use-from-other-net-languages"></a>Instructions pour les bibliothèques à utiliser à partir d’autres langages .NET

Lorsque vous concevez des bibliothèques à utiliser à partir d’autres langages .NET, il est important de respecter le [directives de conception de bibliothèque .NET](../../standard/design-guidelines/index.md). Dans ce document, ces bibliothèques sont étiquetés comme des bibliothèques .NET vanille, par opposition à F#-accessible sur les bibliothèques qui utilisent F# construit sans restriction. Conception des bibliothèques .NET vanille on entend : fournir des API familières et idiomatiques cohérents avec le reste du .NET Framework en réduisant l’utilisation de F#-des constructions spécifiques dans l’API publique. Les règles sont expliquées dans les sections suivantes.

### <a name="namespace-and-type-design-for-libraries-for-use-from-other-net-languages"></a>Conception Namespace et Type (pour les bibliothèques à utiliser à partir d’autres langages .NET)

#### <a name="apply-the-net-naming-conventions-to-the-public-api-of-your-components"></a>Appliquer les conventions d’affectation de noms .NET à l’API publique de vos composants

Faites particulièrement attention à l’utilisation de noms abrégés et les règles de mise en majuscules de .NET.

```fsharp
type pCoord = ...
    member this.theta = ...

type PolarCoordinate = ...
    member this.Theta = ...
```

#### <a name="use-namespaces-types-and-members-as-the-primary-organizational-structure-for-your-components"></a>Utilisez des espaces de noms, types et membres en tant que la structure organisationnelle principale pour vos composants

Tous les fichiers contenant des fonctionnalités publiques doivent commencer par un `namespace` déclaration et que les seules entités destinées au public dans les espaces de noms doivent être des types. N’utilisez pas F# modules.

Utilisez les modules non publics pour contenir le code d’implémentation, les types de l’utilitaire et les fonctions utilitaires.

Les types static doivent avoir priorité sur les modules, car elles permettent une évolution future de l’API à utiliser la surcharge et d’autres principes de conception de l’API .NET qui ne peuvent pas être utilisés au sein de F# modules.

Par exemple, à la place de l’API publique suivante :

```fsharp
module Fabrikam

module Utilities =
    let Name = "Bob"
    let Add2 x y = x + y
    let Add3 x y z = x + y + z
```

Pensez à la place :

```fsharp
namespace Fabrikam

[<AbstractClass; Sealed>]
type Utilities =
    static member Name = "Bob"
    static member Add(x,y) = x + y
    static member Add(x,y,z) = x + y + z
```

#### <a name="use-f-record-types-in-vanilla-net-apis-if-the-design-of-the-types-wont-evolve"></a>Utilisez F# types d’enregistrements dans l’API .NET de vanille si la conception des types ne sont pas évoluer.

F#types d’enregistrements compilent à une classe .NET simple. Ils ne conviennent pas pour certains types simples, stables dans les API. Vous devez envisager d’utiliser le `[<NoEquality>]` et `[<NoComparison>]` attributs à supprimer la génération automatique des interfaces. Évitez également à l’aide des champs d’enregistrement mutable dans vanille API .NET en tant que ces expose un champ public. Toujours envisager si une classe fournirait une option plus flexible pour l’évolution future de l’API.

Par exemple, ce qui suit F# code expose l’API publique pour un C# consommateur :

F# :

```fsharp
[<NoEquality; NoComparison>]
type MyRecord =
    { FirstThing: int
        SecondThing: string }
```

C# :

```csharp
public sealed class MyRecord
{
    public MyRecord(int firstThing, string secondThing);
    public int FirstThing { get; }
    public string SecondThing { get; }
}
```

#### <a name="hide-the-representation-of-f-union-types-in-vanilla-net-apis"></a>Masquer la représentation sous forme de F# types union dans vanille API .NET

F#les types d’union ne sont pas utilisés au-delà des limites de composant, généralement même pour F#- au -F# de codage. Il s’agit d’un appareil de mise en œuvre une excellente lorsqu’il est utilisé en interne au sein des composants et des bibliothèques.

Lorsque vous concevez une API .NET vanille, vous pouvez le masquer la représentation sous forme d’un type union en utilisant une déclaration privée ou un fichier de signature.

```fsharp
type PropLogic =
    private
    | And of PropLogic * PropLogic
    | Not of PropLogic
    | True
```

Vous pouvez également augmenter les types qui permettent une représentation union en interne avec les membres de fournir un texte souhaité. API NET orientés.

```fsharp
type PropLogic =
    private
    | And of PropLogic * PropLogic
    | Not of PropLogic
    | True

    /// A public member for use from C#
    member x.Evaluate =
        match x with
        | And(a,b) -> a.Evaluate && b.Evaluate
        | Not a -> not a.Evaluate
        | True -> true

    /// A public member for use from C#
    static member CreateAnd(a,b) = And(a,b)
```

#### <a name="design-gui-and-other-components-using-the-design-patterns-of-the-framework"></a>Conception de l’interface graphique utilisateur et d’autres composants à l’aide de modèles de conception de l’infrastructure

Plusieurs environnements différents sont disponibles dans .NET, tels que ASP.NET, WinForms et WPF. Conventions d’affectation de noms et de conception pour chacun doivent être utilisées si vous concevez des composants pour une utilisation dans ces infrastructures. Par exemple, pour la programmation WPF, adopter les modèles de conception WPF pour les classes que vous concevez. Pour les modèles de programmation de l’interface utilisateur, utilisez les modèles de conception tels que des événements et basé sur la notification de collections tels que ceux trouvent dans <xref:System.Collections.ObjectModel>.

### <a name="object-and-member-design-for-libraries-for-use-from-other-net-languages"></a>Conception de membre et d’objet (pour les bibliothèques à utiliser à partir d’autres langages .NET)

#### <a name="use-the-clievent-attribute-to-expose-net-events"></a>Utilisez l’attribut CLIEvent pour exposer des événements .NET

Construire un `DelegateEvent` avec .NET spécifique le type qui prend un objet de délégué et `EventArgs` (plutôt qu’un `Event`, qui utilise simplement le `FSharpHandler` type par défaut) afin que les événements sont publiés dans le moyen familier d’autres langages .NET.

```fsharp
type MyBadType() =
    let myEv = new Event<int>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish

type MyEventArgs(x: int) =
    inherit System.EventArgs()
    member this.X = x

    /// A type in a component designed for use from other .NET languages
type MyGoodType() =
    let myEv = new DelegateEvent<EventHandler<MyEventArgs>>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish
```

#### <a name="expose-asynchronous-operations-as-methods-which-return-net-tasks"></a>Exposer des opérations asynchrones en tant que méthodes qui retournent des tâches de .NET

Tâches sont utilisées dans .NET pour représenter les calculs asynchrones actives. Les tâches sont en général moins composition que F# `Async<T>` objets, car ils représentent les tâches « en cours d’exécution » et ne peut pas être combinées dans les méthodes qui effectuent la composition parallèle, ou qui masquer la propagation de signaux de l’annulation et d’autres paramètres contextuelles.

Toutefois, en dépit de cela, les méthodes qui retournent des tâches sont la représentation de la programmation asynchrone dans .NET standard.

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =

    let compute (x: int): Async<int> = async { ... }

    member this.ComputeAsync(x) = compute x |> Async.StartAsTask
```

Vous allez souvent que vous souhaitez également accepter un jeton d’annulation explicite :

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =
    let compute(x: int): Async<int> = async { ... }
    member this.ComputeAsTask(x, cancellationToken) = Async.StartAsTask(compute x, cancellationToken)
```

#### <a name="use-net-delegate-types-instead-of-f-function-types"></a>Utiliser des types de délégués .NET à la place de F# types de fonction

Ici «F# types de fonction » signifie que les types « flèche » comme `int -> int`.

Au lieu de cela :

```fsharp
member this.Transform(f: int->int) =
    ...
```

Procédez comme suit :

```fsharp
member this.Transform(f: Func<int,int>) =
    ...
```

Le F# type de fonction apparaît sous la forme `class FSharpFunc<T,U>` à d’autres langages .NET et est moins adaptée pour les fonctionnalités de langage et outils qui comprennent les types délégués. Lors de la création d’une méthode d’ordre supérieur qui ciblent .NET Framework 3.5 ou version ultérieure, le `System.Func` et `System.Action` les délégués sont les API de droite à publier pour permettre aux développeurs .NET de consommer ces API de manière faible friction. (Si vous ciblez .NET Framework 2.0, les types délégués définis par le système sont plus limités ; envisagez d’utiliser des types de délégué prédéfinis, tels que `System.Converter<T,U>` ou définition d’un type délégué spécifique.)

En revanche, les délégués .NET ne sont pas naturelles pour F#-accessible sur les bibliothèques (consultez la Section suivante sur F#-accessible sur les bibliothèques). Par conséquent, une stratégie d’implémentation courantes lors du développement des méthodes d’ordre supérieur pour les bibliothèques .NET vanille consiste à créer tout l’implémentation en utilisant F# types de fonction et puis créer l’API publique à l’aide de délégués comme une façade mince située en haut de la F#implémentation.

#### <a name="use-the-trygetvalue-pattern-instead-of-returning-f-option-values-and-prefer-method-overloading-to-taking-f-option-values-as-arguments"></a>Utiliser le modèle TryGetValue au lieu de retourner F# les valeurs d’option et préférez la surcharge de méthode pour la prise de F# les valeurs en tant qu’arguments d’option

Modèles courants d’utilisation pour le F# type d’option dans les API sont préférables implémenté dans vanille techniques de création des API de .NET à l’aide de .NET standard. Au lieu de retourner un F# valeur d’option, envisagez d’utiliser le type de retour de bool ainsi qu’un paramètre de sortie, comme dans le modèle « TryGetValue ». Et au lieu de prendre F# les valeurs en tant que paramètres d’option, envisagez d’utiliser des arguments de méthode surcharge ou facultatif.

```fsharp
member this.ReturnOption() = Some 3

member this.ReturnBoolAndOut(outVal: byref<int>) =
    outVal <- 3
    true

member this.ParamOption(x: int, y: int option) =
    match y with
    | Some y2 -> x + y2
    | None -> x

member this.ParamOverload(x: int) = x

member this.ParamOverload(x: int, y: int) = x + y
```

#### <a name="use-the-net-collection-interface-types-ienumerablet-and-idictionarykeyvalue-for-parameters-and-return-values"></a>Utiliser l’interface de collection .NET des types IEnumerable\<T\> et IDictionary\<clé, valeur\> pour les paramètres et valeurs de retour

Évitez d’utiliser des types de collection concrets tels que les tableaux .NET `T[]`, F# types `list<T>`, `Map<Key,Value>` et `Set<T>`, et les types de collection concrets .NET tels que `Dictionary<Key,Value>`. Les règles de conception de bibliothèque .NET ont bon Conseil concernant quand utiliser les différents types de collection comme `IEnumerable<T>`. Une utilisation de tableaux (`T[]`) est acceptable dans certains cas, pour des raisons de performances. Notez en particulier que `seq<T>` est simplement le F# alias `IEnumerable<T>`, et seq est donc souvent un type approprié pour une API .NET vanille.

Au lieu de F# répertorie :

```fsharp
member this.PrintNames(names: string list) =
    ...
```

Utilisez F# séquences :

```fsharp
member this.PrintNames(names: seq<string>) =
    ...
```

#### <a name="use-the-unit-type-as-the-only-input-type-of-a-method-to-define-a-zero-argument-method-or-as-the-only-return-type-to-define-a-void-returning-method"></a>Utiliser le type d’unité en tant que le seul type d’entrée d’une méthode pour définir une méthode sans argument, ou en tant que le seul type de retour par définir une méthode retournant void

Évitez d’autres utilisations du type d’unité. Il s’agit bon :

```fsharp
✔ member this.NoArguments() = 3

✔ member this.ReturnVoid(x: int) = ()
```

Cela est incorrect :

```fsharp
member this.WrongUnit( x: unit, z: int) = ((), ())
```

#### <a name="check-for-null-values-on-vanilla-net-api-boundaries"></a>Vérifier les valeurs null sur les limites de l’API .NET vanille

F#code d’implémentation a tendance à avoir moins de valeurs null, en raison des modèles de conception immuable et les restrictions sur l’utilisation des littéraux null pour F# types. Autres langages .NET utilisent souvent null en tant que valeur beaucoup plus fréquemment. Pour cette raison, F# code qui expose une API .NET vanille doit vérifier les paramètres pour la valeur null à la limite de l’API et ces valeurs empêcher de passer plus profondément dans le F# code d’implémentation. Le `isNull` (fonction) ou des critères spéciaux sur les `null` modèle peut être utilisé.

```fsharp
let checkNonNull argName (arg: obj) =
    match arg with
    | null -> nullArg argName
    | _ -> ()

let checkNonNull` argName (arg: obj) =
    if isNull arg then nullArg argName
    else ()
```

#### <a name="avoid-using-tuples-as-return-values"></a>Évitez d’utiliser des tuples comme valeurs de retour

Au lieu de cela, préférez retournant un type nommé contenant les données d’agrégation ou d’utiliser les paramètres de sortie pour retourner plusieurs valeurs. Bien que les tuples et les tuples de struct existent dans .NET (notamment C# prise en charge linguistique pour les tuples de struct), ils plus souvent ne fournira pas l’API idéale et attendu pour les développeurs .NET.

#### <a name="avoid-the-use-of-currying-of-parameters"></a>Évitez d’utiliser des curryfication de paramètres

Au lieu de cela, utilisez les conventions d’appel de .NET `Method(arg1,arg2,…,argN)`.

```fsharp
member this.TupledArguments(str, num) = String.replicate num str
```

Conseil : Si vous concevez des bibliothèques à utiliser à partir de n’importe quel langage .NET, rien ne vaut pour faire réellement certaines expérimentale C# et pour vous assurer que vos bibliothèques « la convivialité droite » à partir de ces langages de programmation Visual Basic. Vous pouvez également utiliser des outils tels que .NET Reflector et l’Explorateur d’objets Visual Studio pour vous assurer que les bibliothèques et leur documentation apparaissent comme prévu pour les développeurs.

## <a name="appendix"></a>Annexe

### <a name="end-to-end-example-of-designing-f-code-for-use-by-other-net-languages"></a>Exemple de bout en bout de la conception F# code pour une utilisation par d’autres langages .NET

Considérez la classe suivante :

```fsharp
open System

type Point1(angle,radius) =
    new() = Point1(angle=0.0, radius=0.0)
    member x.Angle = angle
    member x.Radius = radius
    member x.Stretch(l) = Point1(angle=x.Angle, radius=x.Radius * l)
    member x.Warp(f) = Point1(angle=f(x.Angle), radius=x.Radius)
    static member Circle(n) =
        [ for i in 1..n -> Point1(angle=2.0*Math.PI/float(n), radius=1.0) ]
```

Le déduit F# est de type de cette classe comme suit :

```fsharp
type Point1 =
    new : unit -> Point1
    new : angle:double * radius:double -> Point1
    static member Circle : n:int -> Point1 list
    member Stretch : l:double -> Point1
    member Warp : f:(double -> double) -> Point1
    member Angle : double
    member Radius : double
```

Examinons comment faire cela F# type s’affiche pour un programmeur à l’aide d’un autre langage .NET. Par exemple, approximatif c# « signature » est la suivante :

```csharp
// C# signature for the unadjusted Point1 class
public class Point1
{
    public Point1();

    public Point1(double angle, double radius);

    public static Microsoft.FSharp.Collections.List<Point1> Circle(int count);

    public Point1 Stretch(double factor);

    public Point1 Warp(Microsoft.FSharp.Core.FastFunc<double,double> transform);

    public double Angle { get; }

    public double Radius { get; }
}
```

Il existe quelques points importants à noter sur la façon F# représente construit ici. Exemple :

* Métadonnées telles que les noms d’arguments a été conservée.

* F#les méthodes qui acceptent deux arguments deviennent C# les méthodes qui acceptent deux arguments.

* Fonctions et les listes deviennent des références à des types correspondants dans le F# bibliothèque.

Le code suivant montre comment ajuster ce code pour tenir compte de ces éléments.

```fsharp
namespace SuperDuperFSharpLibrary.Types

type RadialPoint(angle:double, radius:double) =

    /// Return a point at the origin
    new() = RadialPoint(angle=0.0, radius=0.0)

    /// The angle to the point, from the x-axis
    member x.Angle = angle

    /// The distance to the point, from the origin
    member x.Radius = radius

    /// Return a new point, with radius multiplied by the given factor
    member x.Stretch(factor) =
        RadialPoint(angle=angle, radius=radius * factor)

    /// Return a new point, with angle transformed by the function
    member x.Warp(transform:Func<_,_>) =
        RadialPoint(angle=transform.Invoke angle, radius=radius)

    /// Return a sequence of points describing an approximate circle using
    /// the given count of points
    static member Circle(count) =
        seq { for i in 1..count ->
                RadialPoint(angle=2.0*Math.PI/float(count), radius=1.0) }
```

Le déduit F# est de type de code comme suit :

```fsharp
type RadialPoint =
    new : unit -> RadialPoint
    new : angle:double * radius:double -> RadialPoint
    static member Circle : count:int -> seq<RadialPoint>
    member Stretch : factor:double -> RadialPoint
    member Warp : transform:System.Func<double,double> -> RadialPoint
    member Angle : double
    member Radius : double
```

La signature c# est désormais comme suit :

```csharp
public class RadialPoint
{
    public RadialPoint();

    public RadialPoint(double angle, double radius);

    public static System.Collections.Generic.IEnumerable<RadialPoint> Circle(int count);

    public RadialPoint Stretch(double factor);

    public RadialPoint Warp(System.Func<double,double> transform);

    public double Angle { get; }

    public double Radius { get; }
}
```

Les corrections apportées à préparer ce type à utiliser dans le cadre d’une bibliothèque .NET vanille sont comme suit :

* Ajusté plusieurs noms : `Point1`, `n`, `l`, et `f` est devenu `RadialPoint`, `count`, `factor`, et `transform`, respectivement.

* Utiliser un type de retour `seq<RadialPoint>` au lieu de `RadialPoint list` en modifiant une construction de la liste à l’aide `[ ... ]` à une construction de séquence à l’aide `IEnumerable<RadialPoint>`.

* Utilisé le type de délégué .NET `System.Func` au lieu d’un F# type de fonction.

Cela facilite beaucoup mieux à consommer en code c#.
