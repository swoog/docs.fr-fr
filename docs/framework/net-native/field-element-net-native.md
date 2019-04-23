---
title: <Field> Élément (.NET Native)
ms.date: 03/30/2017
ms.assetid: 6a14125f-1a8d-41a1-8a32-659ca0ad12de
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c58be27334bcb862367464475a4eade5e01bdbb2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59221611"
---
# <a name="field-element-net-native"></a><span data-ttu-id="44a9a-102">\<Champ >, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="44a9a-102">\<Field> Element (.NET Native)</span></span>
<span data-ttu-id="44a9a-103">Applique la stratégie de réflexion runtime à un champ.</span><span class="sxs-lookup"><span data-stu-id="44a9a-103">Applies runtime reflection policy to a field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44a9a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44a9a-104">Syntax</span></span>  
  
```xml  
<Field Name="field_name"  
       Browse="policy_type"  
       Dynamic="policy_type"  
       Serialize="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="44a9a-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="44a9a-105">Attributes and Elements</span></span>  
 <span data-ttu-id="44a9a-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="44a9a-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="44a9a-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="44a9a-107">Attributes</span></span>  
  
|<span data-ttu-id="44a9a-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="44a9a-108">Attribute</span></span>|<span data-ttu-id="44a9a-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="44a9a-109">Attribute type</span></span>|<span data-ttu-id="44a9a-110">Description</span><span class="sxs-lookup"><span data-stu-id="44a9a-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="44a9a-111">Général</span><span class="sxs-lookup"><span data-stu-id="44a9a-111">General</span></span>|<span data-ttu-id="44a9a-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="44a9a-112">Required attribute.</span></span> <span data-ttu-id="44a9a-113">Spécifie le nom du champ.</span><span class="sxs-lookup"><span data-stu-id="44a9a-113">Specifies the field name.</span></span>|  
|`Browse`|<span data-ttu-id="44a9a-114">Réflexion</span><span class="sxs-lookup"><span data-stu-id="44a9a-114">Reflection</span></span>|<span data-ttu-id="44a9a-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="44a9a-115">Optional attribute.</span></span> <span data-ttu-id="44a9a-116">Contrôle la demande d'informations sur le champ ou l'énumération de celui-ci, mais ne permet pas d'effectuer un accès dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="44a9a-116">Controls querying for information about or enumerating the field but does not enable any dynamic access at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="44a9a-117">Réflexion</span><span class="sxs-lookup"><span data-stu-id="44a9a-117">Reflection</span></span>|<span data-ttu-id="44a9a-118">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="44a9a-118">Optional attribute.</span></span> <span data-ttu-id="44a9a-119">Contrôle l'accès au champ au moment de l'exécution pour autoriser la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="44a9a-119">Controls runtime access to the field to enable dynamic programming.</span></span> <span data-ttu-id="44a9a-120">Grâce à cette stratégie, un champ peut être défini ou récupéré dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="44a9a-120">This policy ensures that a field can be set or retrieved dynamically at run time.</span></span>|  
|`Serialize`|<span data-ttu-id="44a9a-121">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="44a9a-121">Serialization</span></span>|<span data-ttu-id="44a9a-122">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="44a9a-122">Optional attribute.</span></span> <span data-ttu-id="44a9a-123">Contrôle l'accès à un champ au moment de l'exécution pour permettre aux instances de type d'être sérialisées par des bibliothèques, telles que le sérialiseur JSON Newtonsoft, ou d'être utilisées pour la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="44a9a-123">Controls runtime access to a field to enable type instances to be serialized by libraries such as the Newtonsoft JSON serializer or to be used for data binding.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="44a9a-124">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="44a9a-124">Name attribute</span></span>  
  
|<span data-ttu-id="44a9a-125">Value</span><span class="sxs-lookup"><span data-stu-id="44a9a-125">Value</span></span>|<span data-ttu-id="44a9a-126">Description</span><span class="sxs-lookup"><span data-stu-id="44a9a-126">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="44a9a-127">*nom_méthode*</span><span class="sxs-lookup"><span data-stu-id="44a9a-127">*method_name*</span></span>|<span data-ttu-id="44a9a-128">Nom du champ.</span><span class="sxs-lookup"><span data-stu-id="44a9a-128">The field name.</span></span> <span data-ttu-id="44a9a-129">Le type du champ est défini par l’élément [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) ou [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) parent.</span><span class="sxs-lookup"><span data-stu-id="44a9a-129">The type of the field is defined by the parent [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) or [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="44a9a-130">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="44a9a-130">All other attributes</span></span>  
  
|<span data-ttu-id="44a9a-131">Value</span><span class="sxs-lookup"><span data-stu-id="44a9a-131">Value</span></span>|<span data-ttu-id="44a9a-132">Description</span><span class="sxs-lookup"><span data-stu-id="44a9a-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="44a9a-133">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="44a9a-133">*policy_setting*</span></span>|<span data-ttu-id="44a9a-134">Paramètre à appliquer à ce type de stratégie pour le champ.</span><span class="sxs-lookup"><span data-stu-id="44a9a-134">The setting to apply to this policy type for the field.</span></span> <span data-ttu-id="44a9a-135">Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`.</span><span class="sxs-lookup"><span data-stu-id="44a9a-135">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="44a9a-136">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="44a9a-136">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="44a9a-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44a9a-137">Child Elements</span></span>  
 <span data-ttu-id="44a9a-138">Aucun.</span><span class="sxs-lookup"><span data-stu-id="44a9a-138">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="44a9a-139">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="44a9a-139">Parent Elements</span></span>  
  
|<span data-ttu-id="44a9a-140">Élément</span><span class="sxs-lookup"><span data-stu-id="44a9a-140">Element</span></span>|<span data-ttu-id="44a9a-141">Description</span><span class="sxs-lookup"><span data-stu-id="44a9a-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="44a9a-142">\<Type></span><span class="sxs-lookup"><span data-stu-id="44a9a-142">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="44a9a-143">Applique la stratégie de réflexion à un type et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="44a9a-143">Applies reflection policy to a type and all its members.</span></span>|  
|[<span data-ttu-id="44a9a-144">\<TypeInstantiation></span><span class="sxs-lookup"><span data-stu-id="44a9a-144">\<TypeInstantiation></span></span>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|<span data-ttu-id="44a9a-145">Applique la stratégie de réflexion à un type générique construit et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="44a9a-145">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="44a9a-146">Notes</span><span class="sxs-lookup"><span data-stu-id="44a9a-146">Remarks</span></span>  
 <span data-ttu-id="44a9a-147">Si la stratégie d'un champ n'est pas définie explicitement, elle hérite la stratégie runtime de son élément parent.</span><span class="sxs-lookup"><span data-stu-id="44a9a-147">If a field's policy is not explicitly defined, it inherits the runtime policy of its parent element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44a9a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a9a-148">See also</span></span>

- [<span data-ttu-id="44a9a-149">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="44a9a-149">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
- [<span data-ttu-id="44a9a-150">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="44a9a-150">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="44a9a-151">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="44a9a-151">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
