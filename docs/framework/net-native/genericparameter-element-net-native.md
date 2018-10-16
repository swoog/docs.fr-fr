---
title: '&lt;GenericParameter&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: cbd49732-3615-49a5-a900-f96947cdc3e6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dd0d9851f62381a16f628607c326c6690492628b
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347849"
---
# <a name="ltgenericparametergt-element-net-native"></a><span data-ttu-id="01389-102">&lt;GenericParameter&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="01389-102">&lt;GenericParameter&gt; Element (.NET Native)</span></span>
<span data-ttu-id="01389-103">Applique la stratégie au type de paramètre d'un type ou d'une méthode générique.</span><span class="sxs-lookup"><span data-stu-id="01389-103">Applies policy to the parameter type of a generic type or method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01389-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01389-104">Syntax</span></span>  
  
```xml  
<GenericParameter Name="generic_parameter_name"  
                  Activate="policy_type"  
                  Browse="policy_type"  
                  Dynamic="policy_type"  
                  Serialize="policy_type" />  
                  DataContractSerializer="policy_type"  
                  DataContractJsonSerializer="policy_type"  
                  XmlSerializer="policy_type"  
                  MarshalObject="policy_type"  
                  MarshalDelegate="policy_type"  
                  MarshalStructure="policy_type"  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="01389-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="01389-105">Attributes and Elements</span></span>  
 <span data-ttu-id="01389-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="01389-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="01389-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="01389-107">Attributes</span></span>  
  
|<span data-ttu-id="01389-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="01389-108">Attribute</span></span>|<span data-ttu-id="01389-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="01389-109">Attribute type</span></span>|<span data-ttu-id="01389-110">Description</span><span class="sxs-lookup"><span data-stu-id="01389-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="01389-111">Général</span><span class="sxs-lookup"><span data-stu-id="01389-111">General</span></span>|<span data-ttu-id="01389-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="01389-112">Required attribute.</span></span> <span data-ttu-id="01389-113">Nom du paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="01389-113">The name of the generic parameter.</span></span> <span data-ttu-id="01389-114">Par exemple, pour le délégué générique <xref:System.Func%603>, la valeur de l'attribut `Name` est « TResult » pour appliquer la stratégie runtime à la valeur de retour du délégué.</span><span class="sxs-lookup"><span data-stu-id="01389-114">For example, for the generic delegate <xref:System.Func%603>, the value of the `Name` attribute is "TResult" to apply runtime policy to the delegate's return value.</span></span>|  
|`Activate`|<span data-ttu-id="01389-115">Réflexion</span><span class="sxs-lookup"><span data-stu-id="01389-115">Reflection</span></span>|<span data-ttu-id="01389-116">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-116">Optional attribute.</span></span> <span data-ttu-id="01389-117">Contrôle l'accès aux constructeurs pour permettre l'activation d'instances au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="01389-117">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="01389-118">Réflexion</span><span class="sxs-lookup"><span data-stu-id="01389-118">Reflection</span></span>|<span data-ttu-id="01389-119">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-119">Optional attribute.</span></span> <span data-ttu-id="01389-120">Contrôle la demande d'informations sur les éléments de programme, mais ne permet pas l'accès au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="01389-120">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="01389-121">Réflexion</span><span class="sxs-lookup"><span data-stu-id="01389-121">Reflection</span></span>|<span data-ttu-id="01389-122">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-122">Optional attribute.</span></span> <span data-ttu-id="01389-123">Contrôle l'accès à l'exécution à tous les membres de types, y compris les constructeurs, les méthodes, les champs, les propriétés et les événements, pour permettre la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="01389-123">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="01389-124">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="01389-124">Serialization</span></span>|<span data-ttu-id="01389-125">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-125">Optional attribute.</span></span> <span data-ttu-id="01389-126">Contrôle l'accès au moment de l'exécution aux constructeurs, champs et propriétés, pour permettre la sérialisation et la désérialisation des instances de types par des bibliothèques comme le sérialiseur JSON Newtonsoft.</span><span class="sxs-lookup"><span data-stu-id="01389-126">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="01389-127">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="01389-127">Serialization</span></span>|<span data-ttu-id="01389-128">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-128">Optional attribute.</span></span> <span data-ttu-id="01389-129">Contrôle la stratégie pour la sérialisation qui utilise la classe <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="01389-129">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="01389-130">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="01389-130">Serialization</span></span>|<span data-ttu-id="01389-131">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-131">Optional attribute.</span></span> <span data-ttu-id="01389-132">Contrôle la stratégie pour la sérialisation JSON qui utilise la classe <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="01389-132">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="01389-133">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="01389-133">Serialization</span></span>|<span data-ttu-id="01389-134">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-134">Optional attribute.</span></span> <span data-ttu-id="01389-135">Contrôle la stratégie pour la sérialisation XML qui utilise la classe <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="01389-135">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="01389-136">Interop</span><span class="sxs-lookup"><span data-stu-id="01389-136">Interop</span></span>|<span data-ttu-id="01389-137">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-137">Optional attribute.</span></span> <span data-ttu-id="01389-138">Contrôle la stratégie pour le marshaling des types de références vers Windows Runtime et COM.</span><span class="sxs-lookup"><span data-stu-id="01389-138">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="01389-139">Interop</span><span class="sxs-lookup"><span data-stu-id="01389-139">Interop</span></span>|<span data-ttu-id="01389-140">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-140">Optional attribute.</span></span> <span data-ttu-id="01389-141">Contrôle la stratégie pour le marshaling des types de délégués comme pointeurs de fonction vers du code natif.</span><span class="sxs-lookup"><span data-stu-id="01389-141">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="01389-142">Interop</span><span class="sxs-lookup"><span data-stu-id="01389-142">Interop</span></span>|<span data-ttu-id="01389-143">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="01389-143">Optional attribute.</span></span> <span data-ttu-id="01389-144">Contrôle la stratégie pour le marshaling des types de valeurs vers du code natif.</span><span class="sxs-lookup"><span data-stu-id="01389-144">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="01389-145">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="01389-145">Name attribute</span></span>  
  
|<span data-ttu-id="01389-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="01389-146">Value</span></span>|<span data-ttu-id="01389-147">Description</span><span class="sxs-lookup"><span data-stu-id="01389-147">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="01389-148">*nom_paramètre_générique*</span><span class="sxs-lookup"><span data-stu-id="01389-148">*generic_parameter_name*</span></span>|<span data-ttu-id="01389-149">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="01389-149">Required attribute.</span></span> <span data-ttu-id="01389-150">Nom du paramètre de type générique.</span><span class="sxs-lookup"><span data-stu-id="01389-150">The name of the generic type parameter.</span></span> <span data-ttu-id="01389-151">Par exemple, pour le délégué générique <xref:System.Func%603>, la valeur *nom_paramètre_générique* « TResult » applique la stratégie runtime à la valeur de retour du délégué.</span><span class="sxs-lookup"><span data-stu-id="01389-151">For example, for the generic delegate <xref:System.Func%603>, a *generic_parameter_name* value of "TResult" applies runtime policy to the delegate's return value.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="01389-152">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="01389-152">All other attributes</span></span>  
  
|<span data-ttu-id="01389-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="01389-153">Value</span></span>|<span data-ttu-id="01389-154">Description</span><span class="sxs-lookup"><span data-stu-id="01389-154">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="01389-155">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="01389-155">*policy_setting*</span></span>|<span data-ttu-id="01389-156">Paramètre à appliquer à ce type de stratégie.</span><span class="sxs-lookup"><span data-stu-id="01389-156">The setting to apply to this policy type.</span></span> <span data-ttu-id="01389-157">Les valeurs possibles sont `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal` et `Required All`.</span><span class="sxs-lookup"><span data-stu-id="01389-157">Possible values are `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="01389-158">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="01389-158">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="01389-159">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="01389-159">Child Elements</span></span>  
 <span data-ttu-id="01389-160">Aucun.</span><span class="sxs-lookup"><span data-stu-id="01389-160">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="01389-161">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="01389-161">Parent Elements</span></span>  
  
|<span data-ttu-id="01389-162">Élément</span><span class="sxs-lookup"><span data-stu-id="01389-162">Element</span></span>|<span data-ttu-id="01389-163">Description</span><span class="sxs-lookup"><span data-stu-id="01389-163">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="01389-164">\<Method></span><span class="sxs-lookup"><span data-stu-id="01389-164">\<Method></span></span>](../../../docs/framework/net-native/method-element-net-native.md)|<span data-ttu-id="01389-165">Applique une stratégie de réflexion runtime à un constructeur ou à une méthode.</span><span class="sxs-lookup"><span data-stu-id="01389-165">Applies runtime reflection policy to a constructor or method.</span></span>|  
|[<span data-ttu-id="01389-166">\<Type></span><span class="sxs-lookup"><span data-stu-id="01389-166">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="01389-167">Applique la stratégie de réflexion runtime à un type particulier, tel qu'une classe ou une structure.</span><span class="sxs-lookup"><span data-stu-id="01389-167">Applies runtime reflection policy to a particular type, such as a class or structure.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="01389-168">Notes</span><span class="sxs-lookup"><span data-stu-id="01389-168">Remarks</span></span>  
 <span data-ttu-id="01389-169">L’élément `<GenericParameter>` est un enfant de l’élément [\<Method>](../../../docs/framework/net-native/method-element-net-native.md) ou [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) et permet d’appliquer la stratégie à un paramètre de type générique particulier, qui est spécifié par son nom dans la signature de type ou de méthode générique.</span><span class="sxs-lookup"><span data-stu-id="01389-169">The `<GenericParameter>` element is a child of either the [\<Method>](../../../docs/framework/net-native/method-element-net-native.md) or [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) element and is used to apply policy to a particular generic type parameter, which is specified by its name in the generic type or method signature.</span></span>  
  
 <span data-ttu-id="01389-170">L'élément `<GenericParameter>` est particulièrement utile quand il est employé avec des sérialiseurs.</span><span class="sxs-lookup"><span data-stu-id="01389-170">The `<GenericParameter>` element is most useful when used with serializers.</span></span> <span data-ttu-id="01389-171">L’exemple suivant utilise l’élément `<GenericParameter>` pour appliquer la stratégie au type `T` dans les appels aux surcharges de méthode [JsonConvert.DeserializeObject\<T>(String)](https://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_JsonConvert_DeserializeObject__1.htm) du sérialiseur JSON Newtonsoft.</span><span class="sxs-lookup"><span data-stu-id="01389-171">The following example uses the `<GenericParameter>` element to apply policy to the type `T` in calls to the NewtonSoft JSON serializer's [JsonConvert.DeserializeObject\<T>(String)](https://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_JsonConvert_DeserializeObject__1.htm) method overloads.</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <Type Name="Newtonsoft.Json.JsonConvert" >  
      <Method Name="DeserializeObject{T}">  
         <GenericParameter Name="T" Serialize="Required All" />  
      </Method>  
   </Type>  
</Directives>  
```  
  
## <a name="see-also"></a><span data-ttu-id="01389-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01389-172">See Also</span></span>  
 [<span data-ttu-id="01389-173">\<Method>, élément</span><span class="sxs-lookup"><span data-stu-id="01389-173">\<Method> Element</span></span>](../../../docs/framework/net-native/method-element-net-native.md)  
 [<span data-ttu-id="01389-174">\<Type > élément</span><span class="sxs-lookup"><span data-stu-id="01389-174">\<Type> Element</span></span>](../../../docs/framework/net-native/type-element-net-native.md)  
 [<span data-ttu-id="01389-175">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="01389-175">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)  
 [<span data-ttu-id="01389-176">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="01389-176">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)  
 [<span data-ttu-id="01389-177">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="01389-177">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
