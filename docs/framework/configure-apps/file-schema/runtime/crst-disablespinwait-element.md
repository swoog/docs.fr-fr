---
title: élément de < Crst_DisableSpinWait >
ms.date: 04/18/2019
f1_keywords:
- Crst_DisableSpinWait
helpviewer_keywords:
- Crst_DisableSpinWait element
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6cde26250db0b3d11c51a18b7ebd378953ae0958
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59981253"
---
# <a name="crstdisablespinwait-element"></a>\<Crst_DisableSpinWait > élément

Spécifie s’il faut désactiver l’attente de spins pour une section critique lors de conflits. \ 
  
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
|**enabled**|Spécifie si la rotation-en attente pour les sections critiques est activée quand ils sont de conflits.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Value|Description|  
|-----------|-----------------|  
|1|Attente de spins est activé.|  
|0|Attente de spins est désactivé. Ceci est la valeur par défaut|  
  
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
