---
title: Instances
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 668cfb3026b9ab7259665f5e53873a512b1e2238
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59975583"
---
# <a name="instances"></a>Instances
Nom du compteur : instances.  
  
## <a name="description"></a>Description  
 Nombre de contextes d'instance que le service contient actuellement.  
  
 La plupart du temps, le nombre de contextes d'instance est identique au nombre d'instances. Toutefois, les scénarios suivants constituent des exceptions à cette règle.  
  
-   Une méthode de service appelle la méthode <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> de manière explicite.  
  
-   Un <xref:System.ServiceModel.ReleaseInstanceMode> est appliqué à une instance <xref:System.ServiceModel.OperationBehaviorAttribute>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.OperationBehaviorAttribute>
