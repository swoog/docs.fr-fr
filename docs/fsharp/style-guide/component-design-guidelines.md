---
title: 'Règles de conception du composant F #'
description: 'Découvrez les instructions pour l’écriture de composants F # destinés à la consommation par les autres appelants.'
ms.date: 05/14/2018
ms.openlocfilehash: 7e71710b1bc2fe3e8d7a5a091513a1432650dc04
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="f-component-design-guidelines"></a>Règles de conception du composant F #

Ce document est un ensemble de règles de conception de composant pour F # de programmation, selon les F # composant règles de conception, v14, Microsoft Research, et [une autre version](https://fsharp.org/specs/component-design-guidelines/) à l’origine organisé et géré par le Software Foundation F #.

Ce document suppose que vous êtes familiarisé avec la programmation F #. Un grand merci de la Communauté pour obtenir des commentaires utiles sur les différentes versions de ce guide et leurs contributions F #.

## <a name="overview"></a>Vue d'ensemble

Ce document présente certains des problèmes liés à la conception du composant F # et de codage. Un composant peut signifier que les éléments suivants :

* Une couche dans votre projet F # qui a des consommateurs externes dans ce projet.
* Une bibliothèque destinée à la consommation par le code F # sur les limites de l’assembly.
* Une bibliothèque destinée à la consommation par n’importe quel langage .NET sur les limites de l’assembly.
* Une bibliothèque prévue pour la distribution via un référentiel de packages, tels que [NuGet](https://nuget.org).

Suivent des techniques décrites dans cet article la [cinq principes du bon code F #](index.md#five-principles-of-good-f-code)et donc utiliser des fonctionnalités et de l’objet de programmation comme il convient.

Quelle que soit la méthode, le Concepteur de composant et de la bibliothèque fait face à un nombre de problèmes prosaïques et pratiques lorsque vous tentez de créer une API qui n’est plus facilement utilisable par les développeurs. Application consciencieux de la [la conception de bibliothèque .NET](../../standard/design-guidelines/index.md) sera vous diriger vers la création d’un ensemble cohérent d’API est agréable à consommer.

## <a name="general-guidelines"></a>Indications générales

Il existe quelques instructions universelles qui s’appliquent aux bibliothèques F #, quel que soit le public concerné par la bibliothèque.

### <a name="learn-the-net-library-design-guidelines"></a>Découvrez les règles de conception de bibliothèque .NET

Quel que soit le type de F # vous effectuez de codage, il est utile de disposer d’une connaissance de la [la conception de bibliothèque .NET](../../standard/design-guidelines/index.md). La plupart des autres F # et aux programmeurs .NET seront connaissance de ces instructions et attendre le code .NET pour se conformer à leur.

Les règles de conception de bibliothèque .NET fournissent des recommandations générales concernant d’affectation de noms, la conception des classes et interfaces, conception de membres (propriétés, méthodes, événements, etc.) et bien plus encore et sont utile premier point de référence pour une variété de guide de conception.

### <a name="add-xml-documentation-comments-to-your-code"></a>Ajouter des commentaires de documentation XML à votre code

Documentation XML sur les API publiques vous assurer que les utilisateurs peuvent obtenir excellent Intellisense et info Express à l’aide de ces types et membres et activer construction documentation fichiers pour la bibliothèque. Consultez le [Documentation XML](../language-reference/xml-documentation.md) sur différentes balises xml qui peuvent être utilisés pour le balisage supplémentaire dans les commentaires de xmldoc.

```fsharp
/// A class for representing (x,y) coordinates
type Point =

    /// Computes the distance between this point and another
    member DistanceTo : otherPoint:Point -> float
```

Vous pouvez utiliser des commentaires XML forme abrégée (`/// comment`), ou les commentaires XML standard (`///<summary>comment</summary>`).

### <a name="consider-using-explicit-signature-files-fsi-for-stable-library-and-component-apis"></a>Envisagez d’utiliser des fichiers de signature explicite (.fsi) pour la bibliothèque stable et API de composant

À l’aide des fichiers de signature explicite dans une bibliothèque F # fournit un résumé succinct des API publique, qui permet de se pour assurer que vous connaissez la surface publique complète de la bibliothèque, ainsi que fournit une séparation nette entre la documentation public et internes détails d’implémentation. Notez que les fichiers de signature ajoutent friction à l’évolution de l’API publique, en exigeant que les modifications à apporter dans les fichiers de l’implémentation et la signature. Par conséquent, les fichiers de signature en général uniquement convient lorsqu’une API a deviennent consolidée et est censée ne sont plus changer de manière significative.

### <a name="always-follow-best-practices-for-using-strings-in-net"></a>Suivez toujours les meilleures pratiques pour l’utilisation de chaînes dans .NET

Suivez [meilleures pratiques pour l’utilisation de chaînes dans .NET](../../standard/base-types/best-practices-strings.md) des conseils. En particulier, l’état toujours explicitement *intention culturelle* dans la conversion et la comparaison de chaînes (le cas échéant).

## <a name="guidelines-for-f-facing-libraries"></a>Instructions pour F #-faisant face à des bibliothèques

Cette section présente des recommandations pour le développement publique F #-faisant face à des bibliothèques. Autrement dit, les bibliothèques exposer des API publiques qui sont destinés à être consommés par les développeurs de F #. Il existe une variété de recommandations sur la conception de la bibliothèque s’applique spécifiquement à F #. En l’absence de recommandations spécifiques qui suivent, les règles de conception de bibliothèque .NET sont les conseils de secours.

### <a name="naming-conventions"></a>Conventions d'attribution d'un nom

#### <a name="use-net-naming-and-capitalization-conventions"></a>Utilisez les conventions d’affectation de noms et de mise en majuscules de .NET

Le tableau suivant suit les conventions d’affectation de noms et de mise en majuscules de .NET. Il existe des petites ajouts d’inclure également les constructions F #.

| Construction | Case | Élément | Exemples | Notes |
|-----------|------|------|----------|-------|
| Types concrets | PascalCase | Nom / adjectivale | La liste, Double, complexe | Types concrets sont des structs, des classes, des énumérations, des délégués, des enregistrements et des unions. Bien que les noms de types sont généralement en minuscules dans OCaml, F # a arrêté le schéma d’affectation de noms .NET pour les types.
| DLL           | PascalCase |                 | Fabrikam.Core.dll |  |
| Balises d’union     | PascalCase | nom | Certains, ajouter, réussite | N’utilisez pas de préfixe dans les API publiques. Éventuellement utiliser un préfixe lorsque internes, tels que ''' les équipes de type = TAlpha | TBeta | TDelta. » » |
| événement          | PascalCase | Verbe | ValueChanged / ValueChanging |  |
| Exceptions     | PascalCase |      | WebException | Nom doit se terminer par « Exception ». |
| Champ          | PascalCase | nom | CurrentName  | |
| Types interface |  PascalCase | Nom / adjectivale | IDisposable | Nom doit commencer par « I ». |
| Méthode |  PascalCase |  Verbe | ToString | |
| Espace de noms | PascalCase | | Microsoft.FSharp.Core | En général utiliser `<Organization>.<Technology>[.<Subnamespace>]`, bien que de supprimer l’organisation si la technologie est indépendante de l’organisation. |
| Paramètres | camelCase | nom |  typeName, transformation, d’une plage | |
| permettent de valeurs (internes) | camelCase ou PascalCase | Nom / verbe |  getValue, myTable |
| permettent de valeurs (externe) | camelCase ou PascalCase | Nom/verbe  | List.Map, Dates.Today | les valeurs liées à Let sont souvent publiques lorsqu’ils suivent les modèles de design fonctionnels traditionnel. Toutefois, en général utiliser PascalCase lorsque l’identificateur peut être utilisé à partir d’autres langages .NET. |
| Propriété  | PascalCase  | Nom / adjectivale  | IsEndOfFile, couleur d’arrière-plan  | Propriétés booléennes en général utiliser est et peut et doit être positive, comme dans IsEndOfFile, IsNotEndOfFile pas.

#### <a name="avoid-abbreviations"></a>Éviter les abréviations

Les instructions de .NET déconseillons l’utilisation des abréviations (par exemple, « utiliser `OnButtonClick` plutôt que `OnBtnClick`»). Les abréviations courantes, telles que `Async` pour « Asynchrone », sont tolérés. Cette règle est parfois ignorée pour la programmation fonctionnelle ; par exemple, `List.iter` utilise une abréviation pour « parcourir ». Pour cette raison, à l’aide des abréviations a tendance à être tolérée à un niveau plus élevé en F #-à-programmation F #, mais doit toujours généralement être évitée dans la conception du composant public.

#### <a name="avoid-casing-name-collisions"></a>Éviter les collisions de noms de la casse

Les instructions de .NET dire que casse seul ne peut pas être utilisée pour lever l’ambiguïté des collisions de noms, étant donné que certains langages de client (par exemple, Visual Basic) respectent la casse.

#### <a name="use-acronyms-where-appropriate"></a>Utiliser des acronymes approprié

Les acronymes telles que XML ne sont pas des abréviations et sont couramment utilisés dans les bibliothèques .NET dans le formulaire en minuscule (Xml). Uniquement les acronymes connues, largement reconnues doivent être utilisés.

#### <a name="use-pascalcase-for-generic-parameter-names"></a>Utilisez PascalCase pour les noms de paramètre générique

Utilisez PascalCase pour les noms de paramètre générique dans les API publiques, y compris pour F #-faisant face à des bibliothèques. En particulier, utilisez des noms tels que `T`, `U`, `T1`, `T2` pour les paramètres génériques arbitraires, et lorsque des noms spécifiques ont un sens, puis pour F #-bibliothèques exposés à utilisent des noms tels que `Key`, `Value`, `Arg`(mais pas par exemple, `TKey`).

#### <a name="use-either-pascalcase-or-camelcase-for-public-functions-and-values-in-f-modules"></a>Utilisez PascalCase ou camelCase pour les fonctions publiques et les valeurs dans les modules F #

camelCase est utilisé pour les fonctions publiques qui sont conçues pour être utilisées non qualifié (par exemple, `invalidArg`) et pour les fonctions de collection standard « » (par exemple, List.map). Dans ces deux cas, les noms de fonctions fonctionnant un peu comme mots clés du langage.

### <a name="object-type-and-module-design"></a>Création d’objet, le Type et le Module

#### <a name="use-namespaces-or-modules-to-contain-your-types-and-modules"></a>Utiliser des espaces de noms ou des modules pour contenir vos types et des modules

Chaque fichier F # dans un composant doit commencer par une déclaration d’espace de noms ou une déclaration de module.

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
* Espaces de noms ne peut pas contenir de fonctions F #, sauf si elles sont dans un module interne
* Le code de n’importe quel module donné doit être contenu dans un seul fichier
* Modules de niveau supérieur peuvent contenir des fonctions F # sans recourir à un module interne

Le choix entre un espace de noms de niveau supérieur ou un module a une incidence sur la forme compilée du code et donc affectera la vue à partir d’autres langages .NET doit votre API être consommée en dehors du code F #.

#### <a name="use-methods-and-properties-for-operations-intrinsic-to-object-types"></a>Utilisez les méthodes et propriétés pour les opérations intrinsèques aux types d’objet

Lorsque vous travaillez avec des objets, il est préférable pour vous assurer que les fonctionnalités consommable sont implémentée en tant que les méthodes et propriétés de ce type.

```fsharp
type HardwareDevice() =

    member this.ID = ...

    member this.SupportedProtocols = ...

type HashTable<'Key,'Value>(comparer: IEqualityComparer<'Key>) =

    member this.Add(key, value) = ...

    member this.ContainsKey(key) = ...

    member this.ContainsValue(value) = ...
```

Le bloc de fonctionnalité pour un membre donné ne doive pas nécessairement être implémenté dans ce membre, mais la partie consommable de cette fonctionnalité doit être.

#### <a name="use-classes-to-encapsulate-mutable-state"></a>Utiliser les classes pour encapsuler un état mutable

En F #, cela ne doit être effectué où qu’état n’est pas déjà encapsulé par une autre construction de langage, tel qu’une fermeture, une expression de séquence ou un calcul asynchrone.

```fsharp
type Counter() =
    // let-bound values are private in classes.
    let mutable count = 0

    member this.Next() =
        count <- count + 1
        count
```

#### <a name="use-interfaces-to-group-related-operations"></a>Utiliser des interfaces pour regrouper les opérations connexes

Utiliser les types d’interfaces pour représenter un ensemble d’opérations. Cela est préférable aux autres options, telles que des tuples de fonctions ou les enregistrements de fonctions.

```fsharp
type Serializer =
    abstract Serialize<'T> : preserveRefEq: bool -> value: 'T -> string
    abstract Deserialize<'T> : preserveRefEq: bool -> pickle: string -> 'T
```

De préférence à :

```fsharp
type Serializer<'T> = {
    Serialize : bool -> 'T -> string
    Deserialize : bool -> string -> 'T
}
```

Les interfaces sont des concepts de première classe dans .NET, ce qui vous permet d’obtenir les Foncteurs normalement vous donnera. En outre, ils peuvent être utilisés pour encoder des types existentiels dans votre programme, les enregistrements de fonctions ne peuvent pas.

#### <a name="use-a-module-to-group-functions-which-act-on-collections"></a>Utiliser un module à des fonctions de groupe qui agissent sur des collections

Lorsque vous définissez un type de collection, envisagez de fournir un ensemble standard d’opérations telles que `CollectionType.map` et `CollectionType.iter`) pour les nouveaux types de collection.

```fsharp
module CollectionType =
    let map f c =
        ...
    let iter f c =
        ...
```

Si vous incluez un tel module, suivez les conventions d’affectation de noms standards pour les fonctions FSharp.Core.

#### <a name="use-a-module-to-group-functions-for-common-canonical-functions-especially-in-math-and-dsl-libraries"></a>Utiliser un module à des fonctions de groupe pour les fonctions canoniques communes, en particulier dans les mathématiques et des bibliothèques DSL

Par exemple, `Microsoft.FSharp.Core.Operators` est une collection automatiquement ouverte de fonctions de niveau supérieur (comme `abs` et `sin`) fournies par FSharp.Core.dll.

De même, une bibliothèque de statistiques peut inclure un module avec des fonctions `erf` et `erfc`, où ce module est conçu pour être ouvert explicitement ou automatiquement.

#### <a name="consider-using-requirequalifiedaccess-and-carefully-apply-autoopen-attributes"></a>Envisagez d’utiliser RequireQualifiedAccess et soigneusement appliquer les attributs AutoOpen

Ajout de la `[<RequireQualifiedAccess>]` attribut à un module indique que le module ne peut-être pas être ouvertes et des références aux éléments du module doivent explicite qualifié accès. Par exemple, le `Microsoft.FSharp.Collections.List` module a cet attribut.

Cela est utile lorsque les valeurs dans le module et les fonctions ont des noms qui sont susceptibles d’entrer en conflit avec les noms dans d’autres modules. Nécessitant un accès complet peut considérablement améliorer la facilité de maintenance à long terme et evolvability d’une bibliothèque.

Ajout de la `[<AutoOpen>]` attribut à un module signifie que le module s’ouvre quand l’espace de noms qui le contient est ouvert. Le `[<AutoOpen>]` attribut peut également être appliqué à un assembly pour indiquer un module qui s’ouvre automatiquement lorsque l’assembly est référencé.

Par exemple, une bibliothèque de statistiques **MathsHeaven.Statistics** peut contenir un `module MathsHeaven.Statistics.Operators` contenant des fonctions `erf` et `erfc`. Il est raisonnable de marquer ce module en tant que `[<AutoOpen>]`. Cela signifie que `open MathsHeaven.Statistics` également ouvrir ce module et mettre les noms `erf` et `erfc` dans l’étendue. Utiliser un autre bon `[<AutoOpen>]` est pour les modules contenant des méthodes d’extension.

Une surutilisation de `[<AutoOpen>]` aboutissent à des espaces de noms pollués et de l’attribut doit être utilisée avec précaution. Pour les bibliothèques spécifiques dans des domaines spécifiques, utiliser judicieusement des `[<AutoOpen>]` peut entraîner une meilleure facilité d’utilisation.

#### <a name="consider-defining-operator-members-on-classes-where-using-well-known-operators-is-appropriate"></a>Envisagez de définir des membres de l’opérateur sur les classes, où il est nécessaire de l’utilisation d’opérateurs bien connus

Parfois, les classes sont utilisées pour modéliser des constructions mathématiques telles que les vecteurs. Quand le domaine en cours de modélisation possède des opérateurs bien connus, il est utile de les définir en tant que membres intrinsèques à la classe.

```fsharp
type Vector(x:float) =

    member v.X = x

    static member (*) (vector:Vector, scalar:float) = Vector(vector.X * scalar)

    static member (+) (vector1:Vector, vector2:Vector) = Vector(vector1.X + vector2.X)

let v = Vector(5.0)

let u = v * 10.0
```

Ce guide correspond à des indications générales pour ces types .NET. Toutefois, il peut être plus important dans F # car cela permet à ces types à utiliser dans la liaison avec les fonctions F # et les méthodes avec des contraintes de membres, tels que List.sumBy de codage.

#### <a name="consider-using-compiledname-to-provide-a-net-friendly-name-for-other-net-language-consumers"></a>Envisagez d’utiliser CompiledName pour fournir une. Nom convivial NET pour les autres consommateurs de langage .NET

Vous pouvez parfois souhaiter donnez un nom d’un style pour les consommateurs) (F # (tel qu’un membre statique en minuscules afin qu’il apparaisse comme s’il s’agissait d’une fonction liée au module), mais ont un style différent pour le nom lorsqu’il est compilé dans un assembly. Vous pouvez utiliser la `[<CompiledName>]` attribut pour fournir un style différent pour le code non F # consommation de l’assembly.

```fsharp
type Vector(x:float, y:float) =

    member v.X = x
    member v.Y = y

    [<CompiledName("Create")>]
    static member create x y = Vector (x, y)

let v = Vector.create 5.0 3.0
```

À l’aide de `[<CompiledName>]`, vous pouvez utiliser les conventions d’affectation de noms .NET pour les consommateurs non F # de l’assembly.

#### <a name="use-method-overloading-for-member-functions-if-doing-so-provides-a-simpler-api"></a>Utilisez la surcharge de méthode pour les fonctions de membre, si cela fournit une API simple

La surcharge de méthode est un outil puissant permettant de simplifier une API qui devra peut-être effectuer des fonctionnalités similaires, mais avec différentes options ou les arguments.

```fsharp
type Logger() =

    member this.Log(message) =
        ...
    member this.Log(message, retryPolicy) =
        ...
```

En F #, il est plus courant de surcharge sur le nombre d’arguments plutôt que des types d’arguments.

#### <a name="hide-the-representations-of-record-and-union-types-if-the-design-of-these-types-is-likely-to-evolve"></a>Masquer les représentations sous forme d’enregistrement et les types union si la conception de ces types est susceptible d’évoluer

Éviter de révéler des représentations concrètes des objets. Par exemple, la représentation concrète de <xref:System.DateTime> valeurs n’est pas révélé par l’API publique externe de la conception de la bibliothèque .NET. Au moment de l’exécution, le Common Language Runtime sait l’implémentation validée qui sera utilisée dans l’ensemble de l’exécution. Toutefois, code compilé ne lui-même récupérer de dépendances sur la représentation concrète.

#### <a name="avoid-the-use-of-implementation-inheritance-for-extensibility"></a>Évitez d’utiliser l’héritage d’implémentation pour l’extensibilité

En F #, l’héritage d’implémentation est rarement utilisée. En outre, les hiérarchies d’héritage sont souvent complexe et difficile à modifier lors de l’arrivent de nouvelles exigences. Implémentation de l’héritage existe toujours dans F # pour les rares cas où il est la meilleure solution à un problème, mais les autres techniques doivent être recherchées dans vos programmes F # lors de la conception pour le polymorphisme, telles que l’implémentation d’interface et de compatibilité.

### <a name="function-and-member-signatures"></a>Signatures de fonction et de membre

#### <a name="use-tuples-for-return-values-when-returning-a-small-number-of-multiple-unrelated-values"></a>Utiliser des tuples pour les valeurs retournées lors du retour d’un petit nombre de plusieurs valeurs non liées

Voici un bon exemple d’utilisation d’un tuple dans un type de retour :

```fsharp
val divrem : BigInteger -> BigInteger -> BigInteger * BigInteger
```

Pour retourner les types contenant de nombreux composants ou où les composants sont associés à une seule entité identifiable, envisagez d’utiliser un type nommé à la place d’un tuple.

#### <a name="use-asynct-for-async-programming-at-f-api-boundaries"></a>Utilisez `Async<T>` pour la programmation asynchrone au niveau des limites d’API F #

S’il existe une opération synchrone correspondante nommée `Operation` qui retourne un `T`, l’opération asynchrone doit être nommé `AsyncOperation` si elle retourne `Async<T>` ou `OperationAsync` si elle retourne `Task<T>`. Pour les types .NET couramment utilisés qui exposent des méthodes Begin/End, envisagez d’utiliser `Async.FromBeginEnd` pour écrire des méthodes d’extension comme une façade pour fournir le F # async modèle de programmation à l’API .NET.

```fsharp
type SomeType =
    member this.Compute(x:int) : int =
        ...
    member this.AsyncCompute(x:int) : Async<int> =
        ...

type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        ...
```

### <a name="exceptions"></a>Exceptions

Les exceptions sont exceptionnelles dans .NET ; Autrement dit, ils ne doivent pas se produire fréquemment lors de l’exécution. Dans ce cas, les informations qu’ils contiennent sont précieuses. Les exceptions sont un cœur de première classe concept de .NET ; informatique donc approprié à l’application des Exceptions qui suit doit être utilisé dans le cadre de la conception de l’interface d’un composant.

#### <a name="follow-the-net-guidelines-for-exceptions"></a>Suivez les instructions de .NET pour les exceptions

Le [la conception de bibliothèque .NET](../../standard/design-guidelines/exceptions.md) conseils excellente sur l’utilisation d’exceptions dans le contexte de toute programmation .NET. Certaines de ces indications sont les suivantes :

* N’utilisez pas d’exceptions pour le flux de contrôle normal. Bien que cette technique est souvent utilisée dans des langages tels que OCaml, il est susceptible d’engendrer des bogues et peut être inefficace sur .NET. Au lieu de cela, envisagez de retourner un `None` valeur pour indiquer un échec qui est une occurrence courantes ou attendue de l’option.

* Documentez les exceptions levées par vos composants lorsqu’une fonction est utilisée de manière incorrecte.

* Si possible, utiliser des exceptions existantes des espaces de noms système. Éviter <xref:System.ApplicationException>, même si.

* Ne levez pas <xref:System.Exception> lorsqu’il échappe au code utilisateur. Cela inclut les éviter l’utilisation de `failwith`, `failwithf`, qui sont des fonctions très pratiques pour une utilisation dans les scripts et le code en cours de développement, mais doit être supprimé à partir de code de la bibliothèque F # en faveur de la levée d’un type d’exception plus spécifique.

* Utilisez `nullArg`, `invalidArg`, et `invalidOp` comme mécanisme de lever <xref:System.ArgumentNullException>, <xref:System.ArgumentException>, et <xref:System.InvalidOperationException> quand cela est approprié.

#### <a name="consider-using-option-values-for-return-types-when-failure-is-not-an-exceptional-scenario"></a>Envisagez d’utiliser des valeurs d’option pour les types de retournés lors de l’échec n’est pas un scénario exceptionnel

L’approche de .NET pour les exceptions est qu’ils doivent être « exceptionnelles » ; Autrement dit, ils doivent peu fréquentes. Toutefois, certaines opérations (par exemple, rechercher une table) peuvent échouer fréquemment. Les valeurs d’option F # sont un excellent moyen de représenter les types de retour de ces opérations. Ces opérations sont traditionnellement démarrer avec le préfixe de nom « try » :

```fsharp
// bad: throws exception if no element meets criteria
member this.FindFirstIndex(pred : 'T -> bool) : int =
    ...

// bad: returns -1 if no element meets criteria
member this.FindFirstIndex(pred : 'T -> bool) : int =
    ...

// good: returns None if no element meets criteria
member this.TryFindFirstIndex(pred : 'T -> bool) : int option =
    ...
```

### <a name="extension-members"></a>Membres d’extension

#### <a name="carefully-apply-f-extension-members-in-f-to-f-components"></a>Appliquer attentivement les membres d’extension F # en F #-à-composants F #

Membres d’extension F # doivent uniquement être utilisées pour les opérations qui se trouvent dans la clôture des intrinsèques opérations associées à un type dans la plupart de ses modes d’utilisation. Une utilisation courante consiste à fournir des API qui est plus IDIOMATIQUE à F # pour différents types .NET :

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

#### <a name="use-discriminated-unions-instead-of-class-hierarchies-for-tree-structured-data"></a>Utilisez les unions discriminées au lieu de hiérarchies de classes pour l’arborescence de la structure de données

Structures d’arborescence sont définies de manière récursive. Il s’agit maladroite avec héritage mais élégante avec les Unions discriminées.

```fsharp
type BST<'T> =
    | Empty
    | Node of 'T * BST<'T> * BST<'T>
```

Représentant les données sous forme d’arborescence avec les Unions discriminées vous permet également de bénéficier d’exhaustivité dans les critères spéciaux.

#### <a name="use-requirequalifiedaccess-on-union-types-whose-case-names-are-not-sufficiently-unique"></a>Utilisez `[<RequireQualifiedAccess>]` sur les types d’union dont les noms cas ne sont pas suffisamment uniques

Vous pouvez trouver vous-même dans un domaine où le même nom est le meilleur nom pour différents éléments, tels que des cas discriminée Union. Vous pouvez utiliser `[<RequireQualifiedAccess>]` pour lever l’ambiguïté des noms d’incidents pour éviter de déclencher des erreurs à confusion en raison d’une occultation dépendantes de l’ordre de `open` instructions

#### <a name="hide-the-representations-of-discriminated-unions-for-binary-compatible-apis-if-the-design-of-these-types-is-likely-to-evolve"></a>Masquer les représentations sous forme d’unions discriminées pour les API compatible binaire si la conception de ces types est susceptible d’évoluer

Types d’unions s’appuient sur F # correspondance formulaires pour un modèle de programmation concis. Comme mentionné précédemment, vous devez éviter de révéler les représentations sous forme de données concrètes si la conception de ces types est susceptible d’évoluer.

Par exemple, la représentation sous forme d’une union discriminée peut être masquée à l’aide d’une déclaration privée ou interne, ou à l’aide d’un fichier de signature.

```fsharp
type Union =
    private
    | CaseA of int
    | CaseB of string
```

Si vous révéler les unions discriminées sans discrimination, il peut s’avérer difficiles à la version de votre bibliothèque sans rupture du code de l’utilisateur. Envisagez plutôt de révéler un ou plusieurs modèles actifs pour permettre la mise en correspondance sur les valeurs de ce type.

Modèles actifs fournissent une autre façon de fournir aux consommateurs) (F # en correspondance tout en évitant d’exposer directement les Types d’Union F #.

### <a name="inline-functions-and-member-constraints"></a>Les fonctions inline et les contraintes de membre

#### <a name="define-generic-numeric-algorithms-using-inline-functions-with-implied-member-constraints-and-statically-resolved-generic-types"></a>Définir les algorithmes génériques de numériques à l’aide des fonctions inline avec les contraintes de membre implicite et les types génériques résolus statiquement

Membre arithmétique contraintes et F # comparaison sont une norme pour la programmation F #. Considérons par exemple le code suivant :

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

Il est possible de simuler « volante en tapant » à l’aide des contraintes de membre) (F #. Toutefois, les membres qui rendent utiliser de ce pas en général de données doit être utilisé en F #-à-conceptions de bibliothèque F #. Il s’agit, car les conceptions de bibliothèque selon les contraintes implicites inconnus ou non standard ont tendance à provoquer le code utilisateur deviennent fixes et liée au modèle d’une infrastructure particulière.

En outre, il est probable que les délais de compilation très longue peut entraîner une utilisation intensive de contraintes de membre de cette manière.

### <a name="operator-definitions"></a>Définitions d’opérateur

#### <a name="avoid-defining-custom-symbolic-operators"></a>Évitez de définir des opérateurs symboliques personnalisés

Opérateurs personnalisés sont essentiels dans certaines situations et appareils de notation très utiles au sein d’un grand nombre de code d’implémentation. Pour les nouveaux utilisateurs d’une bibliothèque, les fonctions nommées sont souvent plus faciles à utiliser. En outre, opérateurs symboliques personnalisés peuvent être difficiles de document et les utilisateurs s’avérer plus difficile de rechercher de l’aide sur les opérateurs, en raison des limitations existantes dans les moteurs de l’IDE et de recherche.

Par conséquent, il est préférable de publier vos fonctionnalités en tant que fonctions nommées et les membres et plus exposer les opérateurs pour cette fonctionnalité que si les notation avantages l’emportent sur la documentation et les coûts cognitifs les.

### <a name="units-of-measure"></a>Unités de mesure

#### <a name="carefully-use-units-of-measure-for-added-type-safety-in-f-code"></a>Avec soin les unités de mesure pour la sécurité de l’ajout d’un type dans le code F #

Information de type supplémentaire pour les unités de mesure est effacée lorsqu’ils sont affichés par d’autres langages .NET. N’oubliez pas que réflexion, des outils et composants .NET seront affiche sans unités de types. Par exemple, C# consommateurs verront `float` plutôt que `float<kg>`.

### <a name="type-abbreviations"></a>Abréviations de types

#### <a name="carefully-use-type-abbreviations-to-simplify-f-code"></a>Utiliser avec soin les abréviations de type pour simplifier le code F #

Réflexion, des outils et composants .NET ne verront pas les noms abrégés pour les types. Utilisation intensive des abréviations de type peut également afficher un domaine plus complexe qu’il est en fait, ce qui peut induire en erreur les consommateurs.

#### <a name="avoid-type-abbreviations-for-public-types-whose-members-and-properties-should-be-intrinsically-different-to-those-available-on-the-type-being-abbreviated"></a>Éviter les abréviations de type pour les types publics dont les membres et les propriétés doivent être intrinsèquement différentes de celles qui sont disponibles sur le type abrégé

Dans ce cas, le type abrégé révèle trop sur la représentation sous forme de type réel qui est défini. Au lieu de cela, envisagez d’encapsuler l’abréviation dans un type de classe ou d’une union discriminée seul cas (ou, lorsque les performances sont essentielles, envisagez d’utiliser un type struct pour encapsuler l’abréviation).

Par exemple, il est tentant de définir un mappage multi comme un cas spécial d’une F # interactive, par exemple :

```fsharp
type MultiMap<'Key,'Value> = Map<'Key,'Value list>
```

Toutefois, les opérations logiques-notation par points sur ce type ne sont pas le même que les opérations sur une carte : par exemple, il est raisonnable que l’opérateur de recherche sont mappés. [clé] Retourne la liste vide si la clé n’est pas dans le dictionnaire, au lieu de lever une exception.

## <a name="guidelines-for-libraries-for-use-from-other-net-languages"></a>Recommandations pour les bibliothèques à utiliser à partir d’autres langages .NET

Lorsque vous concevez des bibliothèques pour une utilisation à partir d’autres langages .NET, il est important de respecter le [la conception de bibliothèque .NET](../../standard/design-guidelines/index.md). Dans ce document, ces bibliothèques sont étiquetés vanille bibliothèques .NET, par opposition à F #-faisant face à des bibliothèques qui utilisent F # construit sans restriction. Conception des bibliothèques .NET vanille signifie fournissant des API familière et idiomatiques cohérents avec le reste du .NET Framework en réduisant l’utilisation de F #-des constructions spécifiques dans l’API publique. Les règles sont expliquées dans les sections suivantes.

### <a name="namespace-and-type-design-for-libraries-for-use-from-other-net-languages"></a>Conception Namespace et Type (pour les bibliothèques à utiliser à partir d’autres langages .NET)

#### <a name="apply-the-net-naming-conventions-to-the-public-api-of-your-components"></a>Appliquer les conventions d’affectation de noms .NET à l’API publique de vos composants

Faites particulièrement attention à l’utilisation de noms abrégés et les instructions de mise en majuscules de .NET.

```fsharp
type pCoord = ...
    member this.theta = ...

type PolarCoordinate = ...
    member this.Theta = ...
```

#### <a name="use-namespaces-types-and-members-as-the-primary-organizational-structure-for-your-components"></a>Utilisez des espaces de noms, types et membres en tant que la structure organisationnelle principale pour vos composants

Tous les fichiers contenant les fonctionnalités publiques doivent commencer par un `namespace` déclaration, les seules entités publics dans les espaces de noms doivent être des types. N’utilisez pas de modules F #.

Utilisez les modules non publics pour contenir le code d’implémentation, les types d’utilitaire et les fonctions d’utilitaire.

Les types static doivent être préférés sur les modules, car elles permettent une évolution ultérieure de l’API à utiliser la surcharge et d’autres concepts de conception de l’API .NET qui ne peuvent pas être utilisées dans des modules F #.

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

#### <a name="use-f-record-types-in-vanilla-net-apis-if-the-design-of-the-types-wont-evolve"></a>Utiliser des types d’enregistrement F # dans vanille API .NET si la conception de types ne sont pas évoluer.

Types d’enregistrement F # compilées en une classe .NET simple. Ils ne conviennent pas pour certains types simples, stables dans les API. Vous devez envisager d’utiliser le `[<NoEquality>]` et `[<NoComparison>]` attributs à supprimer la génération automatique des interfaces. Évitez également à l’aide des champs d’enregistrement mutable dans vanille API .NET en tant que ces expose un champ public. Envisagez toujours si une classe fournirait une option plus souple pour l’évolution ultérieure de l’API.

Par exemple, le code F # suivant expose l’API publique à un consommateur c# :

F #:

```fsharp
[<NoEquality; NoComparison>]
type MyRecord =
    { FirstThing : int
        SecondThing : string }
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

#### <a name="hide-the-representation-of-f-union-types-in-vanilla-net-apis"></a>Masquer la représentation sous forme de types union F # dans vanille API .NET

Types d’union F # ne sont pas utilisés au-delà des limites de composant, même dans F #-à-F # de codage. Il s’agit d’un appareil de l’implémentation d’un excellent lorsqu’il est utilisé en interne au sein des composants et des bibliothèques.

Lorsque vous concevez une API .NET vanille, envisagez de le masquer la représentation sous forme d’un type union à l’aide d’une déclaration privée ou un fichier de signature.

```fsharp
type PropLogic =
    private
    | And of PropLogic * PropLogic
    | Not of PropLogic
    | True
```

Vous pouvez également augmenter les types qui utilisent une représentation sous forme d’union en interne avec les membres pour fournir un souhaitée. NET avec accès via l’API.

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

#### <a name="design-gui-and-other-components-using-the-design-patterns-of-the-framework"></a>Conception de l’interface graphique utilisateur et d’autres composants à l’aide de l’infrastructure, les modèles de conception

Plusieurs infrastructures de différents sont disponibles dans .NET, tels que Windows Forms, WPF et ASP.NET. Conventions d’affectation de noms et de conception pour chaque doivent être utilisées si vous concevez des composants pour une utilisation dans ces infrastructures. Par exemple, pour la programmation WPF, adopter les modèles de conception WPF pour les classes que vous créez. Pour les modèles de programmation de l’interface utilisateur, utilisez les modèles de conception tels que des événements et les collections basées sur les notifications, tels que ceux trouvent dans <xref:System.Collections.ObjectModel>.

### <a name="object-and-member-design-for-libraries-for-use-from-other-net-languages"></a>Conception de membre et d’objet (pour les bibliothèques à utiliser à partir d’autres langages .NET)

#### <a name="use-the-clievent-attribute-to-expose-net-events"></a>Utilisez l’attribut CLIEvent pour exposer des événements .NET

Construire un `DelegateEvent` avec .NET spécifique le type qui prend un objet de délégué et `EventArgs` (plutôt qu’une `Event`, qui utilise uniquement la `FSharpHandler` type par défaut) afin que les événements sont publiées dans la façon familier à d’autres langages .NET.

```fsharp
type MyBadType() =
    let myEv = new Event<int>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish

type MyEventArgs(x:int) =
    inherit System.EventArgs()
    member this.X = x

    /// A type in a component designed for use from other .NET languages
type MyGoodType() =
    let myEv = new DelegateEvent<EventHandler<MyEventArgs>>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish
```

#### <a name="expose-asynchronous-operations-as-methods-which-return-net-tasks"></a>Exposer des opérations asynchrones en tant que méthodes qui retournent des tâches de .NET

Tâches permettent de représenter les calculs asynchrones dans .NET. Les tâches sont en général moins composition que F # `Async<T>` car ils représentent les tâches « exécute déjà » et ne peut pas être un ensemble composés de façon qui effectuer une composition parallèle, ou qui masquer la propagation des signaux d’annulation et d’autres objets paramètres contextuelles.

Toutefois, en dépit de cela, les méthodes qui retournent des tâches sont la représentation standard de la programmation asynchrone sur .NET.

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =

    let compute (x: int) : Async<int> = async { ... }

    member this.ComputeAsync(x) = compute x |> Async.StartAsTask
```

Vous allez souvent que vous souhaitez également accepter un jeton d’annulation explicite :

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =
    let compute(x:int) : Async<int> = async { ... }
    member this.ComputeAsTask(x, cancellationToken) = Async.StartAsTask(compute x, cancellationToken)
```

#### <a name="use-net-delegate-types-instead-of-f-function-types"></a>Utiliser des types de délégués de .NET au lieu de types de fonction) (F #

Ici « types de fonction) (F # » signifie que les types « direction » comme `int -> int`.

Au lieu de cela :

```fsharp
member this.Transform(f:int->int) =
    ...
```

Procédez comme suit :

```fsharp
member this.Transform(f:Func<int,int>) =
    ...
```

Le type de fonction F # apparaît sous la forme `class FSharpFunc<T,U>` à d’autres langages .NET et est moins adapté pour les fonctionnalités de langage et les outils qui comprennent les types délégués. Lors de la création d’une méthode d’ordre supérieur ciblant .NET Framework 3.5 ou version ultérieure, le `System.Func` et `System.Action` les délégués sont les API de droite à publier pour permettre aux développeurs de .NET utiliser ces API selon des problèmes. (Lorsque vous ciblez .NET Framework 2.0, les types définis par le système de délégués sont plus limitées, envisagez d’utiliser des types de délégué prédéfinis, tels que `System.Converter<T,U>` ou de la définition d’un type délégué spécifique.)

Sur l’autre côté, les délégués .NET ne sont pas naturelles pour F #-faisant face à des bibliothèques (consultez la Section suivante sur F #-faisant face à des bibliothèques). Par conséquent, une stratégie de mise en œuvre courants lors du développement des méthodes d’ordre supérieur pour les bibliothèques .NET vanille va créer toutes l’implémentation à l’aide des types de fonction) (F # et puis créer l’API publique de l’utilisation de délégués comme façade dynamique au-dessus réel F # mise en œuvre.

#### <a name="use-the-trygetvalue-pattern-instead-of-returning-f-option-values-and-prefer-method-overloading-to-taking-f-option-values-as-arguments"></a>Utilisez le modèle TryGetValue au lieu de retourner des valeurs d’option F #, préférez la surcharge de méthode à effectuer des valeurs d’option F # en tant qu’arguments

Modèles courants d’utilisation pour le type d’option F # dans les API sont mieux implémenté dans vanille techniques de création des API .NET à l’aide de .NET standard. Au lieu de retourner une valeur d’option F #, envisagez d’utiliser le type de retour bool plus un paramètre de sortie comme dans le modèle « TryGetValue ». Et plutôt qu’à partir des valeurs d’option F # en tant que paramètres, envisagez d’utiliser la surcharge de méthode ou les arguments facultatifs.

```fsharp
member this.ReturnOption() = Some 3

member this.ReturnBoolAndOut(outVal : byref<int>) =
    outVal <- 3
    true

member this.ParamOption(x : int, y : int option) =
    match y with
    | Some y2 -> x + y2
    | None -> x

member this.ParamOverload(x : int) = x

member this.ParamOverload(x : int, y : int) = x + y
```

#### <a name="use-the-net-collection-interface-types-ienumerablet-and-idictionarykeyvalue-for-parameters-and-return-values"></a>Utilisez l’interface de collection .NET types IEnumerable\<T\> et IDictionary\<de clé, la valeur\> pour les paramètres et valeurs de retour

Évitez d’utiliser des types de collection concrets tels que les tableaux de .NET `T[]`, types F # `list<T>`, `Map<Key,Value>` et `Set<T>`, et les types de collection concrète .NET tels que `Dictionary<Key,Value>`. Les règles de conception de bibliothèque .NET ont bon conseil savoir à quel moment utiliser différents types de collection comme `IEnumerable<T>`. Une utilisation de tableaux (`T[]`) est acceptable dans certains cas, pour des raisons de performances. Notez en particulier que `seq<T>` est simplement le F # alias pour `IEnumerable<T>`, et seq est donc souvent un type approprié pour une API .NET vanille.

À la place de F # répertorie :

```fsharp
member this.PrintNames(names : string list) =
    ...
```

Utiliser des séquences de F # :

```fsharp
member this.PrintNames(names : seq<string>) =
    ...
```

#### <a name="use-the-unit-type-as-the-only-input-type-of-a-method-to-define-a-zero-argument-method-or-as-the-only-return-type-to-define-a-void-returning-method"></a>Le type d’unité en tant que le seul type d’entrée d’une méthode pour définir une méthode sans argument, ou en tant que le seul type pour définir une méthode retournant void

Évitez d’autres utilisations du type d’unité. Voici une bonne :

```fsharp
✔ member this.NoArguments() = 3

✔ member this.ReturnVoid(x : int) = ()
```

Cela est incorrect :

```fsharp
member this.WrongUnit( x:unit, z:int) = ((), ())
```

#### <a name="check-for-null-values-on-vanilla-net-api-boundaries"></a>Vérifier les valeurs null sur les limites de l’API .NET vanille

Code d’implémentation F # a tendance à avoir moins de valeurs null, en raison de restrictions sur l’utilisation de littéraux null pour des types F # et les modèles de conception immuable. Autres langages .NET utilisent souvent null en tant que valeur beaucoup plus fréquemment. Pour cette raison, code F # qui expose une API .NET vanille doit vérifier les paramètres pour la valeur null à la limite de l’API et empêche que ces valeurs transférée plus approfondie dans le code d’implémentation F #. Le `isNull` fonction ou critères spéciaux sur les `null` modèle peut être utilisé.

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

Au lieu de cela, préférez retournant un type nommé contenant les données d’agrégation, ou à l’aide des paramètres de sortie pour retourner plusieurs valeurs. Bien que les tuples et les tuples du struct existent dans .NET (y compris c# prise en charge linguistique pour les tuples du struct), ils vont souvent pas fournir l’API idéale et attendu pour les développeurs .NET.

#### <a name="avoid-the-use-of-currying-of-parameters"></a>Évitez d’utiliser curryfication de paramètres

Au lieu de cela, utilisez les conventions d’appel de .NET ``Method(arg1,arg2,…,argN)``.

```fsharp
member this.TupledArguments(str, num) = String.replicate num str
```

Conseil : Si vous concevez des bibliothèques pour une utilisation à partir de n’importe quel langage .NET, puis il est ne remplace en fait certains expérimentale Visual c# et Visual Basic de programmation pour vous assurer que vos bibliothèques « convivialité droite » à partir de ces langues. Vous pouvez également utiliser des outils tels que .NET Reflector et l’Explorateur d’objets Visual Studio pour vous assurer que les bibliothèques et leur documentation apparaissent comme prévu pour les développeurs.

## <a name="appendix"></a>Annexe

### <a name="end-to-end-example-of-designing-f-code-for-use-by-other-net-languages"></a>Exemple de bout en bout de la conception de code F # pour une utilisation par d’autres langages .NET

Considérons la classe suivante :

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

Le type déduit F # de cette classe est la suivante :

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

Jetons un œil à la façon dont ce type) (F # s’affiche pour un programmeur à l’aide d’un autre langage .NET. Par exemple, approximatif c# « signature » est la suivante :

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

Il existe quelques points importants à noter sur comment F # représente les constructions ici. Par exemple :

* Métadonnées telles que les noms d’arguments a été conservée.

* Les méthodes F # qui prennent deux arguments sont les méthodes c# qui prennent deux arguments.

* Fonctions et des listes deviennent des références à des types correspondants dans la bibliothèque F #.

Le code suivant montre comment ajuster le code pour tenir compte de ces éléments.

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

Le type) (F # déduit du code est la suivante :

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

Les corrections apportées pour préparer ce type à utiliser comme partie d’une bibliothèque .NET vanille sont les suivantes :

* Ajustée plusieurs noms : `Point1`, `n`, `l`, et `f` est devenu `RadialPoint`, `count`, `factor`, et `transform`, respectivement.

* Utiliser un type de retour de `seq<RadialPoint>` au lieu de `RadialPoint list` en modifiant une construction de la liste à l’aide `[ ... ]` une à l’aide de la construction de séquence `IEnumerable<RadialPoint>`.

* Utiliser le type de délégué .NET `System.Func` au lieu d’un type de fonction F #.

Il est ainsi beaucoup mieux à utiliser dans le code c#.
