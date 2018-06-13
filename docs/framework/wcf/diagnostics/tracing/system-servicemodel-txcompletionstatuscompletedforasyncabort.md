---
title: System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort
ms.date: 03/30/2017
ms.assetid: 155c3203-2e17-4709-b896-2254e22da45e
ms.openlocfilehash: a243acc3d8a17e4a53b3d05e3420f481f7b6dc6b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33486027"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforasyncabort"></a>System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort
La transaction spécifiée pour l’opération indiquée s’est terminée en raison d’un abandon asynchrone.  
  
## <a name="description"></a>Description  
 La transaction courante a été abandonnée car un autre participant a voté Abort, le délai a été dépassé et une autre erreur s'est produite à l'intérieur du participant d'une transaction.  
  
## <a name="troubleshooting"></a>Résolution des problèmes  
 Si cet abandon est inattendu, vérifiez tous les journaux système afin de déterminer la véritable raison de l'abandon.  
  
## <a name="see-also"></a>Voir aussi  
 [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
