---
title: '&lt;élément persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: 23724957398ed1ade2c81a3932e9773d7cf4c642
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltpersistabletypegt"></a>&lt;élément persistableType&gt;
Spécifie tous les types persistants.  
  
 \<system.ServiceModel>  
\<comContracts>  
\<comContract >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<comContracts>  
  <comContract>  
      <persistableTypes>  
         <persistableType id="string"  
            name="string">  
         </persistableType>  
      </persistableTypes>  
  </comContract>  
</comContracts>  
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|id|Attribut requis qui contient une chaîne spécifiant un identificateur unique pour un type persistant.|  
|name|Attribut facultatif qui contient une chaîne spécifiant le nom du type persistant.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<persistableTypes>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|Collection d'éléments `persistableType`.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>  
 [\<comContracts>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [Intégration à des applications COM+](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [Guide pratique pour configurer des paramètres de service COM+](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
