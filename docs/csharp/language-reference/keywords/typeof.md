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
ms.openlocfilehash: f218414bf60a86b95461d747fb6c557f03bcfcb3
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57846114"
---
# <a name="typeof-c-reference"></a><span data-ttu-id="fac09-102">typeof (référence C#)</span><span class="sxs-lookup"><span data-stu-id="fac09-102">typeof (C# Reference)</span></span>

<span data-ttu-id="fac09-103">Permet d’obtenir l’objet <xref:System.Type?displayProperty=nameWithType> pour un type.</span><span class="sxs-lookup"><span data-stu-id="fac09-103">Used to obtain the <xref:System.Type?displayProperty=nameWithType> object for a type.</span></span> <span data-ttu-id="fac09-104">Une expression `typeof` prend la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="fac09-104">A `typeof` expression takes the following form:</span></span>

```csharp
System.Type type = typeof(int);
```

## <a name="remarks"></a><span data-ttu-id="fac09-105">Notes</span><span class="sxs-lookup"><span data-stu-id="fac09-105">Remarks</span></span>

<span data-ttu-id="fac09-106">Pour obtenir le type au moment de l’exécution d’une expression, vous pouvez utiliser la méthode <xref:System.Object.GetType%2A> du .NET Framework, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fac09-106">To obtain the run-time type of an expression, you can use the .NET Framework method <xref:System.Object.GetType%2A>, as in the following example:</span></span>

```csharp
int i = 0;
System.Type type = i.GetType();
```

<span data-ttu-id="fac09-107">L’opérateur `typeof` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="fac09-107">The `typeof` operator cannot be overloaded.</span></span>

<span data-ttu-id="fac09-108">L’opérateur `typeof` peut également être utilisé sur les types génériques ouverts.</span><span class="sxs-lookup"><span data-stu-id="fac09-108">The `typeof` operator can also be used on open generic types.</span></span> <span data-ttu-id="fac09-109">Les types avec plusieurs paramètres de type doivent avoir le nombre approprié de virgules dans la spécification.</span><span class="sxs-lookup"><span data-stu-id="fac09-109">Types with more than one type parameter must have the appropriate number of commas in the specification.</span></span> <span data-ttu-id="fac09-110">Par exemple, <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWIthType> a deux arguments de type ; on utilise donc une virgule :</span><span class="sxs-lookup"><span data-stu-id="fac09-110">For example, the <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWIthType> has two type arguments, so you use one comma:</span></span>

```csharp
Type t = typeof(System.Collection.Generic.Dictionary<,>);
```

<span data-ttu-id="fac09-111">L’exemple suivant montre comment déterminer si le type de retour d’une méthode est un <xref:System.Collections.Generic.IEnumerable%601> générique.</span><span class="sxs-lookup"><span data-stu-id="fac09-111">The following example shows how to determine whether the return type of a method is a generic <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="fac09-112"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> retourne `null` si le type de retour n’est pas un type générique <xref:System.Collections.Generic.IEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="fac09-112"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> will return `null` if the return type is not an <xref:System.Collections.Generic.IEnumerable%601> generic type.</span></span>

[!code-csharp[typeof_3.cs](~/samples/snippets/csharp/keywords/typeof/typeof_3.cs)]

## <a name="example"></a><span data-ttu-id="fac09-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="fac09-113">Example</span></span>

[!code-csharp[csrefKeywordsOperator#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#12)] 

## <a name="example"></a><span data-ttu-id="fac09-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="fac09-114">Example</span></span>

<span data-ttu-id="fac09-115">Cet exemple utilise la méthode <xref:System.Object.GetType%2A> pour déterminer le type utilisé pour contenir le résultat d’un calcul numérique.</span><span class="sxs-lookup"><span data-stu-id="fac09-115">This sample uses the <xref:System.Object.GetType%2A> method to determine the type that is used to contain the result of a numeric calculation.</span></span> <span data-ttu-id="fac09-116">Cela dépend des besoins de stockage du nombre résultant.</span><span class="sxs-lookup"><span data-stu-id="fac09-116">This depends on the storage requirements of the resulting number.</span></span>

[!code-csharp[csrefKeywordsOperator#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#13)]

## <a name="c-language-specification"></a><span data-ttu-id="fac09-117">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="fac09-117">C# language specification</span></span>

<span data-ttu-id="fac09-118">Pour plus d’informations, consultez [Opérateur typeof](~/_csharplang/spec/expressions.md#the-typeof-operator) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="fac09-118">For more information, see [The typeof operator](~/_csharplang/spec/expressions.md#the-typeof-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="fac09-119">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="fac09-119">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="fac09-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fac09-120">See also</span></span>

- <xref:System.Type?displayProperty=nameWithType>
- [<span data-ttu-id="fac09-121">Référence C#</span><span class="sxs-lookup"><span data-stu-id="fac09-121">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="fac09-122">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="fac09-122">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="fac09-123">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="fac09-123">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="fac09-124">is</span><span class="sxs-lookup"><span data-stu-id="fac09-124">is</span></span>](../../../csharp/language-reference/keywords/is.md)
- [<span data-ttu-id="fac09-125">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="fac09-125">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
