---
title: <clear> de <claimTypeRequirements> élément
ms.date: 03/30/2017
ms.assetid: ef42fde7-f292-4610-9111-9fea382c3b5f
ms.openlocfilehash: b20d5c1808bf41d1ecd6b3e3a61606ae45b0fbdd
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270336"
---
# <a name="clear-of-claimtyperequirements-element"></a>\<Désactivez > de \<claimTypeRequirements > élément
Indique que tous les types de revendications doivent être supprimés dans les informations d'identification fédérées. Cela garantit que la collection est vide au démarrage.  
  
 \<system.ServiceModel>  
\<bindings>  
\<wsFederatedBinding>  
\<binding>  
\<security>  
\<message>  
\<claimTypeRequirements>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<claimTypeRequirements>
  <clear />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<claimTypeRequirements>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-for-message.md)|Spécifie une collection de types de revendications requis. Chaque élément est de type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.<br /><br /> Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes. Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini. Chaque élément de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d’identification fédérées.|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
