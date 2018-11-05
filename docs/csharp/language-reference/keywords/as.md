---
title: as (référence C#)
ms.date: 10/11/2018
f1_keywords:
- as_CSharpKeyword
- as
helpviewer_keywords:
- type conversion [C#], as keyword
- as keyword [C#]
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
ms.openlocfilehash: ce3163f7d957df96a5c0304adc0b3083d8e20104
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49122712"
---
# <a name="as-c-reference"></a><span data-ttu-id="fb882-102">as (référence C#)</span><span class="sxs-lookup"><span data-stu-id="fb882-102">as (C# Reference)</span></span>
<span data-ttu-id="fb882-103">Vous pouvez utiliser l’opérateur `as` pour effectuer certains types de conversions entre des types référence ou des [types Nullable](../../../csharp/programming-guide/nullable-types/index.md) compatibles.</span><span class="sxs-lookup"><span data-stu-id="fb882-103">You can use the `as` operator to perform certain types of conversions between compatible reference types or [nullable types](../../../csharp/programming-guide/nullable-types/index.md).</span></span> <span data-ttu-id="fb882-104">Le code suivant fournit un exemple.</span><span class="sxs-lookup"><span data-stu-id="fb882-104">The following code shows an example.</span></span>  
  
[!code-csharp[csrefKeywordsOperator#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#1)]

<span data-ttu-id="fb882-105">Comme le montre l’exemple, vous devez comparer le résultat de l’expression `as` avec `null` pour vérifier si la conversion a réussi.</span><span class="sxs-lookup"><span data-stu-id="fb882-105">As the example shows, you need to compare the result of the `as` expression with `null` to check if a conversion is successful.</span></span> <span data-ttu-id="fb882-106">À partir de C# 7.0, vous pouvez utiliser l’expression [is](is.md) pour effectuer ce test et affecter une variable de manière conditionnelle en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="fb882-106">Beginning with C# 7.0, you can use the [is](is.md) expression both to test that a conversion succeeds and conditionally assign a variable when the conversion succeeds.</span></span> <span data-ttu-id="fb882-107">Dans de nombreux scénarios, elle est plus concise que l’opérateur `as`.</span><span class="sxs-lookup"><span data-stu-id="fb882-107">In many scenarios, it's more concise than using the `as` operator.</span></span> <span data-ttu-id="fb882-108">Pour plus d’informations, voir la section [Modèle de type](is.md#type) de l’article [Opérateur `is`](is.md).</span><span class="sxs-lookup"><span data-stu-id="fb882-108">For more information, see the [Type pattern](is.md#type) section of the [`is` operator](is.md) article.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb882-109">Notes</span><span class="sxs-lookup"><span data-stu-id="fb882-109">Remarks</span></span>  
 <span data-ttu-id="fb882-110">L’opérateur `as` est semblable à une opération de cast.</span><span class="sxs-lookup"><span data-stu-id="fb882-110">The `as` operator is like a cast operation.</span></span> <span data-ttu-id="fb882-111">Toutefois, si la conversion n’est pas possible, `as` retourne `null` au lieu de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="fb882-111">However, if the conversion isn't possible, `as` returns `null` instead of raising an exception.</span></span> <span data-ttu-id="fb882-112">Prenons l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fb882-112">Consider the following example:</span></span>  
  
```csharp  
expression as type  
```  
  
 <span data-ttu-id="fb882-113">Le code est équivalent à l’expression suivante, à la différence que la variable `expression` n’est évaluée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="fb882-113">The code is equivalent to the following expression except that the `expression` variable is evaluated only one time.</span></span>  
  
```csharp  
expression is type ? (type)expression : (type)null  
```  
  
 <span data-ttu-id="fb882-114">Notez que l’opérateur `as` effectue uniquement des conversions de référence, des conversions Nullable et des conversions boxing.</span><span class="sxs-lookup"><span data-stu-id="fb882-114">Note that the `as` operator performs only reference conversions, nullable conversions, and boxing conversions.</span></span> <span data-ttu-id="fb882-115">L’opérateur `as` ne peut pas effectuer d’autres conversions, telles que les conversions définies par l’utilisateur, qui doivent être effectuées à l’aide d’expressions cast.</span><span class="sxs-lookup"><span data-stu-id="fb882-115">The `as` operator can't perform other conversions, such as user-defined conversions, which should instead be performed by using cast expressions.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fb882-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb882-116">Example</span></span>  

[!code-csharp[csrefKeywordsOperator#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#2)]
  
## <a name="c-language-specification"></a><span data-ttu-id="fb882-117">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="fb882-117">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fb882-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb882-118">See Also</span></span>  
- [<span data-ttu-id="fb882-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="fb882-119">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="fb882-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="fb882-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="fb882-121">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="fb882-121">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="fb882-122">is</span><span class="sxs-lookup"><span data-stu-id="fb882-122">is</span></span>](../../../csharp/language-reference/keywords/is.md)  
- [<span data-ttu-id="fb882-123">?, opérateur</span><span class="sxs-lookup"><span data-stu-id="fb882-123">?: Operator</span></span>](../../../csharp/language-reference/operators/conditional-operator.md)  
- [<span data-ttu-id="fb882-124">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="fb882-124">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
