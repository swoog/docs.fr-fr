---
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: 9bc519509b00383be333ac605688950d2709117c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153135"
---
# <a name="xmldictionaryreaderquotas"></a>XmlDictionaryReaderQuotas
XmlDictionaryReaderQuotas  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class XmlDictionaryReaderQuotas  
{  
  sint32 MaxArrayLength;  
  sint32 MaxBytesPerRead;  
  sint32 MaxDepth;  
  sint32 MaxNameTableCharCount;  
  sint32 MaxStringContentLength;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe XmlDictionaryReaderQuotas ne définit aucune méthode.  
  
## <a name="properties"></a>Properties  
 La classe XmlDictionaryReaderQuotas a les propriétés suivantes :  
  
### <a name="maxarraylength"></a>MaxArrayLength  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 La longueur de tableau maximale autorisée.  
  
### <a name="maxbytesperread"></a>MaxBytesPerRead  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Le nombre maximal d'octets autorisés retournés pour chaque lecture.  
  
### <a name="maxdepth"></a>MaxDepth  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Profondeur maximale de nœud imbriqué par lecture.  
  
### <a name="maxnametablecharcount"></a>MaxNameTableCharCount  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Le nombre maximal de caractères autorisés dans un nom de table.  
  
### <a name="maxstringcontentlength"></a>MaxStringContentLength  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de caractères autorisés dans un contenu d'élément XML.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.XmlDictionaryReaderQuotas>  
 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
