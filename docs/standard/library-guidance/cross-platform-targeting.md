---
title: Ciblage d’inter-plateformes
description: Meilleures pratiques recommandées pour la création des bibliothèques inter-plateformes .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 72fa891d5b1054af485a98d89b4efb11d6b0018b
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374885"
---
# <a name="cross-platform-targeting"></a>Ciblage d’inter-plateformes

.NET modernes prend en charge plusieurs systèmes d’exploitation et les appareils. Il est important pour les bibliothèques .NET open source prendre en charge les développeurs autant que possible, que leur développiez un site Web ASP.NET hébergé dans Azure, ou une partie de .NET dans Unity.

## <a name="net-standard"></a>.NET Standard

.NET standard est la meilleure façon d’ajouter la prise en charge multiplateforme dans une bibliothèque .NET. [.NET standard](../net-standard.md) est une spécification d’API .NET qui sont disponibles sur toutes les implémentations de .NET. Ciblage de .NET Standard vous permet de générer des bibliothèques qui sont contraints d’utiliser des API qui se trouvent dans une version donnée de .NET Standard, ce qui signifie qu’il est utilisable par toutes les plateformes qui implémentent cette version de .NET Standard.

![.NET standard](./media/cross-platform-targeting/platforms-netstandard.png ".NET Standard")

Ciblage de .NET Standard et la compilation avec succès votre projet, ne garantissent pas que la bibliothèque fonctionne correctement sur toutes les plateformes :

1. API propres aux plateformes échouera sur d’autres plateformes. Par exemple, <xref:Microsoft.Win32.Registry?displayProperty=nameWithType> réussissent sur Windows et de lever <xref:System.PlatformNotSupportedException> lorsqu’il est utilisé sur n’importe quel autre système d’exploitation.
2. API peuvent se comporter différemment. Par exemple, la réflexion API ont les caractéristiques de performances différentes lorsqu’une application utilise la compilation ahead of time sur iOS ou UWP.

> [!TIP]
> L’équipe .NET [offre un analyseur Roslyn](../analyzers/api-analyzer.md) pour vous aider à détecter les éventuels problèmes.

**FAIRE ✔️** commencer par y compris un `netstandard2.0` cible.

> Plus les bibliothèques à usage général ne devez pas les API en dehors de .NET Standard 2.0. .NET standard 2.0 est pris en charge par toutes les plateformes modernes et est la méthode recommandée pour prendre en charge plusieurs plateformes avec une cible.

**Évitez de ❌** , y compris un `netstandard1.x` cible.

> .NET standard 1.x est distribué sous la forme d’un ensemble précis de packages NuGet, qui crée un graphique de dépendance de package volumineux et entraîne le téléchargement d’un grand nombre de packages lors de la génération de développeurs. Les plateformes .NET modernes, y compris .NET Framework 4.6.1, UWP et Xamarin, tous les prennent en charge .NET Standard 2.0. Vous devez uniquement cibler .NET Standard 1.x si vous avez besoin de cibler une plateforme plus ancienne.

**FAIRE ✔️** incluent un `netstandard2.0` cible si vous avez besoin d’un `netstandard1.x` cible.

> Toutes les plateformes prenant en charge .NET Standard 2.0 utilisera le `netstandard2.0` cible et de profiter d’un graphique de package plus petit tandis que les anciennes plateformes toujours travaillera et revenir à l’utilisation du `netstandard1.x` cible.

**N’est pas le cas de ❌** incluent une cible .NET Standard si la bibliothèque s’appuie sur un modèle d’application spécifique à la plateforme.

> Par exemple, une bibliothèque de boîte à outils contrôles UWP dépend d’un modèle d’application qui est uniquement disponible sur UWP. Modèle spécifiques de l’application API ne sera pas disponibles dans .NET Standard.

## <a name="multi-targeting"></a>Multi-ciblage

Parfois, vous avez besoin accéder aux API de framework spécifique à partir de vos bibliothèques. La meilleure façon d’appeler des API spécifiques à l’infrastructure est grâce au multi-ciblage, qui génère votre projet pour un grand nombre [frameworks cibles de .NET](../frameworks.md) plutôt que pour un seul.

Pour protéger vos consommateurs d’avoir à créer pour chaque infrastructure, vous devez vous efforcer d’avoir une sortie Standard de .NET ainsi qu’une ou plusieurs sorties spécifiques à l’infrastructure. Avec la fonctionnalité de multi-ciblage, tous les assemblys sont empaquetées dans un seul package NuGet. Les consommateurs peuvent ensuite référencer le même package et NuGet choisit l’implémentation appropriée. Votre bibliothèque .NET Standard sert de la bibliothèque de secours est utilisé partout, sauf pour les cas où votre package NuGet offre une implémentation spécifique de framework. Multi-ciblage permet d’utiliser la compilation conditionnelle dans votre code et appeler des API spécifiques à l’infrastructure.

![Package NuGet avec plusieurs assemblys](./media/cross-platform-targeting/nuget-package-multiple-assemblies.png "package NuGet avec plusieurs assemblys")

**ENVISAGEZ de ✔️** ciblant les implémentations de .NET en plus de .NET Standard.

> Ciblage des implémentations de .NET vous permet d’appeler les API spécifiques à la plateforme qui sont trouvent en dehors de .NET Standard.
>
> Ne pas supprimer de prise en charge de .NET Standard lorsque vous effectuez cette opération. Au lieu de cela, lever à partir de l’implémentation et offre la fonctionnalité API. De cette façon, votre bibliothèque peut être utilisée partout et prend en charge le runtime mise en évidence des fonctionnalités.

**Évitez de ❌** à l’aide de multi-ciblage avec .NET Standard si votre code source est identique pour toutes les cibles.

> L’assembly .NET Standard est automatiquement utilisé par NuGet. Ciblage des implémentations .NET individuelles augmente la `*.nupkg` taille sans recevoir aucun avantage.

**✔️ Envisagez** Ajout d’une cible pour `net461` lorsque que vous proposez un `netstandard2.0` cible. 

> À l’aide de .NET Standard 2.0 de .NET Framework a certains problèmes qui ont été résolus dans .NET Framework 4.7.2. Vous pouvez améliorer l’expérience pour les développeurs qui se trouvent toujours sur .NET Framework 4.6.1 - 4.7.1 en leur offrant un fichier binaire qui est conçu pour le .NET Framework 4.6.1.

**FAIRE ✔️** distribuer votre bibliothèque à l’aide d’un package NuGet.

> NuGet sélectionne la meilleure cible pour les développeurs et de protéger les avoir à choisir l’implémentation appropriée.

**FAIRE ✔️** utiliser un fichier de projet `TargetFrameworks` propriété lors de la fonctionnalité de multi-ciblage.

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <!-- This project will output netstandard2.0 and net461 assemblies -->
    <TargetFrameworks>netstandard2.0;net461</TargetFrameworks>
  </PropertyGroup>
</Project>
```

**✔️ Envisagez** à l’aide de [MSBuild.Sdk.Extras](https://github.com/onovotny/MSBuildSdkExtras) lorsque multi-targeting pour UWP et Xamarin car il simplifie considérablement votre fichier projet.

## <a name="older-targets"></a>Cibles plus anciens

.NET prend en charge des versions ciblage du .NET Framework qui sont longues en dehors de la prise en charge, ainsi que des plateformes n’est plus couramment utilisées. Pendant de valeur pour effectuer votre travail de bibliothèque sur comme de nombreux objectifs que possible, de devoir contourner manque des API peuvent ajouter importante surcharge. Nous pensons que certaines infrastructures ne sont plus intéressant de ciblage, envisagez leur portée et les limitations.

**N’est pas le cas de ❌** inclure une cible de la bibliothèque de classes Portable (PCL). Par exemple, `portable-net45+win8+wpa81+wp8`.

> .NET standard est la manière moderne pour prendre en charge les bibliothèques .NET multiplateforme et remplace les bibliothèques de classes portables.

**N’est pas le cas de ❌** incluent des cibles pour les plateformes .NET qui ne sont plus prises en charge. Par exemple, `SL4`, `WP`.

>[!div class="step-by-step"]
[Précédent](./get-started.md)
[Suivant](./strong-naming.md)
