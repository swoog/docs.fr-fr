---
title: Bibliothèques SourceLink et .NET
description: Meilleures pratiques recommandées pour l’utilisation de SourceLink pour améliorer le débogage pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: fa4af47eaa5dd1510640c2bf0ebb2187b56efae0
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49370043"
---
# <a name="sourcelink"></a>SourceLink

SourceLink est une technologie qui permet le débogage du code source des assemblys .NET à partir de NuGet par les développeurs. SourceLink s’exécute lors de la création du package NuGet et incorpore des métadonnées de contrôle de source à l’intérieur des assemblys et le package. Les développeurs qui téléchargent le package et ont SourceLink activée dans Visual Studio peuvent accéder à son code source. SourceLink fournit les métadonnées de contrôle de source pour créer une excellente expérience de débogage.

## <a name="sourcelink-demo"></a>Démonstration de SourceLink

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a>À l’aide de SourceLink

Vous trouverez des instructions sur l’utilisation de SourceLink sur le [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) référentiel GitHub.

Vous pouvez utiliser [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) pour confirmer que les métadonnées SourceLink a été correctement incorporée dans le package. Vérifier le `Repository` métadonnées soient établie avec un identificateur de commentaire et qui se trouvent les fichiers .pdb avec .dll chaque cible.

![SourceLink dans l’Explorateur de Package NuGet](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink dans l’Explorateur de Package NuGet")

**ENVISAGEZ de ✔️** à l’aide de SourceLink pour ajouter les métadonnées de contrôle de code source à vos assemblys et le package NuGet.

**ENVISAGEZ de ✔️** , y compris les fichiers PDB dans le package NuGet.

>[!div class="step-by-step"]
[Précédent](./dependencies.md)
[Suivant](./publish-nuget-package.md)
