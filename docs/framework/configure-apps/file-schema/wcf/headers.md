---
title: <headers>
ms.date: 03/30/2017
ms.assetid: c79b897d-8ea3-40b5-a8b6-2471941f7ed3
ms.openlocfilehash: 660497012dd057e4ecf95524833e2573fe03a8b0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670675"
---
# <a name="headers"></a>\<headers>
Un point de terminaison peut être adressé par un ou plusieurs en-têtes SOAP en plus de son URI de base. Le jeu de scénarios où cette opération est utile est un jeu de scénarios intermédiaires SOAP où un point de terminaison requiert que les clients de ce point de terminaison incluent des en-têtes SOAP destinés à des intermédiaires. Cet élément de configuration peut être utilisé pour définir ces en-têtes d'adresse personnalisés. Les entrées de la collection d’en-têtes de points de terminaison sont des éléments XML définis par l’utilisateur. Chaque élément doit être au format XML adéquat.  
  
 \<system.ServiceModel>  
\<client>  
\<endpoint>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<headers>
  <region xmlns="Uri">"String"</region>
  <member xmlns="Uri">"String"</member>
</headers>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
 Éléments XML définis par l’utilisateur.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<endpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-of-client.md)|Configure différents types de points de terminaison.|  
  
## <a name="remarks"></a>Notes  
 Les en-têtes facultatifs fournissent des informations d'adressage plus détaillées pour identifier ou interagir avec le point de terminaison. Par exemple, les en-tête peuvent indiquer comment traiter un message entrant, où le point de terminaison doit envoyer un message de réponse ou quelle instance d'un service utiliser pour traiter un message entrant d'un utilisateur particulier lorsque plusieurs instances sont disponibles.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Headers%2A>
- <xref:System.ServiceModel.Channels.AddressHeaderCollection>
- [Points de terminaison : Adresses, liaisons et contrats](../../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
