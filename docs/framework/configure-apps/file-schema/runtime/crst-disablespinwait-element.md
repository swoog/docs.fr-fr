---
title: élément de < Crst_DisableSpinWait >
ms.date: 04/18/2019
f1_keywords:
- Crst_DisableSpinWait
helpviewer_keywords:
- Crst_DisableSpinWait element
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f89f0558c11e229fef2ca3cd619e3c033f12c858
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64754673"
---
# <a name="crstdisablespinwait-element"></a>\<Crst_DisableSpinWait > élément

Spécifie s’il faut désactiver l’attente de spins pour une section critique lors de conflits.  
  
 \<configuration>  
\<runtime>  
\<Crst_DisableSpinWait>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<Crst_DisableSpinWait enabled="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|**enabled**|Spécifie si l’attente de spins pour les sections critiques lorsqu’ils sont de conflits est désactivé.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Value|Description|  
|-----------|-----------------|  
|1|Désactiver l’attente de toupie (spin) lorsqu’une section critique ne peut pas être acquis.|  
|0|Ne désactivez pas l’attente de spins lorsqu’une section critique ne peut pas être acquis. Valeur par défaut.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les différents paramètres de configuration du runtime.|  
  
## <a name="example"></a>Exemple  

L’exemple suivant désactive toupie (spin) en attente dans des sections critiques de conflits.  
  
```xml  
<configuration>  
   <runtime>  
      <Crst_DisableSpinWait enabled="1"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
