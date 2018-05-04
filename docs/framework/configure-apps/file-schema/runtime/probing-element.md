---
title: '&lt;détection&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/probing
- http://schemas.microsoft.com/.NetConfiguration/v2.0#probing
helpviewer_keywords:
- <probing> element
- container tags, <probing> element
- probing element
ms.assetid: 09c80fc9-1ba5-4192-89f7-3a79b2e4b024
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8cab16e83466b5954bfebac07dd79c9a8b5e4594
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltprobinggt-element"></a>&lt;détection&gt; élément
Spécifie les sous-répertoires de base d’application pour le common language runtime à rechercher lors du chargement d’assemblys.  
  
 \<configuration>  
\<runtime>  
\<assemblyBinding >  
\<probing >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<probing privatePath="paths"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`privatePath`|Attribut requis.<br /><br /> Spécifie les sous-répertoires du répertoire de base de l’application contenant des assemblys. Délimiter chaque sous-répertoire par un point-virgule.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`assemblyBinding`|Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier les sous-répertoires base que le runtime doit rechercher les assemblys de l’application.  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <probing privatePath="bin;bin2\subbin;bin3"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [Spécification de l'emplacement d'un assembly](../../../../../docs/framework/configure-apps/specify-assembly-location.md)  
 [Méthode de localisation des assemblys par le runtime](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
