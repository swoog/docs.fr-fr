---
title: Microsoft.Transactions.TransactionBridge.PreparedMessageRetry
ms.date: 03/30/2017
ms.assetid: 2194292d-bf5f-4aef-9336-cd3c4795cb71
ms.openlocfilehash: e5735596f1b724e47cdaadd30f07629ea6b772eb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585927"
---
# <a name="microsofttransactionstransactionbridgepreparedmessageretry"></a>Microsoft.Transactions.TransactionBridge.PreparedMessageRetry
Une nouvelle tentative de message Prepared a été envoyée à un coordinateur qui ne répond pas.  
  
## <a name="description"></a>Description  
 Suivi lorsque le gestionnaire de transactions local a dû renvoyer un message Prepared à un coordinateur supérieur parce qu’il n’a pas reçu de réponse dans un délai donné.  
  
## <a name="troubleshooting"></a>Résolution des problèmes  
 Recherchez d'éventuels problèmes liés au réseau ou au produit pouvant empêcher la réponse d'être remise à temps.  Si un nombre élevé de ces messages apparaissent, cela peut indiquer des problèmes d'infrastructure ou des délais de réponse anormalement longs. Ces deux problèmes réduiront considérablement le débit des transactions au sein du système.  
  
## <a name="see-also"></a>Voir aussi
- [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
