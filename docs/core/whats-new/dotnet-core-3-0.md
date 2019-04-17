---
title: Nouveautés de .NET Core 3.0
description: Découvrez les nouvelles fonctionnalités de .NET Core 3.0.
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/31/2018
ms.openlocfilehash: e9a69c61df574ea391622ebb709c14948c71014d
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59341723"
---
# <a name="whats-new-in-net-core-30-preview-2"></a>Nouveautés de .NET Core 3.0 (Preview 2)

Cet article décrit les nouveautés de .NET Core 3.0 (Preview 2). Une des principales améliorations est la prise en charge des applications de bureau Windows (Windows uniquement). En utilisant un composant du SDK .NET Core 3.0 appelé Windows Desktop, vous pouvez porter vos applications Windows Forms et Windows Presentation Foundation (WPF). Pour être clair, le composant Windows Desktop est pris en charge et inclus seulement sur Windows. Pour plus d'informations, consultez la section [Bureau Windows](#windows-desktop) ci-dessous.

.NET Core 3.0 prend en charge C# 8.0.

[Téléchargez et commencez à utiliser .NET Core 3.0 Preview 2](https://aka.ms/netcore3download) dès maintenant sur Windows, Mac et Linux. Vous pouvez consulter les détails complets de la version dans les [notes de publication de .NET Core 3.0 Preview 2](https://aka.ms/netcore3releasenotes).

Pour plus d’informations sur les caractéristiques de chaque version, consultez les annonces suivantes :

- [Annonce de .NET Core 3.0 Preview 1](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/)
- [Annonce de .NET Core 3.0 Preview 2](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-2/)

## <a name="c-8"></a>C# 8

.NET Core 3.0 prend en charge C# 8 et, à compter de .NET Core 3.0 Preview 2, prend en charge ces nouvelles fonctionnalités. Pour plus d’informations sur les fonctionnalités de C# 8.0, consultez les billets de blog suivants :

- [Do more with patterns in C# 8.0](https://devblogs.microsoft.com/dotnet/do-more-with-patterns-in-c-8-0/)
- [Take C# 8.0 for a spin](https://devblogs.microsoft.com/dotnet/take-c-8-0-for-a-spin/)
- [Building C# 8.0](https://devblogs.microsoft.com/dotnet/building-c-8-0/)

### <a name="ranges-and-indices"></a>Plages et index

Le nouveau type `Index` peut être utilisé pour l’indexation. Vous pouvez en créer un à partir d’un `int` qui compte à partir du début, ou avec un opérateur (C#) `^` préfixé qui compte à partir de la fin :

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

Il existe également un type `Range`, composé de deux `Index` valeurs, une pour le début et une pour la fin, et qui peut être écrit avec une expression de plage (C#) `x..y`. Vous pouvez indexer ensuite avec un `Range` afin de produire une tranche :

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

### <a name="async-streams"></a>Flux asynchrones

Le type `IAsyncEnumerable<T>` est une nouvelle version asynchrone de `IEnumerable<T>`. Le langage vous permet d’utiliser `await foreach` sur `IAsyncEnumerable<T>` pour consommer ses éléments, et `yield return` sur ceux-ci pour produire des éléments.

L’exemple suivant montre la production et la consommation de flux de données asynchrones. L’instruction `foreach` est asynchrone et utilise elle-même `yield return` afin de produire un flux asynchrone pour les appelants. Ce modèle (qui utilise `yield return`) est le modèle recommandé pour produire des flux de données asynchrones.

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

Outre la possibilité d’effectuer une opération `await foreach`, vous pouvez également créer des itérateurs asynchrones, par exemple un itérateur qui retourne un objet `IAsyncEnumerable/IAsyncEnumerator` auquel vous pouvez à la fois appliquer des opérations `await` et `yield`. Pour les objets qui doivent être supprimés, vous pouvez utiliser `IAsyncDisposable`, qui implémentent différents types BCL, notamment `Stream` et `Timer`.

> [!NOTE]
> Vous avez besoin de .NET Core 3.0 Preview 2 pour utiliser des flux asynchrones si vous voulez développer avec Visual Studio 2019 ou avec la dernière préversion de l’[extension C# pour Visual Studio Code](https://github.com/OmniSharp/omnisharp-vscode/releases/tag/v1.18.0-beta5). Si vous utilisez .NET Core 3.0 Preview 2 sur la ligne de commande, tout fonctionnera comme prévu.

### <a name="using-declarations"></a>Déclarations using

Les *déclarations using* sont une nouvelle façon de vérifier que votre objet est correctement supprimé. Une *déclaration using* maintient l’objet actif tant qu’il se trouve dans l’étendue. Une fois que l’objet se trouve en dehors de l’étendue, il est automatiquement supprimé. Ceci réduit les *instructions using* imbriquées et rend votre code plus propre.

```csharp
static void Main(string[] args)
{
    using var options = Parse(args);
    if (options["verbose"]) { WriteLine("Logging..."); }

} // options disposed here
```

### <a name="switch-expressions"></a>Expressions switch

Les *expressions switch* sont un moyen plus propre d’effectuer une *instruction switch* ; cependant, comme il s’agit d’expressions, elles retournent une valeur. Les *expressions switch* sont aussi entièrement intégrées aux critères spéciaux et utilisent le modèle d’élément ignoré, `_`, pour représenter la valeur `default`.

Vous pouvez voir la syntaxe des *expressions switch* dans l’exemple suivant :

```csharp
static string Display(object o) => o switch
{
    Point { X: 0, Y: 0 }         => "origin",
    Point { X: var x, Y: var y } => $"({x}, {y})",
    _                            => "unknown"
};
```

Deux modèles sont mis en œuvre dans cet exemple. `o` correspond d’abord au `Point` *modèle de type*, puis au *modèle de propriété* à l’intérieur des *{accolades}*. Le `_` décrit le `discard pattern`, qui est identique à `default` pour les *instructions switch*.

Les modèles vous permettent d’écrire du code déclaratif qui capture votre intention, au lieu d’un code procédural qui implémente des tests de celle-ci. Le compilateur devient responsable de l’implémentation de ce code procédural fastidieux, et il est garanti qu’il le fait toujours correctement.

Il y a toujours cas où les *instructions switch* sont un meilleur choix que des *expressions switch* ; vous pouvez utiliser des modèles avec les deux styles de syntaxe.

Pour plus d’informations, consultez [Do more with patterns in C# 8.0](https://devblogs.microsoft.com/dotnet/do-more-with-patterns-in-c-8-0/).

## <a name="ieee-floating-point-improvements"></a>Améliorations apportées à la virgule flottante IEEE

Les API de virgule flottante sont en cours de mise à jour pour devenir conformes à la [révision 754-2008 d’IEEE](https://en.wikipedia.org/wiki/IEEE_754-2008_revision). L’objectif de ces modifications est d’exposer toutes les opérations « obligatoires » et de garantir que leur comportement est conforme à la spécification IEEE.

Correctifs de l’analyse et de la mise en forme :

* Analyse et arrondi corrects des entrées, quelle que soit leur longueur.
* Analyse et mise en forme correctes des zéros négatifs.
* Analyse correcte de l’infini et des valeurs NaN en effectuant une vérification sans tenir compte de la casse et en autorisant un signe `+` facultatif de début là où c’est applicable.

Les nouvelles API mathématiques ont :

* `BitIncrement/BitDecrement`\
Correspond aux opérations IEEE `nextUp` et `nextDown`. Elles retournent le plus petit nombre à virgule flottante dont la valeur est supérieure ou inférieure à l’entrée (respectivement). Par exemple, `Math.BitIncrement(0.0)` retourne `double.Epsilon`.

* `MaxMagnitude/MinMagnitude`\
Correspond aux opérations IEEE `maxNumMag` et `minNumMag`. Elles retournent la valeur la plus grande ou la plus petite des deux entrées (respectivement). Par exemple, `Math.MaxMagnitude(2.0, -3.0)` retourne `-3.0`.

* `ILogB`\
Correspond à l’opération IEEE `logB` qui retourne une valeur intégrale ; elle retourne le logarithme de base 2 intégral du paramètre d’entrée. Ceci est identique à `floor(log2(x))`, mais effectué avec une erreur d’arrondi minimale.

* `ScaleB`\
Correspond à l’opération IEEE `scaleB` qui prend une valeur intégrale ; elle retourne `x * pow(2, n)`, mais est effectuée avec une erreur d’arrondi minimale.

* `Log2`\
Correspond à l’opération IEEE `log2` ; elle retourne le logarithme de base 2. Son erreur d’arrondi est minimale.

* `FusedMultiplyAdd`\
Correspond à l’opération IEEE `fma` ; elle effectue une multiplication-addition fusionnée. Elle effectue `(x * y) + z` comme une seule opération, avec une erreur d’arrondi minimale. Par exemple, `FusedMultiplyAdd(1e308, 2.0, -1e308)` retourne `1e308`. L’opération régulière `(1e308 * 2.0) - 1e308` retourne `double.PositiveInfinity`.

* `CopySign`\
Correspond à l’opération IEEE `copySign` ; elle retourne la valeur de `x`, mais avec le signe de `y`.

## <a name="net-platform-dependent-intrinsics"></a>Intrinsèques dépendant de la plateforme .NET

Des API ont été ajoutées, qui permettent d’accéder à certaines instructions de l’UC orientées performances, comme les ensembles **SIMD** ou les ensembles d’**instructions de manipulation de bits**. Ces instructions peuvent améliorer grandement les performances dans certains scénarios, comme le traitement efficace de données en parallèle. En plus d’exposer les API pour permettre à vos programmes de les utiliser, les bibliothèques .NET ont commencé à utiliser ces instructions pour améliorer les performances.

Les demandes de tirage CoreCLR suivantes illustrent quelques-uns des intrinsèques, via l’implémentation ou l’utilisation :

* [Implement simple SSE2 hardware intrinsics](https://github.com/dotnet/coreclr/pull/15585)
* [Implement the SSE hardware intrinsics](https://github.com/dotnet/coreclr/pull/15538)
* [Arm64 Base HW Intrinsics](https://github.com/dotnet/coreclr/pull/16822)
* [Use TZCNT and LZCNT for Locate{First|Last}Found{Byte|Char}](https://github.com/dotnet/coreclr/pull/21073)

Pour plus d’informations, consultez [.NET Platform Dependent Intrinsics](https://github.com/dotnet/designs/blob/master/accepted/platform-intrinsics.md), qui établit une approche pour la définition de cette infrastructure matérielle, permettant à Microsoft, aux fournisseurs de circuits intégrés, ou à d’autres entreprises ou personnes de définir des API de matériel/circuit intégré qui doivent être exposées au code .NET.

## <a name="default-executables"></a>Exécutables par défaut

.NET core génère désormais des [exécutables dépendant du framework](../deploying/index.md#framework-dependent-executables-fde) par défaut. Il s’agit d’une nouvelle fonctionnalité pour les applications qui utilisent une version .NET Core installée de façon globale. Jusqu’à présent, seuls les [déploiements autonomes](../deploying/index.md#self-contained-deployments-scd) produisaient un exécutable.

Lors de l’étape `dotnet build` ou `dotnet publish`, un exécutable est créé s’il correspond à l’environnement et à la plateforme du Kit de développement que vous utilisez. Vous pouvez obtenir le même résultat avec ces exécutables, comme vous le feriez avec d’autres exécutables natifs comme :

* Vous pouvez double-cliquer sur l’exécutable.
* Vous pouvez lancer l’application directement à partir d’une invite de commandes, par exemple `myapp.exe` sous Windows, et `./myapp` sous Linux et macOS.

## <a name="build-copies-dependencies"></a>Dépendances de copies de build

`dotnet build` copie maintenant les dépendances NuGet pour votre application à partir du cache NuGet vers le dossier de sortie de build. Auparavant, les dépendances étaient copiées uniquement dans le cadre de `dotnet publish`. 

Certaines opérations, par exemple la liaison et la publication d’une page de type Razor, nécessiteront toujours une publication.

## <a name="local-dotnet-tools"></a>Outils dotnet locaux

>[!WARNING]
>Il y a eu un changement dans les outils .NET Core locaux entre .NET Core 3.0 Preview 1 et .NET Core 3.0 Preview 2.  Si vous avez essayé les outils locaux dans la version Preview 1 en exécutant une commande comme `dotnet tool restore` ou `dotnet tool install`, vous devez supprimer votre dossier de cache des outils locaux pour que ces outils fonctionnent correctement dans la version Preview 2. Ce dossier se trouve à ces emplacements :
>
>Sur Mac, Linux : `rm -r $HOME/.dotnet/toolResolverCache`
>
>Sur Windows : `rmdir /s %USERPROFILE%\.dotnet\toolResolverCache`
>
>Si vous ne supprimez pas ce dossier, vous recevez une erreur.

Alors que .NET Core 2.1 prenant en charge des outils globaux, .NET Core 3.0 dispose maintenant d’outils locaux. Les outils locaux sont similaires aux outils globales mais ils sont associés à un emplacement particulier sur le disque. Cela permet une utilisation par projet et par référentiel. Un outil installé localement n’est pas disponible de façon globale. Les outils sont distribués sous forme de packages NuGet.

Les outils locaux s’appuient sur un nom de fichier manifeste `dotnet-tools.json` dans votre répertoire actuel. Ce fichier manifeste définit les outils qui doivent être disponibles dans ce dossier et sous-celui-ci. En créant ce fichier manifeste à la racine de votre référentiel, vous garantissez que toute personne qui clone votre code pourra restaurer et utiliser les outils nécessaires pour fonctionner correctement avec votre code.

Pour créer un fichier manifeste `dotnet-tools.json`, utilisez :

```console
dotnet new tool-manifest
```

Ajoutez un nouvel outil au manifeste local avec :

```console
dotnet tool install <packageId>
```

Vous pouvez également lister les outils dans le manifeste local avec :

```console
dotnet tool list
```

Pour voir quels outils sont installés globalement, utilisez :

```console
dotnet tool list -g
```

Quand le fichier manifeste des outils locaux est disponible, mais que les outils définis dans le manifeste n’ont pas été installés, utilisez la commande suivante pour télécharger et installer automatiquement ces outils :

```console
dotnet tool restore
```

Exécutez l’outil local avec la commande suivante :

```console
dotnet tool run <tool-command-name>
```

Quand un outil local est exécuté, dotnet recherche un manifeste dans la structure du répertoire actuel. Si le fichier manifeste d’un outil est trouvé, la commande recherche l’outil demandé. Si l’outil est trouvé dans le manifeste mais pas dans le cache, l’utilisateur reçoit une erreur et doit exécuter `dotnet tool restore`.

Pour supprimer un outil du fichier manifeste des outils locaux, exécutez la commande suivante :

```console
dotnet tool uninstall <packageId>
```

Le fichier manifeste de l’outil est conçu pour permettre des modifications manuelles et ainsi mettre à jour la version requise pour une utilisation avec le référentiel. Voici un exemple de fichier `dotnet-tools.json` :

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

Pour les outils locaux et globaux, une version compatible du runtime est requise. De nombreux outils actuellement sur NuGet.org ciblent le runtime .NET Core 2.1. Pour installer ces outils de façon locale ou globale, vous devez toujours installer le [runtime NET Core 2.1](https://dotnet.microsoft.com/download/dotnet-core/2.1).

## <a name="windows-desktop"></a>Bureau Windows

À compter de .NET Core 3.0 Préversion 1, vous pouvez créer des applications de bureau Windows à l’aide des outils WPF et Windows Forms. Ces infrastructures prennent également en charge l’utilisation de contrôles modernes et le style Fluent à partir de la bibliothèque XAML de l’interface utilisateur Windows (WinUI) via des [îles XAML](/windows/uwp/xaml-platform/xaml-host-controls).

Le composant Bureau Windows fait partie du SDK .NET Core 3.0 Windows.

Vous pouvez créer une nouvelle application WPF ou Windows Forms à l’aide des commandes `dotnet` suivantes :

```console
dotnet new wpf
dotnet new winforms
```

Visual Studio 2019 ajoute des modèles **Nouveau projet** pour Windows Forms et WPF .NET Core 3.0. Les concepteurs ne sont pas encore pris en charge. Vous pouvez ouvrir, lancer et déboguer ces projets dans Visual Studio 2019.

Visual Studio 2017 15.9 ajoute la possibilité d’[activer les préversions de .NET Core](https://devblogs.microsoft.com/dotnet/net-core-tooling-update-for-visual-studio-2017-version-15-9/), mais vous devez activer cette fonctionnalité, et il ne s’agit pas d’un scénario pris en charge.

Les nouveaux projets sont identiques aux projets .NET Core existants, avec quelques ajouts. Voici une comparaison entre le projet de console .NET Core de base et un projet Windows Forms et WPF de base.

Dans un projet de console .NET Core, le projet utilise le SDK `Microsoft.NET.Sdk` et déclare une dépendance sur .NET Core 3.0 via l’infrastructure cible `netcoreapp3.0`. Pour créer une application Bureau Windows, utilisez le SDK `Microsoft.NET.Sdk.WindowsDesktop` et choisissez l’infrastructure d’interface utilisateur à utiliser :

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

Pour choisir Windows Forms plutôt que WPF, définissez `UseWindowsForms` au lieu de `UseWPF` :

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

`UseWPF` et `UseWindowsForms` peuvent être définies sur `true` si l’application utilise les deux infrastructures, par exemple lorsqu’une boîte de dialogue Windows Forms héberge un contrôle WPF.

Partagez vos commentaires sur les référentiels [dotnet/winforms](https://github.com/dotnet/winforms/issues), [dotnet/wpf](https://github.com/dotnet/wpf/issues) et [dotnet/core](https://github.com/dotnet/core/issues).

## <a name="msix-deployment-for-windows-desktop"></a>Déploiement MSIX pour Windows Desktop

[MSIX](https://docs.microsoft.com/windows/msix/) est un nouveau format de package d’application Windows. Il peut être utilisé pour déployer des applications de poste de travail .NET Core 3.0 pour Windows 10.

Le [projet de package d’application Windows](https://docs.microsoft.com/windows/uwp/porting/desktop-to-uwp-packaging-dot-net), disponible dans Visual Studio 2019, vous permet de créer des packages MSIX avec des applications .NET Core [autonomes](../deploying/index.md#self-contained-deployments-scd).

>Remarque : Le fichier projet .NET Core doit spécifier les runtimes pris en charge dans la propriété `<RuntimeIdentifiers>` :
```xml
<RuntimeIdentifiers>win-x86;win-x64</RuntimeIdentifiers>
```

## <a name="fast-built-in-json-support"></a>Prise en charge JSON intégrée rapide

L’écosystème .NET s’est appuyé sur [**Json.NET**](https://www.newtonsoft.com/json) et d’autres bibliothèques JSON populaires, qui restent de bons choix. **Json.NET** utilise des chaînes .NET comme type de données de base, au format UTF-16.

La nouvelle prise en charge JSON intégrée offre des hautes performances et une allocation faible, et elle est basée sur `Span<byte>`. Trois nouveaux types principaux liés à JSON ont été ajoutés à l’espace de noms `System.Text.Json` de .NET Core 3.0.

### <a name="utf8jsonreader"></a>Utf8JsonReader

`System.Text.Json.Utf8JsonReader` est un lecteur hautes performances et à faible allocation de type forward-only pour le texte JSON codé au format UTF-8 et lu à partir de `ReadOnlySpan<byte>`. `Utf8JsonReader` est un type fondamental de bas niveau, permettant de générer des analyseurs et des désérialiseurs personnalisés. La lecture d’une charge utile JSON à l’aide du nouveau `Utf8JsonReader` est 2 fois plus rapide qu’avec le lecteur proposé par **Json.NET**. Ce lecteur n’alloue aucune ressource tant que vous n’avez pas besoin d’actualiser des jetons JSON sous forme de chaînes (UTF-16).

Cette nouvelle API inclura les composants suivants :

* Préversion 1 : lecteur JSON (accès séquentiel)
* Prochainement : enregistreur JSON, DOM (accès aléatoire), sérialiseur poco, désérialiseur poco

Voici la boucle de lecteur de base pour le `Utf8JsonReader`, utilisable comme point de départ :

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

### <a name="utf8jsonwriter"></a>Utf8JsonWriter

`System.Text.Json.Utf8JsonWriter` fournit un moyen d’écrire du texte JSON encodé en UTF-8 partir de types .NET courants, comme `String`, `Int32`, et `DateTime`, avec de hautes performances, sans mise en cache et vers l’avant uniquement. Comme le lecteur, l’enregistreur (writer) est un type fondamental de bas niveau, permettant de générer des sérialiseurs personnalisés. L’écriture d’une charge utile JSON avec le nouveau `Utf8JsonWriter` est de 30 à 80 % plus rapide qu’avec l’enregistreur (writer) de **Json.NET** et il n’effectue pas d’allocation.

Voici un exemple d’utilisation de `Utf8JsonWriter`, qui peut être utilisé comme point de départ :

```csharp
static int WriteJson(IBufferWriter<byte> output, long[] extraData)
{
    var json = new Utf8JsonWriter(output, state: default);

    json.WriteStartObject();

    json.WriteNumber("age", 15, escape: false);
    json.WriteString("date", DateTime.Now);
    json.WriteString("first", "John");
    json.WriteString("last", "Smith");

    json.WriteStartArray("phoneNumbers", escape: false);
    json.WriteStringValue("425-000-1212", escape: false);
    json.WriteStringValue("425-000-1213");
    json.WriteEndArray();

    json.WriteStartObject("address");
    json.WriteString("street", "1 Microsoft Way");
    json.WriteString("city", "Redmond");
    json.WriteNumber("zip", 98052);
    json.WriteEndObject();

    json.WriteStartArray("ExtraArray");
    for (var i = 0; i < extraData.Length; i++)
    {
        json.WriteNumberValue(extraData[i]);
    }
    json.WriteEndArray();

    json.WriteEndObject();

    json.Flush(isFinalBlock: true);

    return (int)json.BytesWritten;
}
```

Le `Utf8JsonWriter` accepte `IBufferWriter<byte>` comme emplacement de sortie pour y écrire de façon synchrone les données JSON, et en tant qu’appelant, vous devez fournir une implémentation concrète. Actuellement, la plateforme n’inclut pas d’implémentation de cette interface. Pour obtenir un exemple de `IBufferWriter<byte>`, consultez [https://gist.github.com/ahsonkhan/c76a1cc4dc7107537c3fdc0079a68b35](https://gist.github.com/ahsonkhan/c76a1cc4dc7107537c3fdc0079a68b35)

### <a name="jsondocument"></a>JsonDocument

`System.Text.Json.JsonDocument` est basé sur le `Utf8JsonReader`. Le `JsonDocument` fournit la possibilité d’analyser les données JSON et de générer un modèle DOM (Document Object Model) qui peut être interrogé, et prendre en charge l’accès aléatoire et l’énumération. Les éléments JSON qui composent les données sont accessibles via le type `JsonElement` qui est exposé par le `JsonDocument` comme propriété appelée `RootElement`. Le `JsonElement` contient le tableau et les énumérateurs d’objets JSON, ainsi que des API pour convertir le texte JSON en types .NET courants. L’analyse d’une charge utile JSON classique et l’accès à tous ses membres avec le `JsonDocument` est de 2 à 3 fois plus rapide que **Json.NET**, avec très peu d’allocations pour les données de dimension raisonnable (par exemple < 1 Mo).

Voici un exemple d’utilisation de `JsonDocument` et de `JsonElement`, qui peut être utilisé comme point de départ :

```csharp
static double ParseJson()
{
    const string json = " [ { \"name\": \"John\" }, [ \"425-000-1212\", 15 ], { \"grades\": [ 90, 80, 100, 75 ] } ]";

    double average = -1;

    using (JsonDocument doc = JsonDocument.Parse(json))
    {
        JsonElement root = doc.RootElement;
        JsonElement info = root[1];

        string phoneNumber = info[0].GetString();
        int age = info[1].GetInt32();

        JsonElement grades = root[2].GetProperty("grades");

        double sum = 0;
        foreach (JsonElement grade in grades.EnumerateArray())
        {
            sum += grade.GetInt32();
        }

        int numberOfCourses = grades.GetArrayLength();
        average = sum / numberOfCourses;
    }

    return average;
}
```

## <a name="assembly-unloadability"></a>Non-chargeabilité d’assembly

La non-chargeabilité d’assembly est une nouveauté de `AssemblyLoadContext`. Cette nouvelle fonctionnalité est largement transparente du point de vue d’une API, exposée avec seulement quelques nouvelles API. Elle permet à un contexte de chargeur d’être déchargé, libérant toute la mémoire pour les types instanciés, pour les champs statiques et pour l’assembly lui-même. Une application doit être en mesure de charger et de décharger définitivement des assemblys via ce mécanisme sans subir de fuite de mémoire.

Cette nouvelle fonctionnalité peut être utilisée pour les scénarios similaires à ceux-ci :

* Scénarios avec des plug-ins, où le chargement et le déchargement de plug-in dynamique est nécessaire. 
* Compilation dynamique, exécution puis vidage du code. Pratique pour les sites web, les moteurs de script, etc.
* Le chargement des assemblys pour introspection (comme ReflectionOnlyLoad), bien que [MetadataLoadContext](#type-metadataloadcontext) (publiée dans la version Preview 1) soit un meilleur choix dans de nombreux cas.

Pour plus d’informations, consultez [Using Unloadability](https://github.com/dotnet/coreclr/pull/22221).

Le déchargement d’assembly nécessite des précautions considérables pour garantir que toutes les références à des objets gérés d’en dehors d’un contexte de chargeur sont comprises et gérées. Quand la demande de déchargement du contexte de chargeur est faite, toutes les références qui se trouvent en dehors doivent être déréférencées, afin que le contexte de chargeur soit en cohérence seulement avec lui-même.

La non-chargeabilité d’assembly a été fournie dans le .NET Framework par les domaines d’application (AppDomains), qui ne sont pas pris en charge avec .NET Core. Les domaines d’application avaient des avantages et des limitations par rapport à ce nouveau modèle. Considérez ce nouveau modèle de chargeur comme étant plus flexible et plus performant que les domaines d’application.

## <a name="windows-native-interop"></a>Interopérabilité native Windows

Windows offre une API native riche, sous la forme d’API C plates, de COM et de WinRT. À compter de .NET Core 1.0, **P/Invoke** est pris en charge. Désormais, avec .NET Core 3.0, la prise en charge de la capacité de **cocréer des API COM** et d’**activer des API WinRT** a été ajouté.

Vous pouvez voir un exemple d’utilisation de COM avec le [code de source de la démonstration Excel](https://github.com/dotnet/samples/tree/master/core/extensions/ExcelDemo).

## <a name="type-sequencereader"></a>Type : SequenceReader

Dans .NET Core 3.0, `System.Buffers.SequenceReader` a été ajouté et peut servir de lecteur pour `ReadOnlySequence<T>`. Cela permet une analyse facile, hautes performances et à faible allocation des données `System.IO.Pipelines`, capable de couvrir plusieurs mémoires tampon de stockage. 

L’exemple suivant segmente une entrée `Sequence` en plusieurs lignes délimitées `CR/LF` valides :

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a>Type : MetadataLoadContext

Le type `MetadataLoadContext` a été ajouté et permet la lecture des métadonnées de l'assembly sans affecter le domaine d’application de l’appelant. Les assemblys sont lus comme des données, y compris ceux générés pour des architectures et plateformes différentes de l’environnement d’exécution actuel. `MetadataLoadContext` se superpose à <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, qui est uniquement disponible dans .NET Framework.

`MetdataLoadContext` est disponible dans le [package System.Reflection.MetadataLoadContext](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext). Il s’agit d’un package .NET Standard 2.0.

`MetadataLoadContext` expose les API semblables au type <xref:System.Runtime.Loader.AssemblyLoadContext>, mais il n’est pas basé sur ce type. Tout comme <xref:System.Runtime.Loader.AssemblyLoadContext>, `MetadataLoadContext` permet le chargement d’assemblys dans un univers de chargement d’assemblys isolé. `MetdataLoadContext` Les API retournent des objets <xref:System.Reflection.Assembly>, permettant l’utilisation des API de réflexion courantes. Les API orientées exécution, par exemple [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), ne sont pas autorisées et renverront une exception InvalidOperationException.

L’exemple suivant montre comment rechercher des types concrets dans un assembly qui implémente une interface donnée :

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

Les scénarios pour `MetadataLoadContext` incluent des fonctionnalités et des outils au moment de la conception, ainsi que des fonctionnalités de runtime qui doivent inspecter un ensemble d’assemblys en tant que données et dont l’intégralité des verrous appliqués aux fichiers et à la mémoire doivent être supprimés une l’inspection terminée.

`MetadataLoadContext` contient une classe de résolution passée à son constructeur. La tâche du programme de résolution consiste à charger un `Assembly` en fonction de son `AssemblyName`. La classe de résolution est dérivée de la classe abstraite `MetadataAssemblyResolver`. Une implémentation du programme de résolution pour des scénarios basés sur le chemin d’accès est fournie avec `PathAssemblyResolver`.

Les [tests MetadataLoadContext](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) illustrent de nombreux cas d’usage. Les [tests Assembly](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) constituent un bon point de départ.

## <a name="tls-13--openssl-111-on-linux"></a>TLS 1.3 et OpenSSL 1.1.1 sous Linux

.NET Core tire désormais parti de la [prise en charge de TLS 1.3 dans OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), si disponible dans un environnement donné. Selon l’[équipe OpenSSL](https://www.openssl.org/blog/blog/2018/09/11/release111/), TLS 1.3 présentent plusieurs avantages :

* Délais de connexion améliorés grâce à une réduction du nombre d’allers-retours requis entre le client et le serveur.

* Sécurité améliorée grâce à la suppression de différents algorithmes de chiffrement obsolètes et non sécurisés et à un chiffrement plus complet de la négociation de connexion.

.NET Core 3.0 Préversion 1 est capable d’utiliser **OpenSSL 1.1.1**, **OpenSSL 1.1.0** ou **OpenSSL 1.0.2** (soit la meilleure version trouvée, sur un système Linux).  Si **OpenSSL 1.1.1** est disponible, les types SslStream et HttpClient utiliseront **TLS 1.3** avec `SslProtocols.None` (protocoles système par défaut), en supposant que le client et le serveur prennent en charge **TLS 1.3**.

L’exemple suivant montre comment .NET Core 3.0 Préversion 1 sous Ubuntu 18.10 se connecte à <https://www.cloudflare.com> :

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
>Windows et macOS ne prennent pas encore en charge **TLS 1.3**. .NET Core 3.0 prendra en charge **TLS 1.3** sur ces systèmes d’exploitation dès que de la prise en charge sera disponible.

## <a name="cryptography"></a>Chiffrement

La prise en charge a été ajoutée pour les chiffrements **AES-GCM** et **AES-CCM**, avec une implémentation via `System.Security.Cryptography.AesGcm` et `System.Security.Cryptography.AesCcm`. Ces algorithmes sont de type [Authenticated Encryption with Association Data (AEAD)](https://en.wikipedia.org/wiki/Authenticated_encryption), et les premiers algorithmes Authenticated Encryption (AE) ont été ajoutés à .NET Core.

Le code suivant montre l’utilisation du chiffrement **AesGcm** pour chiffrer et déchiffrer des données aléatoires.

Le code pour **AesCcm** sera presque identique (seuls les noms des variables de classe seraient différents).

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a>Importation/exportation d’une clé de chiffrement

.NET Core 3.0 Préversion 1 prend en charge l’importation et l’exportation de clés publiques et privées asymétriques aux formats standard, sans avoir à utiliser un certificat X.509.

Tous les types de clés (RSA, DSA, ECDsa, ECDiffieHellman) prennent en charge le format **X.509 SubjectPublicKeyInfo** pour les clés publiques, et les formats **PKCS #8 PrivateKeyInfo** et **PKCS #8 EncryptedPrivateKeyInfo** pour les clés privées. Le chiffrement RSA prend également en charge **PKCS #1 RSAPublicKey** et **PKCS #1 RSAPrivateKey**. Les méthodes d’exportation produisent toutes des données binaires encodées au format DER, tout comme les méthodes d’importation. Si une clé est stockée au format PEM compatible avec le texte, l’appelant devra décoder le contenu au format base64 avant d’appeler une méthode d’importation.

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

Les fichiers PKCS #8 peuvent être inspectés avec la classe `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo`.

Les fichiers PFX/PKCS#12 peuvent être inspectés et manipulés avec `System.Security.Cryptography.Pkcs.Pkcs12Info` et `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectivement.

## <a name="serialport-for-linux"></a>SerialPort pour Linux

.NET Core 3.0 prend désormais en charge <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> sous Linux.

Auparavant, .NET Core était uniquement pris en charge grâce au type `SerialPort` sous Windows.

## <a name="more-bcl-improvements"></a>Plusieurs améliorations BCL

Les types `Span<T>`, `Memory<T>` et autres types associés qui avaient été introduits dans .NET Core 2.1 ont été optimisées dans .NET Core 3.0. Les opérations courantes comme la construction de type span, le découpage, l’analyse et la mise en forme sont maintenant plus performantes. 

En outre, les types comme `String` ont bénéficié d’améliorations en arrière-plan pour les rendre plus efficaces lorsqu’ils sont utilisés comme des clés avec `Dictionary<TKey, TValue>` et d’autres collections. Aucune modification de code n’est nécessaire pour tirer parti de ces améliorations.

Les améliorations suivantes sont également des nouveautés dans .NET Core 3 Préversion 1 :

* Prise en charge de Brotli intégrée à HttpClient
* ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)
* Unsafe.Unbox
* CancellationToken.Unregister
* Opérateurs arithmétiques complexes
* API de socket pour TCP keep alive
* StringBuilder.GetChunks
* Analyse IPEndPoint
* RandomNumberGenerator.GetInt32

## <a name="tiered-compilation"></a>Compilation hiérarchisée

La [compilation hiérarchisée](https://devblogs.microsoft.com/dotnet/tiered-compilation-preview-in-net-core-2-1/) est activée par défaut avec .NET Core 3.0. Cette fonctionnalité permet au runtime d’utiliser de manière plus adaptative le compilateur juste-à-temps (Just-In-Time ou JIT) pour obtenir de meilleures performances, à la fois au démarrage et pour optimiser le débit.

Cette fonctionnalité avait été ajoutée en option dans [.NET Core 2.1](https://devblogs.microsoft.com/dotnet/announcing-net-core-2-1/) et était activée par défaut dans [.NET Core 2.2 Préversion 2](https://devblogs.microsoft.com/dotnet/announcing-net-core-2-2-preview-2/). Elle est ensuite redevenue une option dans la version .NET Core 2.2.

## <a name="arm64-linux-support"></a>Support ARM64 Linux

La prise en charge d’ARM64 pour Linux a été ajoutée. Actuellement, ARM64 est principallement utilisé dans des scénarios IoT.

Des [images Docker Alpine, Debian et Ubuntu sont disponibles avec .NET Core pour ARM64](https://hub.docker.com/r/microsoft/dotnet/).

Consultez [État de .NET Core ARM64](https://github.com/dotnet/announcements/issues/82) pour plus d’informations.

>[!NOTE]
> La prise en charge d’**ARM64** sous Windows n’est pas encore disponible.

## <a name="install-net-core-30-previews-on-linux-with-snap"></a>Installer des préversions de .NET Core 3.0 sur Linux avec Snap

Snap est le meilleur moyen d’installer et d’essayer les préversions de .NET Core sur les [distributions Linux qui prennent en charge Snap](https://docs.snapcraft.io/installing-snapd/6735).

Après avoir configuré Snap sur votre système, exécutez la commande suivante pour installer le [SDK de .NET Core SDK 3.0 Preview](https://snapcraft.io/dotnet-sdk).

```console
sudo snap install dotnet-sdk --beta --classic
```
 
Quand .NET Core est installé en utilisant le package Snap, la commande .NET Core par défaut est `dotnet-sdk.dotnet`, et non pas simplement `dotnet`. L’avantage de la commande avec l’espace de noms est qu’elle ne sera pas en conflit avec une éventuelle version de .NET Core installée globalement. Vous pouvez créer l’alias `dotnet` pour cette commande avec :

```console
sudo snap alias dotnet-sdk.dotnet dotnet
```

Certaines distributions nécessitent une étape supplémentaire pour permettre l’accès au certificat SSL. Pour plus d’informations, consultez notre [configuration de Linux](https://github.com/dotnet/core/blob/master/Documentation/linux-setup.md).

## <a name="gpio-support-for-raspberry-pi"></a>Prise en charge de GPIO pour Raspberry Pi

Deux nouveaux packages ont été publiés sur NuGet, que vous pouvez utiliser pour la programmation de GPIO.

* [System.Device.Gpio](https://www.nuget.org/packages/System.Device.Gpio/0.1.0-prerelease.19078.2)
* [Iot.Device.Bindings](https://www.nuget.org/packages/Iot.Device.Bindings/0.1.0-prerelease.19078.2)

Les packages GPIO incluent des API pour les appareils GPIO, SPI, I2C et PWM. Le package de liaisons IoT inclut [des liaisons d’appareil](https://github.com/dotnet/iot/blob/master/src/devices/README.md) pour différents circuits intégrés et capteurs, les mêmes que ceux qui sont disponibles dans [dotnet/iot - src/devices](https://github.com/dotnet/iot/tree/master/src/devices).

Les API de port série mis à jour qui ont été annoncés dans le cadre de .NET Core 3.0 Preview 1 ne font pas partie de ces packages, mais elles sont disponibles dans le cadre de la plateforme .NET Core.

## <a name="platform-support"></a>Prise en charge de plateforme

.NET Core 3 sera pris en charge sur les systèmes d’exploitation suivants :

* Client Windows : 7, 8.1, 10 (1607+)
* Windows Server : 2012 R2 SP1+
* macOS : 10.12+
* RHEL : 6+
* Fedora : 26+
* Ubuntu : 16.04+
* Debian : 9+
* SLES : 12+
* openSUSE : 42.3+
* Alpine : 3.8+

La prise en charge des circuits intégrés suit :

* x64 sur Windows, macOS et Linux
* x86 sur Windows
* ARM32 sur Windows et Linux
* ARM64 sur Linux

Pour Linux, ARM32 est pris en charge sur Debian 9+ et Ubuntu 16.04+. Pour ARM64, la prise en charge est identique à ARM32, avec en plus Alpine 3.8. Il s’agit des mêmes versions de ces distributions que ce qui est pris en charge pour X64.

Les images Docker pour .NET Core 3.0 sont disponibles dans [microsoft/dotnet sur Docker Hub](https://hub.docker.com/r/microsoft/dotnet/). Microsoft travaille actuellement à l’adoption du [Registre de conteneurs Microsoft (MCR, Microsoft Container Registry)](https://cloudblogs.microsoft.com/opensource/2019/01/17/improved-discovery-experience-microsoft-containers-docker-hub/) et il est prévu que les images .NET Core 3.0 finales soient publiées seulement sur MCR.
