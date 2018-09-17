---
title: lock, instruction (référence C#)
description: Utilisez l’instruction lock en C# pour synchroniser l’accès des threads à une ressource partagée
ms.date: 08/28/2018
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 2b6fbfb2f81d7745c4effb9ea0087f34cc872a6c
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858354"
---
# <a name="lock-statement-c-reference"></a><span data-ttu-id="d6257-103">lock, instruction (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d6257-103">lock statement (C# Reference)</span></span>

<span data-ttu-id="d6257-104">L’instruction `lock` obtient le verrou d’exclusion mutuelle d’un objet donné, exécute un bloc d’instructions, puis libère le verrou.</span><span class="sxs-lookup"><span data-stu-id="d6257-104">The `lock` statement obtains the mutual-exclusion lock for a given object, executes a statement block, and then releases the lock.</span></span> <span data-ttu-id="d6257-105">Tant qu’un verrou est maintenu, le thread qui contient le verrou peut à nouveau obtenir et libérer le verrou.</span><span class="sxs-lookup"><span data-stu-id="d6257-105">While a lock is held, the thread that holds the lock can again obtain and release the lock.</span></span> <span data-ttu-id="d6257-106">Tout autre thread se voit bloquer l’obtention du verrou et attend que ce dernier soit libéré.</span><span class="sxs-lookup"><span data-stu-id="d6257-106">Any other thread is blocked from obtaining the lock and waits until the lock is released.</span></span>

<span data-ttu-id="d6257-107">L’instruction `lock` se présente sous la forme</span><span class="sxs-lookup"><span data-stu-id="d6257-107">The `lock` statement is of the form</span></span>

```csharp
lock (x)
{
    // Your code...
}
```

<span data-ttu-id="d6257-108">où `x` est une expression de [type référence](reference-types.md).</span><span class="sxs-lookup"><span data-stu-id="d6257-108">where `x` is an expression of a [reference type](reference-types.md).</span></span> <span data-ttu-id="d6257-109">Elle équivaut précisément à</span><span class="sxs-lookup"><span data-stu-id="d6257-109">It's precisely equivalent to</span></span>

```csharp
object __lockObj = x;
bool __lockWasTaken = false;
try
{
    System.Threading.Monitor.Enter(__lockObj, ref __lockWasTaken);
    // Your code...
}
finally
{
    if (__lockWasTaken) System.Threading.Monitor.Exit(__lockObj);
}
```

<span data-ttu-id="d6257-110">Dans la mesure où le code utilise un bloc [try...finally](try-finally.md), le verrou est libéré même si une exception est levée dans le corps d’une instruction `lock`.</span><span class="sxs-lookup"><span data-stu-id="d6257-110">Since the code uses a [try...finally](try-finally.md) block, the lock is released even if an exception is thrown within the body of a `lock` statement.</span></span>

<span data-ttu-id="d6257-111">Vous ne pouvez pas utiliser le mot clé [await](await.md) dans le corps d’une instruction `lock`.</span><span class="sxs-lookup"><span data-stu-id="d6257-111">You can't use the [await](await.md) keyword in the body of a `lock` statement.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6257-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d6257-112">Remarks</span></span>

<span data-ttu-id="d6257-113">Quand vous synchronisez l’accès des threads à une ressource partagée, verrouillez une instance d’objet dédiée (par exemple `private readonly object balanceLock = new object();`) ou toute autre instance peu susceptible d’être utilisée comme objet de verrouillage par des parties du code non associées.</span><span class="sxs-lookup"><span data-stu-id="d6257-113">When you synchronize thread access to shared resource, lock on a dedicated object instance (for example, `private readonly object balanceLock = new object();`) or another instance that is unlikely to be used as a lock object by unrelated parts of the code.</span></span> <span data-ttu-id="d6257-114">Évitez d’utiliser la même instance d’objet de verrouillage pour différentes ressources partagées, car cela peut entraîner une contention d’interblocage ou de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="d6257-114">Avoid using the same lock object instance for different shared resources, as it might result in deadlock or lock contention.</span></span> <span data-ttu-id="d6257-115">En particulier, évitez</span><span class="sxs-lookup"><span data-stu-id="d6257-115">In particular, avoid using</span></span>

- <span data-ttu-id="d6257-116">`this` (peut être utilisé en tant que verrou par les appelants)</span><span class="sxs-lookup"><span data-stu-id="d6257-116">`this` (might be used by the callers as a lock),</span></span>
- <span data-ttu-id="d6257-117">Les instances de <xref:System.Type> (peuvent être obtenues par l’opérateur [typeof](typeof.md) ou par réflexion)</span><span class="sxs-lookup"><span data-stu-id="d6257-117"><xref:System.Type> instances (might be obtained by the [typeof](typeof.md) operator or reflection),</span></span>
- <span data-ttu-id="d6257-118">Les instances de chaîne, notamment les littéraux de chaîne</span><span class="sxs-lookup"><span data-stu-id="d6257-118">string instances, including string literals,</span></span>

<span data-ttu-id="d6257-119">en tant qu’objets de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="d6257-119">as lock objects.</span></span>

## <a name="example"></a><span data-ttu-id="d6257-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="d6257-120">Example</span></span>

<span data-ttu-id="d6257-121">L’exemple suivant définit une classe `Account`, qui synchronise l’accès à son champ `balance` privé en verrouillant une instance `balanceLock` dédiée.</span><span class="sxs-lookup"><span data-stu-id="d6257-121">The following example defines an `Account` class that synchronizes access to its private `balance` field by locking on a dedicated `balanceLock` instance.</span></span> <span data-ttu-id="d6257-122">L’utilisation de la même instance pour le verrouillage permet de garantir que le champ `balance` ne peut pas être mis à jour simultanément par deux threads qui tentent d’appeler les méthodes `Debit` ou `Credit` en même temps.</span><span class="sxs-lookup"><span data-stu-id="d6257-122">Using the same instance for locking ensures that the `balance` field cannot be updated simultaneously by two threads attempting to call the `Debit` or `Credit` methods simultaneously.</span></span>

[!code-csharp[lock-statement-example](~/samples/snippets/csharp/keywords/LockStatementExample.cs)]

## <a name="c-language-specification"></a><span data-ttu-id="d6257-123">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="d6257-123">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="d6257-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6257-124">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.SpinLock?displayProperty=nameWithType>
- <xref:System.Threading.Interlocked?displayProperty=nameWithType>
- [<span data-ttu-id="d6257-125">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d6257-125">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d6257-126">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="d6257-126">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="d6257-127">Mots clés d’instructions</span><span class="sxs-lookup"><span data-stu-id="d6257-127">Statement Keywords</span></span>](statement-keywords.md)
- [<span data-ttu-id="d6257-128">Opérations verrouillées</span><span class="sxs-lookup"><span data-stu-id="d6257-128">Interlocked operations</span></span>](../../../standard/threading/interlocked-operations.md)
- [<span data-ttu-id="d6257-129">Vue d’ensemble des primitives de synchronisation</span><span class="sxs-lookup"><span data-stu-id="d6257-129">Overview of synchronization primitives</span></span>](../../../standard/threading/overview-of-synchronization-primitives.md)