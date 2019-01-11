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
ms.openlocfilehash: 66de3e30ce862cd317e80ea267bf22ce728aca82
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222127"
---
# <a name="ltrequiredruntimegt-element"></a><span data-ttu-id="fa9c6-102">&lt;requiredRuntime&gt; élément</span><span class="sxs-lookup"><span data-stu-id="fa9c6-102">&lt;requiredRuntime&gt; element</span></span>

<span data-ttu-id="fa9c6-103">Spécifie que l’application prend en charge uniquement la version 1.0 du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-103">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="fa9c6-104">Cet élément est déconseillé et ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-104">This element is deprecated and should no longer be used.</span></span> <span data-ttu-id="fa9c6-105">Le [ `supportedRuntime` ](supportedruntime-element.md) élément doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-105">The [`supportedRuntime`](supportedruntime-element.md) element should be used instead.</span></span>

<span data-ttu-id="fa9c6-106">\<configuration > \<démarrage > \<requiredRuntime ></span><span class="sxs-lookup"><span data-stu-id="fa9c6-106">\<configuration> \<startup> \<requiredRuntime></span></span>

## <a name="syntax"></a><span data-ttu-id="fa9c6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa9c6-107">Syntax</span></span>

```xml
   <requiredRuntime  
version="runtime version"
safemode="true|false"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="fa9c6-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fa9c6-108">Attributes and elements</span></span>

<span data-ttu-id="fa9c6-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="fa9c6-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="fa9c6-110">Attributes</span></span>

|<span data-ttu-id="fa9c6-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="fa9c6-111">Attribute</span></span>|<span data-ttu-id="fa9c6-112">Description</span><span class="sxs-lookup"><span data-stu-id="fa9c6-112">Description</span></span>|
|---------------|-----------------|
|`version`|<span data-ttu-id="fa9c6-113">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-113">Optional attribute.</span></span><br /><br /> <span data-ttu-id="fa9c6-114">Valeur de chaîne qui spécifie la version du .NET Framework qui prend en charge de cette application.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-114">A string value that specifies the version of the .NET Framework that this application supports.</span></span> <span data-ttu-id="fa9c6-115">La valeur de chaîne doit correspondre au nom de répertoire trouvé sous la racine d’installation de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-115">The string value must match the directory name found under the .NET Framework installation root.</span></span> <span data-ttu-id="fa9c6-116">Le contenu de la valeur de chaîne n’est pas analysé.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-116">The contents of the string value are not parsed.</span></span>|
|`safemode`|<span data-ttu-id="fa9c6-117">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-117">Optional attribute.</span></span><br /><br /> <span data-ttu-id="fa9c6-118">Spécifie si le code de démarrage runtime recherche dans le Registre pour déterminer la version du runtime.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-118">Specifies whether the runtime startup code searches the registry to determine the runtime version.</span></span>|

## <a name="safemode-attribute"></a><span data-ttu-id="fa9c6-119">attribut de mode sans échec</span><span class="sxs-lookup"><span data-stu-id="fa9c6-119">safemode attribute</span></span>

|<span data-ttu-id="fa9c6-120">Value</span><span class="sxs-lookup"><span data-stu-id="fa9c6-120">Value</span></span>|<span data-ttu-id="fa9c6-121">Description</span><span class="sxs-lookup"><span data-stu-id="fa9c6-121">Description</span></span>|
|-----------|-----------------|
|`false`|<span data-ttu-id="fa9c6-122">Le code de démarrage runtime recherche dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-122">The runtime startup code looks in the registry.</span></span> <span data-ttu-id="fa9c6-123">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-123">This is the default value.</span></span>|
|`true`|<span data-ttu-id="fa9c6-124">Le code de démarrage runtime ne recherche pas dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-124">The runtime startup code does not look in the registry.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="fa9c6-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa9c6-125">Child elements</span></span>

<span data-ttu-id="fa9c6-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-126">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="fa9c6-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fa9c6-127">Parent elements</span></span>

|<span data-ttu-id="fa9c6-128">Élément</span><span class="sxs-lookup"><span data-stu-id="fa9c6-128">Element</span></span>|<span data-ttu-id="fa9c6-129">Description</span><span class="sxs-lookup"><span data-stu-id="fa9c6-129">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="fa9c6-130">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`startup`|<span data-ttu-id="fa9c6-131">Contient le `<requiredRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-131">Contains the `<requiredRuntime>` element.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fa9c6-132">Notes</span><span class="sxs-lookup"><span data-stu-id="fa9c6-132">Remarks</span></span>
 <span data-ttu-id="fa9c6-133">Les applications générées pour prendre en charge uniquement la version 1.0 du runtime doivent utiliser le `<requiredRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-133">Applications built to support only version 1.0 of the runtime must use the `<requiredRuntime>` element.</span></span> <span data-ttu-id="fa9c6-134">Les applications générées à l’aide de la version 1.1 ou ultérieure du runtime doivent utiliser le `<supportedRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-134">Applications built using version 1.1 or later of the runtime must use the `<supportedRuntime>` element.</span></span>

> [!NOTE]
> <span data-ttu-id="fa9c6-135">Si vous utilisez le [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md) de fonction pour spécifier le fichier de configuration, vous devez utiliser le `<requiredRuntime>` élément pour toutes les versions du runtime.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-135">If you use the [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md) function to specify the configuration file, you must use the `<requiredRuntime>` element for all versions of the runtime.</span></span> <span data-ttu-id="fa9c6-136">Le `<supportedRuntime>` élément est ignoré lorsque vous utilisez [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span><span class="sxs-lookup"><span data-stu-id="fa9c6-136">The `<supportedRuntime>` element is ignored when you use [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span></span>

 <span data-ttu-id="fa9c6-137">Le `version` chaîne de l’attribut doit correspondre au nom de dossier d’installation de la version spécifiée du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-137">The `version` attribute string must match the installation folder name for the specified version of the .NET Framework.</span></span> <span data-ttu-id="fa9c6-138">Cette chaîne n’est pas interprétée.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-138">This string is not interpreted.</span></span> <span data-ttu-id="fa9c6-139">Si le code de démarrage runtime ne trouve pas de dossier correspondant, le runtime n’est pas chargé ; le code de démarrage affiche un message d’erreur et se ferme.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-139">If the runtime startup code does not find a matching folder, the runtime is not loaded; the startup code shows an error message and quits.</span></span>

> [!NOTE]
> <span data-ttu-id="fa9c6-140">Le code de démarrage pour une application qui est hébergé dans Microsoft Internet Explorer ignore les `<requiredRuntime>` élément.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-140">The startup code for an application that is hosted in Microsoft Internet Explorer ignores the `<requiredRuntime>` element.</span></span>

## <a name="example"></a><span data-ttu-id="fa9c6-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="fa9c6-141">Example</span></span>

<span data-ttu-id="fa9c6-142">L’exemple suivant montre comment spécifier la version du runtime dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-142">The following example shows how to specify the runtime version in a configuration file.</span></span>

```xml
<configuration>
   <startup>
      <requiredRuntime version="v1.0.3705" safemode="true"/>
   </startup>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="fa9c6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa9c6-143">See also</span></span>

- [<span data-ttu-id="fa9c6-144">Schéma des paramètres de démarrage</span><span class="sxs-lookup"><span data-stu-id="fa9c6-144">Startup Settings Schema</span></span>](index.md)
- [<span data-ttu-id="fa9c6-145">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="fa9c6-145">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="fa9c6-146">Guide pratique pour Configurer une application pour prendre en charge de .NET Framework 4 ou versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="fa9c6-146">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)