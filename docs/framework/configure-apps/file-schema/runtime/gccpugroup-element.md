---
title: '&lt;GCCpuGroup&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- GCCpuGroup element
- <GCCpuGroup> element
ms.assetid: c1fc7d6c-7220-475c-a312-5b8b201f66e0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d4461667bdb47d410c857b4ac2c9dd268438a02f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltgccpugroupgt-element"></a><span data-ttu-id="abcb1-102">&lt;GCCpuGroup&gt; élément</span><span class="sxs-lookup"><span data-stu-id="abcb1-102">&lt;GCCpuGroup&gt; Element</span></span>
<span data-ttu-id="abcb1-103">Indique si le garbage collection prend en charge plusieurs groupes de processeurs.</span><span class="sxs-lookup"><span data-stu-id="abcb1-103">Specifies whether garbage collection supports multiple CPU groups.</span></span>  
  
 <span data-ttu-id="abcb1-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="abcb1-104">\<configuration></span></span>  
<span data-ttu-id="abcb1-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="abcb1-105">\<runtime></span></span>  
<span data-ttu-id="abcb1-106">\<GCCpuGroup></span><span class="sxs-lookup"><span data-stu-id="abcb1-106">\<GCCpuGroup></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abcb1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abcb1-107">Syntax</span></span>  
  
```xml  
<GCCpuGroup    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="abcb1-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="abcb1-108">Attributes and Elements</span></span>  
 <span data-ttu-id="abcb1-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="abcb1-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="abcb1-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="abcb1-110">Attributes</span></span>  
  
|<span data-ttu-id="abcb1-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="abcb1-111">Attribute</span></span>|<span data-ttu-id="abcb1-112">Description</span><span class="sxs-lookup"><span data-stu-id="abcb1-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="abcb1-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="abcb1-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="abcb1-114">Indique si le garbage collection prend en charge plusieurs groupes de processeurs.</span><span class="sxs-lookup"><span data-stu-id="abcb1-114">Specifies whether garbage collection supports multiple CPU groups.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="abcb1-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="abcb1-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="abcb1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="abcb1-116">Value</span></span>|<span data-ttu-id="abcb1-117">Description</span><span class="sxs-lookup"><span data-stu-id="abcb1-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="abcb1-118">Le garbage collection ne prend pas en charge plusieurs groupes de l’UC.</span><span class="sxs-lookup"><span data-stu-id="abcb1-118">Garbage collection does not support multiple CPU groups.</span></span> <span data-ttu-id="abcb1-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="abcb1-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="abcb1-120">Le garbage collection prend en charge plusieurs groupes de l’UC, si le garbage collection côté serveur est activé.</span><span class="sxs-lookup"><span data-stu-id="abcb1-120">Garbage collection supports multiple CPU groups, if server garbage collection is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="abcb1-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="abcb1-121">Child Elements</span></span>  
 <span data-ttu-id="abcb1-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="abcb1-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="abcb1-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="abcb1-123">Parent Elements</span></span>  
  
|<span data-ttu-id="abcb1-124">Élément</span><span class="sxs-lookup"><span data-stu-id="abcb1-124">Element</span></span>|<span data-ttu-id="abcb1-125">Description</span><span class="sxs-lookup"><span data-stu-id="abcb1-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="abcb1-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="abcb1-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="abcb1-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="abcb1-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="abcb1-128">Notes</span><span class="sxs-lookup"><span data-stu-id="abcb1-128">Remarks</span></span>  
 <span data-ttu-id="abcb1-129">Quand un ordinateur dispose de plusieurs groupes de l’UC et de garbage collection côté serveur est activé (voir la [ \<gcServer >](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) élément), l’activation de cet élément s’étend le garbage collection dans tous les groupes de l’UC et accepte tous les cœurs dans compte lors de la création et l’équilibrage des segments de mémoire.</span><span class="sxs-lookup"><span data-stu-id="abcb1-129">When a computer has multiple CPU groups and server garbage collection is enabled (see the [\<gcServer>](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) element), enabling this element extends garbage collection across all CPU groups and takes all cores into account when creating and balancing heaps.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="abcb1-130">Cet élément s’applique uniquement aux threads de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="abcb1-130">This element applies only to garbage collection threads.</span></span> <span data-ttu-id="abcb1-131">Pour activer l’exécution pour distribuer des threads de l’utilisateur sur tous les groupes de l’UC, vous devez également activer le [< Thread_UseAllCpuGroups >](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="abcb1-131">To enable the runtime to distribute user threads across all CPU groups, you must also enable the [<Thread_UseAllCpuGroups>](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="abcb1-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="abcb1-132">Example</span></span>  
 <span data-ttu-id="abcb1-133">L’exemple suivant montre comment activer un garbage collection pour les groupes de plusieurs UC.</span><span class="sxs-lookup"><span data-stu-id="abcb1-133">The following example shows how to enable garbage collection for multiple CPU groups.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <GCCpuGroup enabled="true"/>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="abcb1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abcb1-134">See Also</span></span>  
 [<span data-ttu-id="abcb1-135">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="abcb1-135">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="abcb1-136">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="abcb1-136">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="abcb1-137">Comment : désactiver le Garbage Collection simultané</span><span class="sxs-lookup"><span data-stu-id="abcb1-137">How to: Disable Concurrent Garbage Collection</span></span>](http://msdn.microsoft.com/library/ba2c6c67-5778-497c-9fac-5f793b5500c7)  
 [<span data-ttu-id="abcb1-138">Garbage collection de station de travail et de serveur</span><span class="sxs-lookup"><span data-stu-id="abcb1-138">Workstation and server garbage collection</span></span>](../../../../../docs/standard/garbage-collection/fundamentals.md#workstation_and_server_garbage_collection)
