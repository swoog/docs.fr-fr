---
title: '&lt;etwEnable&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- etwEnable element
- <etwEnable> element
ms.assetid: 29dde982-6d8b-4099-8867-ad0d7733f6dc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b6ea2f8a32a18dfce6be54ce52ce8fef4abf92ce
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610773"
---
# <a name="ltetwenablegt-element"></a><span data-ttu-id="ac97a-102">&lt;etwEnable&gt; élément</span><span class="sxs-lookup"><span data-stu-id="ac97a-102">&lt;etwEnable&gt; Element</span></span>
<span data-ttu-id="ac97a-103">Indique s’il faut activer le Suivi d’événements pour Windows (ETW) pour les événements du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="ac97a-103">Specifies whether to enable event tracing for Windows (ETW) for common language runtime events.</span></span>  
  
 <span data-ttu-id="ac97a-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="ac97a-104">\<configuration> Element</span></span>  
<span data-ttu-id="ac97a-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="ac97a-105">\<runtime> Element</span></span>  
<span data-ttu-id="ac97a-106">\<etwEnabled ></span><span class="sxs-lookup"><span data-stu-id="ac97a-106">\<etwEnabled></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac97a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac97a-107">Syntax</span></span>  
  
```xml  
<etwEnable enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ac97a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ac97a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="ac97a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ac97a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ac97a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="ac97a-110">Attributes</span></span>  
  
|<span data-ttu-id="ac97a-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="ac97a-111">Attribute</span></span>|<span data-ttu-id="ac97a-112">Description</span><span class="sxs-lookup"><span data-stu-id="ac97a-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ac97a-113">enabled</span><span class="sxs-lookup"><span data-stu-id="ac97a-113">enabled</span></span>|<span data-ttu-id="ac97a-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="ac97a-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="ac97a-115">Spécifie si ETW doit être activée.</span><span class="sxs-lookup"><span data-stu-id="ac97a-115">Specifies whether ETW should be enabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="ac97a-116">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="ac97a-116">enabled Attribute</span></span>  
  
|<span data-ttu-id="ac97a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac97a-117">Value</span></span>|<span data-ttu-id="ac97a-118">Description</span><span class="sxs-lookup"><span data-stu-id="ac97a-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ac97a-119">true</span><span class="sxs-lookup"><span data-stu-id="ac97a-119">true</span></span>|<span data-ttu-id="ac97a-120">Activer ETW.</span><span class="sxs-lookup"><span data-stu-id="ac97a-120">Enable ETW.</span></span> <span data-ttu-id="ac97a-121">Il s’agit de la valeur par défaut pour les versions d’à partir de Windows avec les systèmes d’exploitation Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ac97a-121">This is the default for versions of Windows beginning with the Windows Vista and Windows Server 2008 operating systems.</span></span>|  
|<span data-ttu-id="ac97a-122">False</span><span class="sxs-lookup"><span data-stu-id="ac97a-122">false</span></span>|<span data-ttu-id="ac97a-123">Désactiver ETW.</span><span class="sxs-lookup"><span data-stu-id="ac97a-123">Disable ETW.</span></span> <span data-ttu-id="ac97a-124">Il s’agit de la valeur par défaut pour les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="ac97a-124">This is the default for earlier versions of Windows.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ac97a-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ac97a-125">Child Elements</span></span>  
 <span data-ttu-id="ac97a-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ac97a-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ac97a-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ac97a-127">Parent Elements</span></span>  
  
|<span data-ttu-id="ac97a-128">Élément</span><span class="sxs-lookup"><span data-stu-id="ac97a-128">Element</span></span>|<span data-ttu-id="ac97a-129">Description</span><span class="sxs-lookup"><span data-stu-id="ac97a-129">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="ac97a-130">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ac97a-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="ac97a-131">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="ac97a-131">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac97a-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ac97a-132">Remarks</span></span>  
 <span data-ttu-id="ac97a-133">À compter de Windows Vista, ETW est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ac97a-133">Beginning with Windows Vista, ETW is enabled by default.</span></span> <span data-ttu-id="ac97a-134">Utilisez cet élément pour désactiver ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="ac97a-134">Use this element to disable ETW for an application.</span></span> <span data-ttu-id="ac97a-135">Dans les versions antérieures de Windows, utilisez cet élément pour activer ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="ac97a-135">In earlier versions of Windows, use this element to enable ETW for an application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ac97a-136">ETW peut être activé ou désactivé globalement sur un serveur à l’aide d’un paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="ac97a-136">ETW can be enabled or disabled globally on a server by using a registry setting.</span></span> <span data-ttu-id="ac97a-137">Consultez [contrôle de l’enregistrement .NET Framework](../../../../../docs/framework/performance/controlling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="ac97a-137">See [Controlling .NET Framework Logging](../../../../../docs/framework/performance/controlling-logging.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ac97a-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="ac97a-138">Example</span></span>  
 <span data-ttu-id="ac97a-139">L’exemple suivant montre comment activer le suivi ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="ac97a-139">The following example shows how to enable ETW tracing for an application.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <etwEnable enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ac97a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac97a-140">See Also</span></span>  
- [<span data-ttu-id="ac97a-141">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="ac97a-141">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
- [<span data-ttu-id="ac97a-142">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="ac97a-142">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [<span data-ttu-id="ac97a-143">Contrôle de l’enregistrement .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ac97a-143">Controlling .NET Framework Logging</span></span>](../../../../../docs/framework/performance/controlling-logging.md)
