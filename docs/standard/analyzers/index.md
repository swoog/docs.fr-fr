---
title: Les analyseurs de Roslyn - .NET
description: En savoir plus sur les analyseurs de Roslyn capables de détecter les problèmes et de suggérer des correctifs pour les résoudre.
author: billwagner
ms.author: billwagner
ms.date: 01/24/2018
ms.technology: dotnet-standard
ms.openlocfilehash: ec153b8fed08ef245a3a0f58970b4e3955dfacb5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="the-roslyn-based-analyzers"></a>Les analyseurs de Roslyn

Les analyseurs de Roslyn utilisent le Kit de développement logiciel du compilateur .NET (API Roslyn) pour analyser le code source de votre projet pour détecter les problèmes et suggérer des corrections. Différents analyseurs recherchent différentes classes de problèmes, allant des pratiques susceptibles de provoquer des bogues à des problèmes de sécurité liés à la compatibilité avec les API.

Les analyseurs de Roslyn fonctionnent à la fois et de manière interactive pendant les builds. L’analyseur guide de différentes façons dans Visual Studio ou dans les builds de ligne de commande.

Lorsque vous modifiez le code dans Visual Studio, les analyseurs s’exécutent au moment de l’apport des modifications, interceptant d’éventuels problèmes dès que vous créez le code qui déclenche des problèmes. Les problèmes sont mis en surbrillance avec des tildes en-dessous. Visual Studio affiche une ampoule et lorsque vous cliquez dessus l’analyseur propose des solutions possibles à ce problème. Lorsque vous générez le projet, dans Visual Studio ou à partir de la ligne de commande, tout le code source est analysé et l’analyseur fournit une liste complète des problèmes potentiels. La figure suivante illustre un exemple.

![problèmes signalés par l’analyseur d’infrastructure](./media/framework-analyzers-2.png)

Les analyseurs de roslyn signalent des problèmes potentiels sous forme d’erreurs, d’avertissements ou d’informations en fonction de la gravité du problème.

Vous installez des analyseurs de Roslyn sous forme de packages NuGet dans votre projet. Les analyseurs configurés et tous les paramètres de chaque analyseur sont restaurés et s’exécutent sur l’ordinateur d’un développeur pour ce projet.

> [!NOTE]
> L’expérience utilisateur des analyseurs de Roslyn est différente de celle pour les bibliothèques d’analyse du code telles que les versions plus anciennes de FxCop et les outils d’analyse de sécurité.  Vous n’avez pas besoin exécuter explicitement les analyseurs de Roslyn. Il est inutile d’utiliser les éléments de menu « Exécuter l’analyse du code » dans le menu « Analyser » de Visual Studio. Les analyseurs de Roslyn s’exécutent de façon asynchrone lorsque vous travaillez. 

## <a name="more-information-on-specific-analyzers"></a>En savoir plus sur les analyseurs spécifiques

Les analyseurs suivants sont couverts dans la présente section :

[Analyseur d’API](api-analyzer.md) : cet analyseur examine votre code à la recherche de risques potentiels de compatibilité ou utilisations d’API déconseillées.    
[Analyseur d’infrastructure](framework-analyzer.md) : cet outil examine votre code pour s’assurer qu’il suit les instructions pour les applications .NET Framework. Ces règles incluent plusieurs recommandations de sécurité.
