---
title: Bibliothèques NuGet et .NET
description: Meilleures pratiques recommandées pour l’empaquetage avec NuGet pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: d0ea462a7f52dd9a6b2f14be9ed5770160bf66b1
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374490"
---
# <a name="nuget"></a>NuGet

NuGet est un gestionnaire de package pour l’écosystème .NET et est passé, les développeurs principal découvrir et d’obtenir les bibliothèques .NET open source. [NuGet.org](https://www.nuget.org/), un service gratuit fourni par Microsoft pour l’hébergement de packages NuGet, est l’hôte principal pour les packages NuGet publiques, mais vous pouvez publier dans les services de NuGet personnalisés tels que [MyGet](https://www.myget.org/) et [les artefacts Azure ](https://azure.microsoft.com/services/devops/artifacts/).

![NuGet](./media/nuget/nuget-logo.png "NuGet")

## <a name="create-a-nuget-package"></a>Créer un package NuGet

Un package NuGet (`*.nupkg`) est un fichier zip qui contient les assemblys .NET et les métadonnées associées.

Il existe deux façons de créer un package NuGet. La plus récente et recommandée consiste à créer un package à partir d’un projet de SDK-style (fichier de projet dont le contenu commence par `<Project Sdk="Microsoft.NET.Sdk">`). Assemblys et cibles sont automatiquement ajoutés au package et restant des métadonnées est ajoutée au fichier MSBuild, comme le numéro de version et de nom de package. Compilation avec le [ `dotnet pack` ](../../core/tools/dotnet-pack.md) commande sorties un `*.nupkg` fichier au lieu des assemblys.

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFramework>netstandard2.0</TargetFramework>
    <AssemblyName>Contoso.Api</AssemblyName>
    <PackageVersion>1.1.0</PackageVersion>
    <Authors>John Doe</Authors>
  </PropertyGroup>
</Project>
```

L’ancienne méthode de création d’un package NuGet est avec un `*.nuspec` fichier et le `nuget.exe` outil de ligne de commande. Un fichier nuspec vous donne un contrôle, mais vous devez spécifier soigneusement les assemblys et les cibles à inclure dans le package NuGet final. Il est facile de commettre une erreur ou pour une personne d’oublier de mettre à jour le fichier nuspec lors des modifications. L’avantage d’un fichier nuspec est de vous permet de créer des packages NuGet pour les infrastructures qui ne gèrent pas encore un fichier de projet de style SDK.

**ENVISAGEZ de ✔️** à l’aide d’un fichier de projet de style SDK pour créer le package NuGet.

**ENVISAGEZ de ✔️** configuration SourceLink afin d’ajouter les métadonnées de contrôle de code source à vos assemblys et le package NuGet.

## <a name="package-dependencies"></a>Dépendances de package

Dépendances de package NuGet sont traitées en détail dans le [dépendances](./dependencies.md) article.

## <a name="important-nuget-package-metadata"></a>Métadonnées de package NuGet importantes

Un package NuGet prend en charge plusieurs [propriétés de métadonnées](/nuget/reference/nuspec). Le tableau suivant contient les métadonnées de base que chaque projet open source doit fournir :

| Nom de la propriété MSBuild              | Nom de fichier NuSpec              | Description  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | L’identificateur du package. Un préfixe de l’identificateur peut être réservé s’il répond à la [critères](/nuget/reference/id-prefix-reservation). |
| `PackageVersion`                   | `version`                  | Version du package NuGet. Pour plus d’informations, consultez [version du package NuGet](./versioning.md#nuget-package-version).             |
| `Title`                            | `title`                    | Un titre convivial du package. Les valeurs par défaut pour le `PackageId`.             |
| `Description`                      | `description`              | Longue description du package affiché dans l’interface utilisateur.             |
| `Authors`                          | `authors`                  | Liste séparée par des virgules des auteurs de packages, correspondent aux noms de profil sur nuget.org.             |
| `PackageTags`                      | `tags`                     | Une liste délimitée de balises et les mots clés qui décrivent le package. Les balises sont utilisées lors de la recherche pour les packages.             |
| `PackageIconUrl`                   | `iconUrl`                  | URL d’une image à utiliser comme icône pour le package. URL doit être HTTPS et l’image doit être de 64 x 64 et un arrière-plan transparent.             |
| `PackageProjectUrl`                | `projectUrl`               | Une URL pour le dépôt source ou de la page d’accueil du projet.             |
| `PackageLicenseUrl`                | `licenseUrl`               | Une URL à la licence de projet. Peut être l’URL vers le `LICENSE` fichier dans le contrôle de code source.             |

**ENVISAGEZ de ✔️** choisir un nom de package NuGet avec un préfixe qui répond à la réservation du préfixe de NuGet [critères](/nuget/reference/id-prefix-reservation).

**✔️ Envisagez** à l’aide de la `LICENSE` fichier dans le contrôle de code source en tant que le `LicenseUrl`. Par exemple, [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md).

> [!IMPORTANT]
> Un projet sans une licence par défaut est [copyright exclusif](https://choosealicense.com/no-permission/), ce qui empêche d’autres personnes à utiliser.

**FAIRE ✔️** utiliser une href HTTPS à l’icône de votre package.

> Exécutent des sites comme NuGet.org avec le protocole HTTPS est activé et afficher une image non-HTTPS créera un avertissement de contenu mixte.

**FAIRE ✔️** utiliser une image d’icône de package qui est de 64 x 64 et a un arrière-plan transparent pour optimiser l’affichage.

## <a name="pre-release-packages"></a>Packages de préversion

Les packages NuGet avec un suffixe de version sont considérés comme [préliminaires](/nuget/create-packages/prerelease-packages). Par défaut, le Gestionnaire de Package NuGet UI affiche les versions stables, sauf si un utilisateur choisit de pré-version de packages, ce qui rend les packages de la version préliminaire idéal pour les tests utilisateur limité.

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> Un package stable ne peut pas dépendre d’un package de version préliminaire. Vous devez mettre votre propre package préliminaires ou dépendent d’une version stable antérieure.

![Dépendance de package de version préliminaire de NuGet](./media/nuget/nuget-prerelease-package.png "dépendance de package de version préliminaire de NuGet")

**FAIRE ✔️** publier un package de version préliminaire lors de tests, l’aperçu ou de l’expérimentation.

**FAIRE ✔️** publier un package stable lorsque son prêt pour que d’autres packages stables y faire référence.

## <a name="symbol-packages"></a>Packages de symboles

NuGet prend en charge [génération d’un package de symboles distincts](/nuget/create-packages/symbol-packages) contenant de déboguer les fichiers PDB en même temps que le package principal contenant les assemblys .NET. L’idée de packages de symboles est qu’ils sont hébergés sur un serveur de symboles et sont téléchargés uniquement par un outil tel que Visual Studio à la demande.

Actuellement l’hôte publique principale pour les symboles - [SymbolSource](http://www.symbolsource.org/) -ne prend pas en charge les fichiers PDB portables créés par le Kit de développement logiciel-style projets et packages de symboles ne sont pas utiles.

**ENVISAGEZ de ✔️** l’incorporation de fichiers PDB dans le package NuGet principal.

**Évitez de ❌** création d’un package de symboles contenant les fichiers PDB.

>[!div class="step-by-step"]
[Précédent](./strong-naming.md)
[Suivant](./dependencies.md)
