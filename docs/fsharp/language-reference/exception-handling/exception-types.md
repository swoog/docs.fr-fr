---
title: Types d'exceptions
description: Découvrez comment définir et utiliser F# types d’exception.
ms.date: 05/16/2016
ms.openlocfilehash: b7203dc042c7207bca95cfd0372790bfe52e0226
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645572"
---
# <a name="exception-types"></a><span data-ttu-id="59930-103">Types d'exceptions</span><span class="sxs-lookup"><span data-stu-id="59930-103">Exception Types</span></span>

<span data-ttu-id="59930-104">Il existe deux catégories d’exceptions dans F#: types d’exceptions .NET et F# types d’exception.</span><span class="sxs-lookup"><span data-stu-id="59930-104">There are two categories of exceptions in F#: .NET exception types and F# exception types.</span></span> <span data-ttu-id="59930-105">Cette rubrique décrit comment définir et utiliser F# types d’exception.</span><span class="sxs-lookup"><span data-stu-id="59930-105">This topic describes how to define and use F# exception types.</span></span>

## <a name="syntax"></a><span data-ttu-id="59930-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59930-106">Syntax</span></span>

```fsharp
exception exception-type of argument-type
```

## <a name="remarks"></a><span data-ttu-id="59930-107">Notes</span><span class="sxs-lookup"><span data-stu-id="59930-107">Remarks</span></span>

<span data-ttu-id="59930-108">Dans la syntaxe précédente, *type d’exception* est le nom d’un nouveau F# type d’exception, et *type d’argument* représente le type d’un argument qui peut être fourni lorsque vous déclenchez une exception de ce type.</span><span class="sxs-lookup"><span data-stu-id="59930-108">In the previous syntax, *exception-type* is the name of a new F# exception type, and *argument-type* represents the type of an argument that can be supplied when you raise an exception of this type.</span></span> <span data-ttu-id="59930-109">Vous pouvez spécifier plusieurs arguments à l’aide d’un type de tuple pour *type d’argument*.</span><span class="sxs-lookup"><span data-stu-id="59930-109">You can specify multiple arguments by using a tuple type for *argument-type*.</span></span>

<span data-ttu-id="59930-110">Une définition classique pour un F# exception ressemble à ceci.</span><span class="sxs-lookup"><span data-stu-id="59930-110">A typical definition for an F# exception resembles the following.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5501.fs)]

<span data-ttu-id="59930-111">Vous pouvez générer une exception de ce type à l’aide de la `raise` de fonction, comme suit.</span><span class="sxs-lookup"><span data-stu-id="59930-111">You can generate an exception of this type by using the `raise` function, as follows.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5502.fs)]

<span data-ttu-id="59930-112">Vous pouvez utiliser un F# type d’exception directement dans les filtres dans un `try...with` expression, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="59930-112">You can use an F# exception type directly in the filters in a `try...with` expression, as shown in the following example.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5503.fs)]

<span data-ttu-id="59930-113">Le type d’exception que vous définissez avec le `exception` mot clé dans F# est un nouveau type qui hérite de `System.Exception`.</span><span class="sxs-lookup"><span data-stu-id="59930-113">The exception type that you define with the `exception` keyword in F# is a new type that inherits from `System.Exception`.</span></span>

## <a name="see-also"></a><span data-ttu-id="59930-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59930-114">See also</span></span>

- [<span data-ttu-id="59930-115">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="59930-115">Exception Handling</span></span>](index.md)
- [<span data-ttu-id="59930-116">Exceptions : fonction `raise`</span><span class="sxs-lookup"><span data-stu-id="59930-116">Exceptions: the `raise` Function</span></span>](the-raise-function.md)
- [<span data-ttu-id="59930-117">Hiérarchie des exceptions</span><span class="sxs-lookup"><span data-stu-id="59930-117">Exception Hierarchy</span></span>](https://msdn.microsoft.com/library/z4c5tckx.aspx)
