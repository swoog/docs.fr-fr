---
title: "&lt;diagnostics&gt; pour l'activation"
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: 4e5332eed87ded51cebcd614f45cbc8e80e570fb
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltdiagnosticsgt-for-activation"></a>&lt;diagnostics&gt; pour l'activation
Configure les fonctionnalités de diagnostic de l’écouteur Windows Communication Foundation (WCF).  
  
 \<system.serviceModel.activation>  
\<Diagnostics >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<configuration>  
   <system.serviceModel.activation>  
       <diagnostics performanceCountersEnabled="Boolean" />  
   </system.serviceModel.activation>  
</configuration>  
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`performanceCountersEnabled`|Valeur booléenne qui indique si les compteurs de performance sont activés à des fins de diagnostic.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<system.serviceModel.activation>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|Contient les paramètres de configuration du processus de l'écouteur SMSvcHost.exe.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
