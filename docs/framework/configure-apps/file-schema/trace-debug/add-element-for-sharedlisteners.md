---
title: Élément <add> pour <sharedListeners>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add
helpviewer_keywords:
- initializeData attribute
- <add> element for <sharedListeners>
- add element for <sharedListeners>
ms.assetid: 1595e1bc-2492-421f-8384-7f382eb8eb57
ms.openlocfilehash: e7934ed5e71005cfd28271298ff6ce1eb8829a0d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59095631"
---
# <a name="add-element-for-sharedlisteners"></a><span data-ttu-id="51e5e-102">\<Ajouter > élément pour \<sharedListeners ></span><span class="sxs-lookup"><span data-stu-id="51e5e-102">\<add> Element for \<sharedListeners></span></span>
<span data-ttu-id="51e5e-103">Ajoute un écouteur à la collection `sharedListeners`.</span><span class="sxs-lookup"><span data-stu-id="51e5e-103">Adds a listener to the `sharedListeners` collection.</span></span> <span data-ttu-id="51e5e-104">`sharedListeners` est une collection d’écouteurs que tout [ \<source >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) ou [ \<trace >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md) peut faire référence.</span><span class="sxs-lookup"><span data-stu-id="51e5e-104">`sharedListeners` is a collection of listeners that any [\<source>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) or [\<trace>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md) can reference.</span></span>  <span data-ttu-id="51e5e-105">Par défaut, les écouteurs dans le `sharedListeners` collection ne sont pas placées dans un `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="51e5e-105">By default, listeners in the `sharedListeners` collection are not placed in a `Listeners` collection.</span></span> <span data-ttu-id="51e5e-106">Ils doivent être ajoutés par un nom pour le [ \<source >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) ou [ \<trace >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md).</span><span class="sxs-lookup"><span data-stu-id="51e5e-106">They must be added by name to the [\<source>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) or [\<trace>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md).</span></span> <span data-ttu-id="51e5e-107">Il n’est pas possible d’obtenir les écouteurs de la `sharedListeners` collection dans le code en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="51e5e-107">It is not possible to get the listeners in the `sharedListeners` collection in code at run time.</span></span>  
  
 <span data-ttu-id="51e5e-108">\<configuration></span><span class="sxs-lookup"><span data-stu-id="51e5e-108">\<configuration></span></span>  
<span data-ttu-id="51e5e-109">&nbsp;&nbsp;\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="51e5e-109">&nbsp;&nbsp;\<system.diagnostics></span></span>  
<span data-ttu-id="51e5e-110">&nbsp;&nbsp;&nbsp;&nbsp;\<sharedListeners > élément</span><span class="sxs-lookup"><span data-stu-id="51e5e-110">&nbsp;&nbsp;&nbsp;&nbsp;\<sharedListeners> Element</span></span>  
<span data-ttu-id="51e5e-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<add></span><span class="sxs-lookup"><span data-stu-id="51e5e-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51e5e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51e5e-112">Syntax</span></span>  
  
```xml  
<add name="name"   
  type="TraceListenerClassName, Version, Culture, PublicKeyToken"  
  initializeData="data"
  traceOutputOptions = "None"
/>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="51e5e-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="51e5e-113">Attributes and Elements</span></span>  
 <span data-ttu-id="51e5e-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="51e5e-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="51e5e-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="51e5e-115">Attributes</span></span>  
  
|<span data-ttu-id="51e5e-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="51e5e-116">Attribute</span></span>|<span data-ttu-id="51e5e-117">Description</span><span class="sxs-lookup"><span data-stu-id="51e5e-117">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="51e5e-118">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="51e5e-118">Required attribute.</span></span><br /><br /> <span data-ttu-id="51e5e-119">Spécifie le nom de l’écouteur est utilisé pour ajouter l’écouteur partagé à une `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="51e5e-119">Specifies the name of the listener that is used to add the shared listener to a `Listeners` collection.</span></span>|  
|`type`|<span data-ttu-id="51e5e-120">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="51e5e-120">Required attribute.</span></span><br /><br /> <span data-ttu-id="51e5e-121">Spécifie le type de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="51e5e-121">Specifies the type of the listener.</span></span> <span data-ttu-id="51e5e-122">Vous devez utiliser une chaîne conforme aux exigences spécifiées dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="51e5e-122">You must use a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|`initializeData`|<span data-ttu-id="51e5e-123">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="51e5e-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="51e5e-124">La chaîne passée au constructeur pour la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="51e5e-124">The string passed to the constructor for the specified class.</span></span>|  
|`traceOutputOptions`|<span data-ttu-id="51e5e-125">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="51e5e-125">Optional attribute.</span></span><br/><br/><span data-ttu-id="51e5e-126">La représentation sous forme de chaîne d’un ou plusieurs <xref:System.Diagnostics.TraceOptions> membres de l’énumération qui indique les données à écrire dans la sortie de trace.</span><span class="sxs-lookup"><span data-stu-id="51e5e-126">The string representation of one or more <xref:System.Diagnostics.TraceOptions> enumeration members that indicates the data to be written to the trace output.</span></span> <span data-ttu-id="51e5e-127">Plusieurs éléments sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="51e5e-127">Multiple items are separated by commas.</span></span> <span data-ttu-id="51e5e-128">La valeur par défaut est « None ».</span><span class="sxs-lookup"><span data-stu-id="51e5e-128">The default value is "None".</span></span>|

### <a name="child-elements"></a><span data-ttu-id="51e5e-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="51e5e-129">Child Elements</span></span>  
  
|<span data-ttu-id="51e5e-130">Élément</span><span class="sxs-lookup"><span data-stu-id="51e5e-130">Element</span></span>|<span data-ttu-id="51e5e-131">Description</span><span class="sxs-lookup"><span data-stu-id="51e5e-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51e5e-132">\<filter></span><span class="sxs-lookup"><span data-stu-id="51e5e-132">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-sharedlisteners.md)|<span data-ttu-id="51e5e-133">Ajoute un filtre à un écouteur dans la collection `sharedListeners`.</span><span class="sxs-lookup"><span data-stu-id="51e5e-133">Adds a filter to a listener in the `sharedListeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="51e5e-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="51e5e-134">Parent Elements</span></span>  
  
|<span data-ttu-id="51e5e-135">Élément</span><span class="sxs-lookup"><span data-stu-id="51e5e-135">Element</span></span>|<span data-ttu-id="51e5e-136">Description</span><span class="sxs-lookup"><span data-stu-id="51e5e-136">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="51e5e-137">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="51e5e-137">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="51e5e-138">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="51e5e-138">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sharedListeners`|<span data-ttu-id="51e5e-139">Une collection d’écouteurs de n’importe quel élément trace ou une source peut faire référence.</span><span class="sxs-lookup"><span data-stu-id="51e5e-139">A collection of listeners that any source or trace element can reference.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="51e5e-140">Notes</span><span class="sxs-lookup"><span data-stu-id="51e5e-140">Remarks</span></span>  
 <span data-ttu-id="51e5e-141">Les classes de l’écouteur fournis avec le .NET Framework dérivent la <xref:System.Diagnostics.TraceListener> classe.</span><span class="sxs-lookup"><span data-stu-id="51e5e-141">The listener classes shipped with the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span> <span data-ttu-id="51e5e-142">La valeur de la `name` attribut est utilisé pour ajouter l’écouteur partagé à une `Listeners` collection pour une trace ou une source de suivi.</span><span class="sxs-lookup"><span data-stu-id="51e5e-142">The value for the `name` attribute is used to add the shared listener to a `Listeners` collection for either a trace or a trace source.</span></span> <span data-ttu-id="51e5e-143">La valeur de la `initializeData` attribut varie selon le type d’écouteur que vous créez.</span><span class="sxs-lookup"><span data-stu-id="51e5e-143">The value for the `initializeData` attribute depends on the type of listener you create.</span></span> <span data-ttu-id="51e5e-144">Pas tous les écouteurs de trace nécessitent que vous spécifiez `initializeData`.</span><span class="sxs-lookup"><span data-stu-id="51e5e-144">Not all trace listeners require that you specify `initializeData`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="51e5e-145">Lorsque vous utilisez le `initializeData` attribut, vous risquez d’obtenir le compilateur Avertissement : « l’attribut 'initializeData' n’est pas déclaré. ».</span><span class="sxs-lookup"><span data-stu-id="51e5e-145">When you use the `initializeData` attribute, you may get the compiler warning "The 'initializeData' attribute is not declared."</span></span> <span data-ttu-id="51e5e-146">Cet avertissement se produit parce que les paramètres de configuration sont validés par rapport à la classe de base abstraite <xref:System.Diagnostics.TraceListener>, qui ne reconnaît pas le `initializeData` attribut.</span><span class="sxs-lookup"><span data-stu-id="51e5e-146">This warning occurs because the configuration settings are validated against the abstract base class <xref:System.Diagnostics.TraceListener>, which does not recognize the `initializeData` attribute.</span></span> <span data-ttu-id="51e5e-147">En règle générale, vous pouvez ignorer cet avertissement pour les implémentations d’écouteur de trace qui ont un constructeur qui accepte un paramètre.</span><span class="sxs-lookup"><span data-stu-id="51e5e-147">Typically, you can ignore this warning for trace listener implementations that have a constructor that takes a parameter.</span></span>  
  
 <span data-ttu-id="51e5e-148">Le tableau suivant présente les écouteurs de trace qui sont inclus avec le .NET Framework et décrit la valeur de leur `initializeData` attributs.</span><span class="sxs-lookup"><span data-stu-id="51e5e-148">The following table shows the trace listeners that are included with the .NET Framework and describes the value of their `initializeData` attributes.</span></span>  
  
|<span data-ttu-id="51e5e-149">Classe d’écouteur de trace</span><span class="sxs-lookup"><span data-stu-id="51e5e-149">Trace listener class</span></span>|<span data-ttu-id="51e5e-150">valeur de l’attribut initializeData</span><span class="sxs-lookup"><span data-stu-id="51e5e-150">initializeData attribute value</span></span>|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener>|<span data-ttu-id="51e5e-151">Le `useErrorStream` valeur pour le <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="51e5e-151">The `useErrorStream` value for the <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructor.</span></span>  <span data-ttu-id="51e5e-152">Définir le `initializeData` l’attribut «`true`« écrire trace et debug de sortie pour le flux d’erreurs standard ; affectez-lui la valeur »`false`» à écrire dans le flux de sortie standard.</span><span class="sxs-lookup"><span data-stu-id="51e5e-152">Set the `initializeData` attribute to "`true`" to write trace and debug output to the standard error stream; set it to "`false`" to write to the standard output stream.</span></span>|  
|<xref:System.Diagnostics.DelimitedListTraceListener>|<span data-ttu-id="51e5e-153">Le nom du fichier le <xref:System.Diagnostics.DelimitedListTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="51e5e-153">The name of the file the <xref:System.Diagnostics.DelimitedListTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|<span data-ttu-id="51e5e-154">Le nom d’une source existante de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="51e5e-154">The name of an existing event log source.</span></span>|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|<span data-ttu-id="51e5e-155">Le nom du fichier qui le <xref:System.Diagnostics.EventSchemaTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="51e5e-155">The name of the file that the <xref:System.Diagnostics.EventSchemaTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|<span data-ttu-id="51e5e-156">Le nom du fichier qui le <xref:System.Diagnostics.TextWriterTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="51e5e-156">The name of the file that the <xref:System.Diagnostics.TextWriterTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.XmlWriterTraceListener>|<span data-ttu-id="51e5e-157">Le nom du fichier qui le <xref:System.Diagnostics.XmlWriterTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="51e5e-157">The name of the file that the <xref:System.Diagnostics.XmlWriterTraceListener> writes to.</span></span>|  
  
## <a name="configuration-file"></a><span data-ttu-id="51e5e-158">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="51e5e-158">Configuration File</span></span>  
 <span data-ttu-id="51e5e-159">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="51e5e-159">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51e5e-160">Exemple</span><span class="sxs-lookup"><span data-stu-id="51e5e-160">Example</span></span>  
 <span data-ttu-id="51e5e-161">L’exemple suivant montre comment utiliser `<add>` éléments à ajouter le <xref:System.Diagnostics.TextWriterTraceListener> `textListener` à la `sharedListeners` collection.</span><span class="sxs-lookup"><span data-stu-id="51e5e-161">The following example shows how to use `<add>` elements to add the <xref:System.Diagnostics.TextWriterTraceListener>`textListener` to the `sharedListeners` collection.</span></span>   <span data-ttu-id="51e5e-162">`textListener` est ajouté par nom à la `Listeners` collection pour la source de suivi `TraceSourceApp`.</span><span class="sxs-lookup"><span data-stu-id="51e5e-162">`textListener` is added by name to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span> <span data-ttu-id="51e5e-163">Le `textListener` écouteur écrit la sortie de trace dans le fichier myListener.log.</span><span class="sxs-lookup"><span data-stu-id="51e5e-163">The `textListener` listener writes trace output to the file myListener.log.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
          <remove name="Default"/>  
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
  
## <a name="see-also"></a><span data-ttu-id="51e5e-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51e5e-164">See also</span></span>

- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="51e5e-165">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="51e5e-165">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [<span data-ttu-id="51e5e-166">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="51e5e-166">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
