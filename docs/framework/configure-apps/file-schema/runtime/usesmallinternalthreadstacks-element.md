---
title: <UseSmallInternalThreadStacks> Élément
ms.date: 03/30/2017
helpviewer_keywords:
- UseSmallInternalThreadStacks element
- <UseSmallInternalThreadStacks> element
ms.assetid: 1e3f6ec0-1cac-4e1c-9c81-17d948ae5874
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b9833d768b84faaf6e1dcf8c9cb8b00b92adc3d1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59144821"
---
# <a name="usesmallinternalthreadstacks-element"></a><span data-ttu-id="19756-102">\<UseSmallInternalThreadStacks > élément</span><span class="sxs-lookup"><span data-stu-id="19756-102">\<UseSmallInternalThreadStacks> Element</span></span>
<span data-ttu-id="19756-103">Les demandes que le common language runtime (CLR) réduire la mémoire utilisent en spécifiant des tailles de pile explicites lorsqu’il crée certains threads qu’il utilise en interne, au lieu d’utiliser la taille de pile par défaut pour ces threads.</span><span class="sxs-lookup"><span data-stu-id="19756-103">Requests that the common language runtime (CLR) reduce memory use by specifying explicit stack sizes when it creates certain threads that it uses internally, instead of using the default stack size for those threads.</span></span>  
  
 <span data-ttu-id="19756-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="19756-104">\<configuration> Element</span></span>  
<span data-ttu-id="19756-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="19756-105">\<runtime> Element</span></span>  
<span data-ttu-id="19756-106">\<UseSmallInternalThreadStacks > élément</span><span class="sxs-lookup"><span data-stu-id="19756-106">\<UseSmallInternalThreadStacks> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19756-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19756-107">Syntax</span></span>  
  
```xml  
<UseSmallInternalThreadStacks enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="19756-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="19756-108">Attributes and Elements</span></span>  
 <span data-ttu-id="19756-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="19756-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="19756-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="19756-110">Attributes</span></span>  
  
|<span data-ttu-id="19756-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="19756-111">Attribute</span></span>|<span data-ttu-id="19756-112">Description</span><span class="sxs-lookup"><span data-stu-id="19756-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="19756-113">enabled</span><span class="sxs-lookup"><span data-stu-id="19756-113">enabled</span></span>|<span data-ttu-id="19756-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="19756-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="19756-115">Spécifie s’il faut demander que les tailles de pile explicites d’utilisation CLR au lieu de la taille de pile par défaut lorsqu’il crée certains threads qu’il utilise en interne.</span><span class="sxs-lookup"><span data-stu-id="19756-115">Specifies whether to request that the CLR use explicit stack sizes instead of the default stack size when it creates certain threads that it uses internally.</span></span> <span data-ttu-id="19756-116">Les tailles de pile explicites sont inférieures à la taille de pile par défaut de 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="19756-116">The explicit stack sizes are smaller than the default stack size of 1 MB.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="19756-117">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="19756-117">enabled Attribute</span></span>  
  
|<span data-ttu-id="19756-118">Value</span><span class="sxs-lookup"><span data-stu-id="19756-118">Value</span></span>|<span data-ttu-id="19756-119">Description</span><span class="sxs-lookup"><span data-stu-id="19756-119">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="19756-120">true</span><span class="sxs-lookup"><span data-stu-id="19756-120">true</span></span>|<span data-ttu-id="19756-121">Demander des tailles de pile explicites.</span><span class="sxs-lookup"><span data-stu-id="19756-121">Request explicit stack sizes.</span></span>|  
|<span data-ttu-id="19756-122">False</span><span class="sxs-lookup"><span data-stu-id="19756-122">false</span></span>|<span data-ttu-id="19756-123">Utiliser la taille de pile par défaut.</span><span class="sxs-lookup"><span data-stu-id="19756-123">Use the default stack size.</span></span> <span data-ttu-id="19756-124">Il s’agit par défaut pour le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="19756-124">This is the default for the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="19756-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="19756-125">Child Elements</span></span>  
 <span data-ttu-id="19756-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="19756-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="19756-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="19756-127">Parent Elements</span></span>  
  
|<span data-ttu-id="19756-128">Élément</span><span class="sxs-lookup"><span data-stu-id="19756-128">Element</span></span>|<span data-ttu-id="19756-129">Description</span><span class="sxs-lookup"><span data-stu-id="19756-129">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="19756-130">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="19756-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="19756-131">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="19756-131">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="19756-132">Notes</span><span class="sxs-lookup"><span data-stu-id="19756-132">Remarks</span></span>  
 <span data-ttu-id="19756-133">Cet élément de configuration est utilisé pour demander l’utilisation réduite de la mémoire virtuelle dans un processus, étant donné que les tailles de thread explicites que le CLR utilise pour ses threads internes, si la demande est honorée, sont plus petites que la taille par défaut.</span><span class="sxs-lookup"><span data-stu-id="19756-133">This configuration element is used to request reduced virtual memory use in a process, because the explicit thread sizes that the CLR uses for its internal threads, if the request is honored, are smaller than the default size.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="19756-134">Cet élément de configuration est une demande au CLR plutôt qu’une exigence absolue.</span><span class="sxs-lookup"><span data-stu-id="19756-134">This configuration element is a request to the CLR rather than an absolute requirement.</span></span> <span data-ttu-id="19756-135">Dans le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], la demande est honorée uniquement pour le x86 architecture.</span><span class="sxs-lookup"><span data-stu-id="19756-135">In the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], the request is honored only for the x86 architecture.</span></span> <span data-ttu-id="19756-136">Cet élément peut complètement ignoré dans les futures versions du CLR ou remplacé par des tailles de pile explicites qui sont toujours utilisés pour les threads internes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="19756-136">This element might be ignored completely in future versions of the CLR, or replaced by explicit stack sizes that are always used for selected internal threads.</span></span>  
  
 <span data-ttu-id="19756-137">Spécification de que cet élément de configuration entretient des relations fiabilité pour une utilisation de mémoire virtuelle plus petits si le CLR répond à la requête, car il est plus petite taille de pile peut augmenter les débordements plus probablement.</span><span class="sxs-lookup"><span data-stu-id="19756-137">Specifying this configuration element trades reliability for smaller virtual memory use if the CLR honors the request, because smaller stack sizes could potentially make stack overflows more likely.</span></span>  
  
## <a name="example"></a><span data-ttu-id="19756-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="19756-138">Example</span></span>  
 <span data-ttu-id="19756-139">L’exemple suivant montre comment demander que la CLR utilisation tailles de pile explicites pour certains threads qu’il utilise en interne.</span><span class="sxs-lookup"><span data-stu-id="19756-139">The following example shows how to request that the CLR use explicit stack sizes for certain threads that it uses internally.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <UseSmallInternalThreadStacks enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="19756-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19756-140">See also</span></span>

- [<span data-ttu-id="19756-141">Schéma des paramètres d'exécution</span><span class="sxs-lookup"><span data-stu-id="19756-141">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="19756-142">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="19756-142">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
