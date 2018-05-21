---
title: -&gt;, opérateur (Informations de référence sur C#)
ms.date: 07/20/2015
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: 037229b2081a43077cb4b5d02a8929b06ba9e077
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="-gt-operator-c-reference"></a><span data-ttu-id="8eafe-102">-&gt;, opérateur (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="8eafe-102">-&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="8eafe-103">L’opérateur `->` allie l’annulation de la référence d’un pointeur et l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="8eafe-103">The `->` operator combines pointer dereferencing and member access.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8eafe-104">Notes</span><span class="sxs-lookup"><span data-stu-id="8eafe-104">Remarks</span></span>  
 <span data-ttu-id="8eafe-105">Une expression de forme</span><span class="sxs-lookup"><span data-stu-id="8eafe-105">An expression of the form,</span></span>  
  
```csharp  
x->y  
```  
  
 <span data-ttu-id="8eafe-106">(où `x` est un pointeur de type `T*` et `y` un membre de `T`) est équivalente à</span><span class="sxs-lookup"><span data-stu-id="8eafe-106">(where `x` is a pointer of type `T*` and `y` is a member of `T`) is equivalent to,</span></span>  
  
```csharp  
(*x).y  
```  
  
 <span data-ttu-id="8eafe-107">L’opérateur `->` peut être utilisé uniquement dans du code marqué comme [unsafe](../../../csharp/language-reference/keywords/unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="8eafe-107">The `->` operator can be used only in code that is marked as [unsafe](../../../csharp/language-reference/keywords/unsafe.md).</span></span>  
  
 <span data-ttu-id="8eafe-108">L’opérateur `->` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="8eafe-108">The `->` operator cannot be overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8eafe-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="8eafe-109">Example</span></span>  
 [!code-csharp[csRefOperators#15](../../../csharp/language-reference/operators/codesnippet/CSharp/dereference-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="8eafe-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8eafe-110">See Also</span></span>  
 [<span data-ttu-id="8eafe-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="8eafe-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="8eafe-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8eafe-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="8eafe-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="8eafe-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
