---
title: '&lt;useManagedPresentation&gt;'
ms.date: 03/30/2017
ms.assetid: 17a0dd77-af54-41db-a9d0-4b17ff42878f
ms.openlocfilehash: a60e1e16b9b41cc5df4ded51cc05d6109dd7b3dc
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147705"
---
# <a name="ltusemanagedpresentationgt"></a>&lt;useManagedPresentation&gt;
Élément de liaison utilisé pour communiquer avec un service d’émission de jeton de sécurité CardSpace qui prend en charge le profil CardSpace de WS-Trust. Cet élément n'a aucun attribut et est présent en tant que commutateur vide.  
  
 \<system.serviceModel>  
\<liaisons >  
\<customBinding >  
\<liaison >  
\<useManagedPresentation >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<useManagedPresentation />
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
|[\<liaison >](../../../../../docs/framework/misc/binding.md)|Définit toutes les fonctions de liaison d’une liaison personnalisée.|  
  
## <a name="remarks"></a>Notes  
 Cet élément est utilisé par un fournisseur d'identité pour exprimer dans sa stratégie le fait qu'il prend en charge le profil CardSpace de WS-Trust. Les fournisseurs d'identité qui publient une telle assertion de stratégie doivent être en mesure de publier des jetons selon ce profil CardSpace.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.UseManagedPresentationElement>  
 <xref:System.ServiceModel.Channels.UseManagedPresentationBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [Liaisons](../../../../../docs/framework/wcf/bindings.md)  
 [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
