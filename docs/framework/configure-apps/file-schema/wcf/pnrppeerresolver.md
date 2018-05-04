---
title: '&lt;pnrpPeerResolver&gt;'
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: f0874d38c3432f066d1bec5cc84f53e1f3730180
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltpnrppeerresolvergt"></a>&lt;pnrpPeerResolver&gt;
Spécifie que le programme de résolution PNRP (Peer Name Resolution Protocol) doit être utilisé comme un programme de résolution. Cet élément est facultatif parce que PNRP est le programme de résolution par défaut.  
  
 \<system.serviceModel>  
\<liaisons >  
\<customBinding >  
\<liaison >  
\<pnrpResolver >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<pnrpResolver resolverType="String" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|resolverType|Chaîne qui spécifie le programme de résolution à utiliser. Cet attribut est facultatif. S'il n'est pas défini ou s'il a pour valeur une chaîne vide, PNRP est utilisé.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<liaison >](../../../../../docs/framework/misc/binding.md)|Définit toutes les fonctions de liaison d’une liaison personnalisée.|  
  
## <a name="example"></a>Exemple  
  
```xml  
<pnrpResolver resolverType="" />  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>  
 <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [Liaisons](../../../../../docs/framework/wcf/bindings.md)  
 [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [Programmes de résolution d’homologue](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
