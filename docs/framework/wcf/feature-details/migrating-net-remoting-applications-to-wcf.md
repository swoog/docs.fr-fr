---
title: Migration d'applications .NET Remoting vers WCF
ms.date: 03/30/2017
helpviewer_keywords:
- ',NET remoting [WCF]'
ms.assetid: 24793465-65ae-4308-8c12-dce4fd12a583
ms.openlocfilehash: 53f63352503a48ee849580e676b5fe98f3dcf2cd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33492494"
---
# <a name="migrating-net-remoting-applications-to-wcf"></a>Migration d'applications .NET Remoting vers WCF
**Cette rubrique est spécifique à une technologie héritée qui assure la compatibilité descendante avec des applications existantes et n'est pas recommandée en cas de nouveau développement. Les applications distribuées doivent maintenant être développées à l’aide de WCF.**  
  
 Il existe deux façons pour tirer parti de WCF avec les applications .NET Remoting existantes : l’intégration et migration. Intégration vous permet d’avoir .net Remoting 2.0 et WCF en cours d’exécution côte à côte, ce qui vous permet d’exposer les mêmes objets métier sur ces deux technologies simultanément sans avoir à modifier votre .net existant code 2.0 de la communication à distance. L'intégration requiert l'utilisation de [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 ou version ultérieure. Si vous souhaitez tirer parti des fonctionnalités de WCF et que vous n’avez pas besoin de câble la compatibilité avec les systèmes Remoting 2.0, vous pouvez migrer l’ensemble de votre service WCF. Migration à partir de .NET Remoting 2.0 vers WCF requiert des modifications apportées à l’interface de l’objet distant et ses paramètres de configuration. Deux de ces rubriques sont abordés dans [à partir de la communication à distance de Windows Communication Foundation](http://go.microsoft.com/fwlink/?LinkId=74403).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble conceptuelle](../../../../docs/framework/wcf/conceptual-overview.md)
