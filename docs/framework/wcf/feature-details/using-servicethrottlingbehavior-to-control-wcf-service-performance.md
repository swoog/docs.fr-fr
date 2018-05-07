---
title: Utilisation de ServiceThrottlingBehavior pour contrôler les performances du service WCF
ms.date: 03/30/2017
helpviewer_keywords:
- behavior [WCF], service performance
ms.assetid: f9dc120c-dc24-49d5-930e-b22f5bc73423
ms.openlocfilehash: b54d1d6146b9751fdd12502771de01fe52854c07
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="using-servicethrottlingbehavior-to-control-wcf-service-performance"></a>Utilisation de ServiceThrottlingBehavior pour contrôler les performances du service WCF
La classe <xref:System.ServiceModel.Description.ServiceThrottlingBehavior> expose les propriétés que vous pouvez utiliser pour limiter le nombre d'instances ou de sessions créées au niveau de l'application. À l’aide de ce comportement, vous pouvez optimiser les performances de votre application Windows Communication Foundation (WCF).  
  
## <a name="controlling-service-instances-and-concurrent-calls"></a>Contrôle des instances de service et des appels simultanés  
 Utilisez la propriété <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentCalls%2A> pour spécifier le nombre maximal des messages en cours de traitement actif dans une classe <xref:System.ServiceModel.ServiceHost>, et la propriété <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentInstances%2A> pour spécifier le nombre maximal d'objets <xref:System.ServiceModel.InstanceContext> dans le service.  
  
 Car généralement à déterminer les paramètres de ces propriétés a lieu après l’exécution de l’application par rapport à l’expérience réelle charge, les paramètres pour le <xref:System.ServiceModel.Description.ServiceThrottlingBehavior> propriétés est généralement spécifié dans un fichier de configuration d’application à l’aide du [ \<serviceThrottling >](../../../../docs/framework/configure-apps/file-schema/wcf/servicethrottling.md) élément.  
  
 L'exemple de code suivant illustre l'utilisation de la classe <xref:System.ServiceModel.Description.ServiceThrottlingBehavior> à partir d'un fichier de configuration de l'application qui affecte aux propriétés <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentSessions%2A>, <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentCalls%2A> et <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentInstances%2A> la valeur 1 en guise d'exemple simple. L'expérience détermine les paramètres optimaux pour toute application particulière.  
  
 [!code-xml[ServiceThrottlingBehavior#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/servicethrottlingbehavior/cs/hostapplication.exe.config#3)]  
  
 Le comportement exact au moment de l'exécution dépend des valeurs des propriétés <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> et <xref:System.ServiceModel.ServiceBehaviorAttribute.InstanceContextMode%2A> qui contrôlent le nombre de messages pouvant s'exécuter simultanément dans une opération et les durées de vie du service <xref:System.ServiceModel.InstanceContext> en fonction des sessions de canal entrantes, respectivement.  
  
 Pour plus d'informations, consultez <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentCalls%2A> et <xref:System.ServiceModel.Description.ServiceThrottlingBehavior.MaxConcurrentInstances%2A>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>  
 <xref:System.ServiceModel.NetTcpBinding.MaxConnections%2A>
