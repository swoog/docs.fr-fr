---
title: System.ServiceModel.Channels.MsmqMessageDropped
ms.date: 03/30/2017
ms.assetid: 8b6e644d-fa68-4be7-abe9-3659671a37c1
ms.openlocfilehash: 6218948e89288e76034d7c3f032f3c585e286c3d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54570536"
---
# <a name="systemservicemodelchannelsmsmqmessagedropped"></a>System.ServiceModel.Channels.MsmqMessageDropped
MSMQ a supprimé le message.  
  
## <a name="description"></a>Description  
 Cette trace indique qu’un message MSMQ a été déposé. Messages MSMQ peuvent être supprimés lorsque Windows Communication Foundation (WCF) (utilisé avec NetMsmqBinding ou MsmqIntegrationBinding) ne peut pas les traiter. Ces messages sont appelés des messages incohérents.  
  
 Un message incohérent est supprimé lorsque la propriété `ReceiveErrorHandling` sur NetMsmqBinding ou MsmqIntegrationBinding a la valeur `Drop`. Ce message est supprimé de la file d’attente et ne peut plus être récupéré.  
  
 Consultez [des messages incohérents](https://go.microsoft.com/fwlink/?LinkID=99546) pour plus d’informations sur le moment où les messages deviennent incohérents et comment configurer votre service pour traiter de manière appropriée.  
  
## <a name="see-also"></a>Voir aussi
- [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
- [Messages incohérents](https://go.microsoft.com/fwlink/?LinkID=99546)
