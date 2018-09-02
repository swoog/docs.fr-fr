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
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43416772"
---
# <a name="ltgccpugroupgt-element"></a><span data-ttu-id="4aed3-102">&lt;GCCpuGroup&gt; élément</span><span class="sxs-lookup"><span data-stu-id="4aed3-102">&lt;GCCpuGroup&gt; Element</span></span>
<span data-ttu-id="4aed3-103">Indique si le garbage collection prend en charge plusieurs groupes de processeurs.</span><span class="sxs-lookup"><span data-stu-id="4aed3-103">Specifies whether garbage collection supports multiple CPU groups.</span></span>  
  
 <span data-ttu-id="4aed3-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4aed3-104">\<configuration></span></span>  
<span data-ttu-id="4aed3-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="4aed3-105">\<runtime></span></span>  
<span data-ttu-id="4aed3-106">\<GCCpuGroup></span><span class="sxs-lookup"><span data-stu-id="4aed3-106">\<GCCpuGroup></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4aed3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aed3-107">Syntax</span></span>  
  
```xml  
<GCCpuGroup    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4aed3-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4aed3-108">Attributes and Elements</span></span>  
 <span data-ttu-id="4aed3-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4aed3-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4aed3-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="4aed3-110">Attributes</span></span>  
  
|<span data-ttu-id="4aed3-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="4aed3-111">Attribute</span></span>|<span data-ttu-id="4aed3-112">Description</span><span class="sxs-lookup"><span data-stu-id="4aed3-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="4aed3-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="4aed3-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="4aed3-114">Indique si le garbage collection prend en charge plusieurs groupes de processeurs.</span><span class="sxs-lookup"><span data-stu-id="4aed3-114">Specifies whether garbage collection supports multiple CPU groups.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="4aed3-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="4aed3-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="4aed3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aed3-116">Value</span></span>|<span data-ttu-id="4aed3-117">Description</span><span class="sxs-lookup"><span data-stu-id="4aed3-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="4aed3-118">Le garbage collection ne prend pas en charge plusieurs groupes d’UC.</span><span class="sxs-lookup"><span data-stu-id="4aed3-118">Garbage collection does not support multiple CPU groups.</span></span> <span data-ttu-id="4aed3-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4aed3-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="4aed3-120">Le garbage collection prend en charge plusieurs groupes d’UC, si le garbage collection côté serveur est activé.</span><span class="sxs-lookup"><span data-stu-id="4aed3-120">Garbage collection supports multiple CPU groups, if server garbage collection is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4aed3-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4aed3-121">Child Elements</span></span>  
 <span data-ttu-id="4aed3-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4aed3-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4aed3-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4aed3-123">Parent Elements</span></span>  
  
|<span data-ttu-id="4aed3-124">Élément</span><span class="sxs-lookup"><span data-stu-id="4aed3-124">Element</span></span>|<span data-ttu-id="4aed3-125">Description</span><span class="sxs-lookup"><span data-stu-id="4aed3-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="4aed3-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4aed3-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="4aed3-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="4aed3-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4aed3-128">Notes</span><span class="sxs-lookup"><span data-stu-id="4aed3-128">Remarks</span></span>  
 <span data-ttu-id="4aed3-129">Quand un ordinateur a plusieurs groupes d’UC et de garbage collection côté serveur est activé (voir la [ \<< gcServer >](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) élément), l’activation de cet élément s’étend le garbage collection dans tous les groupes d’UC et prend tous les cœurs dans compte lors de la création et l’équilibrage des segments de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4aed3-129">When a computer has multiple CPU groups and server garbage collection is enabled (see the [\<gcServer>](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) element), enabling this element extends garbage collection across all CPU groups and takes all cores into account when creating and balancing heaps.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4aed3-130">Cet élément s’applique uniquement aux threads de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="4aed3-130">This element applies only to garbage collection threads.</span></span> <span data-ttu-id="4aed3-131">Pour activer le runtime distribuer les threads utilisateur sur tous les groupes d’UC, vous devez également activer le [< Thread_UseAllCpuGroups >](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="4aed3-131">To enable the runtime to distribute user threads across all CPU groups, you must also enable the [<Thread_UseAllCpuGroups>](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4aed3-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="4aed3-132">Example</span></span>  
 <span data-ttu-id="4aed3-133">L’exemple suivant montre comment activer le garbage collection pour plusieurs groupes d’UC.</span><span class="sxs-lookup"><span data-stu-id="4aed3-133">The following example shows how to enable garbage collection for multiple CPU groups.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <GCCpuGroup enabled="true"/>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4aed3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aed3-134">See Also</span></span>  
 [<span data-ttu-id="4aed3-135">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="4aed3-135">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="4aed3-136">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="4aed3-136">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="4aed3-137">Comment : désactiver le Garbage Collection simultané</span><span class="sxs-lookup"><span data-stu-id="4aed3-137">How to: Disable Concurrent Garbage Collection</span></span>](https://msdn.microsoft.com/library/ba2c6c67-5778-497c-9fac-5f793b5500c7)  
 [<span data-ttu-id="4aed3-138">Garbage collection de station de travail et serveur</span><span class="sxs-lookup"><span data-stu-id="4aed3-138">Workstation and server garbage collection</span></span>](../../../../../docs/standard/garbage-collection/fundamentals.md#workstation_and_server_garbage_collection)
