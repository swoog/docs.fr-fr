---
title: Minuteries
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [.NET Framework], timers
- timers, about timers
ms.assetid: 7091500d-be18-499b-a942-95366ce185e5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 478484651bf839f842148f0b4164c9387db3b98a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="timers"></a>Minuteries
Les minuteurs sont des objets légers qui vous permettent de spécifier un délégué à appeler à une heure définie. Un thread du pool de threads exécute l’opération d’attente.  
  
 L’utilisation de la classe <xref:System.Threading.Timer?displayProperty=nameWithType> est simple. Vous créez un **minuteur** en passant un délégué <xref:System.Threading.TimerCallback> à la méthode de rappel, un objet représentant l’état qui sera passé au rappel, une heure de déclenchement initiale et une heure représentant l’intervalle entre les appels de rappel. Pour annuler un minuteur en attente, appelez la fonction **Timer.Dispose**.  
  
> [!NOTE]
>  Il existe deux autres classes de minuteur. La classe <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> est un contrôle qui fonctionne avec les concepteurs visuels et qui est destiné à une utilisation dans des contextes d’interface utilisateur. Il déclenche des événements sur le thread d’interface utilisateur. La classe <xref:System.Timers.Timer?displayProperty=nameWithType> dérive de <xref:System.ComponentModel.Component>, ce qui permet de l’utiliser avec des concepteurs visuels. Elle déclenche également des événements, mais sur un thread <xref:System.Threading.ThreadPool>. La classe <xref:System.Threading.Timer?displayProperty=nameWithType> effectue les rappels sur un thread <xref:System.Threading.ThreadPool> et n’utilise jamais le modèle d’événement. Elle fournit également un objet d’état à la méthode de rappel, à la différence des autres minuteurs. Elle est très légère.  
  
 L’exemple de code suivant lance un minuteur qui se déclenche après une seconde (1 000 millisecondes) et qui marque chaque seconde jusqu'à ce que vous appuyiez sur la touche **Entrée**. La variable contenant la référence au minuteur est un champ de niveau classe qui garantit que le minuteur ne sera pas soumis au nettoyage de mémoire durant son exécution. Pour plus d’informations sur le nettoyage de mémoire agressif, consultez <xref:System.GC.KeepAlive%2A>.  
  
 [!code-cpp[System.Threading.Timer#2](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.Threading.Timer/CPP/source2.cpp#2)]
 [!code-csharp[System.Threading.Timer#2](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.Threading.Timer/CS/source2.cs#2)]
 [!code-vb[System.Threading.Timer#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.Threading.Timer/VB/source2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.Timer>  
 [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)
