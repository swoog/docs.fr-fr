---
title: Espaces de noms (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, namespaces
- namespaces [C#]
ms.assetid: b1c4ab46-3fad-4ffa-9deb-dd50a2d8c65a
ms.openlocfilehash: 0e678f6577c07e4d56c485e0fd104397eddbd079
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517453"
---
# <a name="namespaces-c-programming-guide"></a><span data-ttu-id="6a705-102">Espaces de noms (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="6a705-102">Namespaces (C# Programming Guide)</span></span>
<span data-ttu-id="6a705-103">Les espaces de noms sont largement utilisés de deux façons dans la programmation avec C#.</span><span class="sxs-lookup"><span data-stu-id="6a705-103">Namespaces are heavily used in C# programming in two ways.</span></span> <span data-ttu-id="6a705-104">Premièrement, le .NET Framework utilise des espaces de noms pour organiser ses nombreuses classes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="6a705-104">First, the .NET Framework uses namespaces to organize its many classes, as follows:</span></span>  
  
 [!code-csharp[csProgGuide#22](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/index_1.cs)]  
  
 <span data-ttu-id="6a705-105">`System` est un espace de noms et `Console` est une classe de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6a705-105">`System` is a namespace and `Console` is a class in that namespace.</span></span> <span data-ttu-id="6a705-106">Vous pouvez utiliser le mot clé `using`. Ainsi, le nom complet n’est pas obligatoire, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6a705-106">The `using` keyword can be used so that the complete name is not required, as in the following example:</span></span>  
  
 [!code-csharp[csProgGuide#1](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/index_2.cs)]  
  
 [!code-csharp[csProgGuide#25](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/index_3.cs)]  
  
 <span data-ttu-id="6a705-107">Pour plus d’informations, consultez [using, directive](../../../csharp/language-reference/keywords/using-directive.md).</span><span class="sxs-lookup"><span data-stu-id="6a705-107">For more information, see [using Directive](../../../csharp/language-reference/keywords/using-directive.md).</span></span>  
  
 <span data-ttu-id="6a705-108">Deuxièmement, la déclaration de vos propres espaces de noms peut vous aider à contrôler l’étendue des noms de classes et de méthodes dans les projets de programmation plus vastes.</span><span class="sxs-lookup"><span data-stu-id="6a705-108">Second, declaring your own namespaces can help you control the scope of class and method names in larger programming projects.</span></span> <span data-ttu-id="6a705-109">Utilisez le mot clé [namespace](../../../csharp/language-reference/keywords/namespace.md) pour déclarer un espace de noms, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6a705-109">Use the [namespace](../../../csharp/language-reference/keywords/namespace.md) keyword to declare a namespace, as in the following example:</span></span>  
  
 [!code-csharp[csProgGuideNamespaces#6](../../../csharp/programming-guide/namespaces/codesnippet/CSharp/index_4.cs)]  
  
## <a name="namespaces-overview"></a><span data-ttu-id="6a705-110">Vue d'ensemble des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="6a705-110">Namespaces Overview</span></span>  
 <span data-ttu-id="6a705-111">Les espaces de noms ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a705-111">Namespaces have the following properties:</span></span>  
  
-   <span data-ttu-id="6a705-112">Ils organisent les projets de code de taille importante.</span><span class="sxs-lookup"><span data-stu-id="6a705-112">They organize large code projects.</span></span>  
  
-   <span data-ttu-id="6a705-113">Ils sont délimités à l’aide de l’opérateur `.`.</span><span class="sxs-lookup"><span data-stu-id="6a705-113">They are delimited by using the `.` operator.</span></span>  
  
-   <span data-ttu-id="6a705-114">La `using directive` évite de devoir spécifier le nom de l’espace de noms pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="6a705-114">The `using directive` obviates the requirement to specify the name of the namespace for every class.</span></span>  
  
-   <span data-ttu-id="6a705-115">L’espace de noms `global` est l’espace de noms « racine » : `global::System` fait toujours référence à l’espace de noms `System` du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6a705-115">The `global` namespace is the "root" namespace: `global::System` will always refer to the .NET Framework namespace `System`.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="6a705-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a705-116">Related Sections</span></span>  
 <span data-ttu-id="6a705-117">Pour plus d’informations sur les espaces de noms, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a705-117">See the following topics for more information about namespaces:</span></span>  
  
-   [<span data-ttu-id="6a705-118">Utilisation d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="6a705-118">Using Namespaces</span></span>](../../../csharp/programming-guide/namespaces/using-namespaces.md)  
  
-   [<span data-ttu-id="6a705-119">Comment : utiliser l’alias d’espace de noms global</span><span class="sxs-lookup"><span data-stu-id="6a705-119">How to: Use the Global Namespace Alias</span></span>](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
-   [<span data-ttu-id="6a705-120">Comment : utiliser l’espace de noms My</span><span class="sxs-lookup"><span data-stu-id="6a705-120">How to: Use the My Namespace</span></span>](../../../csharp/programming-guide/namespaces/how-to-use-the-my-namespace.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="6a705-121">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="6a705-121">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6a705-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a705-122">See Also</span></span>

- [<span data-ttu-id="6a705-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="6a705-123">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="6a705-124">Mots clés d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="6a705-124">Namespace Keywords</span></span>](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [<span data-ttu-id="6a705-125">using, directive</span><span class="sxs-lookup"><span data-stu-id="6a705-125">using Directive</span></span>](../../../csharp/language-reference/keywords/using-directive.md)  
- [<span data-ttu-id="6a705-126">:: (opérateur)</span><span class="sxs-lookup"><span data-stu-id="6a705-126">:: Operator</span></span>](../../../csharp/language-reference/operators/namespace-alias-qualifer.md)  
- [<span data-ttu-id="6a705-127">. Opérateur</span><span class="sxs-lookup"><span data-stu-id="6a705-127">. Operator</span></span>](../../../csharp/language-reference/operators/member-access-operator.md)
