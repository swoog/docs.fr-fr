---
title: '&lt;MethodInstantiation&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: a3355d78-2a88-4109-8521-830d7cae260a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3d741e8df8f2b8c6d90a1d867c73495a2ffd1304
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33397791"
---
# <a name="ltmethodinstantiationgt-element-net-native"></a><span data-ttu-id="debfa-102">&lt;MethodInstantiation&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="debfa-102">&lt;MethodInstantiation&gt; Element (.NET Native)</span></span>
<span data-ttu-id="debfa-103">Applique la stratégie de réflexion runtime à une méthode générique construite.</span><span class="sxs-lookup"><span data-stu-id="debfa-103">Applies runtime reflection policy to a constructed generic method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="debfa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="debfa-104">Syntax</span></span>  
  
```xml  
<MethodInstantiation Name="method_name"  
                     Signature="method_signature"  
                     Arguments="method_arguments"  
                     Browse="policy_type"  
                     Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="debfa-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="debfa-105">Attributes and Elements</span></span>  
 <span data-ttu-id="debfa-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="debfa-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="debfa-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="debfa-107">Attributes</span></span>  
  
|<span data-ttu-id="debfa-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="debfa-108">Attribute</span></span>|<span data-ttu-id="debfa-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="debfa-109">Attribute type</span></span>|<span data-ttu-id="debfa-110">Description</span><span class="sxs-lookup"><span data-stu-id="debfa-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="debfa-111">Général</span><span class="sxs-lookup"><span data-stu-id="debfa-111">General</span></span>|<span data-ttu-id="debfa-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="debfa-112">Required attribute.</span></span> <span data-ttu-id="debfa-113">Spécifie le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="debfa-113">Specifies the method name.</span></span>|  
|`Signature`|<span data-ttu-id="debfa-114">Général</span><span class="sxs-lookup"><span data-stu-id="debfa-114">General</span></span>|<span data-ttu-id="debfa-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="debfa-115">Optional attribute.</span></span> <span data-ttu-id="debfa-116">Spécifie les paramètres nommés de la méthode.</span><span class="sxs-lookup"><span data-stu-id="debfa-116">Specifies named parameters of the method.</span></span> <span data-ttu-id="debfa-117">Si plusieurs paramètres nommés sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="debfa-117">Multiple named parameters are separated by commas.</span></span> <span data-ttu-id="debfa-118">L'attribut `Signature` est utilisé pour différencier les méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="debfa-118">The `Signature` attribute is used to differentiate overloaded methods.</span></span>|  
|`Arguments`|<span data-ttu-id="debfa-119">Général</span><span class="sxs-lookup"><span data-stu-id="debfa-119">General</span></span>|<span data-ttu-id="debfa-120">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="debfa-120">Required attribute.</span></span> <span data-ttu-id="debfa-121">Spécifie les arguments de type générique.</span><span class="sxs-lookup"><span data-stu-id="debfa-121">Specifies the generic type arguments.</span></span> <span data-ttu-id="debfa-122">Si plusieurs arguments sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="debfa-122">If multiple arguments are present, they are separated by commas.</span></span>|  
|`Browse`|<span data-ttu-id="debfa-123">Réflexion</span><span class="sxs-lookup"><span data-stu-id="debfa-123">Reflection</span></span>|<span data-ttu-id="debfa-124">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="debfa-124">Optional attribute.</span></span> <span data-ttu-id="debfa-125">Contrôle la demande d'informations sur une méthode ou l'énumération de celle-ci, mais ne permet pas d'effectuer un appel dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="debfa-125">Controls querying for information about or enumerating a method but does not enable any dynamic invocation at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="debfa-126">Réflexion</span><span class="sxs-lookup"><span data-stu-id="debfa-126">Reflection</span></span>|<span data-ttu-id="debfa-127">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="debfa-127">Optional attribute.</span></span> <span data-ttu-id="debfa-128">Contrôle l'accès à un constructeur ou à une méthode au moment de l'exécution pour activer la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="debfa-128">Controls runtime access to a constructor or method to enable dynamic programming.</span></span> <span data-ttu-id="debfa-129">Cette stratégie garantit que le membre peut être appelé dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="debfa-129">This policy ensures that a member can be invoked dynamically at run time.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="debfa-130">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="debfa-130">Name attribute</span></span>  
  
|<span data-ttu-id="debfa-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="debfa-131">Value</span></span>|<span data-ttu-id="debfa-132">Description</span><span class="sxs-lookup"><span data-stu-id="debfa-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="debfa-133">*nom_méthode*</span><span class="sxs-lookup"><span data-stu-id="debfa-133">*method_name*</span></span>|<span data-ttu-id="debfa-134">Nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="debfa-134">The method name.</span></span> <span data-ttu-id="debfa-135">Le type de la méthode est défini par le [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) parent ou l’élément [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="debfa-135">The type of the method is defined by the parent [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) or [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="signature-attribute"></a><span data-ttu-id="debfa-136">Attribut de signature</span><span class="sxs-lookup"><span data-stu-id="debfa-136">Signature attribute</span></span>  
  
|<span data-ttu-id="debfa-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="debfa-137">Value</span></span>|<span data-ttu-id="debfa-138">Description</span><span class="sxs-lookup"><span data-stu-id="debfa-138">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="debfa-139">*signature_méthode*</span><span class="sxs-lookup"><span data-stu-id="debfa-139">*method_signature*</span></span>|<span data-ttu-id="debfa-140">Spécifie les paramètres nommés de la méthode.</span><span class="sxs-lookup"><span data-stu-id="debfa-140">Specifies the named parameters of the method.</span></span> <span data-ttu-id="debfa-141">Si plusieurs paramètres sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="debfa-141">If multiple parameters are present, they are separated by commas.</span></span>|  
  
## <a name="arguments-attribute"></a><span data-ttu-id="debfa-142">Attribut Arguments</span><span class="sxs-lookup"><span data-stu-id="debfa-142">Arguments attribute</span></span>  
  
|<span data-ttu-id="debfa-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="debfa-143">Value</span></span>|<span data-ttu-id="debfa-144">Description</span><span class="sxs-lookup"><span data-stu-id="debfa-144">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="debfa-145">*arguments_méthode*</span><span class="sxs-lookup"><span data-stu-id="debfa-145">*method_arguments*</span></span>|<span data-ttu-id="debfa-146">Spécifie les arguments de type générique.</span><span class="sxs-lookup"><span data-stu-id="debfa-146">Specifies the generic type arguments.</span></span> <span data-ttu-id="debfa-147">Si plusieurs arguments sont présents, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="debfa-147">If multiple arguments are present, they are separated by commas.</span></span> <span data-ttu-id="debfa-148">Chaque argument doit être composé du nom de type qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="debfa-148">Each argument must consist of the fully qualified type name.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="debfa-149">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="debfa-149">All other attributes</span></span>  
  
|<span data-ttu-id="debfa-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="debfa-150">Value</span></span>|<span data-ttu-id="debfa-151">Description</span><span class="sxs-lookup"><span data-stu-id="debfa-151">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="debfa-152">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="debfa-152">*policy_setting*</span></span>|<span data-ttu-id="debfa-153">Paramètre à appliquer à ce type de stratégie pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="debfa-153">The setting to apply to this policy type for the method.</span></span> <span data-ttu-id="debfa-154">Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`.</span><span class="sxs-lookup"><span data-stu-id="debfa-154">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="debfa-155">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="debfa-155">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="debfa-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="debfa-156">Child Elements</span></span>  
 <span data-ttu-id="debfa-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="debfa-157">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="debfa-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="debfa-158">Parent Elements</span></span>  
  
|<span data-ttu-id="debfa-159">Élément</span><span class="sxs-lookup"><span data-stu-id="debfa-159">Element</span></span>|<span data-ttu-id="debfa-160">Description</span><span class="sxs-lookup"><span data-stu-id="debfa-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="debfa-161">\<Type></span><span class="sxs-lookup"><span data-stu-id="debfa-161">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="debfa-162">Applique la stratégie de réflexion à un type et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="debfa-162">Applies reflection policy to a type and all its members.</span></span>|  
|[<span data-ttu-id="debfa-163">\<TypeInstantiation></span><span class="sxs-lookup"><span data-stu-id="debfa-163">\<TypeInstantiation></span></span>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|<span data-ttu-id="debfa-164">Applique la stratégie de réflexion à un type générique construit et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="debfa-164">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="debfa-165">Notes</span><span class="sxs-lookup"><span data-stu-id="debfa-165">Remarks</span></span>  
 <span data-ttu-id="debfa-166">L'élément `<MethodInstantiation>` remplace la stratégie de réflexion runtime de la méthode générique ouverte correspondante.</span><span class="sxs-lookup"><span data-stu-id="debfa-166">The `<MethodInstantiation>` element overrides the runtime reflection policy of its corresponding open generic method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="debfa-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="debfa-167">See Also</span></span>  
 [<span data-ttu-id="debfa-168">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="debfa-168">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)  
 [<span data-ttu-id="debfa-169">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="debfa-169">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)  
 [<span data-ttu-id="debfa-170">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="debfa-170">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)  
 [<span data-ttu-id="debfa-171">\<Method>, élément</span><span class="sxs-lookup"><span data-stu-id="debfa-171">\<Method> Element</span></span>](../../../docs/framework/net-native/method-element-net-native.md)
