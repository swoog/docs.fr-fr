---
title: Élément <developmentMode>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/developmentMode
- http://schemas.microsoft.com/.NetConfiguration/v2.0#developmentMode
helpviewer_keywords:
- developmentMode element
- container tags, <developmentMode> element
- <developmentMode> element
ms.assetid: 60e79a8c-415a-497d-be29-b9d0fd9bdee3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fdf840035150f08c894c984213af9a0abe6e95af
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59192054"
---
# <a name="developmentmode-element"></a><span data-ttu-id="fa411-102">\<developmentMode > élément</span><span class="sxs-lookup"><span data-stu-id="fa411-102">\<developmentMode> Element</span></span>
<span data-ttu-id="fa411-103">Indique si le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fa411-103">Specifies whether the runtime searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
 <span data-ttu-id="fa411-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="fa411-104">\<configuration></span></span>  
<span data-ttu-id="fa411-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="fa411-105">\<runtime></span></span>  
<span data-ttu-id="fa411-106">\<developmentMode></span><span class="sxs-lookup"><span data-stu-id="fa411-106">\<developmentMode></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa411-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa411-107">Syntax</span></span>  
  
```xml  
<developmentMode developerInstallation="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fa411-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fa411-108">Attributes and Elements</span></span>  
 <span data-ttu-id="fa411-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fa411-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fa411-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="fa411-110">Attributes</span></span>  
  
|<span data-ttu-id="fa411-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="fa411-111">Attribute</span></span>|<span data-ttu-id="fa411-112">Description</span><span class="sxs-lookup"><span data-stu-id="fa411-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fa411-113">**developerInstallation**</span><span class="sxs-lookup"><span data-stu-id="fa411-113">**developerInstallation**</span></span>|<span data-ttu-id="fa411-114">Indique si le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fa411-114">Specifies whether the runtime searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>|  
  
## <a name="developerinstallation-attribute"></a><span data-ttu-id="fa411-115">developerInstallation attribut</span><span class="sxs-lookup"><span data-stu-id="fa411-115">developerInstallation Attribute</span></span>  
  
|<span data-ttu-id="fa411-116">Value</span><span class="sxs-lookup"><span data-stu-id="fa411-116">Value</span></span>|<span data-ttu-id="fa411-117">Description</span><span class="sxs-lookup"><span data-stu-id="fa411-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="fa411-118">**true**</span><span class="sxs-lookup"><span data-stu-id="fa411-118">**true**</span></span>|<span data-ttu-id="fa411-119">Recherche les assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fa411-119">Searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>|  
|<span data-ttu-id="fa411-120">**false**</span><span class="sxs-lookup"><span data-stu-id="fa411-120">**false**</span></span>|<span data-ttu-id="fa411-121">Ne recherche pas les assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fa411-121">Does not search for assemblies in directories specified by the DEVPATH environment variable.</span></span> <span data-ttu-id="fa411-122">Ceci est la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fa411-122">This is the default</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fa411-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa411-123">Child Elements</span></span>  
 <span data-ttu-id="fa411-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa411-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fa411-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fa411-125">Parent Elements</span></span>  
  
|<span data-ttu-id="fa411-126">Élément</span><span class="sxs-lookup"><span data-stu-id="fa411-126">Element</span></span>|<span data-ttu-id="fa411-127">Description</span><span class="sxs-lookup"><span data-stu-id="fa411-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="fa411-128">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fa411-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="fa411-129">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="fa411-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fa411-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fa411-130">Remarks</span></span>  
 <span data-ttu-id="fa411-131">Utilisez ce paramètre uniquement au moment du développement.</span><span class="sxs-lookup"><span data-stu-id="fa411-131">Use this setting only at development time.</span></span> <span data-ttu-id="fa411-132">Le runtime ne vérifie pas les versions sur les assemblys avec nom fort trouvés dans DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fa411-132">The runtime does not check the versions on strong-named assemblies found in the DEVPATH.</span></span> <span data-ttu-id="fa411-133">Elle utilise simplement le premier assembly qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="fa411-133">It simply uses the first assembly it finds.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fa411-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="fa411-134">Example</span></span>  
 <span data-ttu-id="fa411-135">L’exemple suivant montre comment entraîner le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fa411-135">The following example shows how to cause the runtime to search for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <developmentMode developerInstallation="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fa411-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa411-136">See also</span></span>

- [<span data-ttu-id="fa411-137">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="fa411-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="fa411-138">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="fa411-138">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="fa411-139">Guide pratique pour Localiser des assemblys à l’aide de DEVPATH</span><span class="sxs-lookup"><span data-stu-id="fa411-139">How to: Locate Assemblies by Using DEVPATH</span></span>](../../../../../docs/framework/configure-apps/how-to-locate-assemblies-by-using-devpath.md)
