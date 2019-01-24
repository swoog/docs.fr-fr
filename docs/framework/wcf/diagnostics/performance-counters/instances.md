---
title: Instances
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 1b2801b5df3a5d2ca6d7fd03299ecdf4b7df426a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520263"
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
