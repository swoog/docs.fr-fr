---
title: continue (référence C#)
ms.date: 07/20/2015
f1_keywords:
- continue_CSharpKeyword
- continue
helpviewer_keywords:
- continue keyword [C#]
ms.assetid: 8a5ac96f-f98a-4519-b32d-345847ed7be0
ms.openlocfilehash: b3a9a17bb16ded19330cbc880b2e5e7271f269c3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33215668"
---
# <a name="continue-c-reference"></a><span data-ttu-id="12824-102">continue (référence C#)</span><span class="sxs-lookup"><span data-stu-id="12824-102">continue (C# Reference)</span></span>
<span data-ttu-id="12824-103">L’instruction `continue` passe le contrôle à l’itération suivante de l’instruction [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md) ou [foreach](../../../csharp/language-reference/keywords/foreach-in.md) englobante dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="12824-103">The `continue` statement passes control to the next iteration of the enclosing [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md), or [foreach](../../../csharp/language-reference/keywords/foreach-in.md) statement in which it appears.</span></span>  
  
## <a name="example"></a><span data-ttu-id="12824-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="12824-104">Example</span></span>  
 <span data-ttu-id="12824-105">Dans cet exemple, un compteur est initialisé pour compter de 1 à 10.</span><span class="sxs-lookup"><span data-stu-id="12824-105">In this example, a counter is initialized to count from 1 to 10.</span></span> <span data-ttu-id="12824-106">Si vous utilisez l’instruction `continue` conjointement avec l’expression `(i < 9)`, les instructions entre `continue` et la fin du corps de `for` sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="12824-106">By using the `continue` statement in conjunction with the expression `(i < 9)`, the statements between `continue` and the end of the `for` body are skipped.</span></span>  
  
 [!code-csharp[csrefKeywordsJump#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/continue_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="12824-107">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="12824-107">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="12824-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12824-108">See Also</span></span>  
 [<span data-ttu-id="12824-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="12824-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="12824-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="12824-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="12824-111">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="12824-111">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="12824-112">Instruction break</span><span class="sxs-lookup"><span data-stu-id="12824-112">break Statement</span></span>](/cpp/cpp/break-statement-cpp)  
 [<span data-ttu-id="12824-113">Instructions de saut</span><span class="sxs-lookup"><span data-stu-id="12824-113">Jump Statements</span></span>](../../../csharp/language-reference/keywords/jump-statements.md)
