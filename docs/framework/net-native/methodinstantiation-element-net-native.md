---
title: <MethodInstantiation> Élément (.NET Native)
ms.date: 03/30/2017
ms.assetid: a3355d78-2a88-4109-8521-830d7cae260a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ae15e6d61267feb0388170ee27dcd939035329b0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59121691"
---
# <a name="methodinstantiation-element-net-native"></a><span data-ttu-id="430cb-102">\<MethodInstantiation >, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="430cb-102">\<MethodInstantiation> Element (.NET Native)</span></span>
<span data-ttu-id="430cb-103">Applique la stratégie de réflexion runtime à une méthode générique construite.</span><span class="sxs-lookup"><span data-stu-id="430cb-103">Applies runtime reflection policy to a constructed generic method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="430cb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="430cb-104">Syntax</span></span>  
  
```xml  
<MethodInstantiation Name="method_name"  
                     Signature="method_signature"  
                     Arguments="method_arguments"  
                     Browse="policy_type"  
                     Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="430cb-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="430cb-105">Attributes and Elements</span></span>  
 <span data-ttu-id="430cb-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="430cb-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="430cb-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="430cb-107">Attributes</span></span>  
  
|<span data-ttu-id="430cb-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="430cb-108">Attribute</span></span>|<span data-ttu-id="430cb-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="430cb-109">Attribute type</span></span>|<span data-ttu-id="430cb-110">Description</span><span class="sxs-lookup"><span data-stu-id="430cb-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="430cb-111">Général</span><span class="sxs-lookup"><span data-stu-id="430cb-111">General</span></span>|<span data-ttu-id="430cb-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="430cb-112">Required attribute.</span></span> <span data-ttu-id="430cb-113">Spécifie le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="430cb-113">Specifies the method name.</span></span>|  
|`Signature`|<span data-ttu-id="430cb-114">Général</span><span class="sxs-lookup"><span data-stu-id="430cb-114">General</span></span>|<span data-ttu-id="430cb-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="430cb-115">Optional attribute.</span></span> <span data-ttu-id="430cb-116">Spécifie les paramètres nommés de la méthode.</span><span class="sxs-lookup"><span data-stu-id="430cb-116">Specifies named parameters of the method.</span></span> <span data-ttu-id="430cb-117">Si plusieurs paramètres nommés sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="430cb-117">Multiple named parameters are separated by commas.</span></span> <span data-ttu-id="430cb-118">L'attribut `Signature` est utilisé pour différencier les méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="430cb-118">The `Signature` attribute is used to differentiate overloaded methods.</span></span>|  
|`Arguments`|<span data-ttu-id="430cb-119">Général</span><span class="sxs-lookup"><span data-stu-id="430cb-119">General</span></span>|<span data-ttu-id="430cb-120">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="430cb-120">Required attribute.</span></span> <span data-ttu-id="430cb-121">Spécifie les arguments de type générique.</span><span class="sxs-lookup"><span data-stu-id="430cb-121">Specifies the generic type arguments.</span></span> <span data-ttu-id="430cb-122">Si plusieurs arguments sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="430cb-122">If multiple arguments are present, they are separated by commas.</span></span>|  
|`Browse`|<span data-ttu-id="430cb-123">Réflexion</span><span class="sxs-lookup"><span data-stu-id="430cb-123">Reflection</span></span>|<span data-ttu-id="430cb-124">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="430cb-124">Optional attribute.</span></span> <span data-ttu-id="430cb-125">Contrôle la demande d'informations sur une méthode ou l'énumération de celle-ci, mais ne permet pas d'effectuer un appel dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="430cb-125">Controls querying for information about or enumerating a method but does not enable any dynamic invocation at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="430cb-126">Réflexion</span><span class="sxs-lookup"><span data-stu-id="430cb-126">Reflection</span></span>|<span data-ttu-id="430cb-127">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="430cb-127">Optional attribute.</span></span> <span data-ttu-id="430cb-128">Contrôle l'accès à un constructeur ou à une méthode au moment de l'exécution pour activer la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="430cb-128">Controls runtime access to a constructor or method to enable dynamic programming.</span></span> <span data-ttu-id="430cb-129">Cette stratégie garantit que le membre peut être appelé dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="430cb-129">This policy ensures that a member can be invoked dynamically at run time.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="430cb-130">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="430cb-130">Name attribute</span></span>  
  
|<span data-ttu-id="430cb-131">Value</span><span class="sxs-lookup"><span data-stu-id="430cb-131">Value</span></span>|<span data-ttu-id="430cb-132">Description</span><span class="sxs-lookup"><span data-stu-id="430cb-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="430cb-133">*nom_méthode*</span><span class="sxs-lookup"><span data-stu-id="430cb-133">*method_name*</span></span>|<span data-ttu-id="430cb-134">Nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="430cb-134">The method name.</span></span> <span data-ttu-id="430cb-135">Le type de la méthode est défini par le [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) parent ou l’élément [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="430cb-135">The type of the method is defined by the parent [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) or [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="signature-attribute"></a><span data-ttu-id="430cb-136">Attribut de signature</span><span class="sxs-lookup"><span data-stu-id="430cb-136">Signature attribute</span></span>  
  
|<span data-ttu-id="430cb-137">Value</span><span class="sxs-lookup"><span data-stu-id="430cb-137">Value</span></span>|<span data-ttu-id="430cb-138">Description</span><span class="sxs-lookup"><span data-stu-id="430cb-138">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="430cb-139">*signature_méthode*</span><span class="sxs-lookup"><span data-stu-id="430cb-139">*method_signature*</span></span>|<span data-ttu-id="430cb-140">Spécifie les paramètres nommés de la méthode.</span><span class="sxs-lookup"><span data-stu-id="430cb-140">Specifies the named parameters of the method.</span></span> <span data-ttu-id="430cb-141">Si plusieurs paramètres sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="430cb-141">If multiple parameters are present, they are separated by commas.</span></span>|  
  
## <a name="arguments-attribute"></a><span data-ttu-id="430cb-142">Attribut Arguments</span><span class="sxs-lookup"><span data-stu-id="430cb-142">Arguments attribute</span></span>  
  
|<span data-ttu-id="430cb-143">Value</span><span class="sxs-lookup"><span data-stu-id="430cb-143">Value</span></span>|<span data-ttu-id="430cb-144">Description</span><span class="sxs-lookup"><span data-stu-id="430cb-144">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="430cb-145">*arguments_méthode*</span><span class="sxs-lookup"><span data-stu-id="430cb-145">*method_arguments*</span></span>|<span data-ttu-id="430cb-146">Spécifie les arguments de type générique.</span><span class="sxs-lookup"><span data-stu-id="430cb-146">Specifies the generic type arguments.</span></span> <span data-ttu-id="430cb-147">Si plusieurs arguments sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="430cb-147">If multiple arguments are present, they are separated by commas.</span></span> <span data-ttu-id="430cb-148">Chaque argument doit être composé du nom de type qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="430cb-148">Each argument must consist of the fully qualified type name.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="430cb-149">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="430cb-149">All other attributes</span></span>  
  
|<span data-ttu-id="430cb-150">Value</span><span class="sxs-lookup"><span data-stu-id="430cb-150">Value</span></span>|<span data-ttu-id="430cb-151">Description</span><span class="sxs-lookup"><span data-stu-id="430cb-151">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="430cb-152">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="430cb-152">*policy_setting*</span></span>|<span data-ttu-id="430cb-153">Paramètre à appliquer à ce type de stratégie pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="430cb-153">The setting to apply to this policy type for the method.</span></span> <span data-ttu-id="430cb-154">Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`.</span><span class="sxs-lookup"><span data-stu-id="430cb-154">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="430cb-155">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="430cb-155">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="430cb-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="430cb-156">Child Elements</span></span>  
 <span data-ttu-id="430cb-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="430cb-157">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="430cb-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="430cb-158">Parent Elements</span></span>  
  
|<span data-ttu-id="430cb-159">Élément</span><span class="sxs-lookup"><span data-stu-id="430cb-159">Element</span></span>|<span data-ttu-id="430cb-160">Description</span><span class="sxs-lookup"><span data-stu-id="430cb-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="430cb-161">\<Type></span><span class="sxs-lookup"><span data-stu-id="430cb-161">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="430cb-162">Applique la stratégie de réflexion à un type et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="430cb-162">Applies reflection policy to a type and all its members.</span></span>|  
|[<span data-ttu-id="430cb-163">\<TypeInstantiation></span><span class="sxs-lookup"><span data-stu-id="430cb-163">\<TypeInstantiation></span></span>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|<span data-ttu-id="430cb-164">Applique la stratégie de réflexion à un type générique construit et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="430cb-164">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="430cb-165">Notes</span><span class="sxs-lookup"><span data-stu-id="430cb-165">Remarks</span></span>  
 <span data-ttu-id="430cb-166">L'élément `<MethodInstantiation>` remplace la stratégie de réflexion runtime de la méthode générique ouverte correspondante.</span><span class="sxs-lookup"><span data-stu-id="430cb-166">The `<MethodInstantiation>` element overrides the runtime reflection policy of its corresponding open generic method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="430cb-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="430cb-167">See also</span></span>

- [<span data-ttu-id="430cb-168">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="430cb-168">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="430cb-169">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="430cb-169">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
- [<span data-ttu-id="430cb-170">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="430cb-170">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
- [<span data-ttu-id="430cb-171">\<Method>, élément</span><span class="sxs-lookup"><span data-stu-id="430cb-171">\<Method> Element</span></span>](../../../docs/framework/net-native/method-element-net-native.md)
