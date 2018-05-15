---
title: '&lt;supprimer&gt; élément &lt;écouteurs&gt; pour &lt;source&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/remove
helpviewer_keywords:
- remove element for <listeners> for <source>
- <remove> element for <listeners> for <source>
ms.assetid: 3ff6b578-273d-407f-b07f-8251f1f9f5d0
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: cc6772e7a9b98f09df21fd1acf24f578b66ae51e
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltremovegt-element-for-ltlistenersgt-for-ltsourcegt"></a><span data-ttu-id="a8342-102">&lt;supprimer&gt; élément &lt;écouteurs&gt; pour &lt;source&gt;</span><span class="sxs-lookup"><span data-stu-id="a8342-102">&lt;remove&gt; Element for &lt;listeners&gt; for &lt;source&gt;</span></span>
<span data-ttu-id="a8342-103">Supprime un écouteur de la collection `Listeners` pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="a8342-103">Removes a listener from the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="a8342-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="a8342-104">\<configuration></span></span>  
<span data-ttu-id="a8342-105">\<System.Diagnostics ></span><span class="sxs-lookup"><span data-stu-id="a8342-105">\<system.diagnostics></span></span>  
<span data-ttu-id="a8342-106">\<sources ></span><span class="sxs-lookup"><span data-stu-id="a8342-106">\<sources></span></span>  
<span data-ttu-id="a8342-107">\<source ></span><span class="sxs-lookup"><span data-stu-id="a8342-107">\<source></span></span>  
<span data-ttu-id="a8342-108">\<écouteurs ></span><span class="sxs-lookup"><span data-stu-id="a8342-108">\<listeners></span></span>  
<span data-ttu-id="a8342-109">\<remove></span><span class="sxs-lookup"><span data-stu-id="a8342-109">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8342-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8342-110">Syntax</span></span>  
  
```xml  
<remove name="listenerName" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a8342-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a8342-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a8342-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a8342-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a8342-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8342-113">Attributes</span></span>  
  
|<span data-ttu-id="a8342-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="a8342-114">Attribute</span></span>|<span data-ttu-id="a8342-115">Description</span><span class="sxs-lookup"><span data-stu-id="a8342-115">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="a8342-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="a8342-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="a8342-117">Le nom de l’écouteur à supprimer de la `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="a8342-117">The name of the listener to remove from the `Listeners` collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a8342-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8342-118">Child Elements</span></span>  
 <span data-ttu-id="a8342-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a8342-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a8342-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a8342-120">Parent Elements</span></span>  
  
|<span data-ttu-id="a8342-121">Élément</span><span class="sxs-lookup"><span data-stu-id="a8342-121">Element</span></span>|<span data-ttu-id="a8342-122">Description</span><span class="sxs-lookup"><span data-stu-id="a8342-122">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="a8342-123">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a8342-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="a8342-124">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="a8342-124">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="a8342-125">Contient les sources de trace qui lancent des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="a8342-125">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="a8342-126">Spécifie une source de trace qui lance des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="a8342-126">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="a8342-127">Spécifie les écouteurs de collectent, stocker et acheminer les messages.</span><span class="sxs-lookup"><span data-stu-id="a8342-127">Specifies listeners that collect, store, and route messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a8342-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a8342-128">Remarks</span></span>  
 <span data-ttu-id="a8342-129">Le `<remove>` élément supprime un écouteur spécifié de la `Listeners` collection pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="a8342-129">The `<remove>` element removes a specified listener from the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="a8342-130">Vous pouvez supprimer un élément à partir de la `Listeners` collection pour une source de trace par programme en appelant le <xref:System.Diagnostics.TraceListenerCollection.Remove%2A> méthode sur le <xref:System.Diagnostics.TraceSource.Listeners%2A> propriété de la <xref:System.Diagnostics.TraceSource> instance.</span><span class="sxs-lookup"><span data-stu-id="a8342-130">You can remove an element from the `Listeners` collection for a trace source programmatically by calling the <xref:System.Diagnostics.TraceListenerCollection.Remove%2A> method on the <xref:System.Diagnostics.TraceSource.Listeners%2A> property of the <xref:System.Diagnostics.TraceSource> instance.</span></span>  
  
 <span data-ttu-id="a8342-131">Cet élément peut être utilisé dans le fichier de configuration de l’ordinateur (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="a8342-131">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8342-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8342-132">Example</span></span>  
 <span data-ttu-id="a8342-133">L’exemple suivant montre comment utiliser le `<remove>` élément avant d’utiliser le `<add>` élément pour ajouter l’écouteur `console` à la `Listeners` collection pour la source de suivi `TraceSourceApp`.</span><span class="sxs-lookup"><span data-stu-id="a8342-133">The following example shows how to use the `<remove>` element before using the `<add>` element to add the listener `console` to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch" >  
         <listeners>  
           <remove name="Default"/>  
           <add name="console"   
             type="System.Diagnostics.ConsoleTraceListener" />  
         </listeners>  
      </source>  
    </sources>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="a8342-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8342-134">See Also</span></span>  
 <xref:System.Diagnostics.TraceSource.Listeners%2A>  
 <xref:System.Diagnostics.TraceSource>  
 [<span data-ttu-id="a8342-135">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="a8342-135">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="a8342-136">\<clear></span><span class="sxs-lookup"><span data-stu-id="a8342-136">\<clear></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-source.md)  
 [<span data-ttu-id="a8342-137">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="a8342-137">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
