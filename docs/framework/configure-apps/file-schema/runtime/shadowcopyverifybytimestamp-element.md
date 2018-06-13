---
title: '&lt;shadowCopyVerifyByTimestamp&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- <shadowCopyTimeStampVerification> element
- shadowCopyTimeStampVerification element
ms.assetid: 2f1648e5-997b-435e-a4f9-d236c574c66c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2439a4812163562a73bd3520e65b9973e666a863
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749723"
---
# <a name="ltshadowcopyverifybytimestampgt-element"></a>&lt;shadowCopyVerifyByTimestamp&gt; élément
Indique si les clichés instantanés utilisent le comportement de démarrage par défaut introduit dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], ou reviennent au comportement de démarrage des versions précédentes du .NET Framework.  
  
 \<configuration > élément  
\<runtime > élément  
\<shadowCopyVerifyByTimestamp > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<shadowCopyVerifyByTimestamp enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|enabled|Attribut requis.<br /><br /> Spécifie si les domaines d’application qui utilisent les clichés instantanés comparer les horodatages des assemblys au démarrage, afin de déterminer si un assembly a été mis à jour avant la création de l’assembly de clichés instantanés.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Valeur|Description|  
|-----------|-----------------|  
|true|Au démarrage, copie uniquement les assemblys qui ont été mis à jour depuis leur dernière copie dans le répertoire des clichés instantanés. Ceci est la valeur par défaut pour le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)].|  
|False|Rétablit le comportement de démarrage des versions antérieures du .NET Framework, qui consiste à copier tous les fichiers au démarrage.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 En commençant par le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], les assemblys sont des clichés instantanés uniquement si leurs horodatages indiquent qu’ils ont été modifiés depuis leur dernière copie dans le répertoire des clichés instantanés. Cela améliore les temps de démarrage pour de nombreuses applications qui utilisent les clichés instantanés, comme décrit dans [clichés instantanés d’assemblys](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md). Les applications disposant d’un pourcentage élevé et la fréquence des mises à jour de l’assembly ne peuvent pas bénéficier de ce changement de comportement. Dans ce cas, vous pouvez utiliser cet élément pour restaurer le comportement des versions antérieures du .NET Framework.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment désactiver le comportement de démarrage par défaut de clichés instantanés dans le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]et de rétablir le comportement au démarrage des versions antérieures du .NET Framework.  
  
```xml  
<configuration>  
   <runtime>  
      <shadowCopyVerifyByTimestamp enabled="false" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [Clichés instantanés d'assemblys](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md)
