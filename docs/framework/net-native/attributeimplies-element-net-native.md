---
title: <AttributeImplies> Élément (.NET Native)
ms.date: 03/30/2017
ms.assetid: 82db7193-a860-418b-84fc-fff2fdf2e025
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d59f1f48be19a21ccc7ee5bb73cebfffc387fec2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165059"
---
# <a name="attributeimplies-element-net-native"></a><span data-ttu-id="f8c55-102">\<AttributeImplies >, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="f8c55-102">\<AttributeImplies> Element (.NET Native)</span></span>
<span data-ttu-id="f8c55-103">Définit la stratégie pour les éléments de code auxquels l'attribut conteneur est appliqué.</span><span class="sxs-lookup"><span data-stu-id="f8c55-103">Defines policy for code elements the containing attribute is applied to.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8c55-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8c55-104">Syntax</span></span>  
  
```xml  
<AttributeImplies Activate="policy_type"  
                  Browse="policy_type"  
                  Dynamic="policy_type"  
                  Serialize="policy_type"   
                  DataContractSerializer="policy_setting"  
                  DataContractJsonSerializer="policy_setting"  
                  XmlSerializer="policy_setting"  
                  MarshalObject="policy_setting"  
                  MarshalDelegate="policy_setting"  
                  MarshalStructure="policy_setting" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f8c55-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f8c55-105">Attributes and Elements</span></span>  
 <span data-ttu-id="f8c55-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f8c55-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f8c55-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="f8c55-107">Attributes</span></span>  
  
|<span data-ttu-id="f8c55-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="f8c55-108">Attribute</span></span>|<span data-ttu-id="f8c55-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="f8c55-109">Attribute type</span></span>|<span data-ttu-id="f8c55-110">Description</span><span class="sxs-lookup"><span data-stu-id="f8c55-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Activate`|<span data-ttu-id="f8c55-111">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f8c55-111">Reflection</span></span>|<span data-ttu-id="f8c55-112">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-112">Optional attribute.</span></span> <span data-ttu-id="f8c55-113">Contrôle l'accès aux constructeurs pour permettre l'activation d'instances au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="f8c55-113">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="f8c55-114">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f8c55-114">Reflection</span></span>|<span data-ttu-id="f8c55-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-115">Optional attribute.</span></span> <span data-ttu-id="f8c55-116">Contrôle la demande d'informations sur les éléments de programme, mais ne permet pas l'accès au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="f8c55-116">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="f8c55-117">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f8c55-117">Reflection</span></span>|<span data-ttu-id="f8c55-118">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-118">Optional attribute.</span></span> <span data-ttu-id="f8c55-119">Contrôle l'accès à l'exécution à tous les membres de types, y compris les constructeurs, les méthodes, les champs, les propriétés et les événements, pour permettre la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="f8c55-119">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="f8c55-120">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f8c55-120">Serialization</span></span>|<span data-ttu-id="f8c55-121">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-121">Optional attribute.</span></span> <span data-ttu-id="f8c55-122">Contrôle l'accès au moment de l'exécution aux constructeurs, champs et propriétés, pour permettre la sérialisation et la désérialisation des instances de types par des bibliothèques comme le sérialiseur JSON Newtonsoft.</span><span class="sxs-lookup"><span data-stu-id="f8c55-122">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="f8c55-123">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f8c55-123">Serialization</span></span>|<span data-ttu-id="f8c55-124">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-124">Optional attribute.</span></span> <span data-ttu-id="f8c55-125">Contrôle la stratégie pour la sérialisation qui utilise la classe <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f8c55-125">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="f8c55-126">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f8c55-126">Serialization</span></span>|<span data-ttu-id="f8c55-127">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-127">Optional attribute.</span></span> <span data-ttu-id="f8c55-128">Contrôle la stratégie pour la sérialisation JSON qui utilise la classe <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f8c55-128">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="f8c55-129">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="f8c55-129">Serialization</span></span>|<span data-ttu-id="f8c55-130">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-130">Optional attribute.</span></span> <span data-ttu-id="f8c55-131">Contrôle la stratégie pour la sérialisation XML qui utilise la classe <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f8c55-131">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="f8c55-132">Interop</span><span class="sxs-lookup"><span data-stu-id="f8c55-132">Interop</span></span>|<span data-ttu-id="f8c55-133">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-133">Optional attribute.</span></span> <span data-ttu-id="f8c55-134">Contrôle la stratégie pour le marshaling des types de références vers Windows Runtime et COM.</span><span class="sxs-lookup"><span data-stu-id="f8c55-134">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="f8c55-135">Interop</span><span class="sxs-lookup"><span data-stu-id="f8c55-135">Interop</span></span>|<span data-ttu-id="f8c55-136">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-136">Optional attribute.</span></span> <span data-ttu-id="f8c55-137">Contrôle la stratégie pour le marshaling des types de délégués comme pointeurs de fonction vers du code natif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-137">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="f8c55-138">Interop</span><span class="sxs-lookup"><span data-stu-id="f8c55-138">Interop</span></span>|<span data-ttu-id="f8c55-139">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-139">Optional attribute.</span></span> <span data-ttu-id="f8c55-140">Contrôle la stratégie pour le marshaling des types de valeurs vers du code natif.</span><span class="sxs-lookup"><span data-stu-id="f8c55-140">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="all-attributes"></a><span data-ttu-id="f8c55-141">Tous les attributs</span><span class="sxs-lookup"><span data-stu-id="f8c55-141">All attributes</span></span>  
  
|<span data-ttu-id="f8c55-142">Value</span><span class="sxs-lookup"><span data-stu-id="f8c55-142">Value</span></span>|<span data-ttu-id="f8c55-143">Description</span><span class="sxs-lookup"><span data-stu-id="f8c55-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f8c55-144">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="f8c55-144">*policy_setting*</span></span>|<span data-ttu-id="f8c55-145">Paramètre à appliquer à ce type de stratégie.</span><span class="sxs-lookup"><span data-stu-id="f8c55-145">The setting to apply to this policy type.</span></span> <span data-ttu-id="f8c55-146">Les valeurs possibles sont `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal` et `Required All`.</span><span class="sxs-lookup"><span data-stu-id="f8c55-146">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="f8c55-147">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f8c55-147">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f8c55-148">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f8c55-148">Child Elements</span></span>  
 <span data-ttu-id="f8c55-149">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f8c55-149">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f8c55-150">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f8c55-150">Parent Elements</span></span>  
  
|<span data-ttu-id="f8c55-151">Élément</span><span class="sxs-lookup"><span data-stu-id="f8c55-151">Element</span></span>|<span data-ttu-id="f8c55-152">Description</span><span class="sxs-lookup"><span data-stu-id="f8c55-152">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f8c55-153">\<Type></span><span class="sxs-lookup"><span data-stu-id="f8c55-153">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="f8c55-154">Applique la stratégie de réflexion à un type et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="f8c55-154">Applies reflection policy to a type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f8c55-155">Notes</span><span class="sxs-lookup"><span data-stu-id="f8c55-155">Remarks</span></span>  
 <span data-ttu-id="f8c55-156">L'élément `<AttributeImplies>` est utilisé si son type conteneur est un attribut (autrement dit, une classe dérivée de <xref:System.Attribute?displayProperty=nameWithType>).</span><span class="sxs-lookup"><span data-stu-id="f8c55-156">The `<AttributeImplies>` element is used if its containing type is an attribute (that is, a class derived from <xref:System.Attribute?displayProperty=nameWithType>).</span></span> <span data-ttu-id="f8c55-157">Si l'attribut est appliqué à un élément de programme particulier, la stratégie définie par l'élément `<AttributeImplies>` s'applique à cet élément de programme.</span><span class="sxs-lookup"><span data-stu-id="f8c55-157">If the attribute is applied to a particular program element, the policy defined by the `<AttributeImplies>` element applies to that program element.</span></span>  
  
 <span data-ttu-id="f8c55-158">Les attributs de réflexion, de sérialisation et d'interopérabilité sont tous facultatifs, même si un au moins doit être présent.</span><span class="sxs-lookup"><span data-stu-id="f8c55-158">The reflection, serialization, and interop attributes are all optional, although at least one should be present.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8c55-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c55-159">See also</span></span>

- [<span data-ttu-id="f8c55-160">\<Type > élément</span><span class="sxs-lookup"><span data-stu-id="f8c55-160">\<Type> Element</span></span>](../../../docs/framework/net-native/type-element-net-native.md)
- [<span data-ttu-id="f8c55-161">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="f8c55-161">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="f8c55-162">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="f8c55-162">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
- [<span data-ttu-id="f8c55-163">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="f8c55-163">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
