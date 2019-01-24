---
title: '&lt;écouteurs&gt; élément pour &lt;source&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners
helpviewer_keywords:
- listeners element for <source>
- <listeners> element for <source>
ms.assetid: a2991f43-b4d3-4614-a8e7-da392de9697f
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 949b6c7272b39900698b618760f5e5bad11ccc3d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670639"
---
# <a name="ltlistenersgt-element-for-ltsourcegt"></a><span data-ttu-id="23633-102">&lt;écouteurs&gt; élément pour &lt;source&gt;</span><span class="sxs-lookup"><span data-stu-id="23633-102">&lt;listeners&gt; Element for &lt;source&gt;</span></span>
<span data-ttu-id="23633-103">Ajoute ou supprime des écouteurs dans le <xref:System.Diagnostics.TraceSource.Listeners%2A> collection pour un <xref:System.Diagnostics.TraceSource>.</span><span class="sxs-lookup"><span data-stu-id="23633-103">Adds or removes listeners in the <xref:System.Diagnostics.TraceSource.Listeners%2A> collection for a <xref:System.Diagnostics.TraceSource>.</span></span> <span data-ttu-id="23633-104">Un écouteur dirige la sortie de traçage vers une cible appropriée, par exemple un journal, une fenêtre ou un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="23633-104">A listener directs the tracing output to an appropriate target, such as a log, window, or text file.</span></span>  
  
 <span data-ttu-id="23633-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="23633-105">\<configuration></span></span>  
<span data-ttu-id="23633-106">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="23633-106">\<system.diagnostics></span></span>  
<span data-ttu-id="23633-107">\<sources></span><span class="sxs-lookup"><span data-stu-id="23633-107">\<sources></span></span>  
<span data-ttu-id="23633-108">\<source></span><span class="sxs-lookup"><span data-stu-id="23633-108">\<source></span></span>  
<span data-ttu-id="23633-109">\<écouteurs > élément</span><span class="sxs-lookup"><span data-stu-id="23633-109">\<listeners> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23633-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23633-110">Syntax</span></span>  
  
```xml  
<listeners>   
  <add>...</add>  
  <remove ... />  
  <clear/>  
</listeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="23633-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="23633-111">Attributes and Elements</span></span>  
 <span data-ttu-id="23633-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="23633-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="23633-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="23633-113">Attributes</span></span>  
 <span data-ttu-id="23633-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="23633-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="23633-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="23633-115">Child Elements</span></span>  
  
|<span data-ttu-id="23633-116">Élément</span><span class="sxs-lookup"><span data-stu-id="23633-116">Element</span></span>|<span data-ttu-id="23633-117">Description</span><span class="sxs-lookup"><span data-stu-id="23633-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="23633-118">\<add></span><span class="sxs-lookup"><span data-stu-id="23633-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-listeners-for-source.md)|<span data-ttu-id="23633-119">Ajoute un écouteur à la collection `Listeners`.</span><span class="sxs-lookup"><span data-stu-id="23633-119">Adds a listener to the `Listeners` collection.</span></span>|  
|[<span data-ttu-id="23633-120">\<remove></span><span class="sxs-lookup"><span data-stu-id="23633-120">\<remove></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-source.md)|<span data-ttu-id="23633-121">Supprime un écouteur de la `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="23633-121">Removes a listener from the `Listeners` collection.</span></span>|  
|[<span data-ttu-id="23633-122">\<clear></span><span class="sxs-lookup"><span data-stu-id="23633-122">\<clear></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-source.md)|<span data-ttu-id="23633-123">Efface la collection `Listeners` pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="23633-123">Clears the `Listeners` collection for a trace source.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="23633-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="23633-124">Parent Elements</span></span>  
  
|<span data-ttu-id="23633-125">Élément</span><span class="sxs-lookup"><span data-stu-id="23633-125">Element</span></span>|<span data-ttu-id="23633-126">Description</span><span class="sxs-lookup"><span data-stu-id="23633-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="23633-127">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="23633-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="23633-128">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="23633-128">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="23633-129">Contient les sources de trace qui lancent des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="23633-129">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="23633-130">Spécifie une source de trace qui lance des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="23633-130">Specifies a trace source that initiates tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="23633-131">Notes</span><span class="sxs-lookup"><span data-stu-id="23633-131">Remarks</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="23633-132">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="23633-132">Configuration File</span></span>  
 <span data-ttu-id="23633-133">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="23633-133">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="23633-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="23633-134">Example</span></span>  
 <span data-ttu-id="23633-135">L’exemple suivant montre comment utiliser le `<listeners>` élément à ajouter un écouteur de suivi de console à la `mySource` source et de supprimer l’écouteur de trace par défaut.</span><span class="sxs-lookup"><span data-stu-id="23633-135">The following example shows how to use the `<listeners>` element to add a console trace listener to the `mySource` source and to remove the default trace listener.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="mySource" switchName="sourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener">  
            <filter type="System.Diagnostics.EventTypeFilter"   
              initializeData="Error"/>  
          </add>  
          <remove name="Default"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="23633-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23633-136">See also</span></span>
- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="23633-137">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="23633-137">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [<span data-ttu-id="23633-138">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="23633-138">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
