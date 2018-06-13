---
title: Génériques et attributs (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- generics [C#], attributes
- attributes [C#], with generics
ms.assetid: da9fc326-4648-454a-8e13-3911a2edefd7
ms.openlocfilehash: 3bfb4028fb5efce693abd83b40636b0149962e3b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33339673"
---
# <a name="generics-and-attributes-c-programming-guide"></a><span data-ttu-id="76517-102">Génériques et attributs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="76517-102">Generics and Attributes (C# Programming Guide)</span></span>
<span data-ttu-id="76517-103">Les attributs peuvent être appliqués aux types génériques de la même manière qu’aux types non génériques.</span><span class="sxs-lookup"><span data-stu-id="76517-103">Attributes can be applied to generic types in the same way as non-generic types.</span></span> <span data-ttu-id="76517-104">Pour plus d’informations sur l’application des attributs, consultez [Attributs](../../../csharp/programming-guide/concepts/attributes/index.md).</span><span class="sxs-lookup"><span data-stu-id="76517-104">For more information on applying attributes, see [Attributes](../../../csharp/programming-guide/concepts/attributes/index.md).</span></span>  
  
 <span data-ttu-id="76517-105">Les attributs personnalisés sont uniquement autorisés à référencer des types génériques ouverts, qui sont des types génériques pour lesquels aucun argument de type n’est fourni, et des types génériques construits fermés, qui fournissent des arguments pour tous les paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="76517-105">Custom attributes are only permitted to reference open generic types, which are generic types for which no type arguments are supplied, and closed constructed generic types, which supply arguments for all type parameters.</span></span>  
  
 <span data-ttu-id="76517-106">Les exemples suivants utilisent cet attribut personnalisé :</span><span class="sxs-lookup"><span data-stu-id="76517-106">The following examples use this custom attribute:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#48](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-attributes_1.cs)]  
  
 <span data-ttu-id="76517-107">Un attribut peut référencer un type générique ouvert :</span><span class="sxs-lookup"><span data-stu-id="76517-107">An attribute can reference an open generic type:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#49](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-attributes_2.cs)]  
  
 <span data-ttu-id="76517-108">Spécifiez plusieurs paramètres de type à l’aide du nombre approprié de virgules.</span><span class="sxs-lookup"><span data-stu-id="76517-108">Specify multiple type parameters using the appropriate number of commas.</span></span> <span data-ttu-id="76517-109">Dans cet exemple, `GenericClass2` a deux paramètres de type :</span><span class="sxs-lookup"><span data-stu-id="76517-109">In this example, `GenericClass2` has two type parameters:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#50](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-attributes_3.cs)]  
  
 <span data-ttu-id="76517-110">Un attribut peut référencer un type générique construit fermé :</span><span class="sxs-lookup"><span data-stu-id="76517-110">An attribute can reference a closed constructed generic type:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#51](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-attributes_4.cs)]  
  
 <span data-ttu-id="76517-111">Un attribut qui référence un paramètre de type générique entraîne une erreur de compilation :</span><span class="sxs-lookup"><span data-stu-id="76517-111">An attribute that references a generic type parameter will cause a compile-time error:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#52](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-attributes_5.cs)]  
  
 <span data-ttu-id="76517-112">Un type générique ne peut pas hériter d’<xref:System.Attribute> :</span><span class="sxs-lookup"><span data-stu-id="76517-112">A generic type cannot inherit from <xref:System.Attribute>:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#53](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-attributes_6.cs)]  
  
 <span data-ttu-id="76517-113">Pour obtenir des informations sur un type générique ou un paramètre de type au moment de l’exécution, vous pouvez utiliser les méthodes de <xref:System.Reflection>.</span><span class="sxs-lookup"><span data-stu-id="76517-113">To obtain information about a generic type or type parameter at run time, you can use the methods of <xref:System.Reflection>.</span></span> <span data-ttu-id="76517-114">Pour plus d’informations, consultez [Génériques et réflexion](../../../csharp/programming-guide/generics/generics-and-reflection.md)</span><span class="sxs-lookup"><span data-stu-id="76517-114">For more information, see [Generics and Reflection](../../../csharp/programming-guide/generics/generics-and-reflection.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76517-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76517-115">See Also</span></span>  
 [<span data-ttu-id="76517-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="76517-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="76517-117">Génériques</span><span class="sxs-lookup"><span data-stu-id="76517-117">Generics</span></span>](../../../csharp/programming-guide/generics/index.md)  
 [<span data-ttu-id="76517-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="76517-118">Attributes</span></span>](../../../../docs/standard/attributes/index.md)
