---
title: '&lt;requiredRuntime&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requiredRuntime
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup/requiredRuntime
helpviewer_keywords:
- requiredRuntime element
- <requiredRuntime> element
- container tags, <requiredRuntime> element
ms.assetid: 9fa1639e-beb8-43be-b7a4-12f7b229c34b
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: ac1e1f7bc36d8d2b12b99de2794bb0ba31ddbd7a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398730"
---
# <a name="ltrequiredruntimegt-element"></a><span data-ttu-id="ec1fb-102">&lt;requiredRuntime&gt; élément</span><span class="sxs-lookup"><span data-stu-id="ec1fb-102">&lt;requiredRuntime&gt; Element</span></span>
<span data-ttu-id="ec1fb-103">Spécifie que l’application prend en charge uniquement la version 1.0 du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-103">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="ec1fb-104">Cet élément est déconseillé et ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-104">This element is deprecated and should no longer be used.</span></span> <span data-ttu-id="ec1fb-105">Le [ `supportedRuntime` ](supportedruntime-element.md) élément doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-105">The [`supportedRuntime`](supportedruntime-element.md) element should be used instead.</span></span>
  
 <span data-ttu-id="ec1fb-106">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ec1fb-106">\<configuration></span></span>  
<span data-ttu-id="ec1fb-107">\<startup></span><span class="sxs-lookup"><span data-stu-id="ec1fb-107">\<startup></span></span>  
<span data-ttu-id="ec1fb-108">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="ec1fb-108">\<requiredRuntime></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec1fb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec1fb-109">Syntax</span></span>  
  
```xml  
   <requiredRuntime    
version="runtime version"  
safemode="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ec1fb-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ec1fb-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ec1fb-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ec1fb-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="ec1fb-112">Attributes</span></span>  
  
|<span data-ttu-id="ec1fb-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="ec1fb-113">Attribute</span></span>|<span data-ttu-id="ec1fb-114">Description</span><span class="sxs-lookup"><span data-stu-id="ec1fb-114">Description</span></span>|  
|---------------|-----------------|  
|`version`|<span data-ttu-id="ec1fb-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-115">Optional attribute.</span></span><br /><br /> <span data-ttu-id="ec1fb-116">Valeur de chaîne qui spécifie la version du .NET Framework qui prend en charge de cette application.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-116">A string value that specifies the version of the .NET Framework that this application supports.</span></span> <span data-ttu-id="ec1fb-117">La valeur de chaîne doit correspondre au nom de répertoire trouvé sous la racine d’installation de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-117">The string value must match the directory name found under the .NET Framework installation root.</span></span> <span data-ttu-id="ec1fb-118">Le contenu de la valeur de chaîne n’est pas analysé.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-118">The contents of the string value are not parsed.</span></span>|  
|`safemode`|<span data-ttu-id="ec1fb-119">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-119">Optional attribute.</span></span><br /><br /> <span data-ttu-id="ec1fb-120">Spécifie si le code de démarrage runtime recherche dans le Registre pour déterminer la version du runtime.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-120">Specifies whether the runtime startup code searches the registry to determine the runtime version.</span></span>|  
  
## <a name="safemode-attribute"></a><span data-ttu-id="ec1fb-121">SafeMode attribut</span><span class="sxs-lookup"><span data-stu-id="ec1fb-121">safemode Attribute</span></span>  
  
|<span data-ttu-id="ec1fb-122">Value</span><span class="sxs-lookup"><span data-stu-id="ec1fb-122">Value</span></span>|<span data-ttu-id="ec1fb-123">Description</span><span class="sxs-lookup"><span data-stu-id="ec1fb-123">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="ec1fb-124">Le code de démarrage runtime recherche dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-124">The runtime startup code looks in the registry.</span></span> <span data-ttu-id="ec1fb-125">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-125">This is the default value.</span></span>|  
|`true`|<span data-ttu-id="ec1fb-126">Le code de démarrage runtime ne recherche pas dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-126">The runtime startup code does not look in the registry.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ec1fb-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ec1fb-127">Child Elements</span></span>  
 <span data-ttu-id="ec1fb-128">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-128">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ec1fb-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ec1fb-129">Parent Elements</span></span>  
  
|<span data-ttu-id="ec1fb-130">Élément</span><span class="sxs-lookup"><span data-stu-id="ec1fb-130">Element</span></span>|<span data-ttu-id="ec1fb-131">Description</span><span class="sxs-lookup"><span data-stu-id="ec1fb-131">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="ec1fb-132">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-132">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`startup`|<span data-ttu-id="ec1fb-133">Contient le `<requiredRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-133">Contains the `<requiredRuntime>` element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ec1fb-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ec1fb-134">Remarks</span></span>  
 <span data-ttu-id="ec1fb-135">Les applications générées pour prendre en charge uniquement la version 1.0 du runtime doivent utiliser le `<requiredRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-135">Applications built to support only version 1.0 of the runtime must use the `<requiredRuntime>` element.</span></span> <span data-ttu-id="ec1fb-136">Les applications générées à l’aide de la version 1.1 ou ultérieure du runtime doivent utiliser le `<supportedRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-136">Applications built using version 1.1 or later of the runtime must use the `<supportedRuntime>` element.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ec1fb-137">Si vous utilisez le [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) de fonction pour spécifier le fichier de configuration, vous devez utiliser le `<requiredRuntime>` élément pour toutes les versions du runtime.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-137">If you use the [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) function to specify the configuration file, you must use the `<requiredRuntime>` element for all versions of the runtime.</span></span> <span data-ttu-id="ec1fb-138">Le `<supportedRuntime>` élément est ignoré lorsque vous utilisez [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec1fb-138">The `<supportedRuntime>` element is ignored when you use [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span></span>  
  
 <span data-ttu-id="ec1fb-139">Le `version` chaîne de l’attribut doit correspondre au nom de dossier d’installation de la version spécifiée du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-139">The `version` attribute string must match the installation folder name for the specified version of the .NET Framework.</span></span> <span data-ttu-id="ec1fb-140">Cette chaîne n’est pas interprétée.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-140">This string is not interpreted.</span></span> <span data-ttu-id="ec1fb-141">Si le code de démarrage runtime ne trouve pas de dossier correspondant, le runtime n’est pas chargé ; le code de démarrage affiche un message d’erreur et se ferme.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-141">If the runtime startup code does not find a matching folder, the runtime is not loaded; the startup code shows an error message and quits.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ec1fb-142">Le code de démarrage pour une application qui est hébergé dans Microsoft Internet Explorer ignore les `<requiredRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-142">The startup code for an application that is hosted in Microsoft Internet Explorer ignores the `<requiredRuntime>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec1fb-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec1fb-143">Example</span></span>  
 <span data-ttu-id="ec1fb-144">L’exemple suivant montre comment spécifier la version du runtime dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-144">The following example shows how to specify the runtime version in a configuration file.</span></span>  
  
```xml  
<configuration>  
   <startup>  
      <requiredRuntime version="v1.0.3705" safemode="true"/>  
   </startup>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ec1fb-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec1fb-145">See Also</span></span>  
 [<span data-ttu-id="ec1fb-146">Schéma des paramètres de démarrage</span><span class="sxs-lookup"><span data-stu-id="ec1fb-146">Startup Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)  
 [<span data-ttu-id="ec1fb-147">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="ec1fb-147">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="ec1fb-148">\<PaveOver> Spécification de la version du runtime à utiliser</span><span class="sxs-lookup"><span data-stu-id="ec1fb-148">\<PaveOver> Specifying Which Runtime Version to Use</span></span>](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)
