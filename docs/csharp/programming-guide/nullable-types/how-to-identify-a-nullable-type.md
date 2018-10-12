---
title: Guide pratique pour identifier un type Nullable (Guide de programmation C#)
description: Découvrez comment déterminer si un type est un type Nullable ou si une instance est d’un type Nullable.
ms.date: 09/24/2018
helpviewer_keywords:
- nullable types [C#], identifying
ms.assetid: d4b67ee2-66e8-40c1-ae9d-545d32c71387
ms.openlocfilehash: f9957568d3c68f60cc9286718be9f5a496f876e6
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47400541"
---
# <a name="how-to-identify-a-nullable-type-c-programming-guide"></a><span data-ttu-id="7f23f-103">Guide pratique pour identifier un type Nullable (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="7f23f-103">How to: Identify a nullable type (C# Programming Guide)</span></span>

<span data-ttu-id="7f23f-104">L’exemple suivant montre comment déterminer si une instance <xref:System.Type?displayProperty=nameWithType> représente un type nullable générique fermé, autrement dit, le type <xref:System.Nullable%601?displayProperty=nameWithType> avec un paramètre de type spécifié `T` :</span><span class="sxs-lookup"><span data-stu-id="7f23f-104">The following example shows how to determine whether a <xref:System.Type?displayProperty=nameWithType> instance represents a closed generic nullable type, that is, the <xref:System.Nullable%601?displayProperty=nameWithType> type with a specified type parameter `T`:</span></span>

[!code-csharp-interactive[whether Type is nullable](../../../../samples/snippets/csharp/programming-guide/nullable-types/IdentifyNullableType.cs#1)]

<span data-ttu-id="7f23f-105">Comme l’illustre l’exemple, vous utilisez l’opérateur [typeof](../../language-reference/keywords/typeof.md) pour créer un objet <xref:System.Type?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="7f23f-105">As the example shows, you use the [typeof](../../language-reference/keywords/typeof.md) operator to create a <xref:System.Type?displayProperty=nameWithType> object.</span></span>  
  
<span data-ttu-id="7f23f-106">Si vous souhaitez déterminer si une instance est d’un type Nullable, n’utilisez pas la méthode <xref:System.Object.GetType%2A?displayProperty=nameWithType> pour obtenir une instance <xref:System.Type> à tester avec le code précédent.</span><span class="sxs-lookup"><span data-stu-id="7f23f-106">If you want to determine whether an instance is of a nullable type, don't use the <xref:System.Object.GetType%2A?displayProperty=nameWithType> method to get a <xref:System.Type> instance to be tested with the preceding code.</span></span> <span data-ttu-id="7f23f-107">Quand vous appelez la méthode <xref:System.Object.GetType%2A?displayProperty=nameWithType> sur une instance d’un type Nullable, l’instance est [boxed](using-nullable-types.md#boxing-and-unboxing) à <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="7f23f-107">When you call the <xref:System.Object.GetType%2A?displayProperty=nameWithType> method on an instance of a nullable type, the instance is [boxed](using-nullable-types.md#boxing-and-unboxing) to <xref:System.Object>.</span></span> <span data-ttu-id="7f23f-108">Comme le boxing d’une instance non nulle d’un type Nullable équivaut au boxing d’une valeur du type sous-jacent, <xref:System.Object.GetType%2A> retourne un objet <xref:System.Type> qui représente le type sous-jacent d’un type Nullable :</span><span class="sxs-lookup"><span data-stu-id="7f23f-108">As boxing of a non-null instance of a nullable type is equivalent to boxing of a value of the underlying type, <xref:System.Object.GetType%2A> returns a <xref:System.Type> object that represents the underlying type of a nullable type:</span></span>

[!code-csharp-interactive[GetType example](../../../../samples/snippets/csharp/programming-guide/nullable-types/IdentifyNullableType.cs#2)]

<span data-ttu-id="7f23f-109">N’utilisez pas l’opérateur [is](../../language-reference/keywords/is.md) pour déterminer si une instance est d’un type Nullable.</span><span class="sxs-lookup"><span data-stu-id="7f23f-109">Don't use the [is](../../language-reference/keywords/is.md) operator to determine whether an instance is of a nullable type.</span></span> <span data-ttu-id="7f23f-110">Comme le montre l’exemple suivant, vous ne pouvez pas distinguer les types des instances d’un type Nullable et son type sous-jacent à l’aide de l’opérateur `is` :</span><span class="sxs-lookup"><span data-stu-id="7f23f-110">As the following example shows, you cannot distinguish types of instances of a nullable type and its underlying type with using the `is` operator:</span></span>

[!code-csharp-interactive[is operator example](../../../../samples/snippets/csharp/programming-guide/nullable-types/IdentifyNullableType.cs#3)]

<span data-ttu-id="7f23f-111">Vous pouvez utiliser le code présenté dans l’exemple suivant pour déterminer si une instance est d’un type Nullable :</span><span class="sxs-lookup"><span data-stu-id="7f23f-111">You can use the code presented in the following example to determine whether an instance is of a nullable type:</span></span>

[!code-csharp-interactive[whether an instance is of a nullable type](../../../../samples/snippets/csharp/programming-guide/nullable-types/IdentifyNullableType.cs#4)]
  
## <a name="see-also"></a><span data-ttu-id="7f23f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f23f-112">See also</span></span>

- [<span data-ttu-id="7f23f-113">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="7f23f-113">Nullable types</span></span>](index.md)  
- [<span data-ttu-id="7f23f-114">Utilisation de types Nullable</span><span class="sxs-lookup"><span data-stu-id="7f23f-114">Using nullable types</span></span>](using-nullable-types.md)  
- <xref:System.Nullable.GetUnderlyingType%2A>  
