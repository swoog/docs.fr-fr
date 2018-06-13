---
title: '&lt;nameEntry&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#nameEntry
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping/nameEntry
helpviewer_keywords:
- <nameEntry> element
- nameEntry element
ms.assetid: 7d7535e9-4b4a-4b8c-82e2-e40dff5a7821
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 1bffb72e7c68d10e2c0edd5ec3cb9bcff10cbc0a
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32743051"
---
# <a name="ltnameentrygt-element"></a>&lt;nameEntry&gt; élément
Mappe un nom de classe à un nom d’algorithme convivial, ce qui permet à une classe d’avoir plusieurs noms conviviaux.  
  
 \<configuration>  
\<mscorlib >  
\<cryptographySettings >  
\<cryptoNameMapping >  
\<nameEntry >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<nameEntry name="friendly name" Class="class name" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|**name**|Attribut requis.<br /><br /> Spécifie le nom convivial de l’algorithme de la classe de chiffrement implémente.|  
|**class**|Attribut requis.<br /><br /> Spécifie la valeur de la **nom** d’attribut dans le [ \<cryptoClass >](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md) élément.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.web`|Spécifie l'élément racine de la section de configuration ASP.NET.|  
  
## <a name="remarks"></a>Notes  
 Le **nom** attribut peut être le nom de l’une des classes abstraites trouvées dans le <xref:System.Security.Cryptography> espace de noms. Lorsque vous appelez le **créer** méthode sur une classe de chiffrement abstraite, le nom de la classe abstraite est passé à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A> (méthode). **CreateFromName** retourne une instance du type indiqué par la **classe** attribut. Si le **nom** attribut est un nom court, tels que RSA, vous pouvez utiliser ce nom lorsque vous appelez le **CreateFromName** (méthode).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le  **\<nameEntry >** élément pour référencer une classe de chiffrement et configurer le runtime. Vous pouvez ensuite passer la chaîne « RSA » pour le <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> méthode et l’utilisation du <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> méthode pour retourner un `MyCryptoRSAClass` objet.  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCryptoRSA="MyCryptoRSAClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RSA" class="MyCryptoRSA"/>  
            <nameEntry name="System.Security.Cryptography.AsymmetricAlgorithm"  
                       class="MyCryptoRSA"/>  
         </cryptoNameMapping>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [Schéma des paramètres de chiffrement](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [Services de chiffrement](../../../../../docs/standard/security/cryptographic-services.md)  
 [Configuration des classes de chiffrement](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
