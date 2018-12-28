---
title: 'Exceptions : fonction raise'
description: Découvrez comment la F# 'raise' (fonction) est utilisée pour indiquer qu’une erreur ou une condition exceptionnelle s’est produite.
ms.date: 05/16/2016
ms.openlocfilehash: 87773ead7773c62a325c7e7ff105c729e10dd69c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610149"
---
# <a name="exceptions-the-raise-function"></a><span data-ttu-id="88c64-103">Exceptions : fonction raise</span><span class="sxs-lookup"><span data-stu-id="88c64-103">Exceptions: the raise Function</span></span>

<span data-ttu-id="88c64-104">Le `raise` fonction est utilisée pour indiquer qu’une erreur ou une condition exceptionnelle s’est produite.</span><span class="sxs-lookup"><span data-stu-id="88c64-104">The `raise` function is used to indicate that an error or exceptional condition has occurred.</span></span> <span data-ttu-id="88c64-105">Informations sur l’erreur sont capturées dans un objet d’exception.</span><span class="sxs-lookup"><span data-stu-id="88c64-105">Information about the error is captured in an exception object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c64-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88c64-106">Syntax</span></span>

```fsharp
raise (expression)
```

## <a name="remarks"></a><span data-ttu-id="88c64-107">Notes</span><span class="sxs-lookup"><span data-stu-id="88c64-107">Remarks</span></span>

<span data-ttu-id="88c64-108">Le `raise` fonction génère un objet d’exception et lance une processus de déroulement de la pile.</span><span class="sxs-lookup"><span data-stu-id="88c64-108">The `raise` function generates an exception object and initiates a stack unwinding process.</span></span> <span data-ttu-id="88c64-109">Le processus de déroulement de pile est géré par le common language runtime (CLR), donc le comportement de ce processus est le même comme dans tout autre langage .NET.</span><span class="sxs-lookup"><span data-stu-id="88c64-109">The stack unwinding process is managed by the common language runtime (CLR), so the behavior of this process is the same as it is in any other .NET language.</span></span> <span data-ttu-id="88c64-110">Le processus de déroulement de pile est une recherche pour un gestionnaire d’exceptions qui correspond à l’exception générée.</span><span class="sxs-lookup"><span data-stu-id="88c64-110">The stack unwinding process is a search for an exception handler that matches the generated exception.</span></span> <span data-ttu-id="88c64-111">La recherche commence dans le courant `try...with` expression, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="88c64-111">The search starts in the current `try...with` expression, if there is one.</span></span> <span data-ttu-id="88c64-112">Chaque modèle dans le `with` bloc est activé, dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="88c64-112">Each pattern in the `with` block is checked, in order.</span></span> <span data-ttu-id="88c64-113">Quand un gestionnaire d’exceptions correspondant est trouvé, l’exception est considérée comme gérée ; Sinon, la pile est déroulée et `with` blocs de la chaîne d’appel sont vérifiées jusqu'à ce qu’un gestionnaire correspondant est trouvé.</span><span class="sxs-lookup"><span data-stu-id="88c64-113">When a matching exception handler is found, the exception is considered handled; otherwise, the stack is unwound and `with` blocks up the call chain are checked until a matching handler is found.</span></span> <span data-ttu-id="88c64-114">N’importe quel `finally` blocs qui sont produisent dans la chaîne d’appel sont également exécutées en séquence comme la pile se déroule.</span><span class="sxs-lookup"><span data-stu-id="88c64-114">Any `finally` blocks that are encountered in the call chain are also executed in sequence as the stack unwinds.</span></span>

<span data-ttu-id="88c64-115">Le `raise` fonction est l’équivalent de `throw` en c# ou C++.</span><span class="sxs-lookup"><span data-stu-id="88c64-115">The `raise` function is the equivalent of `throw` in C# or C++.</span></span> <span data-ttu-id="88c64-116">Utilisez `reraise` dans un gestionnaire catch pour propager la même exception en haut de la chaîne d’appel.</span><span class="sxs-lookup"><span data-stu-id="88c64-116">Use `reraise` in a catch handler to propagate the same exception up the call chain.</span></span>

<span data-ttu-id="88c64-117">Les exemples de code suivants illustrent l’utilisation de la `raise` fonction permettant de générer une exception.</span><span class="sxs-lookup"><span data-stu-id="88c64-117">The following code examples illustrate the use of the `raise` function to generate an exception.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5801.fs)]

<span data-ttu-id="88c64-118">Le `raise` fonction peut également être utilisée pour lever des exceptions .NET, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="88c64-118">The `raise` function can also be used to raise .NET exceptions, as shown in the following example.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5802.fs)]

## <a name="see-also"></a><span data-ttu-id="88c64-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88c64-119">See also</span></span>

- [<span data-ttu-id="88c64-120">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="88c64-120">Exception Handling</span></span>](index.md)
- [<span data-ttu-id="88c64-121">Types d'exceptions</span><span class="sxs-lookup"><span data-stu-id="88c64-121">Exception Types</span></span>](exception-types.md)
- [<span data-ttu-id="88c64-122">Exceptions : Le `try...with` Expression</span><span class="sxs-lookup"><span data-stu-id="88c64-122">Exceptions: The `try...with` Expression</span></span>](the-try-with-expression.md)
- [<span data-ttu-id="88c64-123">Exceptions : Le `try...finally` Expression</span><span class="sxs-lookup"><span data-stu-id="88c64-123">Exceptions: The `try...finally` Expression</span></span>](the-try-finally-expression.md)
- [<span data-ttu-id="88c64-124">Exceptions : Le `failwith` (fonction)</span><span class="sxs-lookup"><span data-stu-id="88c64-124">Exceptions: The `failwith` Function</span></span>](the-failwith-function.md)
- [<span data-ttu-id="88c64-125">Exceptions : Le `invalidArg` (fonction)</span><span class="sxs-lookup"><span data-stu-id="88c64-125">Exceptions: The `invalidArg` Function</span></span>](the-invalidArg-function.md)