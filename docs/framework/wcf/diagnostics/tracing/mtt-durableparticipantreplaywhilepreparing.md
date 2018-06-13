---
title: Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing
ms.date: 03/30/2017
ms.assetid: 10ef3876-6f8e-4d4e-8444-f47847b64795
ms.openlocfilehash: fe88e70ab4955305d78baa1158cd73a93ba2ed2c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33476318"
---
# <a name="microsofttransactionstransactionbridgedurableparticipantreplaywhilepreparing"></a>Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing
Le service de protocole WS-AT a reçu un message Replay d'un participant durable n'ayant pas répondu au message Prepared. Par conséquent, la transaction a été abandonnée.  
  
## <a name="description"></a>Description  
 Un suivi est généré si un message Replay est reçu lorsqu'un participant durable est encore en cours de préparation. Il s'agit d'un message illégal pour cet état et la transaction va être abandonnée.  
  
## <a name="troubleshooting"></a>Résolution des problèmes  
 Recevoir ce message d’erreur peut indiquer que la défaillance du participant durable (notamment d’un gestionnaire de transactions subalterne) est à présent résolue. Cependant, le résultat de la transaction étant incertain, une requête de statut est envoyée.  
  
## <a name="see-also"></a>Voir aussi  
 [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
