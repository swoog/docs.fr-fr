---
title: Élément <gcAllowVeryLargeObjects>
ms.date: 03/30/2017
helpviewer_keywords:
- gcAllowVeryLargeObjects element
- <gcAllowVeryLargeObjects> element
ms.assetid: 5c7ea24a-39ac-4e5f-83b7-b9f9a1b556ab
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2988b054030df23ae8ccd8840f83c239f0401321
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64607260"
---
# <a name="gcallowverylargeobjects-element"></a>\<gcAllowVeryLargeObjects> Element
Sur les plateformes 64 bits, autorise les tableaux dont la taille totale est supérieure à 2 gigaoctets (Go).  
  
 \<configuration > élément  
\<runtime > élément  
\<gcAllowVeryLargeObjects> Element  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<gcAllowVeryLargeObjects    
   enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`enabled`|Attribut requis.<br /><br /> Spécifie si les tableaux qui sont supérieures à 2 Go de taille totale sont activés sur les plateformes 64 bits.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Value|Description|  
|-----------|-----------------|  
|`false`|Supérieure à 2 Go de taille totale des tableaux ne sont pas activés. Il s'agit de la valeur par défaut.|  
|`true`|Supérieure à 2 Go de taille totale des tableaux sont activés sur les plateformes 64 bits.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les options d'initialisation du runtime.|  
  
## <a name="remarks"></a>Notes  
 À l’aide de cet élément dans votre fichier de configuration d’application permet de tableaux supérieurs à 2 Go, mais ne modifie pas les autres limites concernant la taille de l’objet ou de la taille du tableau :  
  
- Le nombre maximal d’éléments dans un tableau est <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.  
  
- L’index maximal dans n’importe quelle dimension unique est 2,147,483,591 (0x7FFFFFC7) pour les tableaux d’octets et des tableaux de structures d’un octet et 2,146,435,071 (0X7FEFFFFF) pour les autres types.  
  
- La taille maximale pour les chaînes et autres objets autres que des tableaux est inchangée.  
  
> [!CAUTION]
>  Avant d’activer cette fonctionnalité, assurez-vous que votre application n’inclut pas le code unsafe qui part du principe que tous les tableaux sont inférieures à 2 Go. Par exemple, le code qui utilise des tableaux de mémoires tampons unsafe peut-être expose à des dépassements de mémoire tampon s’il est écrit sur l’hypothèse que les tableaux ne dépassent pas 2 Go.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment activer cette fonctionnalité pour une application.  
  
```xml  
<configuration>  
  <runtime>  
    <gcAllowVeryLargeObjects enabled="true" />  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
