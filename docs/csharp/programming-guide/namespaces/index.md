---
title: Espaces de noms - Guide de programmation C#
ms.custom: seodec18
ms.date: 08/21/2018
helpviewer_keywords:
- C# language, namespaces
- namespaces [C#]
ms.assetid: b1c4ab46-3fad-4ffa-9deb-dd50a2d8c65a
ms.openlocfilehash: 3e05e18225b198e9e34b4b96717cc813dab836c7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61710080"
---
# <a name="namespaces-c-programming-guide"></a><span data-ttu-id="ee291-102">Espaces de noms (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="ee291-102">Namespaces (C# Programming Guide)</span></span>

<span data-ttu-id="ee291-103">Les espaces de noms sont largement utilisés de deux façons dans la programmation avec C#.</span><span class="sxs-lookup"><span data-stu-id="ee291-103">Namespaces are heavily used in C# programming in two ways.</span></span> <span data-ttu-id="ee291-104">Premièrement, le .NET Framework utilise des espaces de noms pour organiser ses nombreuses classes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee291-104">First, the .NET Framework uses namespaces to organize its many classes, as follows:</span></span>  
  
 [!code-csharp[csProgGuide#22](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuide/CS/progGuide.cs#22)]  
  
<span data-ttu-id="ee291-105">`System` est un espace de noms et `Console` est une classe de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ee291-105">`System` is a namespace and `Console` is a class in that namespace.</span></span> <span data-ttu-id="ee291-106">Vous pouvez utiliser le mot clé `using`. Ainsi, le nom complet n’est pas obligatoire, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ee291-106">The `using` keyword can be used so that the complete name is not required, as in the following example:</span></span>  
  
 [!code-csharp[csProgGuide#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuide/CS/using.cs#1)]  
  
 [!code-csharp[csProgGuide#25](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuide/CS/progGuide.cs#25)]  
  
<span data-ttu-id="ee291-107">Pour plus d’informations, consultez [Directive using](../../language-reference/keywords/using-directive.md).</span><span class="sxs-lookup"><span data-stu-id="ee291-107">For more information, see the [using Directive](../../language-reference/keywords/using-directive.md).</span></span>  
  
<span data-ttu-id="ee291-108">Deuxièmement, la déclaration de vos propres espaces de noms peut vous aider à contrôler l’étendue des noms de classes et de méthodes dans les projets de programmation plus vastes.</span><span class="sxs-lookup"><span data-stu-id="ee291-108">Second, declaring your own namespaces can help you control the scope of class and method names in larger programming projects.</span></span> <span data-ttu-id="ee291-109">Utilisez le mot clé [namespace](../../language-reference/keywords/namespace.md) pour déclarer un espace de noms, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ee291-109">Use the [namespace](../../language-reference/keywords/namespace.md) keyword to declare a namespace, as in the following example:</span></span>  
  
 [!code-csharp[csProgGuideNamespaces#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideNamespaces/CS/Namespaces.cs#6)]

<span data-ttu-id="ee291-110">Le nom de l’espace de noms doit être un [nom d’identificateur](../inside-a-program/identifier-names.md) C# valide.</span><span class="sxs-lookup"><span data-stu-id="ee291-110">The name of the namespace must be a valid C# [identifier name](../inside-a-program/identifier-names.md).</span></span>

## <a name="namespaces-overview"></a><span data-ttu-id="ee291-111">Vue d'ensemble des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="ee291-111">Namespaces Overview</span></span>  

<span data-ttu-id="ee291-112">Les espaces de noms ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee291-112">Namespaces have the following properties:</span></span>  
  
- <span data-ttu-id="ee291-113">Ils organisent les projets de code de taille importante.</span><span class="sxs-lookup"><span data-stu-id="ee291-113">They organize large code projects.</span></span>  
- <span data-ttu-id="ee291-114">Ils sont délimités à l’aide de l’opérateur `.`.</span><span class="sxs-lookup"><span data-stu-id="ee291-114">They are delimited by using the `.` operator.</span></span>  
- <span data-ttu-id="ee291-115">La directive `using` évite de devoir spécifier le nom de l’espace de noms pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="ee291-115">The `using` directive obviates the requirement to specify the name of the namespace for every class.</span></span>  
- <span data-ttu-id="ee291-116">L’espace de noms `global` est l’espace de noms « racine » : `global::System` fait toujours référence à l’espace de noms <xref:System> .NET.</span><span class="sxs-lookup"><span data-stu-id="ee291-116">The `global` namespace is the "root" namespace: `global::System` will always refer to the .NET <xref:System> namespace.</span></span>  

## <a name="c-language-specification"></a><span data-ttu-id="ee291-117">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ee291-117">C# Language Specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ee291-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee291-118">See also</span></span>

- [<span data-ttu-id="ee291-119">Utilisation d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="ee291-119">Using Namespaces</span></span>](using-namespaces.md)
- [<span data-ttu-id="ee291-120">Guide pratique pour utiliser l’alias d’espace de noms global</span><span class="sxs-lookup"><span data-stu-id="ee291-120">How to: Use the Global Namespace Alias</span></span>](how-to-use-the-global-namespace-alias.md)
- [<span data-ttu-id="ee291-121">Guide pratique pour utiliser l’espace de noms My</span><span class="sxs-lookup"><span data-stu-id="ee291-121">How to: Use the My Namespace</span></span>](how-to-use-the-my-namespace.md)
- [<span data-ttu-id="ee291-122">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ee291-122">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="ee291-123">Noms d’identificateur</span><span class="sxs-lookup"><span data-stu-id="ee291-123">Identifier names</span></span>](../inside-a-program/identifier-names.md)
- [<span data-ttu-id="ee291-124">Mots clés d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="ee291-124">Namespace Keywords</span></span>](../../language-reference/keywords/namespace-keywords.md)
- [<span data-ttu-id="ee291-125">using, directive</span><span class="sxs-lookup"><span data-stu-id="ee291-125">using Directive</span></span>](../../language-reference/keywords/using-directive.md)
- [<span data-ttu-id="ee291-126">:: Opérateur</span><span class="sxs-lookup"><span data-stu-id="ee291-126">:: Operator</span></span>](../../language-reference/operators/namespace-alias-qualifer.md)
- [<span data-ttu-id="ee291-127">. Opérateur</span><span class="sxs-lookup"><span data-stu-id="ee291-127">. Operator</span></span>](../../language-reference/operators/member-access-operator.md)
