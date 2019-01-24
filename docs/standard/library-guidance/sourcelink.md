---
title: Bibliothèques SourceLink et .NET
description: Recommandations relatives aux bonnes pratiques pour l’utilisation de SourceLink afin d’améliorer le débogage pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 01/15/2019
ms.openlocfilehash: be97f868e2fcfc6c45e4bbac45b033f8914f4d99
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333536"
---
# <a name="sourcelink"></a>SourceLink

SourceLink est une technologie qui permet le débogage du code source des assemblys .NET à partir de NuGet par les développeurs. SourceLink s’exécute lors de la création du package NuGet et incorpore des métadonnées de contrôle de code source à l’intérieur des assemblys et du package. Les développeurs qui téléchargent le package et activent SourceLink dans Visual Studio peuvent effectuer un pas à pas détaillé dans son code source. SourceLink fournit des métadonnées de contrôle de code source pour créer une excellente expérience de débogage.

## <a name="sourcelink-demo"></a>Démonstration de SourceLink

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a>Utilisation de SourceLink

Vous trouverez des instructions sur l’utilisation de SourceLink dans le dépôt GitHub [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md).

Vous pouvez utiliser [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) pour confirmer que les métadonnées SourceLink ont été correctement incorporées dans le package. Vérifiez que les métadonnées `Repository` sont présentes avec un identificateur de commentaire et que les fichiers .pdb se trouvent avec le fichier .dll de chaque cible.

![SourceLink dans NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink dans NuGet Package Explorer")

**✔️ À ENVISAGER** : Utiliser SourceLink pour ajouter des métadonnées de contrôle de code source à vos assemblys et packages NuGet.

> [!TIP]
> Vous pouvez améliorer davantage l’expérience de débogage d’un développeur en ajoutant des attributs de débogueur à vos types.
> * <xref:System.Diagnostics.DebuggerDisplayAttribute> peut personnaliser la façon dont une classe ou un champ s’affiche dans les fenêtres de variables du débogueur.
> * <xref:System.Diagnostics.DebuggerStepThroughAttribute> demande au débogueur de parcourir le code au lieu d’y effectuer un pas à pas détaillé.
> * <xref:System.Diagnostics.DebuggerBrowsableAttribute> contrôle si un membre est affiché dans les fenêtres de variables du débogueur.

**✔️ À ENVISAGER** : publication des fichiers de symboles (`*.pdb`).

> Pour plus d’informations sur les fichiers de symboles et les packages de symboles, consultez [Packages de symboles](./nuget.md#symbol-packages).

>[!div class="step-by-step"]
>[Précédent](dependencies.md)
>[Suivant](publish-nuget-package.md)
