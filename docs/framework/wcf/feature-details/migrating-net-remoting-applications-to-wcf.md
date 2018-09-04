---
title: Migration d'applications .NET Remoting vers WCF
ms.date: 03/30/2017
helpviewer_keywords:
- ',NET remoting [WCF]'
ms.assetid: 24793465-65ae-4308-8c12-dce4fd12a583
ms.openlocfilehash: 3f5556eeaf56ac48dd4f1d578ed2e66b90415677
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503432"
---
# <a name="migrating-net-remoting-applications-to-wcf"></a>Migration d'applications .NET Remoting vers WCF
**Cette rubrique est spécifique à une technologie héritée qui assure la compatibilité descendante avec des applications existantes et n'est pas recommandée en cas de nouveau développement. Les applications distribuées doivent maintenant être développées à l’aide de WCF.**  
  
 Il existe deux façons de tirer parti de WCF avec les applications .NET Remoting existantes : l’intégration et migration. Intégration vous permet de disposer de .net Remoting 2.0 et WCF en cours d’exécution côte à côte, ce qui vous permet d’exposer les mêmes objets métier sur ces deux technologies simultanément sans avoir à modifier votre .net existant code 2.0 de communication à distance. L'intégration requiert l'utilisation de [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 ou version ultérieure. Si vous souhaitez tirer parti des fonctionnalités de WCF et que vous n’avez pas besoin de compatibilité de la communication avec les systèmes Remoting 2.0, vous pouvez migrer votre ensemble du service WCF. Migration de .NET Remoting 2.0 vers WCF nécessite des modifications à l’interface de l’objet distant et ses paramètres de configuration. Ces deux rubriques couvertes dans [de Remoting vers Windows Communication Foundation](https://go.microsoft.com/fwlink/?LinkId=74403).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble conceptuelle](../../../../docs/framework/wcf/conceptual-overview.md)
