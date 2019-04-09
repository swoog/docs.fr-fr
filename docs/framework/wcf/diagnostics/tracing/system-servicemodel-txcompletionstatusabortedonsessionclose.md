---
title: System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
ms.date: 03/30/2017
ms.assetid: 7e142e9d-e81b-4309-974a-02e9cc064ea0
ms.openlocfilehash: 7b1f6a2f4a344b566c76d0095942b84a8a4e76f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59166502"
---
# <a name="systemservicemodeltxcompletionstatusabortedonsessionclose"></a>System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
La transaction spécifiée a été abandonnée car elle était inachevée lorsque la session a été fermée et le OperationBehaviorAttribute TransactionAutoCompleteOnSessionClose a été défini à false.  
  
## <a name="description"></a>Description  
 Suivi si la session active actuelle a été fermée, que la transaction n'a pas été achevée et que TransactionAutoCompleteOnSessionClose a la valeur `false`.  
  
## <a name="troubleshooting"></a>Résolution des problèmes  
 Cette trace indique un bogue d'application potentiel qui doit être étudié.  
  
## <a name="see-also"></a>Voir aussi

- [Traçage](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
