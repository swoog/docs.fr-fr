---
title: Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure
ms.date: 03/30/2017
ms.assetid: 1b9f5139-e122-4716-9ef7-2f38e1813993
ms.openlocfilehash: 9dd2ba5a3e94ff794d4b8a8775944355b105f790
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="microsofttransactionstransactionbridgeenlisttransactionfailure"></a>Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure
Le service du protocole WS-AT a échoué l’enrôlement sur une transaction en utilisant le contexte de coordination fourni.  
  
## <a name="description"></a>Description  
 Suivi lorsque MSDTC ne peut pas enrôler sur une transaction pour un protocole 2PC donné.  Cela peut être dû au fait que la transaction n’existe plus, que l’enrôlement n’est plus autorisé, ou qu’un trop grand nombre d’enrôlements sont déjà présents.  
  
## <a name="troubleshooting"></a>Résolution des problèmes  
 Inspectez la chaîne d'état dans le message de suivi pour déterminer la présence éventuelle d'éléments actionnables.  
  
## <a name="see-also"></a>Voir aussi  
 [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
