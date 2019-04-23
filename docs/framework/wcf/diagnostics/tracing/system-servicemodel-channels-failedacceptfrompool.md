---
title: System.ServiceModel.Channels.FailedAcceptFromPool
ms.date: 03/30/2017
ms.assetid: d535b1b5-ee58-45e8-b400-7d9570f4eb9a
ms.openlocfilehash: de0bdd9e5ab922b09249bf550fde745042be8e58
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59156479"
---
# <a name="systemservicemodelchannelsfailedacceptfrompool"></a>System.ServiceModel.Channels.FailedAcceptFromPool
Échec de la tentative de réutilisation d'une connexion en groupe. Une autre tentative est effectuée dans le délai d'attente spécifié.  
  
## <a name="description"></a>Description  
 Ce suivi d'informations indique qu'une erreur s'est produite lors de la tentative de réutilisation d'une connexion en groupe. Cela peut se produire si la connexion en groupe n'est pas compatible, prête ou toujours active. Toute tentative supplémentaire pour réutiliser une autre connexion en groupe est effectuée au cours d'un délai d'expiration donné et une nouvelle connexion est créée si aucune connexion utilisable n'est trouvée.  
  
## <a name="see-also"></a>Voir aussi

- [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
