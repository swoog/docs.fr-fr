---
title: '&lt;GCCpuGroup&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- GCCpuGroup element
- <GCCpuGroup> element
ms.assetid: c1fc7d6c-7220-475c-a312-5b8b201f66e0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 21ab18cded2b9a16fe2520547287198d3cfe6b74
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43529309"
---
# <a name="ltgccpugroupgt-element"></a>&lt;GCCpuGroup&gt; élément
Indique si le garbage collection prend en charge plusieurs groupes de processeurs.  
  
 \<configuration>  
\<runtime>  
\<GCCpuGroup>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<GCCpuGroup    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`enabled`|Attribut requis.<br /><br /> Indique si le garbage collection prend en charge plusieurs groupes de processeurs.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Valeur|Description|  
|-----------|-----------------|  
|`false`|Le garbage collection ne prend pas en charge plusieurs groupes d’UC. Il s'agit de la valeur par défaut.|  
|`true`|Le garbage collection prend en charge plusieurs groupes d’UC, si le garbage collection côté serveur est activé.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 Quand un ordinateur a plusieurs groupes d’UC et de garbage collection côté serveur est activé (voir la [ \<< gcServer >](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) élément), l’activation de cet élément s’étend le garbage collection dans tous les groupes d’UC et prend tous les cœurs dans compte lors de la création et l’équilibrage des segments de mémoire.  
  
> [!NOTE]
>  Cet élément s’applique uniquement aux threads de garbage collection. Pour activer le runtime distribuer les threads utilisateur sur tous les groupes d’UC, vous devez également activer le [< Thread_UseAllCpuGroups >](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) élément.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment activer le garbage collection pour plusieurs groupes d’UC.  
  
```xml  
<configuration>  
   <runtime>  
      <GCCpuGroup enabled="true"/>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [Comment : désactiver le Garbage Collection simultané](https://msdn.microsoft.com/library/ba2c6c67-5778-497c-9fac-5f793b5500c7)  
 [Garbage collection de station de travail et serveur](../../../../../docs/standard/garbage-collection/fundamentals.md#workstation_and_server_garbage_collection)
