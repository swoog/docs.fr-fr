---
title: '&lt;callbackDebug&gt;'
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: 5bd2356c3bb798e948341cb3c4ba504ac886ed44
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145079"
---
# <a name="ltcallbackdebuggt"></a>&lt;callbackDebug&gt;
Spécifie le débogage de service pour un objet de rappel Windows Communication Foundation (WCF).  
  
 \<system.ServiceModel>  
\<comportements >  
\<endpointBehaviors >  
\<comportement >  
\<callbackDebug >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|Valeur qui spécifie si les objets de rappel client retournent au service des informations sur les exceptions managées dans les erreurs SOAP.<br /><br /> Si vous définissez cet attribut par programme à `true`, vous pouvez activer le retour du flux d'informations sur les exceptions managées dans un objet de rappel client, à des fins de débogage. **Attention :**  Le retour des informations sur les exceptions managées aux clients peut entraîner un problème de sécurité. En effet, les détails de l'exception exposent des informations relatives à l'implémentation d'un service interne qui peuvent être utilisées par des clients non autorisés.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Spécifie un comportement de point de terminaison.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.CallbackDebugElement>  
 <xref:System.ServiceModel.Description.CallbackDebugBehavior>
