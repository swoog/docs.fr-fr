---
title: '&lt;etwEnable&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- etwEnable element
- <etwEnable> element
ms.assetid: 29dde982-6d8b-4099-8867-ad0d7733f6dc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 788eee71c718c003110ad8242505f2d7868e836c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506925"
---
# <a name="ltetwenablegt-element"></a><span data-ttu-id="ff812-102">&lt;etwEnable&gt; élément</span><span class="sxs-lookup"><span data-stu-id="ff812-102">&lt;etwEnable&gt; Element</span></span>
<span data-ttu-id="ff812-103">Indique s’il faut activer le Suivi d’événements pour Windows (ETW) pour les événements du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="ff812-103">Specifies whether to enable event tracing for Windows (ETW) for common language runtime events.</span></span>  
  
 <span data-ttu-id="ff812-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="ff812-104">\<configuration> Element</span></span>  
<span data-ttu-id="ff812-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="ff812-105">\<runtime> Element</span></span>  
<span data-ttu-id="ff812-106">\<etwEnabled></span><span class="sxs-lookup"><span data-stu-id="ff812-106">\<etwEnabled></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff812-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff812-107">Syntax</span></span>  
  
```xml  
<etwEnable enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ff812-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ff812-108">Attributes and Elements</span></span>  
 <span data-ttu-id="ff812-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ff812-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ff812-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff812-110">Attributes</span></span>  
  
|<span data-ttu-id="ff812-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="ff812-111">Attribute</span></span>|<span data-ttu-id="ff812-112">Description</span><span class="sxs-lookup"><span data-stu-id="ff812-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ff812-113">enabled</span><span class="sxs-lookup"><span data-stu-id="ff812-113">enabled</span></span>|<span data-ttu-id="ff812-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="ff812-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="ff812-115">Spécifie si ETW doit être activée.</span><span class="sxs-lookup"><span data-stu-id="ff812-115">Specifies whether ETW should be enabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="ff812-116">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="ff812-116">enabled Attribute</span></span>  
  
|<span data-ttu-id="ff812-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff812-117">Value</span></span>|<span data-ttu-id="ff812-118">Description</span><span class="sxs-lookup"><span data-stu-id="ff812-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ff812-119">true</span><span class="sxs-lookup"><span data-stu-id="ff812-119">true</span></span>|<span data-ttu-id="ff812-120">Activer ETW.</span><span class="sxs-lookup"><span data-stu-id="ff812-120">Enable ETW.</span></span> <span data-ttu-id="ff812-121">Il s’agit de la valeur par défaut pour les versions d’à partir de Windows avec les systèmes d’exploitation Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ff812-121">This is the default for versions of Windows beginning with the Windows Vista and Windows Server 2008 operating systems.</span></span>|  
|<span data-ttu-id="ff812-122">False</span><span class="sxs-lookup"><span data-stu-id="ff812-122">false</span></span>|<span data-ttu-id="ff812-123">Désactiver ETW.</span><span class="sxs-lookup"><span data-stu-id="ff812-123">Disable ETW.</span></span> <span data-ttu-id="ff812-124">Il s’agit de la valeur par défaut pour les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="ff812-124">This is the default for earlier versions of Windows.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ff812-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff812-125">Child Elements</span></span>  
 <span data-ttu-id="ff812-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ff812-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ff812-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ff812-127">Parent Elements</span></span>  
  
|<span data-ttu-id="ff812-128">Élément</span><span class="sxs-lookup"><span data-stu-id="ff812-128">Element</span></span>|<span data-ttu-id="ff812-129">Description</span><span class="sxs-lookup"><span data-stu-id="ff812-129">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="ff812-130">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff812-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="ff812-131">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="ff812-131">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ff812-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ff812-132">Remarks</span></span>  
 <span data-ttu-id="ff812-133">À compter de Windows Vista, ETW est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ff812-133">Beginning with Windows Vista, ETW is enabled by default.</span></span> <span data-ttu-id="ff812-134">Utilisez cet élément pour désactiver ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="ff812-134">Use this element to disable ETW for an application.</span></span> <span data-ttu-id="ff812-135">Dans les versions antérieures de Windows, utilisez cet élément pour activer ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="ff812-135">In earlier versions of Windows, use this element to enable ETW for an application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ff812-136">ETW peut être activé ou désactivé globalement sur un serveur à l’aide d’un paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="ff812-136">ETW can be enabled or disabled globally on a server by using a registry setting.</span></span> <span data-ttu-id="ff812-137">Consultez [contrôle de l’enregistrement .NET Framework](../../../../../docs/framework/performance/controlling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="ff812-137">See [Controlling .NET Framework Logging](../../../../../docs/framework/performance/controlling-logging.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff812-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff812-138">Example</span></span>  
 <span data-ttu-id="ff812-139">L’exemple suivant montre comment activer le suivi ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="ff812-139">The following example shows how to enable ETW tracing for an application.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <etwEnable enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ff812-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff812-140">See also</span></span>
- [<span data-ttu-id="ff812-141">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="ff812-141">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="ff812-142">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="ff812-142">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="ff812-143">Contrôle de l’enregistrement .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ff812-143">Controlling .NET Framework Logging</span></span>](../../../../../docs/framework/performance/controlling-logging.md)
