---
title: Programmation parallèle en .NET
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- parallel programming
ms.assetid: 4d83c690-ad2d-489e-a2e0-b85b898a672d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2765d7bf98c8e22e0bf495ac91ab1c15327bae42
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2018
ms.locfileid: "42907977"
---
# <a name="parallel-programming-in-net"></a>Programmation parallèle en .NET

De nombreux ordinateurs personnels et stations de travail ont plusieurs cœurs de processeur qui permettent à plusieurs threads de s’exécuter simultanément. Les ordinateurs, dans un proche avenir, sont supposés être dotés d'un nombre significativement plus élevé de cœurs. Pour tirer parti du matériel actuel et futur, vous pouvez paralléliser votre code pour distribuer le travail sur plusieurs processeurs. Dans le passé, la parallélisation nécessitait un niveau peu élevé de manipulation de threads et de verrous. Visual Studio 2010 et le .NET Framework 4 améliorent la prise en charge de la programmation parallèle en fournissant une nouvelle exécution, des nouveaux types de bibliothèques de classes et de nouveaux outils de diagnostics. Ces fonctionnalités simplifient le développement parallèle et vous permettent d’écrire du code parallèle efficace, à grains fins et évolutif dans un idiome naturel sans devoir utiliser directement des threads ou le pool de threads. L’illustration suivante fournit une vue d’ensemble générale de l’architecture de programmation parallèle dans le .NET Framework 4.

 ![Architecture de programmation parallèle du .NET](./media/tpl-architecture.png "TPL_Architecture")

## <a name="related-topics"></a>Rubriques connexes

|Technologie|Description|
|----------------|-----------------|
|[La bibliothèque parallèle de tâches](../../../docs/standard/parallel-programming/task-parallel-library-tpl.md)|Fournit la documentation pour la classe <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>, qui inclut des versions parallèles de `For` et des boucles `ForEach`, et également pour la classe <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>, qui représente la meilleure façon d'exprimer des opérations asynchrones.|
|[Parallel LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)|Implémentation parallèle de LINQ to Objects qui améliore de manière significative la performance dans de nombreux scénarios.|
|[Structures de données pour la programmation parallèle](../../../docs/standard/parallel-programming/data-structures-for-parallel-programming.md)|Fournit des liens vers la documentation pour les classes de collection thread-safe, les types de synchronisation légers et les types pour l’initialisation tardive.|
|[Outils de diagnostic parallèle](../../../docs/standard/parallel-programming/parallel-diagnostic-tools.md)|Fournit des liens vers la documentation relative aux fenêtres du débogueur Visual Studio pour les tâches et les piles parallèles, et au [Visualiseur concurrentiel](/visualstudio/profiling/concurrency-visualizer).|
|[Partitionneurs personnalisés pour PLINQ et la bibliothèque parallèle de tâches (TPL)](../../../docs/standard/parallel-programming/custom-partitioners-for-plinq-and-tpl.md)|Décrit le fonctionnement des partitionneurs et comment configurer les partitionneurs par défaut ou en créer.|
|[Planificateurs de tâches](http://msdn.microsoft.com/library/638f8ea5-21db-47a2-a934-86e1e961bf65)|Décrit le fonctionnement des planificateurs et comment les planificateurs par défaut peuvent être configurés.|
|[Expressions lambda en PLINQ et dans la bibliothèque parallèle de tâches](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)|Fournit une vue d’ensemble d’expressions lambda en C#  et Visual Basic, et affiche comment elles sont utilisées dans PLINQ et la bibliothèque parallèle de tâches.|
|[Pour aller plus loin](../../../docs/standard/parallel-programming/for-further-reading-parallel-programming.md)|Fournit des liens vers des informations supplémentaires et des exemples de ressources pour la programmation parallèle dans .NET.|

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble asynchrone](../async.md)
- [Threading managé](../threading/index.md)
