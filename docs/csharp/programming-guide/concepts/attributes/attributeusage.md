---
title: AttributeUsage (C#)
ms.date: 04/25/2018
ms.openlocfilehash: 37657a0611180d5b4c48b3e1778d33861afa5a74
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43500570"
---
# <a name="attributeusage-c"></a><span data-ttu-id="94126-102">AttributeUsage (C#)</span><span class="sxs-lookup"><span data-stu-id="94126-102">AttributeUsage (C#)</span></span>

<span data-ttu-id="94126-103">Détermine de quelle manière une classe d’attributs personnalisés peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="94126-103">Determines how a custom attribute class can be used.</span></span> <span data-ttu-id="94126-104"><xref:System.AttributeUsageAttribute> est un attribut que vous appliquez à des définitions d’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="94126-104"><xref:System.AttributeUsageAttribute> is an attribute you apply to custom attribute definitions.</span></span> <span data-ttu-id="94126-105">L’attribut `AttributeUsage` vous permet de contrôler :</span><span class="sxs-lookup"><span data-stu-id="94126-105">The `AttributeUsage` attribute enables you to control:</span></span>

- <span data-ttu-id="94126-106">À quels éléments de programme les attributs peuvent être appliqués.</span><span class="sxs-lookup"><span data-stu-id="94126-106">Which program elements attribute may be applied to.</span></span> <span data-ttu-id="94126-107">Sauf si vous en limitez l’utilisation, un attribut peut être appliqué aux éléments de programme suivants :</span><span class="sxs-lookup"><span data-stu-id="94126-107">Unless you restrict is usage, an attribute may be applied to any of the following program elements:</span></span>
  - <span data-ttu-id="94126-108">assembly</span><span class="sxs-lookup"><span data-stu-id="94126-108">assembly</span></span>
  - <span data-ttu-id="94126-109">module</span><span class="sxs-lookup"><span data-stu-id="94126-109">module</span></span>
  - <span data-ttu-id="94126-110">champ</span><span class="sxs-lookup"><span data-stu-id="94126-110">field</span></span>
  - <span data-ttu-id="94126-111">événement</span><span class="sxs-lookup"><span data-stu-id="94126-111">event</span></span>
  - <span data-ttu-id="94126-112">méthode</span><span class="sxs-lookup"><span data-stu-id="94126-112">method</span></span>
  - <span data-ttu-id="94126-113">param</span><span class="sxs-lookup"><span data-stu-id="94126-113">param</span></span>
  - <span data-ttu-id="94126-114">propriété</span><span class="sxs-lookup"><span data-stu-id="94126-114">property</span></span>
  - <span data-ttu-id="94126-115">return</span><span class="sxs-lookup"><span data-stu-id="94126-115">return</span></span>
  - <span data-ttu-id="94126-116">type</span><span class="sxs-lookup"><span data-stu-id="94126-116">type</span></span>
- <span data-ttu-id="94126-117">Si un attribut peut être appliqué plusieurs fois à un même élément de programme.</span><span class="sxs-lookup"><span data-stu-id="94126-117">Whether an attribute can be applied to a single program element multiple times.</span></span>
- <span data-ttu-id="94126-118">Si les attributs sont hérités dans les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="94126-118">Whether attributes are inherited by derived classes.</span></span>

<span data-ttu-id="94126-119">L’exemple suivant montre des paramètres par défaut quand ils sont appliqués explicitement :</span><span class="sxs-lookup"><span data-stu-id="94126-119">The default settings look like the following example when applied explicitly:</span></span>

[!code-csharp[Define a new attribute](../../../../../samples/snippets/csharp/attributes/NewAttribute.cs#1)]

<span data-ttu-id="94126-120">Dans cet exemple, la classe `NewAttribute` peut être appliquée à n’importe quel élément de programme pris en charge.</span><span class="sxs-lookup"><span data-stu-id="94126-120">In this example, the `NewAttribute` class can be applied to any supported program element.</span></span> <span data-ttu-id="94126-121">Elle ne peut cependant être appliquée qu’une seule fois à chaque entité.</span><span class="sxs-lookup"><span data-stu-id="94126-121">But it can be applied only once to each entity.</span></span> <span data-ttu-id="94126-122">L’attribut est hérité par les classes dérivées quand il est appliqué à une classe de base.</span><span class="sxs-lookup"><span data-stu-id="94126-122">The attribute is inherited by derived classes when applied to a base class.</span></span>

<span data-ttu-id="94126-123">Les arguments <xref:System.AttributeUsageAttribute.AllowMultiple> et <xref:System.AttributeUsageAttribute.Inherited> étant facultatifs, le code suivant a le même effet :</span><span class="sxs-lookup"><span data-stu-id="94126-123">The <xref:System.AttributeUsageAttribute.AllowMultiple> and <xref:System.AttributeUsageAttribute.Inherited> arguments are optional, so the following code has the same effect:</span></span>

[!code-csharp[Omit optional attributes](../../../../../samples/snippets/csharp/attributes/NewAttribute.cs#2)]

<span data-ttu-id="94126-124">Le premier argument <xref:System.AttributeUsageAttribute> doit correspondre à un ou plusieurs éléments de l’énumération <xref:System.AttributeTargets>.</span><span class="sxs-lookup"><span data-stu-id="94126-124">The first <xref:System.AttributeUsageAttribute> argument must be one or more elements of the <xref:System.AttributeTargets> enumeration.</span></span> <span data-ttu-id="94126-125">Vous pouvez lier ensemble plusieurs types de cibles avec l’opérateur OR, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="94126-125">Multiple target types can be linked together with the OR operator, like the following example shows:</span></span>

[!code-csharp[Create an attribute for fields or properties](../../../../../samples/snippets/csharp/attributes/NewPropertyOrFieldAttribute.cs#1)]

<span data-ttu-id="94126-126">À compter de C# 7.3, les attributs peuvent être appliqués à la propriété ou au champ de stockage pour une propriété implémentée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="94126-126">Beginning in C# 7.3, attributes can be applied to either the property or the backing field for an auto-implemented property.</span></span> <span data-ttu-id="94126-127">L’attribut s’applique à la propriété, sauf si vous spécifiez le spécificateur `field` sur l’attribut.</span><span class="sxs-lookup"><span data-stu-id="94126-127">The attribute applies to the property, unless you specify the `field` specifier on the attribute.</span></span> <span data-ttu-id="94126-128">Les deux cas sont illustrés dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="94126-128">Both are shown in the following example:</span></span>

[!code-csharp[Create an attribute for fields or properties](../../../../../samples/snippets/csharp/attributes/NewPropertyOrFieldAttribute.cs#2)]

<span data-ttu-id="94126-129">Si l’argument <xref:System.AttributeUsageAttribute.AllowMultiple> est défini sur `true`, l’attribut résultant peut être appliqué plusieurs fois à une même entité, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="94126-129">If the <xref:System.AttributeUsageAttribute.AllowMultiple> argument is `true`, then the resulting attribute can be applied more than once to a single entity, as shown in the following example:</span></span>

[!code-csharp[Create and use an attribute that can be applied multiple times](../../../../../samples/snippets/csharp/attributes/MultiUseAttribute.cs#1)]

<span data-ttu-id="94126-130">Dans ce cas, `MultiUseAttribute` peut être appliqué à plusieurs reprises, car `AllowMultiple` est défini sur `true`.</span><span class="sxs-lookup"><span data-stu-id="94126-130">In this case, `MultiUseAttribute` can be applied repeatedly because `AllowMultiple` is set to `true`.</span></span> <span data-ttu-id="94126-131">Les deux formats indiqués pour appliquer plusieurs attributs sont valides.</span><span class="sxs-lookup"><span data-stu-id="94126-131">Both formats shown for applying multiple attributes are valid.</span></span>

<span data-ttu-id="94126-132">Si <xref:System.AttributeUsageAttribute.Inherited> est `false`, l’attribut n’est pas hérité par les classes dérivées d’une classe avec attributs.</span><span class="sxs-lookup"><span data-stu-id="94126-132">If <xref:System.AttributeUsageAttribute.Inherited> is `false`, then the attribute isn't inherited by classes derived from an attributed class.</span></span> <span data-ttu-id="94126-133">Exemple :</span><span class="sxs-lookup"><span data-stu-id="94126-133">For example:</span></span>

[!code-csharp[Create and use an attribute that can be applied multiple times](../../../../../samples/snippets/csharp/attributes/NonInheritedAttribute.cs#1)]

<span data-ttu-id="94126-134">Dans ce cas, `NonInheritedAttribute` n’est pas appliqué à `DClass` via l’héritage.</span><span class="sxs-lookup"><span data-stu-id="94126-134">In this case `NonInheritedAttribute` isn't applied to `DClass` via inheritance.</span></span>

## <a name="remarks"></a><span data-ttu-id="94126-135">Notes</span><span class="sxs-lookup"><span data-stu-id="94126-135">Remarks</span></span>

<span data-ttu-id="94126-136">L’attribut `AttributeUsage` est un attribut à usage unique : il ne peut pas être appliqué plusieurs fois à la même classe.</span><span class="sxs-lookup"><span data-stu-id="94126-136">The `AttributeUsage` attribute is a single-use attribute--it can't be applied more than once to the same class.</span></span> <span data-ttu-id="94126-137">`AttributeUsage` est un alias pour <xref:System.AttributeUsageAttribute>.</span><span class="sxs-lookup"><span data-stu-id="94126-137">`AttributeUsage` is an alias for <xref:System.AttributeUsageAttribute>.</span></span>

<span data-ttu-id="94126-138">Pour plus d’informations, consultez [Accès à des attributs à l’aide de la réflexion (C#)](accessing-attributes-by-using-reflection.md).</span><span class="sxs-lookup"><span data-stu-id="94126-138">For more information, see [Accessing Attributes by Using Reflection (C#)](accessing-attributes-by-using-reflection.md).</span></span>

## <a name="example"></a><span data-ttu-id="94126-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="94126-139">Example</span></span>

<span data-ttu-id="94126-140">L’exemple suivant illustre l’effet des arguments <xref:System.AttributeUsageAttribute.Inherited> et <xref:System.AttributeUsageAttribute.AllowMultiple> sur l’attribut <xref:System.AttributeUsageAttribute>, et la manière dont les attributs personnalisés appliqués à une classe peuvent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="94126-140">The following example demonstrates the effect of the <xref:System.AttributeUsageAttribute.Inherited> and <xref:System.AttributeUsageAttribute.AllowMultiple> arguments to the <xref:System.AttributeUsageAttribute> attribute, and how the custom attributes applied to a class can be enumerated.</span></span>

[!code-csharp[Applying and querying attributes](../../../../../samples/snippets/csharp/attributes/Program.cs#1)]

## <a name="sample-output"></a><span data-ttu-id="94126-141">Résultat de l'exemple</span><span class="sxs-lookup"><span data-stu-id="94126-141">Sample Output</span></span>

```text
Attributes on Base Class:
FirstAttribute
SecondAttribute
Attributes on Derived Class:
ThirdAttribute
ThirdAttribute
SecondAttribute
```

## <a name="see-also"></a><span data-ttu-id="94126-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94126-142">See Also</span></span>

- <xref:System.Attribute>  
- <xref:System.Reflection>  
- [<span data-ttu-id="94126-143">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="94126-143">C# Programming Guide</span></span>](../..//index.md)  
- [<span data-ttu-id="94126-144">Attributs</span><span class="sxs-lookup"><span data-stu-id="94126-144">Attributes</span></span>](../../../..//standard/attributes/index.md)  
- [<span data-ttu-id="94126-145">Réflexion (C#)</span><span class="sxs-lookup"><span data-stu-id="94126-145">Reflection (C#)</span></span>](../reflection.md)  
- [<span data-ttu-id="94126-146">Attributs</span><span class="sxs-lookup"><span data-stu-id="94126-146">Attributes</span></span>](index.md)  
- [<span data-ttu-id="94126-147">Création d’attributs personnalisés (C#)</span><span class="sxs-lookup"><span data-stu-id="94126-147">Creating Custom Attributes (C#)</span></span>](creating-custom-attributes.md)  
- [<span data-ttu-id="94126-148">Accès à des attributs à l’aide de la réflexion (C#)</span><span class="sxs-lookup"><span data-stu-id="94126-148">Accessing Attributes by Using Reflection (C#)</span></span>](accessing-attributes-by-using-reflection.md)
