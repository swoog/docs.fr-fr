---
title: Nouveautés de C# 7.1
description: Vue d’ensemble des nouvelles fonctionnalités de C# 7.1.
ms.date: 08/16/2017
ms.openlocfilehash: 00baec45d7582d3ac12c7b0865241f5cd8159246
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="whats-new-in-c-71"></a>Nouveautés de C# 7.1

C# 7.1 est la première version mineure pour le langage C#. Elle marque une cadence de publication accrue pour le langage. Vous pouvez utiliser les nouvelles fonctionnalités plus tôt, dans l’idéal quand chaque nouvelle fonctionnalité est prête. C# 7.1 ajoute la possibilité de configurer le compilateur pour le faire correspondre à une version spécifiée du langage. Ceci vous permet de séparer la décision de mettre à niveau les outils de la décision de mettre à niveau les versions du langage.

C# 7.1 ajoute l’élément de configuration de [sélection de la version du langage](#language-version-selection), trois nouvelles fonctionnalités du langage et un nouveau comportement du compilateur.

Les nouvelles fonctionnalités de langage de cette version sont :

* [Méthode `async` `Main`](#async-main)
  - Le point d’entrée pour une application peut avoir le modificateur `async`.
* [Expressions littérales `default`](#default-literal-expressions)
  - Vous pouvez utiliser des expressions littérales default dans les expressions de valeur par défaut quand le type cible peut être inféré.
* [Noms des éléments de tuple inférés](#inferred-tuple-element-names)
  - Les noms des éléments de tuple peuvent être inférés dans de nombreux cas à partir de l’initialisation du tuple.

Enfin, le compilateur a deux options, `/refout` et `/refonly`, qui contrôlent la [génération d’assemblys de références](#reference-assembly-generation).

## <a name="language-version-selection"></a>Sélection de la version du langage

Le compilateur C# prend en charge C# 7.1 à compter de Visual Studio 2017 version 15.3 ou du SDK .NET Core 2.0. Cependant, les fonctionnalités 7.1 sont désactivées par défaut. Pour activer les fonctionnalités 7.1, vous devez modifier le paramètre de version du langage pour votre projet.

Dans Visual Studio, cliquez avec le bouton droit sur le nœud du projet dans l’Explorateur de solutions, puis sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **Version mineure la plus récente de C# (latest)** ou la version spécifique **C# 7.1**, comme illustré dans l’image suivante. La valeur `latest` signifie que vous voulez utiliser la dernière version mineure sur l’ordinateur actif. `C# 7.1` signifie que vous voulez utiliser C# 7.1, même après la publication de versions mineures plus récentes.

![Définition de la version du langage](./media/csharp-7-1/advanced-build-settings.png)

Vous pouvez aussi éditer le fichier « csproj », et ajouter ou modifier les lignes suivantes :

```xml
<PropertyGroup>
  <LangVersion>latest</LangVersion>
</PropertyGroup>
```

> [!NOTE]
> Si vous utilisez l’IDE Visual Studio pour mettre à jour vos fichiers csproj, il crée des nœuds distincts pour chaque configuration de build. Vous définissez généralement la même valeur dans toutes les configurations de build, mais vous devez la définir explicitement pour chaque configuration de build ou sélectionner « Toutes les configurations » quand vous modifiez ce paramètre. Vous voyez alors ceci dans votre fichier csproj :

```xml
<PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
  <LangVersion>latest</LangVersion>
</PropertyGroup>

<PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
  <LangVersion>latest</LangVersion>
</PropertyGroup>
```

Les valeurs valides pour l’élément `LangVersion` sont :

* `ISO-1`
* `ISO-2`
* `3`
* `4`
* `5`
* `6`
* `7`
* `7.1`
* `default`
* `latest`

Les chaînes spéciales `default` et `latest` définissent respectivement la dernière version majeure et la dernière version mineure du langage installées sur l’ordinateur de build.

Ce paramètre dissocie l’installation de nouvelles versions du SDK et des outils dans votre environnement de développement du choix d’incorporer les nouvelles fonctionnalités du langage dans un projet. Vous pouvez installer la dernière version du SDK et des outils sur votre ordinateur de build. Chaque projet peut être configuré pour utiliser une version spécifique du langage pour sa build.

## <a name="async-main"></a>Async main

Une méthode *async main* vous permet d’utiliser `await` dans votre méthode `Main`.
Auparavant, vous deviez écrire :

```csharp
static int Main()
{
    return DoAsyncWork().GetAwaiter().GetResult();
}
```

Vous pouvez désormais écrire :

```csharp
static async Task<int> Main()
{
    // This could also be replaced with the body
    // DoAsyncWork, including its await expressions:
    return await DoAsyncWork();
}
```

Si votre programme ne retourne pas de code de sortie, vous pouvez déclarer une méthode `Main` qui retourne une <xref:System.Threading.Tasks.Task> :

```csharp
static async Task Main()
{
    await SomeAsyncMethod();
}
```

Pour plus d’informations, consultez la rubrique [async main](../programming-guide/main-and-command-args/index.md) dans le Guide de programmation.

## <a name="default-literal-expressions"></a>Expressions littérales par défaut

Les expressions littérales par défaut sont une amélioration des expressions de valeur par défaut.
Ces expressions initialisent une variable à la valeur par défaut. Vous deviez écrire auparavant :

```csharp
Func<string, bool> whereClause = default(Func<string, bool>);
```

Vous pouvez désormais omettre le type du côté droit de l’initialisation :

```csharp
Func<string, bool> whereClause = default;
```

Pour plus d’informations sur cette amélioration, consultez la rubrique [Expressions de valeur par défaut](../programming-guide/statements-expressions-operators/default-value-expressions.md) dans le Guide de programmation C# .

Cette amélioration change également certaines des règles d’analyse pour le [mot clé default](../language-reference/keywords/default.md).

## <a name="inferred-tuple-element-names"></a>Noms des éléments de tuple inférés

Cette fonctionnalité est une petite amélioration de la fonctionnalité des tuples introduite dans C# 7.0. Très souvent, quand vous initialisez un tuple, les variables utilisées pour le côté droit de l’affectation sont identiques aux noms que vous souhaitez pour les éléments du tuple :

```csharp
int count = 5;
string label = "Colors used in the map";
var pair = (count: count, label: label);
```

Dans C# 7.1, les noms des éléments du tuple peuvent être inférés à partir des variables utilisées pour initialiser le tuple :

```csharp
int count = 5;
string label = "Colors used in the map";
var pair = (count, label); // element names are "count" and "label"
```

Pour plus d’informations sur cette fonctionnalité, consultez la rubrique [Tuples](../tuples.md).

## <a name="reference-assembly-generation"></a>Génération d’assemblys de références

Il existe deux nouvelles options du compilateur qui génèrent des *assemblys de références uniquement* : [/refout](../language-reference/compiler-options/refout-compiler-option.md) et [/refonly](../language-reference/compiler-options/refonly-compiler-option.md).
Les rubriques en lien expliquent ces options et les assemblys de références plus en détails.
