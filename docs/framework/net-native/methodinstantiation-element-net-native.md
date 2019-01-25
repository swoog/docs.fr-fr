---
title: '&lt;MethodInstantiation&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: a3355d78-2a88-4109-8521-830d7cae260a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e2d05f9c727672c4f249e388a32b1101aaafd2f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538258"
---
# <a name="ltmethodinstantiationgt-element-net-native"></a><span data-ttu-id="1683b-102">&lt;MethodInstantiation&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="1683b-102">&lt;MethodInstantiation&gt; Element (.NET Native)</span></span>
<span data-ttu-id="1683b-103">Applique la stratégie de réflexion runtime à une méthode générique construite.</span><span class="sxs-lookup"><span data-stu-id="1683b-103">Applies runtime reflection policy to a constructed generic method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1683b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1683b-104">Syntax</span></span>  
  
```xml  
<MethodInstantiation Name="method_name"  
                     Signature="method_signature"  
                     Arguments="method_arguments"  
                     Browse="policy_type"  
                     Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1683b-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1683b-105">Attributes and Elements</span></span>  
 <span data-ttu-id="1683b-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1683b-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1683b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="1683b-107">Attributes</span></span>  
  
|<span data-ttu-id="1683b-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="1683b-108">Attribute</span></span>|<span data-ttu-id="1683b-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="1683b-109">Attribute type</span></span>|<span data-ttu-id="1683b-110">Description</span><span class="sxs-lookup"><span data-stu-id="1683b-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="1683b-111">Général</span><span class="sxs-lookup"><span data-stu-id="1683b-111">General</span></span>|<span data-ttu-id="1683b-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="1683b-112">Required attribute.</span></span> <span data-ttu-id="1683b-113">Spécifie le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1683b-113">Specifies the method name.</span></span>|  
|`Signature`|<span data-ttu-id="1683b-114">Général</span><span class="sxs-lookup"><span data-stu-id="1683b-114">General</span></span>|<span data-ttu-id="1683b-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="1683b-115">Optional attribute.</span></span> <span data-ttu-id="1683b-116">Spécifie les paramètres nommés de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1683b-116">Specifies named parameters of the method.</span></span> <span data-ttu-id="1683b-117">Si plusieurs paramètres nommés sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1683b-117">Multiple named parameters are separated by commas.</span></span> <span data-ttu-id="1683b-118">L'attribut `Signature` est utilisé pour différencier les méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="1683b-118">The `Signature` attribute is used to differentiate overloaded methods.</span></span>|  
|`Arguments`|<span data-ttu-id="1683b-119">Général</span><span class="sxs-lookup"><span data-stu-id="1683b-119">General</span></span>|<span data-ttu-id="1683b-120">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="1683b-120">Required attribute.</span></span> <span data-ttu-id="1683b-121">Spécifie les arguments de type générique.</span><span class="sxs-lookup"><span data-stu-id="1683b-121">Specifies the generic type arguments.</span></span> <span data-ttu-id="1683b-122">Si plusieurs arguments sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1683b-122">If multiple arguments are present, they are separated by commas.</span></span>|  
|`Browse`|<span data-ttu-id="1683b-123">Réflexion</span><span class="sxs-lookup"><span data-stu-id="1683b-123">Reflection</span></span>|<span data-ttu-id="1683b-124">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="1683b-124">Optional attribute.</span></span> <span data-ttu-id="1683b-125">Contrôle la demande d'informations sur une méthode ou l'énumération de celle-ci, mais ne permet pas d'effectuer un appel dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="1683b-125">Controls querying for information about or enumerating a method but does not enable any dynamic invocation at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="1683b-126">Réflexion</span><span class="sxs-lookup"><span data-stu-id="1683b-126">Reflection</span></span>|<span data-ttu-id="1683b-127">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="1683b-127">Optional attribute.</span></span> <span data-ttu-id="1683b-128">Contrôle l'accès à un constructeur ou à une méthode au moment de l'exécution pour activer la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="1683b-128">Controls runtime access to a constructor or method to enable dynamic programming.</span></span> <span data-ttu-id="1683b-129">Cette stratégie garantit que le membre peut être appelé dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="1683b-129">This policy ensures that a member can be invoked dynamically at run time.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="1683b-130">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="1683b-130">Name attribute</span></span>  
  
|<span data-ttu-id="1683b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1683b-131">Value</span></span>|<span data-ttu-id="1683b-132">Description</span><span class="sxs-lookup"><span data-stu-id="1683b-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1683b-133">*nom_méthode*</span><span class="sxs-lookup"><span data-stu-id="1683b-133">*method_name*</span></span>|<span data-ttu-id="1683b-134">Nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1683b-134">The method name.</span></span> <span data-ttu-id="1683b-135">Le type de la méthode est défini par le [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) parent ou l’élément [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="1683b-135">The type of the method is defined by the parent [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) or [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="signature-attribute"></a><span data-ttu-id="1683b-136">Attribut de signature</span><span class="sxs-lookup"><span data-stu-id="1683b-136">Signature attribute</span></span>  
  
|<span data-ttu-id="1683b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1683b-137">Value</span></span>|<span data-ttu-id="1683b-138">Description</span><span class="sxs-lookup"><span data-stu-id="1683b-138">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1683b-139">*signature_méthode*</span><span class="sxs-lookup"><span data-stu-id="1683b-139">*method_signature*</span></span>|<span data-ttu-id="1683b-140">Spécifie les paramètres nommés de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1683b-140">Specifies the named parameters of the method.</span></span> <span data-ttu-id="1683b-141">Si plusieurs paramètres sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1683b-141">If multiple parameters are present, they are separated by commas.</span></span>|  
  
## <a name="arguments-attribute"></a><span data-ttu-id="1683b-142">Attribut Arguments</span><span class="sxs-lookup"><span data-stu-id="1683b-142">Arguments attribute</span></span>  
  
|<span data-ttu-id="1683b-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="1683b-143">Value</span></span>|<span data-ttu-id="1683b-144">Description</span><span class="sxs-lookup"><span data-stu-id="1683b-144">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1683b-145">*arguments_méthode*</span><span class="sxs-lookup"><span data-stu-id="1683b-145">*method_arguments*</span></span>|<span data-ttu-id="1683b-146">Spécifie les arguments de type générique.</span><span class="sxs-lookup"><span data-stu-id="1683b-146">Specifies the generic type arguments.</span></span> <span data-ttu-id="1683b-147">Si plusieurs arguments sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1683b-147">If multiple arguments are present, they are separated by commas.</span></span> <span data-ttu-id="1683b-148">Chaque argument doit être composé du nom de type qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="1683b-148">Each argument must consist of the fully qualified type name.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="1683b-149">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="1683b-149">All other attributes</span></span>  
  
|<span data-ttu-id="1683b-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1683b-150">Value</span></span>|<span data-ttu-id="1683b-151">Description</span><span class="sxs-lookup"><span data-stu-id="1683b-151">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1683b-152">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="1683b-152">*policy_setting*</span></span>|<span data-ttu-id="1683b-153">Paramètre à appliquer à ce type de stratégie pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="1683b-153">The setting to apply to this policy type for the method.</span></span> <span data-ttu-id="1683b-154">Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`.</span><span class="sxs-lookup"><span data-stu-id="1683b-154">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="1683b-155">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="1683b-155">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1683b-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1683b-156">Child Elements</span></span>  
 <span data-ttu-id="1683b-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1683b-157">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1683b-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1683b-158">Parent Elements</span></span>  
  
|<span data-ttu-id="1683b-159">Élément</span><span class="sxs-lookup"><span data-stu-id="1683b-159">Element</span></span>|<span data-ttu-id="1683b-160">Description</span><span class="sxs-lookup"><span data-stu-id="1683b-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1683b-161">\<Type></span><span class="sxs-lookup"><span data-stu-id="1683b-161">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="1683b-162">Applique la stratégie de réflexion à un type et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="1683b-162">Applies reflection policy to a type and all its members.</span></span>|  
|[<span data-ttu-id="1683b-163">\<TypeInstantiation></span><span class="sxs-lookup"><span data-stu-id="1683b-163">\<TypeInstantiation></span></span>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|<span data-ttu-id="1683b-164">Applique la stratégie de réflexion à un type générique construit et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="1683b-164">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1683b-165">Notes</span><span class="sxs-lookup"><span data-stu-id="1683b-165">Remarks</span></span>  
 <span data-ttu-id="1683b-166">L'élément `<MethodInstantiation>` remplace la stratégie de réflexion runtime de la méthode générique ouverte correspondante.</span><span class="sxs-lookup"><span data-stu-id="1683b-166">The `<MethodInstantiation>` element overrides the runtime reflection policy of its corresponding open generic method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1683b-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1683b-167">See also</span></span>
- [<span data-ttu-id="1683b-168">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="1683b-168">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="1683b-169">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="1683b-169">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
- [<span data-ttu-id="1683b-170">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="1683b-170">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
- [<span data-ttu-id="1683b-171">\<Method>, élément</span><span class="sxs-lookup"><span data-stu-id="1683b-171">\<Method> Element</span></span>](../../../docs/framework/net-native/method-element-net-native.md)
