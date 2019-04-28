---
title: Élément <legacyCorruptedStateExceptionsPolicy>
ms.date: 03/30/2017
helpviewer_keywords:
- <legacyCorruptedStateExceptionsPolicy> element
- legacyCorruptedStateExceptionsPolicy element
ms.assetid: e0a55ddc-bfa8-4f3e-ac14-d1fc3330e4bb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 777d496614435106b84b47b9aa3d35d964bc3e07
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704737"
---
# <a name="legacycorruptedstateexceptionspolicy-element"></a><span data-ttu-id="5dce4-102">\<legacyCorruptedStateExceptionsPolicy> Element</span><span class="sxs-lookup"><span data-stu-id="5dce4-102">\<legacyCorruptedStateExceptionsPolicy> Element</span></span>
<span data-ttu-id="5dce4-103">Spécifie si le common language runtime permet au code managé d’intercepter les violations d’accès et d’autres exceptions d’état endommagé.</span><span class="sxs-lookup"><span data-stu-id="5dce4-103">Specifies whether the common language runtime allows managed code to catch access violations and other corrupted state exceptions.</span></span>  
  
 <span data-ttu-id="5dce4-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5dce4-104">\<configuration></span></span>  
<span data-ttu-id="5dce4-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="5dce4-105">\<runtime></span></span>  
<span data-ttu-id="5dce4-106">\<legacyCorruptedStateExceptionsPolicy></span><span class="sxs-lookup"><span data-stu-id="5dce4-106">\<legacyCorruptedStateExceptionsPolicy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5dce4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dce4-107">Syntax</span></span>  
  
```xml  
<legacyCorruptedStateExceptionsPolicy enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5dce4-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5dce4-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5dce4-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5dce4-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5dce4-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="5dce4-110">Attributes</span></span>  
  
|<span data-ttu-id="5dce4-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="5dce4-111">Attribute</span></span>|<span data-ttu-id="5dce4-112">Description</span><span class="sxs-lookup"><span data-stu-id="5dce4-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="5dce4-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="5dce4-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="5dce4-114">Spécifie que l’application interceptera endommager des échecs d’état d’exception telles que des violations d’accès.</span><span class="sxs-lookup"><span data-stu-id="5dce4-114">Specifies that the application will catch corrupting state exception failures such as access violations.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="5dce4-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="5dce4-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="5dce4-116">Value</span><span class="sxs-lookup"><span data-stu-id="5dce4-116">Value</span></span>|<span data-ttu-id="5dce4-117">Description</span><span class="sxs-lookup"><span data-stu-id="5dce4-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="5dce4-118">L’application n’intercepte pas endommager les échecs d’état d’exception telles que des violations d’accès.</span><span class="sxs-lookup"><span data-stu-id="5dce4-118">The application will not catch corrupting state exception failures such as access violations.</span></span> <span data-ttu-id="5dce4-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dce4-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="5dce4-120">L’application interceptera endommager des échecs d’état d’exception telles que des violations d’accès.</span><span class="sxs-lookup"><span data-stu-id="5dce4-120">The application will catch corrupting state exception failures such as access violations.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5dce4-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5dce4-121">Child Elements</span></span>  
 <span data-ttu-id="5dce4-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5dce4-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5dce4-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5dce4-123">Parent Elements</span></span>  
  
|<span data-ttu-id="5dce4-124">Élément</span><span class="sxs-lookup"><span data-stu-id="5dce4-124">Element</span></span>|<span data-ttu-id="5dce4-125">Description</span><span class="sxs-lookup"><span data-stu-id="5dce4-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="5dce4-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5dce4-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="5dce4-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="5dce4-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5dce4-128">Notes</span><span class="sxs-lookup"><span data-stu-id="5dce4-128">Remarks</span></span>  
 <span data-ttu-id="5dce4-129">Dans le .NET Framework version 3.5 et versions antérieure, le common language runtime autorise le code managé intercepter les exceptions qui ont été générées par les États de processus endommagé.</span><span class="sxs-lookup"><span data-stu-id="5dce4-129">In the .NET Framework version 3.5 and earlier, the common language runtime allowed managed code to catch exceptions that were raised by corrupted process states.</span></span> <span data-ttu-id="5dce4-130">Une violation d’accès est un exemple de ce type d’exception.</span><span class="sxs-lookup"><span data-stu-id="5dce4-130">An access violation is an example of this type of exception.</span></span>  
  
 <span data-ttu-id="5dce4-131">En commençant par le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)]managé code n’intercepte plus ces types d’exceptions dans `catch` blocs.</span><span class="sxs-lookup"><span data-stu-id="5dce4-131">Starting with the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], managed code no longer catches these types of exceptions in `catch` blocks.</span></span> <span data-ttu-id="5dce4-132">Toutefois, vous pouvez remplacer cette modification et maintenir la gestion des exceptions d’état endommagé de deux manières :</span><span class="sxs-lookup"><span data-stu-id="5dce4-132">However, you can override this change and maintain the handling of corrupted state exceptions in two ways:</span></span>  
  
- <span data-ttu-id="5dce4-133">Définir le `<legacyCorruptedStateExceptionsPolicy>` l’élément `enabled` attribut `true`.</span><span class="sxs-lookup"><span data-stu-id="5dce4-133">Set the `<legacyCorruptedStateExceptionsPolicy>` element's `enabled` attribute to `true`.</span></span> <span data-ttu-id="5dce4-134">Ce paramètre de configuration est appliquée au niveau du processus et affecte toutes les méthodes.</span><span class="sxs-lookup"><span data-stu-id="5dce4-134">This configuration setting is applied processwide and affects all methods.</span></span>  
  
 <span data-ttu-id="5dce4-135">- ou -</span><span class="sxs-lookup"><span data-stu-id="5dce4-135">-or-</span></span>  
  
- <span data-ttu-id="5dce4-136">Appliquer le <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=nameWithType> d’attribut à la méthode qui contient les exceptions `catch` bloc.</span><span class="sxs-lookup"><span data-stu-id="5dce4-136">Apply the <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=nameWithType> attribute to the method that contains the exceptions `catch` block.</span></span>  
  
 <span data-ttu-id="5dce4-137">Cet élément de configuration est disponible uniquement dans le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5dce4-137">This configuration element is available only in the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5dce4-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dce4-138">Example</span></span>  
 <span data-ttu-id="5dce4-139">L’exemple suivant montre comment spécifier que l’application doit rétablir le comportement avant le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]et intercepter des échecs d’exception altérer tout état.</span><span class="sxs-lookup"><span data-stu-id="5dce4-139">The following example shows how to specify that the application should revert to the behavior before the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], and catch all corrupting state exception failures.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <legacyCorruptedStateExceptionsPolicy enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5dce4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dce4-140">See also</span></span>

- <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute>
- [<span data-ttu-id="5dce4-141">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="5dce4-141">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="5dce4-142">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="5dce4-142">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
