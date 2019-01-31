---
title: <clear>, élément de <listeners> pour <source>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/clear
helpviewer_keywords:
- <clear> element for <listeners> for <source>
- clear element for <listeners> for <source>
ms.assetid: 76796bb2-9c0b-4526-8135-8bf18b16d8d9
ms.openlocfilehash: ee4d5f1880cf6b7aac871149bf7bf59a06903bf2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286739"
---
# <a name="clear-element-for-listeners-for-source"></a><span data-ttu-id="e7801-102">\<Désactivez >, élément pour \<écouteurs > pour \<source ></span><span class="sxs-lookup"><span data-stu-id="e7801-102">\<clear> Element for \<listeners> for \<source></span></span>
<span data-ttu-id="e7801-103">Efface la collection `Listeners` pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="e7801-103">Clears the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="e7801-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="e7801-104">\<configuration></span></span>  
<span data-ttu-id="e7801-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="e7801-105">\<system.diagnostics></span></span>  
<span data-ttu-id="e7801-106">\<sources></span><span class="sxs-lookup"><span data-stu-id="e7801-106">\<sources></span></span>  
<span data-ttu-id="e7801-107">\<source></span><span class="sxs-lookup"><span data-stu-id="e7801-107">\<source></span></span>  
<span data-ttu-id="e7801-108">\<listeners></span><span class="sxs-lookup"><span data-stu-id="e7801-108">\<listeners></span></span>  
<span data-ttu-id="e7801-109">\<clear></span><span class="sxs-lookup"><span data-stu-id="e7801-109">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7801-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7801-110">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e7801-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e7801-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e7801-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e7801-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e7801-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="e7801-113">Attributes</span></span>  
 <span data-ttu-id="e7801-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e7801-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="e7801-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e7801-115">Child Elements</span></span>  
 <span data-ttu-id="e7801-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e7801-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e7801-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e7801-117">Parent Elements</span></span>  
  
|<span data-ttu-id="e7801-118">Élément</span><span class="sxs-lookup"><span data-stu-id="e7801-118">Element</span></span>|<span data-ttu-id="e7801-119">Description</span><span class="sxs-lookup"><span data-stu-id="e7801-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="e7801-120">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e7801-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="e7801-121">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="e7801-121">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="e7801-122">Contient les sources de trace qui lancent des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="e7801-122">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="e7801-123">Spécifie une source de trace qui lance des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="e7801-123">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="e7801-124">Spécifie des écouteurs qui collectent, stockent et acheminent les messages.</span><span class="sxs-lookup"><span data-stu-id="e7801-124">Specifies listeners that collect, store, and route messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7801-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e7801-125">Remarks</span></span>  
 <span data-ttu-id="e7801-126">Le `<clear>` élément supprime tous les écouteurs de la `Listeners` collection pour une source de trace, y compris le <xref:System.Diagnostics.DefaultTraceListener>.</span><span class="sxs-lookup"><span data-stu-id="e7801-126">The `<clear>` element removes all listeners from the `Listeners` collection for a trace source, including the <xref:System.Diagnostics.DefaultTraceListener>.</span></span> <span data-ttu-id="e7801-127">Vous pouvez utiliser la `<clear>` élément avant d’utiliser le `<add>` pour garantir l’aucun autres écouteurs actifs dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e7801-127">You can use the `<clear>` element before using the `<add>` element to be certain there are no other active listeners in the collection.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="e7801-128">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="e7801-128">Configuration File</span></span>  
 <span data-ttu-id="e7801-129">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="e7801-129">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e7801-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="e7801-130">Example</span></span>  
 <span data-ttu-id="e7801-131">L’exemple suivant montre comment utiliser le `<clear>` élément avant d’utiliser le `<add>` éléments à ajouter les écouteurs `console` et `textListener` à la `Listeners` collection pour la source de suivi `TraceSourceApp`.</span><span class="sxs-lookup"><span data-stu-id="e7801-131">The following example shows how to use the `<clear>` element before using the `<add>` elements to add the listeners `console` and `textListener` to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="e7801-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7801-132">See also</span></span>
- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="e7801-133">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="e7801-133">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [<span data-ttu-id="e7801-134">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="e7801-134">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
