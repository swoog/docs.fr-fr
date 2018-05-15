---
title: '&lt;etwEnable&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- etwEnable element
- <etwEnable> element
ms.assetid: 29dde982-6d8b-4099-8867-ad0d7733f6dc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 267a4a29282881d18201d0cb2062e91b4ff974a9
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltetwenablegt-element"></a><span data-ttu-id="883fd-102">&lt;etwEnable&gt; élément</span><span class="sxs-lookup"><span data-stu-id="883fd-102">&lt;etwEnable&gt; Element</span></span>
<span data-ttu-id="883fd-103">Indique s’il faut activer le Suivi d’événements pour Windows (ETW) pour les événements du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="883fd-103">Specifies whether to enable event tracing for Windows (ETW) for common language runtime events.</span></span>  
  
 <span data-ttu-id="883fd-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="883fd-104">\<configuration> Element</span></span>  
<span data-ttu-id="883fd-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="883fd-105">\<runtime> Element</span></span>  
<span data-ttu-id="883fd-106">\<etwEnabled ></span><span class="sxs-lookup"><span data-stu-id="883fd-106">\<etwEnabled></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="883fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="883fd-107">Syntax</span></span>  
  
```xml  
<etwEnable enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="883fd-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="883fd-108">Attributes and Elements</span></span>  
 <span data-ttu-id="883fd-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="883fd-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="883fd-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="883fd-110">Attributes</span></span>  
  
|<span data-ttu-id="883fd-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="883fd-111">Attribute</span></span>|<span data-ttu-id="883fd-112">Description</span><span class="sxs-lookup"><span data-stu-id="883fd-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="883fd-113">enabled</span><span class="sxs-lookup"><span data-stu-id="883fd-113">enabled</span></span>|<span data-ttu-id="883fd-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="883fd-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="883fd-115">Spécifie si ETW doit être activé.</span><span class="sxs-lookup"><span data-stu-id="883fd-115">Specifies whether ETW should be enabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="883fd-116">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="883fd-116">enabled Attribute</span></span>  
  
|<span data-ttu-id="883fd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="883fd-117">Value</span></span>|<span data-ttu-id="883fd-118">Description</span><span class="sxs-lookup"><span data-stu-id="883fd-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="883fd-119">true</span><span class="sxs-lookup"><span data-stu-id="883fd-119">true</span></span>|<span data-ttu-id="883fd-120">Activer ETW.</span><span class="sxs-lookup"><span data-stu-id="883fd-120">Enable ETW.</span></span> <span data-ttu-id="883fd-121">Il s’agit de la valeur par défaut pour les versions de Windows qui commence avec les systèmes d’exploitation Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="883fd-121">This is the default for versions of Windows beginning with the Windows Vista and Windows Server 2008 operating systems.</span></span>|  
|<span data-ttu-id="883fd-122">False</span><span class="sxs-lookup"><span data-stu-id="883fd-122">false</span></span>|<span data-ttu-id="883fd-123">Désactiver ETW.</span><span class="sxs-lookup"><span data-stu-id="883fd-123">Disable ETW.</span></span> <span data-ttu-id="883fd-124">Il s’agit de la valeur par défaut pour les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="883fd-124">This is the default for earlier versions of Windows.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="883fd-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="883fd-125">Child Elements</span></span>  
 <span data-ttu-id="883fd-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="883fd-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="883fd-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="883fd-127">Parent Elements</span></span>  
  
|<span data-ttu-id="883fd-128">Élément</span><span class="sxs-lookup"><span data-stu-id="883fd-128">Element</span></span>|<span data-ttu-id="883fd-129">Description</span><span class="sxs-lookup"><span data-stu-id="883fd-129">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="883fd-130">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="883fd-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="883fd-131">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="883fd-131">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="883fd-132">Notes</span><span class="sxs-lookup"><span data-stu-id="883fd-132">Remarks</span></span>  
 <span data-ttu-id="883fd-133">À compter de Windows Vista, ETW est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="883fd-133">Beginning with Windows Vista, ETW is enabled by default.</span></span> <span data-ttu-id="883fd-134">Utilisez cet élément pour désactiver ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="883fd-134">Use this element to disable ETW for an application.</span></span> <span data-ttu-id="883fd-135">Dans les versions antérieures de Windows, utilisez cet élément pour activer ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="883fd-135">In earlier versions of Windows, use this element to enable ETW for an application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="883fd-136">ETW peut être activé ou désactivé globalement sur un serveur à l’aide d’un paramètre du Registre.</span><span class="sxs-lookup"><span data-stu-id="883fd-136">ETW can be enabled or disabled globally on a server by using a registry setting.</span></span> <span data-ttu-id="883fd-137">Consultez [contrôle de l’enregistrement .NET Framework](../../../../../docs/framework/performance/controlling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="883fd-137">See [Controlling .NET Framework Logging](../../../../../docs/framework/performance/controlling-logging.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="883fd-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="883fd-138">Example</span></span>  
 <span data-ttu-id="883fd-139">L’exemple suivant montre comment activer le suivi ETW pour une application.</span><span class="sxs-lookup"><span data-stu-id="883fd-139">The following example shows how to enable ETW tracing for an application.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <etwEnable enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="883fd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="883fd-140">See Also</span></span>  
 [<span data-ttu-id="883fd-141">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="883fd-141">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="883fd-142">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="883fd-142">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="883fd-143">Contrôle de l’enregistrement .NET Framework</span><span class="sxs-lookup"><span data-stu-id="883fd-143">Controlling .NET Framework Logging</span></span>](../../../../../docs/framework/performance/controlling-logging.md)
