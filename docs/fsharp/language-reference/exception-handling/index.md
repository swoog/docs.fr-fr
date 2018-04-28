---
title: Gestion des exceptions (F#)
description: 'Découvrez les principes fondamentaux de la gestion des exceptions dans F # et des liens vers des expressions et des fonctions de gestion des exceptions.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 37b33f9387956ee462ff4977dd4ba34a82e89ec6
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="exception-handling"></a><span data-ttu-id="670f9-103">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="670f9-103">Exception Handling</span></span>

<span data-ttu-id="670f9-104">Cette section contient des informations sur la prise en charge de la gestion des exceptions en langage F#.</span><span class="sxs-lookup"><span data-stu-id="670f9-104">This section contains information about exception handling support in the F# language.</span></span>


## <a name="exception-handling-basics"></a><span data-ttu-id="670f9-105">Concepts de base de la gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="670f9-105">Exception Handling Basics</span></span>
<span data-ttu-id="670f9-106">La gestion des exceptions constitue le moyen standard de gérer les conditions d’erreur dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="670f9-106">Exception handling is the standard way of handling error conditions in the .NET Framework.</span></span> <span data-ttu-id="670f9-107">Par conséquent, tout langage .NET doit prendre en charge ce mécanisme, notamment F#.</span><span class="sxs-lookup"><span data-stu-id="670f9-107">Thus, any .NET language must support this mechanism, including F#.</span></span> <span data-ttu-id="670f9-108">Une *exception* est un objet qui encapsule des informations sur une erreur.</span><span class="sxs-lookup"><span data-stu-id="670f9-108">An *exception* is an object that encapsulates information about an error.</span></span> <span data-ttu-id="670f9-109">Quand des erreurs se produisent, des exceptions sont déclenchées et l’exécution normale s’arrête.</span><span class="sxs-lookup"><span data-stu-id="670f9-109">When errors occur, exceptions are raised and regular execution stops.</span></span> <span data-ttu-id="670f9-110">Le runtime recherche alors un gestionnaire approprié pour l’exception.</span><span class="sxs-lookup"><span data-stu-id="670f9-110">Instead, the runtime searches for an appropriate handler for the exception.</span></span> <span data-ttu-id="670f9-111">La recherche démarre dans la fonction active et remonte dans la pile en passant par les couches d’appelants jusqu’à ce qu’un gestionnaire correspondant soit trouvé.</span><span class="sxs-lookup"><span data-stu-id="670f9-111">The search starts in the current function, and proceeds up the stack through the layers of callers until a matching handler is found.</span></span> <span data-ttu-id="670f9-112">Le gestionnaire est ensuite exécuté.</span><span class="sxs-lookup"><span data-stu-id="670f9-112">Then the handler is executed.</span></span>

<span data-ttu-id="670f9-113">De plus, à mesure que la pile est déroulée, le runtime exécute le code présent dans les blocs `finally` pour garantir que les objets sont nettoyés correctement pendant le processus de déroulement.</span><span class="sxs-lookup"><span data-stu-id="670f9-113">In addition, as the stack is unwound, the runtime executes any code in `finally` blocks, to guarantee that objects are cleaned up correctly during the unwinding process.</span></span>


## <a name="related-topics"></a><span data-ttu-id="670f9-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="670f9-114">Related Topics</span></span>

|<span data-ttu-id="670f9-115">Titre</span><span class="sxs-lookup"><span data-stu-id="670f9-115">Title</span></span>|<span data-ttu-id="670f9-116">Description</span><span class="sxs-lookup"><span data-stu-id="670f9-116">Description</span></span>|
|-----|-----------|
|[<span data-ttu-id="670f9-117">Types d'exceptions</span><span class="sxs-lookup"><span data-stu-id="670f9-117">Exception Types</span></span>](exception-types.md)|<span data-ttu-id="670f9-118">Décrit comment déclarer un type d’exception.</span><span class="sxs-lookup"><span data-stu-id="670f9-118">Describes how to declare an exception type.</span></span>|
|[<span data-ttu-id="670f9-119">Exceptions : expression `try...with`</span><span class="sxs-lookup"><span data-stu-id="670f9-119">Exceptions: The `try...with` Expression</span></span>](the-try-with-expression.md)|<span data-ttu-id="670f9-120">Décrit la construction de langage qui prend en charge la gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="670f9-120">Describes the language construct that supports exception handling.</span></span>|
|[<span data-ttu-id="670f9-121">Exceptions : expression `try...finally`</span><span class="sxs-lookup"><span data-stu-id="670f9-121">Exceptions: The `try...finally` Expression</span></span>](the-try-finally-expression.md)|<span data-ttu-id="670f9-122">Décrit la construction de langage qui vous permet d’exécuter du code de nettoyage à mesure que la pile se déroule quand une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="670f9-122">Describes the language construct that enables you to execute clean-up code as the stack unwinds when an exception is thrown.</span></span>|
|[<span data-ttu-id="670f9-123">Exceptions : fonction `raise`</span><span class="sxs-lookup"><span data-stu-id="670f9-123">Exceptions: the `raise` Function</span></span>](the-raise-Function.md)|<span data-ttu-id="670f9-124">Décrit comment lever un objet exception.</span><span class="sxs-lookup"><span data-stu-id="670f9-124">Describes how to throw an exception object.</span></span>|
|[<span data-ttu-id="670f9-125">Exceptions : fonction `failwith`</span><span class="sxs-lookup"><span data-stu-id="670f9-125">Exceptions: The `failwith` Function</span></span>](the-failwith-function.md)|<span data-ttu-id="670f9-126">Décrit comment générer une exception F# générale.</span><span class="sxs-lookup"><span data-stu-id="670f9-126">Describes how to generate a general F# exception.</span></span>|
|[<span data-ttu-id="670f9-127">Exceptions : fonction `invalidArg`</span><span class="sxs-lookup"><span data-stu-id="670f9-127">Exceptions: The `invalidArg` Function</span></span>](the-invalidArg-function.md)|<span data-ttu-id="670f9-128">Décrit comment générer une exception d’argument non valide.</span><span class="sxs-lookup"><span data-stu-id="670f9-128">Describes how to generate an invalid argument exception.</span></span>|
