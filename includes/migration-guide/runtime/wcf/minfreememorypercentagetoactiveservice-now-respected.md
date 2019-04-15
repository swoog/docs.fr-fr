---
ms.openlocfilehash: fa472b3a142f55f0cbdd83eabbbb00bddd9786d8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235314"
---
### <a name="minfreememorypercentagetoactiveservice-is-now-respected"></a>Le paramètre MinFreeMemoryPercentageToActiveService est désormais pris en compte

|   |   |
|---|---|
|Détails|Ce paramètre détermine la mémoire minimale devant être disponible sur le serveur avant l’activation d’un service WCF. Il a pour but de prévenir les exceptions <xref:System.OutOfMemoryException?displayProperty=name>. Dans le .NET Framework 4.5, ce paramètre était sans effet. Dans le .NET Framework 4.5.1, ce paramètre est pris en compte.|
|Suggestion|Une exception se produit si la mémoire disponible sur le serveur web est inférieure au pourcentage défini par le paramètre de configuration. Certains services WCF qui ont réussi à démarrer et à s'exécuter dans un environnement où la mémoire est limitée risquent à présent d'échouer.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|
