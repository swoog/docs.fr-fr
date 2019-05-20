---
title: partial, type - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- partialtype
- partialtype_CSharpKeyword
helpviewer_keywords:
- partial types [C#]
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
ms.openlocfilehash: 5dba3759d8d0046f2a491e1d3408acb54bd0343d
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633373"
---
# <a name="partial-type-c-reference"></a><span data-ttu-id="42208-102">partial, type (référence C#)</span><span class="sxs-lookup"><span data-stu-id="42208-102">partial type (C# Reference)</span></span>

<span data-ttu-id="42208-103">Les définitions de type partiel permettent le fractionnement de la définition d’une classe, d’un struct ou d’une interface entre plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="42208-103">Partial type definitions allow for the definition of a class, struct, or interface to be split into multiple files.</span></span>

<span data-ttu-id="42208-104">Dans *File1.cs* :</span><span class="sxs-lookup"><span data-stu-id="42208-104">In *File1.cs*:</span></span>

[!code-csharp[csrefKeywordsContextual#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#3)]  

<span data-ttu-id="42208-105">Déclaration dans *File2.cs* :</span><span class="sxs-lookup"><span data-stu-id="42208-105">In *File2.cs* the declaration:</span></span>

[!code-csharp[csrefKeywordsContextual#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#4)]  

## <a name="remarks"></a><span data-ttu-id="42208-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="42208-106">Remarks</span></span>

<span data-ttu-id="42208-107">Fractionner un type de classe, de struct ou d’interface entre plusieurs fichiers peut être utile si vous travaillez sur des projets volumineux ou des projets contenant du code généré automatiquement, comme celui fourni par le [Concepteur Windows Forms](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="42208-107">Splitting a class, struct or interface type over several files can be useful when you are working with large projects, or with automatically generated code such as that provided by the [Windows Forms Designer](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).</span></span> <span data-ttu-id="42208-108">Un type partiel peut contenir une [méthode partielle](partial-method.md).</span><span class="sxs-lookup"><span data-stu-id="42208-108">A partial type may contain a [partial method](partial-method.md).</span></span> <span data-ttu-id="42208-109">Pour plus d’informations, consultez [Classes et méthodes partielles](../../programming-guide/classes-and-structs/partial-classes-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="42208-109">For more information, see [Partial Classes and Methods](../../programming-guide/classes-and-structs/partial-classes-and-methods.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="42208-110">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="42208-110">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="42208-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42208-111">See also</span></span>

- [<span data-ttu-id="42208-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="42208-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="42208-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="42208-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="42208-114">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="42208-114">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="42208-115">Introduction aux génériques</span><span class="sxs-lookup"><span data-stu-id="42208-115">Introduction to Generics</span></span>](../../programming-guide/generics/introduction-to-generics.md)
