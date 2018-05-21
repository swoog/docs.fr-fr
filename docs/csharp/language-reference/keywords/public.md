---
title: public (référence C#)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 9bef5d076d9ab84aa15e2cdec2d176db8d1ac82b
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="public-c-reference"></a><span data-ttu-id="b219b-102">public (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b219b-102">public (C# Reference)</span></span>
<span data-ttu-id="b219b-103">Le mot clé `public` est un modificateur d’accès pour les types et les membres de types.</span><span class="sxs-lookup"><span data-stu-id="b219b-103">The `public` keyword is an access modifier for types and type members.</span></span> <span data-ttu-id="b219b-104">L’accès public est le niveau d’accès le plus permissif.</span><span class="sxs-lookup"><span data-stu-id="b219b-104">Public access is the most permissive access level.</span></span> <span data-ttu-id="b219b-105">Il n’existe pas de restrictions d’accès aux membres publics, comme dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="b219b-105">There are no restrictions on accessing public members, as in this example:</span></span>  
  
```csharp  
class SampleClass  
{  
    public int x; // No access restrictions.  
}  
```  
  
 <span data-ttu-id="b219b-106">Pour plus d’informations, consultez [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md) et [Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b219b-106">See [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md) and [Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md) for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b219b-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="b219b-107">Example</span></span>  
 <span data-ttu-id="b219b-108">Dans l’exemple suivant, deux classes sont déclarées, `PointTest` et `MainClass`.</span><span class="sxs-lookup"><span data-stu-id="b219b-108">In the following example, two classes are declared, `PointTest` and `MainClass`.</span></span> <span data-ttu-id="b219b-109">L’accès aux membres publics `x` et `y` de `PointTest` s’effectue directement à partir de `MainClass`.</span><span class="sxs-lookup"><span data-stu-id="b219b-109">The public members `x` and `y` of `PointTest` are accessed directly from `MainClass`.</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#13](../../../csharp/language-reference/keywords/codesnippet/CSharp/public_1.cs)]  
  
 <span data-ttu-id="b219b-110">Si vous remplacez le niveau d’accès `public` par [private](../../../csharp/language-reference/keywords/private.md) ou [protected](../../../csharp/language-reference/keywords/protected.md), le message d’erreur suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="b219b-110">If you change the `public` access level to [private](../../../csharp/language-reference/keywords/private.md) or [protected](../../../csharp/language-reference/keywords/protected.md), you will get the error message:</span></span>  
  
 <span data-ttu-id="b219b-111">'PointTest.y' est inaccessible en raison de son niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="b219b-111">'PointTest.y' is inaccessible due to its protection level.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="b219b-112">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="b219b-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b219b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b219b-113">See Also</span></span>  
 [<span data-ttu-id="b219b-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b219b-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="b219b-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b219b-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="b219b-116">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="b219b-116">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
 [<span data-ttu-id="b219b-117">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="b219b-117">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="b219b-118">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="b219b-118">Access Modifiers</span></span>](../../../csharp/language-reference/keywords/access-modifiers.md)  
 [<span data-ttu-id="b219b-119">Niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="b219b-119">Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/accessibility-levels.md)  
 [<span data-ttu-id="b219b-120">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="b219b-120">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)  
 [<span data-ttu-id="b219b-121">private</span><span class="sxs-lookup"><span data-stu-id="b219b-121">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
 [<span data-ttu-id="b219b-122">protected</span><span class="sxs-lookup"><span data-stu-id="b219b-122">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)  
 [<span data-ttu-id="b219b-123">internal</span><span class="sxs-lookup"><span data-stu-id="b219b-123">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)
