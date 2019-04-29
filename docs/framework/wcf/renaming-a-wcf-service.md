---
title: Attribution d'un nouveau nom à un service WCF
ms.date: 03/30/2017
ms.assetid: 14235a65-b1c5-409d-b6cc-a979acd54bbd
ms.openlocfilehash: a215523b92757e3bde1dae2e50de22169020e870
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61955140"
---
# <a name="renaming-a-wcf-service"></a>Attribution d'un nouveau nom à un service WCF
Cette rubrique décrit comment vous pouvez renommer un service Windows Communication Foundation (WCF).  
  
## <a name="renaming-a-wcf-service"></a>Attribution d'un nouveau nom à un service WCF  
 Procédez comme suit pour renommer un service dans un modèle de Windows Communication Foundation (WCF)  
  
- Modifiez le nom de la classe qui implémente le service.  
  
- Dans le fichier de configuration du service, remplacez le nom du service par celui que vous avez choisi, comme indiqué dans l'exemple suivant. Selon votre modèle d'hébergement, le fichier de configuration sera app.config ou web.config.  
  
```xml  
<system.servicemodel>  
   <services>  
      <service name="WcfService.NewName">  
      </service>  
   </services>  
</system.servicemodel>  
```  
  
- Si votre service est hébergé sur le Web, il utilise un fichier *.svc. Ouvrez le fichier svc et modifiez le nom de votre service comme indiqué dans l'exemple suivant. Cette étape n'est pas nécessaire pour les applications auto-hébergées, puisqu'il n'y a pas de fichier svc.  
  
```  
<%@ ServiceHost Service="WcfService.NewName">  
```  
  
## <a name="renaming-a-wcf-service-contract"></a>Attribution d'un nouveau nom à un contrat de service WCF  
  
- Effectuez les étapes suivantes pour renommer le contrat de service  
  
- Modifiez le nom du contrat de service.  
  
- Dans le fichier de configuration du service, remplacez le nom du contrat de service par le celui que vous avez choisi, comme indiqué dans l'exemple suivant. Selon votre modèle d'hébergement, le fichier de configuration sera app.config ou web.config.  
  
```xml  
<system.servicemodel>  
   <services>  
      <service>  
         <endpoint contract="WcfService.NewContractName" />  
      </service>  
   </services>  
</system.servicemodel>  
```
