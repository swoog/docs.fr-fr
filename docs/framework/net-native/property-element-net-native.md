---
title: '&lt;Property&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: ad4ba56d-3bcb-4c10-ba90-1cc66e2175a1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 74fd4fa1387836e12d186a604f6996254eabf956
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549416"
---
# <a name="ltpropertygt-element-net-native"></a><span data-ttu-id="81075-102">&lt;Property&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="81075-102">&lt;Property&gt; Element (.NET Native)</span></span>
<span data-ttu-id="81075-103">Applique la stratégie de réflexion runtime à une propriété.</span><span class="sxs-lookup"><span data-stu-id="81075-103">Applies runtime reflection policy to a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81075-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81075-104">Syntax</span></span>  
  
```xml  
<Property Name="property_name"  
          Browse="policy_type"  
          Dynamic="policy_type"  
          Serialize="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="81075-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="81075-105">Attributes and Elements</span></span>  
 <span data-ttu-id="81075-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="81075-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="81075-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="81075-107">Attributes</span></span>  
  
|<span data-ttu-id="81075-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="81075-108">Attribute</span></span>|<span data-ttu-id="81075-109">Type d'attribut</span><span class="sxs-lookup"><span data-stu-id="81075-109">Attribute type</span></span>|<span data-ttu-id="81075-110">Description</span><span class="sxs-lookup"><span data-stu-id="81075-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="81075-111">Général</span><span class="sxs-lookup"><span data-stu-id="81075-111">General</span></span>|<span data-ttu-id="81075-112">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="81075-112">Required attribute.</span></span> <span data-ttu-id="81075-113">Spécifie le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="81075-113">Specifies the property name.</span></span>|  
|`Browse`|<span data-ttu-id="81075-114">Réflexion</span><span class="sxs-lookup"><span data-stu-id="81075-114">Reflection</span></span>|<span data-ttu-id="81075-115">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="81075-115">Optional attribute.</span></span> <span data-ttu-id="81075-116">Contrôle la demande d'informations sur la propriété ou l'énumération de celle-ci, mais ne permet pas d'effectuer un accès dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="81075-116">Controls querying for information about or enumerating the property but does not enable any dynamic access at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="81075-117">Réflexion</span><span class="sxs-lookup"><span data-stu-id="81075-117">Reflection</span></span>|<span data-ttu-id="81075-118">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="81075-118">Optional attribute.</span></span> <span data-ttu-id="81075-119">Contrôle l'accès à la propriété au moment de l'exécution pour autoriser la programmation dynamique.</span><span class="sxs-lookup"><span data-stu-id="81075-119">Controls runtime access to the property to enable dynamic programming.</span></span> <span data-ttu-id="81075-120">Grâce à cette stratégie, une propriété peut être définie ou récupérée dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="81075-120">This policy ensures that a property can be set or retrieved dynamically at run time.</span></span>|  
|`Serialize`|<span data-ttu-id="81075-121">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="81075-121">Serialization</span></span>|<span data-ttu-id="81075-122">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="81075-122">Optional attribute.</span></span> <span data-ttu-id="81075-123">Contrôle l'accès à une propriété au moment de l'exécution pour permettre aux instances de type d'être sérialisées par des bibliothèques, telles que le sérialiseur JSON Newtonsoft, ou d'être utilisées pour la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="81075-123">Controls runtime access to a property to enable type instances to be serialized by libraries such as the Newtonsoft JSON serializer or to be used for data binding.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="81075-124">Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="81075-124">Name attribute</span></span>  
  
|<span data-ttu-id="81075-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="81075-125">Value</span></span>|<span data-ttu-id="81075-126">Description</span><span class="sxs-lookup"><span data-stu-id="81075-126">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="81075-127">*nom_méthode*</span><span class="sxs-lookup"><span data-stu-id="81075-127">*method_name*</span></span>|<span data-ttu-id="81075-128">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="81075-128">The property name.</span></span> <span data-ttu-id="81075-129">Le type de la propriété est défini par l’élément parent [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) ou [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="81075-129">The type of the property is defined by the parent [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) or [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="81075-130">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="81075-130">All other attributes</span></span>  
  
|<span data-ttu-id="81075-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="81075-131">Value</span></span>|<span data-ttu-id="81075-132">Description</span><span class="sxs-lookup"><span data-stu-id="81075-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="81075-133">*paramètre_stratégie*</span><span class="sxs-lookup"><span data-stu-id="81075-133">*policy_setting*</span></span>|<span data-ttu-id="81075-134">Paramètre à appliquer à ce type de stratégie pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="81075-134">The setting to apply to this policy type for the property.</span></span> <span data-ttu-id="81075-135">Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`.</span><span class="sxs-lookup"><span data-stu-id="81075-135">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="81075-136">Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span><span class="sxs-lookup"><span data-stu-id="81075-136">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="81075-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="81075-137">Child Elements</span></span>  
 <span data-ttu-id="81075-138">Aucun.</span><span class="sxs-lookup"><span data-stu-id="81075-138">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="81075-139">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="81075-139">Parent Elements</span></span>  
  
|<span data-ttu-id="81075-140">Élément</span><span class="sxs-lookup"><span data-stu-id="81075-140">Element</span></span>|<span data-ttu-id="81075-141">Description</span><span class="sxs-lookup"><span data-stu-id="81075-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="81075-142">\<Type></span><span class="sxs-lookup"><span data-stu-id="81075-142">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="81075-143">Applique la stratégie de réflexion à un type et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="81075-143">Applies reflection policy to a type and all its members.</span></span>|  
|[<span data-ttu-id="81075-144">\<TypeInstantiation></span><span class="sxs-lookup"><span data-stu-id="81075-144">\<TypeInstantiation></span></span>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|<span data-ttu-id="81075-145">Applique la stratégie de réflexion à un type générique construit et à tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="81075-145">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="81075-146">Notes</span><span class="sxs-lookup"><span data-stu-id="81075-146">Remarks</span></span>  
 <span data-ttu-id="81075-147">Si la stratégie d'une propriété n'est pas définie explicitement, elle hérite la stratégie runtime de son élément parent.</span><span class="sxs-lookup"><span data-stu-id="81075-147">If a property's policy is not explicitly defined, it inherits the runtime policy of its parent element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="81075-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="81075-148">Example</span></span>  
 <span data-ttu-id="81075-149">L'exemple suivant utilise la réflexion pour instancier un objet `Book` et afficher les valeurs de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="81075-149">The following example uses reflection to instantiate a `Book` object and display its property values.</span></span> <span data-ttu-id="81075-150">Le fichier default.rd.xml d'origine du projet se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="81075-150">The original default.rd.xml file for the project appears as follows:</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <Application>  
      <Namespace Name="LibraryApplications"  Browse="Required Public" >  
         <Type Name="Book"   Activate="All" />  
      </Namespace>  
   </Application>  
</Directives>  
```  
  
 <span data-ttu-id="81075-151">Le fichier applique la valeur `All` à la stratégie `Activate` pour la classe `Book`, ce qui permet d'accéder aux constructeurs de classe par réflexion.</span><span class="sxs-lookup"><span data-stu-id="81075-151">The file applies the `All` value to the `Activate` policy for the `Book` class, which allows access to class constructors through reflection.</span></span> <span data-ttu-id="81075-152">La stratégie `Browse` pour la classe `Book` est héritée de son espace de noms parent.</span><span class="sxs-lookup"><span data-stu-id="81075-152">The `Browse` policy for the `Book` class is inherited from its parent namespace.</span></span> <span data-ttu-id="81075-153">Cette option est définie sur `Required Public`, ce qui rend les métadonnées disponibles au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="81075-153">This is set to `Required Public`, which makes metadata available at runtime.</span></span>  
  
 <span data-ttu-id="81075-154">Voici le code source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="81075-154">The following is the source code for the example.</span></span> <span data-ttu-id="81075-155">Le `outputBlock` variable représente un <xref:Windows.UI.Xaml.Controls.TextBlock> contrôle.</span><span class="sxs-lookup"><span data-stu-id="81075-155">The `outputBlock` variable represents a <xref:Windows.UI.Xaml.Controls.TextBlock> control.</span></span>  
  
 [!code-csharp[ProjectN_Reflection#6](../../../samples/snippets/csharp/VS_Snippets_CLR/projectn_reflection/cs/property1.cs#6)]  
  
 <span data-ttu-id="81075-156">Cependant, la compilation et l’exécution de cet exemple lèvent une exception [MissingRuntimeArtifactException](../../../docs/framework/net-native/missingruntimeartifactexception-class-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="81075-156">However, compiling and executing this example throws a [MissingRuntimeArtifactException](../../../docs/framework/net-native/missingruntimeartifactexception-class-net-native.md) exception.</span></span> <span data-ttu-id="81075-157">Bien que les métadonnées soient disponibles pour le type `Book`, nous n'avons pas pu rendre les implémentations des accesseurs Get de propriété disponibles dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="81075-157">Although we've made metadata for the `Book` type available, we've failed to make the implementations of the property getters available dynamically.</span></span> <span data-ttu-id="81075-158">Nous pouvons corriger cette erreur de deux manières :</span><span class="sxs-lookup"><span data-stu-id="81075-158">We can correct this error by either in one of two ways:</span></span>  
  
-   <span data-ttu-id="81075-159">En définissant la stratégie `Dynamic` pour le type `Book` dans son élément [\<Type>](../../../docs/framework/net-native/type-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="81075-159">by defining the `Dynamic` policy for the `Book` type in its [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) element.</span></span>  
  
-   <span data-ttu-id="81075-160">En ajoutant un élément [\<Property>](../../../docs/framework/net-native/property-element-net-native.md) imbriqué pour chaque propriété dont nous souhaitons appeler le getter, comme le fait le fichier default.rd.xml suivant.</span><span class="sxs-lookup"><span data-stu-id="81075-160">By adding a nested [\<Property>](../../../docs/framework/net-native/property-element-net-native.md) element for each property whose getter we'd like to invoke, as the following default.rd.xml file does.</span></span>  
  
    ```xml  
    <Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
       <Application>  
          <Namespace Name="LibraryApplications"  Browse="Required Public" >  
             <Type Name="Book"   Activate="All" >  
                <Property Name="Title" Dynamic="Required" />  
                <Property Name="Author" Dynamic="Required" />  
                  <Property Name="ISBN" Dynamic="Required" />  
             </Type>  
          </Namespace>  
       </Application>  
    </Directives>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="81075-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81075-161">See also</span></span>
- [<span data-ttu-id="81075-162">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="81075-162">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="81075-163">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="81075-163">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
- [<span data-ttu-id="81075-164">Paramètres de stratégie de directive runtime</span><span class="sxs-lookup"><span data-stu-id="81075-164">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
