---
title: as (référence C#)
ms.date: 07/20/2015
f1_keywords:
- as_CSharpKeyword
- as
helpviewer_keywords:
- type conversion [C#], as keyword
- as keyword [C#]
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
ms.openlocfilehash: aee80b3262ccd9432d7c311dddec47185b66d05f
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43003071"
---
# <a name="as-c-reference"></a><span data-ttu-id="9a2ff-102">as (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9a2ff-102">as (C# Reference)</span></span>
<span data-ttu-id="9a2ff-103">Vous pouvez utiliser l’opérateur `as` pour effectuer certains types de conversions entre des types référence ou des [types Nullable](../../../csharp/programming-guide/nullable-types/index.md) compatibles.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-103">You can use the `as` operator to perform certain types of conversions between compatible reference types or [nullable types](../../../csharp/programming-guide/nullable-types/index.md).</span></span> <span data-ttu-id="9a2ff-104">Le code suivant fournit un exemple.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-104">The following code shows an example.</span></span>  
  
[!code-csharp[csrefKeywordsOperator#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#1)]
  
## <a name="remarks"></a><span data-ttu-id="9a2ff-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9a2ff-105">Remarks</span></span>  
 <span data-ttu-id="9a2ff-106">L’opérateur `as` est semblable à une opération de cast.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-106">The `as` operator is like a cast operation.</span></span> <span data-ttu-id="9a2ff-107">Toutefois, si la conversion n’est pas possible, `as` retourne `null` au lieu de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-107">However, if the conversion isn't possible, `as` returns `null` instead of raising an exception.</span></span> <span data-ttu-id="9a2ff-108">Prenons l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="9a2ff-108">Consider the following example:</span></span>  
  
```csharp  
expression as type  
```  
  
 <span data-ttu-id="9a2ff-109">Le code est équivalent à l’expression suivante, à la différence que la variable `expression` n’est évaluée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-109">The code is equivalent to the following expression except that the `expression` variable is evaluated only one time.</span></span>  
  
```csharp  
expression is type ? (type)expression : (type)null  
```  
  
 <span data-ttu-id="9a2ff-110">Notez que l’opérateur `as` effectue uniquement des conversions de référence, des conversions Nullable et des conversions boxing.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-110">Note that the `as` operator performs only reference conversions, nullable conversions, and boxing conversions.</span></span> <span data-ttu-id="9a2ff-111">L’opérateur `as` ne peut pas effectuer d’autres conversions, telles que les conversions définies par l’utilisateur, qui doivent être effectuées à l’aide d’expressions cast.</span><span class="sxs-lookup"><span data-stu-id="9a2ff-111">The `as` operator can't perform other conversions, such as user-defined conversions, which should instead be performed by using cast expressions.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a2ff-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a2ff-112">Example</span></span>  

[!code-csharp[csrefKeywordsOperator#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#2)]
  
## <a name="c-language-specification"></a><span data-ttu-id="9a2ff-113">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9a2ff-113">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9a2ff-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a2ff-114">See Also</span></span>  
- [<span data-ttu-id="9a2ff-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9a2ff-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="9a2ff-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9a2ff-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9a2ff-117">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="9a2ff-117">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="9a2ff-118">is</span><span class="sxs-lookup"><span data-stu-id="9a2ff-118">is</span></span>](../../../csharp/language-reference/keywords/is.md)  
- [<span data-ttu-id="9a2ff-119">?, opérateur</span><span class="sxs-lookup"><span data-stu-id="9a2ff-119">?: Operator</span></span>](../../../csharp/language-reference/operators/conditional-operator.md)  
- [<span data-ttu-id="9a2ff-120">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="9a2ff-120">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
