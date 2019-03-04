---
title: Types imbriqués - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/10/2017
helpviewer_keywords:
- nested types [C#]
ms.assetid: f2e1b315-e3d1-48ce-977f-7bae0960ba99
ms.openlocfilehash: 7269f925b3fc78eea04249984697899b1997c3fb
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976705"
---
# <a name="nested-types-c-programming-guide"></a><span data-ttu-id="68bc1-102">Types imbriqués (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="68bc1-102">Nested Types (C# Programming Guide)</span></span>
<span data-ttu-id="68bc1-103">Un type défini dans une [classe](../../../csharp/language-reference/keywords/class.md) ou un [struct](../../../csharp/language-reference/keywords/struct.md) s’appelle un type imbriqué.</span><span class="sxs-lookup"><span data-stu-id="68bc1-103">A type defined within a [class](../../../csharp/language-reference/keywords/class.md) or [struct](../../../csharp/language-reference/keywords/struct.md) is called a nested type.</span></span> <span data-ttu-id="68bc1-104">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="68bc1-104">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#68](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#68)]  
  
<span data-ttu-id="68bc1-105">Que le type externe soit une classe ou un struct, les types imbriqués sont par défaut [private](../../../csharp/language-reference/keywords/private.md) ; ils sont accessibles uniquement à partir de leur type conteneur.</span><span class="sxs-lookup"><span data-stu-id="68bc1-105">Regardless of whether the outer type is a class or a struct, nested types default to [private](../../../csharp/language-reference/keywords/private.md); they are accessible only from their containing type.</span></span> <span data-ttu-id="68bc1-106">Dans l’exemple précédent, la classe `Nested` est inaccessible aux types externes.</span><span class="sxs-lookup"><span data-stu-id="68bc1-106">In the previous example, the `Nested` class is inaccessible to external types.</span></span> 

<span data-ttu-id="68bc1-107">Vous pouvez aussi spécifier un [modificateur d’accès](../../language-reference/keywords/access-modifiers.md) pour définir l’accessibilité d’un type imbriqué, comme ceci :</span><span class="sxs-lookup"><span data-stu-id="68bc1-107">You can also specify an [access modifier](../../language-reference/keywords/access-modifiers.md) to define the accessibility of a nested type, as follows:</span></span>

- <span data-ttu-id="68bc1-108">Les types imbriqués d’une **classe** peuvent être [public](../../../csharp/language-reference/keywords/public.md), [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md), [protected internal](../../../csharp/language-reference/keywords/protected-internal.md), [private](../../../csharp/language-reference/keywords/private.md) ou [private protected](../../../csharp/language-reference/keywords/private-protected.md).</span><span class="sxs-lookup"><span data-stu-id="68bc1-108">Nested types of a **class** can be [public](../../../csharp/language-reference/keywords/public.md), [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md), [protected internal](../../../csharp/language-reference/keywords/protected-internal.md), [private](../../../csharp/language-reference/keywords/private.md) or [private protected](../../../csharp/language-reference/keywords/private-protected.md).</span></span> 

   <span data-ttu-id="68bc1-109">Cependant, le fait de définir une classe imbriquée `protected`, `protected internal` ou `private protected` à l’intérieur d’une [classe sealed](../../language-reference/keywords/sealed.md) a pour effet de générer l’avertissement de compilateur [CS0628](../../misc/cs0628.md), « nouveau membre protected déclaré dans une classe sealed ».</span><span class="sxs-lookup"><span data-stu-id="68bc1-109">However, defining a `protected`, `protected internal` or `private protected` nested class inside a [sealed class](../../language-reference/keywords/sealed.md) generates compiler warning [CS0628](../../misc/cs0628.md), "new protected member declared in sealed class."</span></span>
  
- <span data-ttu-id="68bc1-110">Les types imbriqués d’un **struct** peuvent être [public](../../../csharp/language-reference/keywords/public.md), [internal](../../../csharp/language-reference/keywords/internal.md) ou [private](../../../csharp/language-reference/keywords/private.md).</span><span class="sxs-lookup"><span data-stu-id="68bc1-110">Nested types of a **struct** can be [public](../../../csharp/language-reference/keywords/public.md), [internal](../../../csharp/language-reference/keywords/internal.md), or [private](../../../csharp/language-reference/keywords/private.md).</span></span>
  
<span data-ttu-id="68bc1-111">L’exemple suivant fait passer le type de la classe `Nested` à public :</span><span class="sxs-lookup"><span data-stu-id="68bc1-111">The following example makes the `Nested` class public:</span></span>
  
 [!code-csharp[csProgGuideObjects#69](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#69)]  
  
 <span data-ttu-id="68bc1-112">Le type imbriqué (ou interne) peut accéder au type conteneur (ou externe).</span><span class="sxs-lookup"><span data-stu-id="68bc1-112">The nested, or inner, type can access the containing, or outer, type.</span></span> <span data-ttu-id="68bc1-113">Pour accéder au type conteneur, passez-le en tant qu’argument au constructeur du type imbriqué.</span><span class="sxs-lookup"><span data-stu-id="68bc1-113">To access the containing type, pass it as an argument to the constructor of the nested type.</span></span> <span data-ttu-id="68bc1-114">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="68bc1-114">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#70](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#70)]  
  
 <span data-ttu-id="68bc1-115">Un type imbriqué a accès à tous les membres qui sont accessibles à son type conteneur.</span><span class="sxs-lookup"><span data-stu-id="68bc1-115">A nested type has access to all of the members that are accessible to its containing type.</span></span> <span data-ttu-id="68bc1-116">Il peut accéder aux membres privés et protégés du type conteneur, y compris à tous les membres protégés hérités.</span><span class="sxs-lookup"><span data-stu-id="68bc1-116">It can access private and protected members of the containing type, including any inherited protected members.</span></span>  
  
 <span data-ttu-id="68bc1-117">Dans la déclaration précédente, le nom complet de classe `Nested` est `Container.Nested`.</span><span class="sxs-lookup"><span data-stu-id="68bc1-117">In the previous declaration, the full name of class `Nested` is `Container.Nested`.</span></span> <span data-ttu-id="68bc1-118">Il s'agit du nom utilisé pour créer une instance de la classe imbriquée, comme suit :</span><span class="sxs-lookup"><span data-stu-id="68bc1-118">This is the name used to create a new instance of the nested class, as follows:</span></span>  
  
 [!code-csharp[csProgGuideObjects#71](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#71)]  
  
## <a name="see-also"></a><span data-ttu-id="68bc1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68bc1-119">See also</span></span>

- [<span data-ttu-id="68bc1-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="68bc1-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="68bc1-121">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="68bc1-121">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
- [<span data-ttu-id="68bc1-122">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="68bc1-122">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)
- [<span data-ttu-id="68bc1-123">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="68bc1-123">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)
