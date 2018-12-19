---
title: typeof - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- typeof
- typeof_CSharpKeyword
helpviewer_keywords:
- typeof keyword [C#]
ms.assetid: 0c08d880-515e-46bb-8cd2-48b8dd62c08d
ms.openlocfilehash: 3fa82a6faee345be77fc8ea3f5aa3342adecb0f5
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53244841"
---
# <a name="typeof-c-reference"></a><span data-ttu-id="b4491-102">typeof (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b4491-102">typeof (C# Reference)</span></span>

<span data-ttu-id="b4491-103">Permet d’obtenir l’objet <xref:System.Type?displayProperty=nameWithType> pour un type.</span><span class="sxs-lookup"><span data-stu-id="b4491-103">Used to obtain the <xref:System.Type?displayProperty=nameWithType> object for a type.</span></span> <span data-ttu-id="b4491-104">Une expression `typeof` prend la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="b4491-104">A `typeof` expression takes the following form:</span></span>

```csharp
System.Type type = typeof(int);
```

## <a name="remarks"></a><span data-ttu-id="b4491-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b4491-105">Remarks</span></span>

<span data-ttu-id="b4491-106">Pour obtenir le type au moment de l’exécution d’une expression, vous pouvez utiliser la méthode <xref:System.Object.GetType%2A> du .NET Framework, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b4491-106">To obtain the run-time type of an expression, you can use the .NET Framework method <xref:System.Object.GetType%2A>, as in the following example:</span></span>

```csharp
int i = 0;
System.Type type = i.GetType();
```

<span data-ttu-id="b4491-107">L’opérateur `typeof` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="b4491-107">The `typeof` operator cannot be overloaded.</span></span>

<span data-ttu-id="b4491-108">L’opérateur `typeof` peut également être utilisé sur les types génériques ouverts.</span><span class="sxs-lookup"><span data-stu-id="b4491-108">The `typeof` operator can also be used on open generic types.</span></span> <span data-ttu-id="b4491-109">Les types avec plusieurs paramètres de type doivent avoir le nombre approprié de virgules dans la spécification.</span><span class="sxs-lookup"><span data-stu-id="b4491-109">Types with more than one type parameter must have the appropriate number of commas in the specification.</span></span> <span data-ttu-id="b4491-110">L’exemple suivant montre comment déterminer si le type de retour d’une méthode est un <xref:System.Collections.Generic.IEnumerable%601> générique.</span><span class="sxs-lookup"><span data-stu-id="b4491-110">The following example shows how to determine whether the return type of a method is a generic <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="b4491-111"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> retourne `null` si le type de retour n’est pas un type générique <xref:System.Collections.Generic.IEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="b4491-111"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> will return `null` if the return type is not an <xref:System.Collections.Generic.IEnumerable%601> generic type.</span></span>

[!code-csharp[typeof_3.cs](~/samples/snippets/csharp/keywords/typeof/typeof_3.cs)]

## <a name="example"></a><span data-ttu-id="b4491-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="b4491-112">Example</span></span>

[!code-csharp[csrefKeywordsOperator#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#12)] 

## <a name="example"></a><span data-ttu-id="b4491-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="b4491-113">Example</span></span>

<span data-ttu-id="b4491-114">Cet exemple utilise la méthode <xref:System.Object.GetType%2A> pour déterminer le type utilisé pour contenir le résultat d’un calcul numérique.</span><span class="sxs-lookup"><span data-stu-id="b4491-114">This sample uses the <xref:System.Object.GetType%2A> method to determine the type that is used to contain the result of a numeric calculation.</span></span> <span data-ttu-id="b4491-115">Cela dépend des besoins de stockage du nombre résultant.</span><span class="sxs-lookup"><span data-stu-id="b4491-115">This depends on the storage requirements of the resulting number.</span></span>

[!code-csharp[csrefKeywordsOperator#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#13)]

## <a name="c-language-specification"></a><span data-ttu-id="b4491-116">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="b4491-116">C# language specification</span></span>

<span data-ttu-id="b4491-117">Pour plus d’informations, consultez [Opérateur typeof](~/_csharplang/spec/expressions.md#the-typeof-operator) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="b4491-117">For more information, see [The typeof operator](~/_csharplang/spec/expressions.md#the-typeof-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="b4491-118">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="b4491-118">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4491-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4491-119">See also</span></span>

- <xref:System.Type?displayProperty=nameWithType>
- [<span data-ttu-id="b4491-120">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b4491-120">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="b4491-121">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b4491-121">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="b4491-122">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="b4491-122">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="b4491-123">is</span><span class="sxs-lookup"><span data-stu-id="b4491-123">is</span></span>](../../../csharp/language-reference/keywords/is.md)
- [<span data-ttu-id="b4491-124">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="b4491-124">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)