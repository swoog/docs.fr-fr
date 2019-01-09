---
title: '&lt;policyImporter&gt;'
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 22d90ff9d0cd5325300cf42437836f075cbf8c31
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148485"
---
# <a name="ltpolicyimportergt"></a>&lt;policyImporter&gt;
Indique un importateur de stratégie qui contrôle l’importation d’assertions de stratégie personnalisées concernant les liaisons.  
  
 \<system.ServiceModel>  
\<client>  
\<métadonnées >  
\<policyImporters >  
\<policyImporter >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`type`|Type de cet élément.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<policyImporters >](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|Indique tous les importateurs de stratégie contrôlant l’importation d’assertions de stratégie personnalisées concernant les liaisons.|  
  
## <a name="remarks"></a>Notes  
 Un importateur de stratégie permet de rechercher des assertions de stratégie personnalisées concernant les fonctionnalités de liaison et de joindre un élément de liaison personnalisé qui implémente les fonctionnalités requises par l’assertion.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>  
 <xref:System.ServiceModel.Configuration.PolicyImporterElement>  
 <xref:System.ServiceModel.Configuration.MetadataElement>  
 <xref:System.ServiceModel.Description.MetadataImporter>  
 [Configuration du client WCF](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [Clients](../../../../../docs/framework/wcf/feature-details/clients.md)
