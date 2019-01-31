---
title: Élément <disableCommitThreadStack>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/disableCommitThreadStack
- http://schemas.microsoft.com/.NetConfiguration/v2.0#disableCommitThreadStack
helpviewer_keywords:
- <disableCommitThreadStack> element
- disableCommitThreadStack element
ms.assetid: 3559d46a-7640-4c72-9a11-7e980768929e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5071b2c23b25d6368c84582b76c1f8d18e2a3dff
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257511"
---
# <a name="disablecommitthreadstack-element"></a>\<disableCommitThreadStack> Element
Spécifie si la pile des threads complète est validée quand un thread est démarré.  
  
 \<configuration>  
\<runtime>  
\<disableCommitThreadStack>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<disableCommitThreadStack enabled="0|1"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|enabled|Attribut requis.<br /><br /> Spécifie si la validation de la pile des threads complète lors du démarrage de thread (comportement par défaut) est désactivée.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Valeur|Description|  
|-----------|-----------------|  
|0|Ne pas désactiver le comportement par défaut du Common Language Runtime, qui consiste à valider la pile des threads complète quand un thread est démarré.|  
|1|Désactiver le comportement par défaut du Common Language Runtime, qui consiste à valider la pile des threads complète quand un thread est démarré.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] .|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 Le comportement par défaut du Common Language Runtime consiste à valider la pile des threads complète quand un thread est démarré. Si un grand nombre de threads doivent être créés sur un serveur disposant d’une mémoire limitée, et que la plupart de ces threads utilisent très peu d’espace de pile, les performances du serveur peuvent être améliorées si le Common Language Runtime ne valide pas la pile des threads complète immédiatement quand un thread est démarré.  
  
> [!NOTE]
>  Les hôtes non managés peuvent utiliser l’indicateur de démarrage `STARTUP_DISABLE_COMMITTHREADSTACK` dans l’énumération [STARTUP_FLAGS](../../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) pour obtenir le même résultat.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment désactiver le comportement par défaut du Common Language Runtime, qui consiste à valider la pile des threads complète lors du démarrage d’un thread.  
  
```xml  
<configuration>  
   <runtime>  
      <disableCommitThreadStack enabled="1" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi
- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
