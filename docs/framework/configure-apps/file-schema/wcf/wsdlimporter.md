---
title: '&lt;wsdlImporter&gt;'
ms.date: 03/30/2017
ms.assetid: 986b2165-8430-4dba-b1b8-00396841bb96
ms.openlocfilehash: 33c2b0e4286ce746f745e4aebe10fd4bbd96810f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltwsdlimportergt"></a>&lt;wsdlImporter&gt;
Indique tous les importateurs WSDL qui importent des métadonnées WSDL (Web Services Description Language) 1.1 avec des pièces jointes WS-Policy.  
  
\<system.ServiceModel>  
\<client>  
\<métadonnées >  
\<wsdlImporters >  
\<wsdlImporter >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<metadata>  
  <wsdlImporters>  
    <wsdlImporter type="string" />  
  </wsdlImporters>  
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
|[\<wsdlImporters >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdlimporters.md)|Indique tous les importateurs WSDL qui importent des métadonnées WSDL (Web Services Description Language) 1.1 avec des pièces jointes WS-Policy.|  
  
## <a name="remarks"></a>Notes  
 Un importateur WSDL permet d'importer des métadonnées et de convertir ces informations en différentes classes représentant les informations de contrat et de point de terminaison. Il peut importer sélectivement des informations de contrat et de point de terminaison ainsi que des propriétés qui exposent toute erreur d'importation et accepte des informations de types liées au processus d'importation et de conversion. Il prend également en charge les informations et les propriétés de liaison qui donnent accès aux documents de stratégie, documents WSDL, extensions WSDL et documents de schéma XML.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.WsdlImporterElement>  
 <xref:System.ServiceModel.Configuration.MetadataElement>  
 <xref:System.ServiceModel.Configuration.WsdlImporterElementCollection>  
 <xref:System.ServiceModel.Description.MetadataImporter>  
 <xref:System.ServiceModel.Description.WsdlImporter>  
 [Configuration du client WCF](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [Clients](../../../../../docs/framework/wcf/feature-details/clients.md)
