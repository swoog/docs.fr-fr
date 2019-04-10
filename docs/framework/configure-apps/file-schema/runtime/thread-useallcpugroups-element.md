---
title: <Thread_UseAllCpuGroups>, élément
ms.date: 03/30/2017
ms.assetid: d30fe7c5-8469-46e2-b804-e3eec7b24256
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 236953cc1a430a1dd2a2fbb633c7ef06e6ba200f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59230835"
---
# <a name="threaduseallcpugroups-element"></a><span data-ttu-id="ed12e-102">\<Thread_UseAllCpuGroups > élément</span><span class="sxs-lookup"><span data-stu-id="ed12e-102">\<Thread_UseAllCpuGroups> Element</span></span>
<span data-ttu-id="ed12e-103">Indique si le runtime distribue les threads managés entre tous les groupes de processeurs.</span><span class="sxs-lookup"><span data-stu-id="ed12e-103">Specifies whether the runtime distributes managed threads across all CPU groups.</span></span>  
  
 <span data-ttu-id="ed12e-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ed12e-104">\<configuration></span></span>  
<span data-ttu-id="ed12e-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="ed12e-105">\<runtime></span></span>  
<span data-ttu-id="ed12e-106"><Thread_UseAllCpuGroups></span><span class="sxs-lookup"><span data-stu-id="ed12e-106"><Thread_UseAllCpuGroups></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed12e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed12e-107">Syntax</span></span>  
  
```xml
<Thread_UseAllCpuGroups    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ed12e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ed12e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="ed12e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ed12e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ed12e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="ed12e-110">Attributes</span></span>  
  
|<span data-ttu-id="ed12e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="ed12e-111">Attribute</span></span>|<span data-ttu-id="ed12e-112">Description</span><span class="sxs-lookup"><span data-stu-id="ed12e-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="ed12e-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="ed12e-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="ed12e-114">Indique si le runtime distribue les threads managés entre tous les groupes de processeurs.</span><span class="sxs-lookup"><span data-stu-id="ed12e-114">Specifies whether the runtime distributes managed threads across all CPU groups.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="ed12e-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="ed12e-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="ed12e-116">Value</span><span class="sxs-lookup"><span data-stu-id="ed12e-116">Value</span></span>|<span data-ttu-id="ed12e-117">Description</span><span class="sxs-lookup"><span data-stu-id="ed12e-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="ed12e-118">Le runtime ne distribue pas les threads managés entre plusieurs groupes d’UC.</span><span class="sxs-lookup"><span data-stu-id="ed12e-118">The runtime does not distribute managed threads across multiple CPU groups.</span></span> <span data-ttu-id="ed12e-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed12e-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="ed12e-120">Le runtime distribue les threads managés entre plusieurs groupes d’UC, si l’ordinateur dispose de plusieurs groupes d’UC et le [ \<GCCpuGroup >](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) élément est activé.</span><span class="sxs-lookup"><span data-stu-id="ed12e-120">The runtime distributes managed threads across multiple CPU groups, if the computer has multiple CPU groups and the [\<GCCpuGroup>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) element is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ed12e-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ed12e-121">Child Elements</span></span>  
 <span data-ttu-id="ed12e-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ed12e-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ed12e-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ed12e-123">Parent Elements</span></span>  
  
|<span data-ttu-id="ed12e-124">Élément</span><span class="sxs-lookup"><span data-stu-id="ed12e-124">Element</span></span>|<span data-ttu-id="ed12e-125">Description</span><span class="sxs-lookup"><span data-stu-id="ed12e-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="ed12e-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ed12e-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="ed12e-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="ed12e-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ed12e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="ed12e-128">Remarks</span></span>  
 <span data-ttu-id="ed12e-129">Lorsqu’un ordinateur a plusieurs groupes d’UC, l’activation de cet élément, le runtime répartir les threads managés entre tous les groupes d’UC.</span><span class="sxs-lookup"><span data-stu-id="ed12e-129">When a computer has multiple CPU groups, enabling this element causes the runtime to distribute managed threads across all CPU groups.</span></span> <span data-ttu-id="ed12e-130">Pour utiliser cette fonctionnalité, vous devez également activer le [ \<GCCpuGroup >](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) élément, qui étend le garbage collection pour tous les groupes d’UC et tous les cœurs ne prend en compte lors de la création et l’équilibrage des segments de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ed12e-130">To use this feature, you must also enable the [\<GCCpuGroup>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) element, which extends garbage collection to all CPU groups and takes all cores into account when creating and balancing heaps.</span></span> <span data-ttu-id="ed12e-131">L’activation de la [ \<GCCpuGroup >](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) élément requiert l’activation de la [ \<< gcServer >](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="ed12e-131">Enabling the [\<GCCpuGroup>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) element requires enabling the [\<gcServer>](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) element.</span></span> <span data-ttu-id="ed12e-132">Si ces éléments ne sont pas activées, l’activation de la `<Thread_UseAllCpuGroups>` élément n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="ed12e-132">If these elements are not enabled, enabling the `<Thread_UseAllCpuGroups>` element has no effect.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed12e-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed12e-133">Example</span></span>  
 <span data-ttu-id="ed12e-134">L’exemple suivant montre comment activer la prise en charge de plusieurs groupes d’UC.</span><span class="sxs-lookup"><span data-stu-id="ed12e-134">The following example shows how to enable support for multiple CPU groups.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <Thread_UseAllCpuGroups enabled="true"/>  
      <GCCpuGroup enabled="true"/>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ed12e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed12e-135">See also</span></span>

- [<span data-ttu-id="ed12e-136">Schéma des paramètres d'exécution</span><span class="sxs-lookup"><span data-stu-id="ed12e-136">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="ed12e-137">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="ed12e-137">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="ed12e-138">\<GCCpuGroup > élément</span><span class="sxs-lookup"><span data-stu-id="ed12e-138">\<GCCpuGroup> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md)
