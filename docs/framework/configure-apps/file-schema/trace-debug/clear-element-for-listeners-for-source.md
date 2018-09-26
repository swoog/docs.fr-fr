---
title: '&lt;Désactivez&gt; élément pour &lt;écouteurs&gt; pour &lt;source&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/clear
helpviewer_keywords:
- <clear> element for <listeners> for <source>
- clear element for <listeners> for <source>
ms.assetid: 76796bb2-9c0b-4526-8135-8bf18b16d8d9
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 3674b5e8f54735010da901c76b77bd617218891e
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47209179"
---
# <a name="ltcleargt-element-for-ltlistenersgt-for-ltsourcegt"></a><span data-ttu-id="c4010-102">&lt;Désactivez&gt; élément pour &lt;écouteurs&gt; pour &lt;source&gt;</span><span class="sxs-lookup"><span data-stu-id="c4010-102">&lt;clear&gt; Element for &lt;listeners&gt; for &lt;source&gt;</span></span>
<span data-ttu-id="c4010-103">Efface la collection `Listeners` pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="c4010-103">Clears the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="c4010-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="c4010-104">\<configuration></span></span>  
<span data-ttu-id="c4010-105">\<System.Diagnostics ></span><span class="sxs-lookup"><span data-stu-id="c4010-105">\<system.diagnostics></span></span>  
<span data-ttu-id="c4010-106">\<sources ></span><span class="sxs-lookup"><span data-stu-id="c4010-106">\<sources></span></span>  
<span data-ttu-id="c4010-107">\<source ></span><span class="sxs-lookup"><span data-stu-id="c4010-107">\<source></span></span>  
<span data-ttu-id="c4010-108">\<écouteurs ></span><span class="sxs-lookup"><span data-stu-id="c4010-108">\<listeners></span></span>  
<span data-ttu-id="c4010-109">\<Désactivez ></span><span class="sxs-lookup"><span data-stu-id="c4010-109">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4010-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4010-110">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c4010-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c4010-111">Attributes and Elements</span></span>  
 <span data-ttu-id="c4010-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c4010-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c4010-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4010-113">Attributes</span></span>  
 <span data-ttu-id="c4010-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c4010-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c4010-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4010-115">Child Elements</span></span>  
 <span data-ttu-id="c4010-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c4010-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c4010-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c4010-117">Parent Elements</span></span>  
  
|<span data-ttu-id="c4010-118">Élément</span><span class="sxs-lookup"><span data-stu-id="c4010-118">Element</span></span>|<span data-ttu-id="c4010-119">Description</span><span class="sxs-lookup"><span data-stu-id="c4010-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="c4010-120">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c4010-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="c4010-121">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="c4010-121">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="c4010-122">Contient les sources de trace qui lancent des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="c4010-122">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="c4010-123">Spécifie une source de trace qui lance des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="c4010-123">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="c4010-124">Spécifie des écouteurs qui collectent, stockent et acheminent les messages.</span><span class="sxs-lookup"><span data-stu-id="c4010-124">Specifies listeners that collect, store, and route messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c4010-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c4010-125">Remarks</span></span>  
 <span data-ttu-id="c4010-126">Le `<clear>` élément supprime tous les écouteurs de la `Listeners` collection pour une source de trace, y compris le <xref:System.Diagnostics.DefaultTraceListener>.</span><span class="sxs-lookup"><span data-stu-id="c4010-126">The `<clear>` element removes all listeners from the `Listeners` collection for a trace source, including the <xref:System.Diagnostics.DefaultTraceListener>.</span></span> <span data-ttu-id="c4010-127">Vous pouvez utiliser la `<clear>` élément avant d’utiliser le `<add>` pour garantir l’aucun autres écouteurs actifs dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c4010-127">You can use the `<clear>` element before using the `<add>` element to be certain there are no other active listeners in the collection.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="c4010-128">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="c4010-128">Configuration File</span></span>  
 <span data-ttu-id="c4010-129">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="c4010-129">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c4010-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4010-130">Example</span></span>  
 <span data-ttu-id="c4010-131">L’exemple suivant montre comment utiliser le `<clear>` élément avant d’utiliser le `<add>` éléments à ajouter les écouteurs `console` et `textListener` à la `Listeners` collection pour la source de suivi `TraceSourceApp`.</span><span class="sxs-lookup"><span data-stu-id="c4010-131">The following example shows how to use the `<clear>` element before using the `<add>` elements to add the listeners `console` and `textListener` to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
       <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <clear/>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"   
        type="System.Diagnostics.TextWriterTraceListener"   
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="c4010-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4010-132">See Also</span></span>  
 <xref:System.Diagnostics.TraceSource>  
 <xref:System.Diagnostics.TraceListener>  
 [<span data-ttu-id="c4010-133">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="c4010-133">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="c4010-134">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="c4010-134">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
