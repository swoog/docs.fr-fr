---
title: <clear> Élément pour <listeners> pour <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/clear
helpviewer_keywords:
- clear element for <listeners> for <trace>
- <clear> element for <listeners> for <trace>
ms.assetid: b44732a8-271f-4a06-ba9e-fe3298d6f192
ms.openlocfilehash: 97b18f9d6baa618b0f535955b232e2119c758b11
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701318"
---
# <a name="clear-element-for-listeners-for-trace"></a><span data-ttu-id="61065-102">\<Désactivez >, élément pour \<écouteurs > pour \<trace ></span><span class="sxs-lookup"><span data-stu-id="61065-102">\<clear> Element for \<listeners> for \<trace></span></span>
<span data-ttu-id="61065-103">Efface la collection `Listeners` de la trace.</span><span class="sxs-lookup"><span data-stu-id="61065-103">Clears the `Listeners` collection for trace.</span></span>  
  
 <span data-ttu-id="61065-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="61065-104">\<configuration></span></span>  
<span data-ttu-id="61065-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="61065-105">\<system.diagnostics></span></span>  
<span data-ttu-id="61065-106">\<trace></span><span class="sxs-lookup"><span data-stu-id="61065-106">\<trace></span></span>  
<span data-ttu-id="61065-107">\<listeners></span><span class="sxs-lookup"><span data-stu-id="61065-107">\<listeners></span></span>  
<span data-ttu-id="61065-108">\<clear></span><span class="sxs-lookup"><span data-stu-id="61065-108">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61065-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61065-109">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="61065-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="61065-110">Attributes and Elements</span></span>  
 <span data-ttu-id="61065-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="61065-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="61065-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="61065-112">Attributes</span></span>  
 <span data-ttu-id="61065-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="61065-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="61065-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="61065-114">Child Elements</span></span>  
 <span data-ttu-id="61065-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="61065-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="61065-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="61065-116">Parent Elements</span></span>  
  
|<span data-ttu-id="61065-117">Élément</span><span class="sxs-lookup"><span data-stu-id="61065-117">Element</span></span>|<span data-ttu-id="61065-118">Description</span><span class="sxs-lookup"><span data-stu-id="61065-118">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="61065-119">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="61065-119">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="61065-120">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="61065-120">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`trace`|<span data-ttu-id="61065-121">Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="61065-121">Contains listeners that collect, store, and route tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="61065-122">Contient des écouteurs qui collectent, stockent et acheminent les messages.</span><span class="sxs-lookup"><span data-stu-id="61065-122">Contains listeners that collect, store, and route messages.</span></span> <span data-ttu-id="61065-123">Les écouteurs dirigent la sortie de traçage vers une cible appropriée.</span><span class="sxs-lookup"><span data-stu-id="61065-123">Listeners direct the tracing output to an appropriate target.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="61065-124">Notes</span><span class="sxs-lookup"><span data-stu-id="61065-124">Remarks</span></span>  
 <span data-ttu-id="61065-125">Le `<clear>` élément supprime tous les écouteurs de la `Listeners` collection de la trace.</span><span class="sxs-lookup"><span data-stu-id="61065-125">The `<clear>` element removes all listeners from the `Listeners` collection for trace.</span></span> <span data-ttu-id="61065-126">Vous pouvez utiliser la `<clear>` élément avant d’utiliser le `<add>` pour garantir l’aucun autres écouteurs actifs dans la collection.</span><span class="sxs-lookup"><span data-stu-id="61065-126">You can use the `<clear>` element before using the `<add>` element to be certain there are no other active listeners in the collection.</span></span>  
  
 <span data-ttu-id="61065-127">Vous pouvez effacer le `Listeners` collection par programmation en appelant le <xref:System.Diagnostics.TraceListenerCollection.Clear%2A> méthode sur le <xref:System.Diagnostics.Trace.Listeners%2A?displayProperty=nameWithType> propriété (`System.Diagnostics.Trace.Listeners.Clear()`).</span><span class="sxs-lookup"><span data-stu-id="61065-127">You can clear the `Listeners` collection programmatically by calling the <xref:System.Diagnostics.TraceListenerCollection.Clear%2A> method on the <xref:System.Diagnostics.Trace.Listeners%2A?displayProperty=nameWithType> property (`System.Diagnostics.Trace.Listeners.Clear()`).</span></span>  
  
 <span data-ttu-id="61065-128">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="61065-128">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="61065-129">Le `<clear>` élément supprime le <xref:System.Diagnostics.DefaultTraceListener> à partir de la `Listeners` collection, la modification du comportement de la <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, et <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> méthodes.</span><span class="sxs-lookup"><span data-stu-id="61065-129">The `<clear>` element removes the <xref:System.Diagnostics.DefaultTraceListener> from the `Listeners` collection, altering the behavior of the <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, and <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="61065-130">Appeler un `Assert` ou `Fail` aboutit généralement à la méthode dans l’affichage d’un message.</span><span class="sxs-lookup"><span data-stu-id="61065-130">Calling an `Assert` or `Fail` method normally results in the display of a message box.</span></span> <span data-ttu-id="61065-131">Toutefois, la boîte de message s’affiche pas si le <xref:System.Diagnostics.DefaultTraceListener> n’est pas dans le `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="61065-131">However, the message box is not displayed if the <xref:System.Diagnostics.DefaultTraceListener> is not in the `Listeners` collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="61065-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="61065-132">Example</span></span>  
 <span data-ttu-id="61065-133">L’exemple suivant montre comment utiliser le `<clear>` élément avant d’utiliser le `<add>` élément pour ajouter l’écouteur `console` à la `Listeners` collection de la trace.</span><span class="sxs-lookup"><span data-stu-id="61065-133">The following example shows how to use the `<clear>` element before using the `<add>` element to add the listener `console` to the `Listeners` collection for trace.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="false" indentsize="4">  
      <listeners>  
        <clear/>  
        <add name="console"   
          type="System.Diagnostics.ConsoleTraceListener" >  
          <filter type="System.Diagnostics.EventTypeFilter"   
            initializeData="Error" />  
        </add>  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="61065-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61065-134">See also</span></span>

- <xref:System.Diagnostics.Trace.Listeners%2A>
- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.Debug>
- <xref:System.Diagnostics.TraceSource>
- [<span data-ttu-id="61065-135">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="61065-135">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [<span data-ttu-id="61065-136">\<remove></span><span class="sxs-lookup"><span data-stu-id="61065-136">\<remove></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-trace.md)
- [<span data-ttu-id="61065-137">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="61065-137">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
