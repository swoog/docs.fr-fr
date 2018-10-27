---
title: '&lt;cryptographySettings&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 4bad1d15bc8e2fd40d42581220888f035e515162
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181379"
---
# <a name="ltcryptographysettingsgt-element"></a>&lt;cryptographySettings&gt; élément
Contient des paramètres de chiffrement.  
  
 \<configuration>  
\<mscorlib >  
\<cryptographySettings >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
      <cryptographySettings>   
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<cryptoNameMapping >](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|Contient des mappages de classes à des noms conviviaux.|  
|[\<oidMap >](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|Contient des mappages d’identificateur (OID) d’objet ASN.1 aux classes.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`mscorlib`|Contient le `cryptographySettings` élément.|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le  **\<cryptographySettings >** élément qui contient les mappages des noms de chiffrement et les mappages d’OID. Cet exemple configure l’exécution afin que <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> retourne un `MyHashClass` objet et le `MyCryptoClass` classe correspond à l’OID 1.3.36.2.1.  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [Schéma des paramètres de chiffrement](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
- [Cryptographic Services](../../../../../docs/standard/security/cryptographic-services.md)
