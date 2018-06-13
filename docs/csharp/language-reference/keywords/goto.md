---
title: goto (référence C#)
ms.date: 07/20/2015
f1_keywords:
- goto_CSharpKeyword
- goto
helpviewer_keywords:
- goto keyword [C#]
ms.assetid: 2c03c9c1-8119-44ef-b740-fb3d287a42fe
ms.openlocfilehash: 2dd70a30b885dcdae9637b02e8c34ac39f4879fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33216802"
---
# <a name="goto-c-reference"></a><span data-ttu-id="ec4ad-102">goto (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ec4ad-102">goto (C# Reference)</span></span>
<span data-ttu-id="ec4ad-103">L’instruction `goto` transfère le contrôle du programme directement à une instruction étiquetée.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-103">The `goto` statement transfers the program control directly to a labeled statement.</span></span>  
  
 <span data-ttu-id="ec4ad-104">Une utilisation courante de `goto` consiste à transférer le contrôle à une étiquette switch-case ou à l’étiquette par défaut d’une instruction `switch`.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-104">A common use of `goto` is to transfer control to a specific switch-case label or the default label in a `switch` statement.</span></span>  
  
 <span data-ttu-id="ec4ad-105">L’instruction `goto` sert aussi à quitter des boucles fortement imbriquées.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-105">The `goto` statement is also useful to get out of deeply nested loops.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec4ad-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec4ad-106">Example</span></span>  
 <span data-ttu-id="ec4ad-107">L’exemple suivant montre comment utiliser `goto` dans une instruction [switch](../../../csharp/language-reference/keywords/switch.md).</span><span class="sxs-lookup"><span data-stu-id="ec4ad-107">The following example demonstrates using `goto` in a [switch](../../../csharp/language-reference/keywords/switch.md) statement.</span></span>  
  
 [!code-csharp[csrefKeywordsJump#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/goto_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="ec4ad-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec4ad-108">Example</span></span>  
 <span data-ttu-id="ec4ad-109">L’exemple suivant montre comment utiliser `goto` pour quitter des boucles imbriquées.</span><span class="sxs-lookup"><span data-stu-id="ec4ad-109">The following example demonstrates using `goto` to break out from nested loops.</span></span>  
  
 [!code-csharp[csrefKeywordsJump#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/goto_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="ec4ad-110">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ec4ad-110">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ec4ad-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec4ad-111">See Also</span></span>  
 [<span data-ttu-id="ec4ad-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ec4ad-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="ec4ad-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ec4ad-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="ec4ad-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="ec4ad-114">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="ec4ad-115">Instruction GoTo</span><span class="sxs-lookup"><span data-stu-id="ec4ad-115">goto Statement</span></span>](/cpp/cpp/goto-statement-cpp)  
 [<span data-ttu-id="ec4ad-116">Instructions de saut</span><span class="sxs-lookup"><span data-stu-id="ec4ad-116">Jump Statements</span></span>](../../../csharp/language-reference/keywords/jump-statements.md)
