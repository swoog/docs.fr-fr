---
title: var (référence C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- var
- var_CSharpKeyword
helpviewer_keywords:
- var keyword [C#]
ms.assetid: 0777850a-2691-4e3e-927f-0c850f5efe15
caps.latest.revision: 13
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e0df25eb46bb769214412646d0ac3a7a576b3b73
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="var-c-reference"></a><span data-ttu-id="f9c66-102">var (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f9c66-102">var (C# Reference)</span></span>
<span data-ttu-id="f9c66-103">Depuis Visual C# 3.0, les variables déclarées à la portée de la méthode peuvent avoir un type implicite `var`.</span><span class="sxs-lookup"><span data-stu-id="f9c66-103">Beginning in Visual C# 3.0, variables that are declared at method scope can have an implicit "type" `var`.</span></span> <span data-ttu-id="f9c66-104">Une variable locale implicitement typée est fortement typée comme si vous aviez déclaré vous-même le type, alors que c’est le compilateur qui détermine le type.</span><span class="sxs-lookup"><span data-stu-id="f9c66-104">An implicitly typed local variable is strongly typed just as if you had declared the type yourself, but the compiler determines the type.</span></span> <span data-ttu-id="f9c66-105">Les deux déclarations suivantes d’`i` sont équivalentes fonctionnellement :</span><span class="sxs-lookup"><span data-stu-id="f9c66-105">The following two declarations of `i` are functionally equivalent:</span></span>  
  
```  
var i = 10; // implicitly typed  
int i = 10; //explicitly typed  
```  
  
 <span data-ttu-id="f9c66-106">Pour plus d’informations, consultez [Variables locales implicitement typées](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md) et [Relations des types dans des opérations de requête LINQ](../../../csharp/programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f9c66-106">For more information, see [Implicitly Typed Local Variables](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md) and [Type Relationships in LINQ Query Operations](../../../csharp/programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f9c66-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f9c66-107">Example</span></span>  
 <span data-ttu-id="f9c66-108">L’exemple suivant présente deux expressions de requête.</span><span class="sxs-lookup"><span data-stu-id="f9c66-108">The following example shows two query expressions.</span></span> <span data-ttu-id="f9c66-109">Dans la première expression, l’utilisation de `var` est autorisée, mais n’est pas obligatoire parce que le type du résultat de la requête peut être déclaré explicitement en tant que `IEnumerable<string>`.</span><span class="sxs-lookup"><span data-stu-id="f9c66-109">In the first expression, the use of `var` is permitted but is not required, because the type of the query result can be stated explicitly as an `IEnumerable<string>`.</span></span> <span data-ttu-id="f9c66-110">Toutefois, dans la deuxième expression où `var` est utilisé, le résultat peut être une collection de types anonymes, et le nom de ce type n’est pas accessible sauf par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="f9c66-110">However, in the second expression, `var` allows the result to be a collection of anonymous types, and the name of that type is not accessible except to the compiler itself.</span></span> <span data-ttu-id="f9c66-111">Si vous utilisez `var`, vous n’avez pas besoin de créer une classe pour le résultat.</span><span class="sxs-lookup"><span data-stu-id="f9c66-111">Use of `var` eliminates the requirement to create a new class for the result.</span></span> <span data-ttu-id="f9c66-112">Notez que, dans le deuxième exemple, la variable d’itération `foreach` `item` doit également être implicitement typée.</span><span class="sxs-lookup"><span data-stu-id="f9c66-112">Note that in Example #2, the `foreach` iteration variable `item` must also be implicitly typed.</span></span>  
  
 [!code-csharp[csrefKeywordsTypes#18](../../../csharp/language-reference/keywords/codesnippet/CSharp/var_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f9c66-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9c66-113">See Also</span></span>  
 [<span data-ttu-id="f9c66-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f9c66-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="f9c66-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f9c66-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="f9c66-116">Variables locales implicitement typées</span><span class="sxs-lookup"><span data-stu-id="f9c66-116">Implicitly Typed Local Variables</span></span>](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md)
