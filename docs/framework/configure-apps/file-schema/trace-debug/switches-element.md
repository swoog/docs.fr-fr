---
title: Élément <switches>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/switches
- http://schemas.microsoft.com/.NetConfiguration/v2.0#switches
helpviewer_keywords:
- <switches> element
- switches element
- trace switches, <switches> element
ms.assetid: 4cf36786-b89a-40e2-a0f1-86bb9b783343
ms.openlocfilehash: 44f5c918f19f84daf827ad4e8f3b6bfbc3e9f439
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196526"
---
# <a name="switches-element"></a><span data-ttu-id="b30d9-102">\<commutateurs > élément</span><span class="sxs-lookup"><span data-stu-id="b30d9-102">\<switches> Element</span></span>
<span data-ttu-id="b30d9-103">Contient des commutateurs de traçage et le niveau auquel ils sont définis.</span><span class="sxs-lookup"><span data-stu-id="b30d9-103">Contains trace switches and the level where the trace switches are set.</span></span>  
  
 <span data-ttu-id="b30d9-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="b30d9-104">\<configuration></span></span>  
<span data-ttu-id="b30d9-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="b30d9-105">\<system.diagnostics></span></span>  
<span data-ttu-id="b30d9-106">\<switches></span><span class="sxs-lookup"><span data-stu-id="b30d9-106">\<switches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b30d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b30d9-107">Syntax</span></span>  
  
```xml  
      <switches>   
</switches>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b30d9-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b30d9-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b30d9-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b30d9-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b30d9-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="b30d9-110">Attributes</span></span>  
 <span data-ttu-id="b30d9-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b30d9-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b30d9-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b30d9-112">Child Elements</span></span>  
  
|<span data-ttu-id="b30d9-113">Élément</span><span class="sxs-lookup"><span data-stu-id="b30d9-113">Element</span></span>|<span data-ttu-id="b30d9-114">Description</span><span class="sxs-lookup"><span data-stu-id="b30d9-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b30d9-115">\<add></span><span class="sxs-lookup"><span data-stu-id="b30d9-115">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-switches.md)|<span data-ttu-id="b30d9-116">Spécifie le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="b30d9-116">Specifies the level where a trace switch is set.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b30d9-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b30d9-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b30d9-118">Élément</span><span class="sxs-lookup"><span data-stu-id="b30d9-118">Element</span></span>|<span data-ttu-id="b30d9-119">Description</span><span class="sxs-lookup"><span data-stu-id="b30d9-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="b30d9-120">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b30d9-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`System.diagnostics`|<span data-ttu-id="b30d9-121">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="b30d9-121">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b30d9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b30d9-122">Remarks</span></span>  
 <span data-ttu-id="b30d9-123">Vous pouvez modifier le niveau d’un commutateur de trace en le plaçant dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="b30d9-123">You can change the level of a trace switch by putting it in a configuration file.</span></span> <span data-ttu-id="b30d9-124">Si le commutateur est un <xref:System.Diagnostics.BooleanSwitch>, vous pouvez l’activer et désactiver.</span><span class="sxs-lookup"><span data-stu-id="b30d9-124">If the switch is a <xref:System.Diagnostics.BooleanSwitch>, you can turn it on and off.</span></span> <span data-ttu-id="b30d9-125">Si le commutateur est un <xref:System.Diagnostics.TraceSwitch>, vous pouvez attribuer différents niveaux pour pouvoir spécifier les types de la trace de messages ou de débogage les sorties de l’application.</span><span class="sxs-lookup"><span data-stu-id="b30d9-125">If the switch is a <xref:System.Diagnostics.TraceSwitch>, you can assign different levels to it to specify the types of trace or debug messages the application outputs.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b30d9-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="b30d9-126">Example</span></span>  
 <span data-ttu-id="b30d9-127">L’exemple suivant montre comment utiliser le  **\<basculer >** élément à définir le `General` commutateur de trace pour la <xref:System.Diagnostics.TraceLevel> niveau et activer le `Data` commutateur de trace booléen.</span><span class="sxs-lookup"><span data-stu-id="b30d9-127">The following example shows how to use the **\<switch>** element to set the `General` trace switch to the <xref:System.Diagnostics.TraceLevel> level, and enable the `Data` Boolean trace switch.</span></span>  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <switches>  
         <add name="General" value="4" />  
         <add name="Data" value="1" />  
      </switches>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b30d9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b30d9-128">See also</span></span>

- <xref:System.Diagnostics.Switch>
- <xref:System.Diagnostics.TraceSwitch>
- <xref:System.Diagnostics.BooleanSwitch>
- [<span data-ttu-id="b30d9-129">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="b30d9-129">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
