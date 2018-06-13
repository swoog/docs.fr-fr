---
title: '&lt;TypeParameter&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: d37bb1b7-1ddc-4c6d-8ecf-583f804a2479
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5cc2faf9768b60d49f573720df8763813000a6b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33393866"
---
# <a name="lttypeparametergt-element-net-native"></a><span data-ttu-id="f6efb-102">&lt;TypeParameter&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="f6efb-102">&lt;TypeParameter&gt; Element (.NET Native)</span></span>
<span data-ttu-id="f6efb-103">Applique la stratégie au type représenté par un argument Type passé à une méthode.</span><span class="sxs-lookup"><span data-stu-id="f6efb-103">Applies policy to the type represented by a Type argument passed to a method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6efb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6efb-104">Syntax</span></span>  
  
```xml  
<Parameter Name="parameter_name"  
           Activate="policy_type"  
           Browse="policy_type"  
           Dynamic="policy_type"  
           Serialize="policy_type"  
           DataContractSerializer="policy_type"  
           DataContractJsonSerializer="policy_type"  
           XmlSerializer="policy_type"  
           MarshalObject="policy_type"  
           MarshalDelegate="policy_type"  
           MarshalStructure="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f6efb-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f6efb-105">Attributes and Elements</span></span>  
 <span data-ttu-id="f6efb-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f6efb-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f6efb-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="f6efb-107">Attributes</span></span>  
  
|<span data-ttu-id="f6efb-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="f6efb-108">Attribute</span></span>|<span data-ttu-id="f6efb-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="f6efb-109">Attribute type</span></span>|<span data-ttu-id="f6efb-110">Description</span><span class="sxs-lookup"><span data-stu-id="f6efb-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="f6efb-111">Général</span><span class="sxs-lookup"><span data-stu-id="f6efb-111">General</span></span>|<span data-ttu-id="f6efb-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="f6efb-112">Required attribute.</span></span> <span data-ttu-id="f6efb-113">Nom du paramètre de type <xref:System.Type>.</span><span class="sxs-lookup"><span data-stu-id="f6efb-113">The name of the parameter of type <xref:System.Type>.</span></span> <span data-ttu-id="f6efb-114">Par exemple, pour la signature de méthode `Type.GetInterfaceMap(Type interfaceType)`, la valeur de l'attribut `Name` est « interfaceType ».</span><span class="sxs-lookup"><span data-stu-id="f6efb-114">For example, for the method signature `Type.GetInterfaceMap(Type interfaceType)`, the value of the `Name` attribute is "interfaceType".</span></span>|  
|`Activate`|<span data-ttu-id="f6efb-115">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f6efb-115">Reflection</span></span>|<span data-ttu-id="f6efb-116">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-116">Optional attribute.</span></span> <span data-ttu-id="f6efb-117">Contrôle l'accès aux constructeurs pour permettre l'activation d'instances au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="f6efb-117">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="f6efb-118">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f6efb-118">Reflection</span></span>|<span data-ttu-id="f6efb-119">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-119">Optional attribute.</span></span> <span data-ttu-id="f6efb-120">Contrôle la demande d'informations sur les éléments de programme, mais ne permet pas l'accès au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="f6efb-120">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="f6efb-121">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f6efb-121">Reflection</span></span>|<span data-ttu-id="f6efb-122">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-122">Optional attribute.</span></span> <span data-ttu-id="f6efb-123">Contrôle l'accès à l'exécution à tous les membres de types, y compris les constructeurs, les méthodes, les champs, les propriétés et les événements, pour permettre la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="f6efb-123">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="f6efb-124">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f6efb-124">Serialization</span></span>|<span data-ttu-id="f6efb-125">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-125">Optional attribute.</span></span> <span data-ttu-id="f6efb-126">Contrôle l'accès au moment de l'exécution aux constructeurs, champs et propriétés, pour permettre la sérialisation et la désérialisation des instances de types par des bibliothèques comme le sérialiseur JSON Newtonsoft.</span><span class="sxs-lookup"><span data-stu-id="f6efb-126">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="f6efb-127">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f6efb-127">Serialization</span></span>|<span data-ttu-id="f6efb-128">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-128">Optional attribute.</span></span> <span data-ttu-id="f6efb-129">Contrôle la stratégie pour la sérialisation qui utilise la classe <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f6efb-129">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="f6efb-130">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f6efb-130">Serialization</span></span>|<span data-ttu-id="f6efb-131">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-131">Optional attribute.</span></span> <span data-ttu-id="f6efb-132">Contrôle la stratégie pour la sérialisation JSON qui utilise la classe <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f6efb-132">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="f6efb-133">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f6efb-133">Serialization</span></span>|<span data-ttu-id="f6efb-134">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-134">Optional attribute.</span></span> <span data-ttu-id="f6efb-135">Contrôle la stratégie pour la sérialisation XML qui utilise la classe <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f6efb-135">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="f6efb-136">Interop</span><span class="sxs-lookup"><span data-stu-id="f6efb-136">Interop</span></span>|<span data-ttu-id="f6efb-137">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-137">Optional attribute.</span></span> <span data-ttu-id="f6efb-138">Contrôle la stratégie pour le marshaling des types de références vers Windows Runtime et COM.</span><span class="sxs-lookup"><span data-stu-id="f6efb-138">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="f6efb-139">Interop</span><span class="sxs-lookup"><span data-stu-id="f6efb-139">Interop</span></span>|<span data-ttu-id="f6efb-140">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-140">Optional attribute.</span></span> <span data-ttu-id="f6efb-141">Contrôle la stratégie pour le marshaling des types de délégués comme pointeurs de fonction vers du code natif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-141">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="f6efb-142">Interop</span><span class="sxs-lookup"><span data-stu-id="f6efb-142">Interop</span></span>|<span data-ttu-id="f6efb-143">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-143">Optional attribute.</span></span> <span data-ttu-id="f6efb-144">Contrôle la stratégie pour le marshaling des types de valeurs vers du code natif.</span><span class="sxs-lookup"><span data-stu-id="f6efb-144">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="f6efb-145">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="f6efb-145">Name attribute</span></span>  
  
|<span data-ttu-id="f6efb-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6efb-146">Value</span></span>|<span data-ttu-id="f6efb-147">Description</span><span class="sxs-lookup"><span data-stu-id="f6efb-147">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f6efb-148">*nom_paramètre*</span><span class="sxs-lookup"><span data-stu-id="f6efb-148">*parameter_name*</span></span>|<span data-ttu-id="f6efb-149">Nom du paramètre de type <xref:System.Type>.</span><span class="sxs-lookup"><span data-stu-id="f6efb-149">The name of the parameter of type <xref:System.Type>.</span></span> <span data-ttu-id="f6efb-150">Par exemple, pour la signature de méthode `Type.GetInterfaceMap(Type interfaceType)`, la valeur de l'attribut `Name` est « interfaceType ».</span><span class="sxs-lookup"><span data-stu-id="f6efb-150">For example, for the method signature `Type.GetInterfaceMap(Type interfaceType)`, the value of the `Name` attribute is "interfaceType".</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="f6efb-151">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="f6efb-151">All other attributes</span></span>  
  
|<span data-ttu-id="f6efb-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6efb-152">Value</span></span>|<span data-ttu-id="f6efb-153">Description</span><span class="sxs-lookup"><span data-stu-id="f6efb-153">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f6efb-154">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="f6efb-154">*policy_setting*</span></span>|<span data-ttu-id="f6efb-155">Paramètre à appliquer à ce type de stratégie.</span><span class="sxs-lookup"><span data-stu-id="f6efb-155">The setting to apply to this policy type.</span></span> <span data-ttu-id="f6efb-156">Les valeurs possibles sont `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal` et `Required All`.</span><span class="sxs-lookup"><span data-stu-id="f6efb-156">Possible values are `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="f6efb-157">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f6efb-157">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f6efb-158">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f6efb-158">Child Elements</span></span>  
 <span data-ttu-id="f6efb-159">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f6efb-159">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f6efb-160">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f6efb-160">Parent Elements</span></span>  
  
|<span data-ttu-id="f6efb-161">Élément</span><span class="sxs-lookup"><span data-stu-id="f6efb-161">Element</span></span>|<span data-ttu-id="f6efb-162">Description</span><span class="sxs-lookup"><span data-stu-id="f6efb-162">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f6efb-163">\<Method></span><span class="sxs-lookup"><span data-stu-id="f6efb-163">\<Method></span></span>](../../../docs/framework/net-native/method-element-net-native.md)|<span data-ttu-id="f6efb-164">Applique une stratégie de réflexion runtime à un constructeur ou à une méthode.</span><span class="sxs-lookup"><span data-stu-id="f6efb-164">Applies runtime reflection policy to a constructor or method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6efb-165">Notes</span><span class="sxs-lookup"><span data-stu-id="f6efb-165">Remarks</span></span>  
 <span data-ttu-id="f6efb-166">L’élément `<TypeParameter>` est similaire à l’élément [\<Parameter>](../../../docs/framework/net-native/parameter-element-net-native.md), à ceci près qu’il peut uniquement être appliqué à des paramètres de type <xref:System.Type>.</span><span class="sxs-lookup"><span data-stu-id="f6efb-166">The `<TypeParameter>` element is similar to the [\<Parameter>](../../../docs/framework/net-native/parameter-element-net-native.md) element, except that it can be applied only to parameters of type <xref:System.Type>.</span></span> <span data-ttu-id="f6efb-167">Il applique la stratégie à tout type représenté au moment de l'exécution par l'argument de type spécifié par l'attribut `Name`.</span><span class="sxs-lookup"><span data-stu-id="f6efb-167">It applies policy to whatever type is represented at run time by the type argument specified by the `Name` attribute.</span></span>  
  
 <span data-ttu-id="f6efb-168">Par exemple, le sérialiseur JSON NewtonSoft inclut une méthode `JsonConvert.DeserializeObject(String value, Type type)` statique.</span><span class="sxs-lookup"><span data-stu-id="f6efb-168">For example, the NewtonSoft JSON serializer includes a static `JsonConvert.DeserializeObject(String value, Type type)` method.</span></span> <span data-ttu-id="f6efb-169">Les directives de réflexion suivantes :</span><span class="sxs-lookup"><span data-stu-id="f6efb-169">The following reflection directives:</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <Type Name="Newtonsoft.Json.JsonConvert" >  
      <Method Name="DeserializeObject">  
         <GenericParameter Name="type" Serialize="Required All" />  
      </Method>  
   </Type>  
</Directives>  
```  
  
 <span data-ttu-id="f6efb-170">spécifient que les métadonnées pour le type de runtime représenté par l’argument `type` doivent être accessibles pour la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="f6efb-170">specify that metadata for the runtime type represented by the `type` argument should be made available for serialization.</span></span> <span data-ttu-id="f6efb-171">Si ces directives runtime s'appliquent à un projet qui inclut le code source suivant :</span><span class="sxs-lookup"><span data-stu-id="f6efb-171">If these runtime directives apply to a project that includes the following source code:</span></span>  
  
```csharp  
Type t = typeof(StockQuote);  
Object obj = JsonConvert.DeserializeObject(data, t);  
```  
  
 <span data-ttu-id="f6efb-172">les directives de réflexion rendent les métadonnées pour le type `StockQuote` disponibles pour le sérialiseur JSON NewtonSoft au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="f6efb-172">the reflection directives make metadata for the `StockQuote` type available for the NewtonSoft JSON serializer at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6efb-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6efb-173">See Also</span></span>  
 [<span data-ttu-id="f6efb-174">\<Method>, élément</span><span class="sxs-lookup"><span data-stu-id="f6efb-174">\<Method> Element</span></span>](../../../docs/framework/net-native/method-element-net-native.md)  
 [<span data-ttu-id="f6efb-175">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="f6efb-175">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)  
 [<span data-ttu-id="f6efb-176">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="f6efb-176">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)  
 [<span data-ttu-id="f6efb-177">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="f6efb-177">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
