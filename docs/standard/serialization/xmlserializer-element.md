---
title: Élément &lt;xmlSerializer&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- <xmlSerializer> element
- XML serialization, configuration
- xmlSerializer element
ms.assetid: d129d10c-3eb7-45d9-8098-5fa853825e47
ms.openlocfilehash: 4b511dc229c9e8321b91fbb0f9395627680e5d12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591953"
---
# <a name="ltxmlserializergt-element"></a>Élément &lt;xmlSerializer&gt;
Spécifie si un contrôle supplémentaire de la progression de <xref:System.Xml.Serialization.XmlSerializer> est effectué.  
  
 \<configuration>  
\<system.xml.serialization>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<xmlSerializer checkDeserializerAdvance = "true"|"false" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|**checkDeserializeAdvances**|Spécifie si la progression de <xref:System.Xml.Serialization.XmlSerializer> est vérifiée. Affectez "true" ou "false" à l'attribut. La valeur par défaut est "true".|  
|**useLegacySerializationGeneration**|Spécifie si <xref:System.Xml.Serialization.XmlSerializer> utilise la génération de sérialisation héritée qui génère des assemblys en écrivant le code C# dans un fichier, puis en le compilant dans un assembly. La valeur par défaut est **false**.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<system.xml.serialization>, élément](../../../docs/standard/serialization/system-xml-serialization-element.md)|Contient des paramètres de configuration pour les classes <xref:System.Xml.Serialization.XmlSerializer> et <xref:System.Xml.Serialization.XmlSchemaImporter>.|  
  
## <a name="remarks"></a>Notes  
 Par défaut, le <xref:System.Xml.Serialization.XmlSerializer> fournit une couche supplémentaire de sécurité contre des attaques par déni de service potentielles lors de la désérialisation de données non fiables. Pour ce faire, il tente de détecter des boucles infinies pendant la désérialisation. Si une telle condition est détectée, une exception est levée avec le message suivant : « Erreur interne : Échec de la désérialisation avancer sur le flux sous-jacent. »  
  
 Le fait de recevoir ce message n'indique pas nécessairement qu'une attaque par déni de service est en cours. Dans de rares circonstances, le mécanisme de détection de boucles infinies génère un faux positif et l'exception est levée pour un message entrant légitime. Si vous voyez, dans votre application, que des messages légitimes sont rejetés par cette couche de protection supplémentaire, définissez l’attribut **checkDeserializeAdvances** sur la valeur false.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant assigne la valeur false à l’attribut **checkDeserializeAdvances**.  
  
```xml  
<configuration>  
  <system.xml.serialization>  
    <xmlSerializer checkDeserializeAdvances="false" />  
  </system.xml.serialization>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Xml.Serialization.XmlSerializer>
- [\<system.xml.serialization>, élément](../../../docs/standard/serialization/system-xml-serialization-element.md)
- [Sérialisation XML et SOAP](../../../docs/standard/serialization/xml-and-soap-serialization.md)
