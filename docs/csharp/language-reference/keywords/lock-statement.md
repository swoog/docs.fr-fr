---
title: lock, instruction (référence C#)
description: 'Le mot-clé lock est utilisé dans le threading '
ms.date: 07/20/2015
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 6ed46837482642dfd7e1a96cd120fc18023c5e9f
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931191"
---
# <a name="lock-statement-c-reference"></a><span data-ttu-id="ade36-103">lock, instruction (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ade36-103">lock statement (C# Reference)</span></span>

<span data-ttu-id="ade36-104">Le mot clé `lock` marque un bloc d’instructions comme étant une section critique en obtenant le verrou d’exclusion mutuelle pour un objet donné, en exécutant une instruction, puis en libérant le verrou.</span><span class="sxs-lookup"><span data-stu-id="ade36-104">The `lock` keyword marks a statement block as a critical section by obtaining the mutual-exclusion lock for a given object, executing a statement, and then releasing the lock.</span></span> <span data-ttu-id="ade36-105">L’exemple suivant inclut une instruction `lock`.</span><span class="sxs-lookup"><span data-stu-id="ade36-105">The following example includes a `lock` statement.</span></span>

```csharp
class Account
{
    decimal balance;
    private Object thisLock = new Object();

    public void Withdraw(decimal amount)
    {
        lock (thisLock)
        {
            if (amount > balance)
            {
                throw new Exception("Insufficient funds");
            }
            balance -= amount;
        }
    }
}
```

<span data-ttu-id="ade36-106">Pour plus d’informations, consultez [Synchronisation des threads](../../programming-guide/concepts/threading/thread-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="ade36-106">For more information, see [Thread Synchronization](../../programming-guide/concepts/threading/thread-synchronization.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ade36-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ade36-107">Remarks</span></span>

<span data-ttu-id="ade36-108">Le mot clé `lock` garantit qu’un thread n’entre pas dans une section critique de code alors qu’un autre thread est dans cette section critique.</span><span class="sxs-lookup"><span data-stu-id="ade36-108">The `lock` keyword ensures that one thread does not enter a critical section of code while another thread is in the critical section.</span></span> <span data-ttu-id="ade36-109">Si un autre thread tente d’entrer dans un code verrouillé, il attend, en restant bloqué jusqu’à ce que l’objet soit libéré.</span><span class="sxs-lookup"><span data-stu-id="ade36-109">If another thread tries to enter a locked code, it will wait, block, until the object is released.</span></span>

<span data-ttu-id="ade36-110">La section [Threading](../../programming-guide/concepts/threading/index.md) présente le threading.</span><span class="sxs-lookup"><span data-stu-id="ade36-110">The section [Threading](../../programming-guide/concepts/threading/index.md) discusses threading.</span></span>

<span data-ttu-id="ade36-111">Le mot clé `lock` appelle <xref:System.Threading.Monitor.Enter%2A> au début du bloc et <xref:System.Threading.Monitor.Exit%2A> à la fin du bloc.</span><span class="sxs-lookup"><span data-stu-id="ade36-111">The `lock` keyword calls <xref:System.Threading.Monitor.Enter%2A> at the start of the block and <xref:System.Threading.Monitor.Exit%2A> at the end of the block.</span></span> <span data-ttu-id="ade36-112">Une exception <xref:System.Threading.ThreadInterruptedException> est levée si <xref:System.Threading.Thread.Interrupt%2A> interrompt un thread qui attend de passer une instruction `lock`.</span><span class="sxs-lookup"><span data-stu-id="ade36-112">A <xref:System.Threading.ThreadInterruptedException> is thrown if <xref:System.Threading.Thread.Interrupt%2A> interrupts a thread that is waiting to enter a `lock` statement.</span></span>

<span data-ttu-id="ade36-113">D’une façon générale, évitez de verrouiller sur un type `public` ou sur des instances qui sont au-delà du contrôle de votre code.</span><span class="sxs-lookup"><span data-stu-id="ade36-113">In general, avoid locking on a `public` type, or instances beyond your code's control.</span></span> <span data-ttu-id="ade36-114">Les constructions courantes `lock (this)`, `lock (typeof (MyType))` et `lock ("myLock")` enfreignent cette directive :</span><span class="sxs-lookup"><span data-stu-id="ade36-114">The common constructs `lock (this)`, `lock (typeof (MyType))`, and `lock ("myLock")` violate this guideline:</span></span>

- <span data-ttu-id="ade36-115">`lock (this)` est un problème si l’instance est accessible publiquement.</span><span class="sxs-lookup"><span data-stu-id="ade36-115">`lock (this)` is a problem if the instance can be accessed publicly.</span></span>

- <span data-ttu-id="ade36-116">`lock (typeof (MyType))` est un problème si `MyType` est accessible publiquement.</span><span class="sxs-lookup"><span data-stu-id="ade36-116">`lock (typeof (MyType))` is a problem if `MyType` is publicly accessible.</span></span>

- <span data-ttu-id="ade36-117">`lock("myLock")` est un problème, car tout autre code dans le processus utilisant la même chaîne partagera le même verrou.</span><span class="sxs-lookup"><span data-stu-id="ade36-117">`lock("myLock")` is a problem because any other code in the process using the same string, will share the same lock.</span></span>

<span data-ttu-id="ade36-118">La bonne pratique consiste à définir un objet `private` à verrouiller, ou une variable objet `private static` pour protéger les données communes à toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="ade36-118">Best practice is to define a `private` object to lock on, or a `private static` object variable to protect data common to all instances.</span></span>

<span data-ttu-id="ade36-119">Vous ne pouvez pas utiliser le mot clé [await](await.md) dans le corps d’une instruction `lock`.</span><span class="sxs-lookup"><span data-stu-id="ade36-119">You can't use the [await](await.md) keyword in the body of a `lock` statement.</span></span>

## <a name="example---threads-without-locking"></a><span data-ttu-id="ade36-120">Exemple - Threads sans verrouillage</span><span class="sxs-lookup"><span data-stu-id="ade36-120">Example - Threads without locking</span></span>

<span data-ttu-id="ade36-121">L’exemple suivant montre une utilisation simple des threads sans verrouillage en C# :</span><span class="sxs-lookup"><span data-stu-id="ade36-121">The following sample shows a simple use of threads without locking in C#:</span></span>

[!code-csharp[csrefKeywordsFixedLock#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#5)]

## <a name="example---threads-using-locking"></a><span data-ttu-id="ade36-122">Exemple : Threads utilisant le verrouillage</span><span class="sxs-lookup"><span data-stu-id="ade36-122">Example - Threads using locking</span></span>

<span data-ttu-id="ade36-123">L’exemple suivant utilise des threads et `lock`.</span><span class="sxs-lookup"><span data-stu-id="ade36-123">The following sample uses threads and `lock`.</span></span> <span data-ttu-id="ade36-124">Tant que l’instruction `lock` est présente, le bloc d’instructions est une section critique et `balance` ne devient jamais un nombre négatif :</span><span class="sxs-lookup"><span data-stu-id="ade36-124">As long as the `lock` statement is present, the statement block is a critical section and `balance` will never become a negative number:</span></span>

[!code-csharp[csrefKeywordsFixedLock#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#6)]

## <a name="c-language-specification"></a><span data-ttu-id="ade36-125">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ade36-125">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="ade36-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ade36-126">See also</span></span>

- <xref:System.Reflection.MethodImplAttributes>
- <xref:System.Threading.Mutex>
- <xref:System.Threading.Monitor>
- [<span data-ttu-id="ade36-127">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ade36-127">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="ade36-128">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ade36-128">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="ade36-129">Thread</span><span class="sxs-lookup"><span data-stu-id="ade36-129">Threading</span></span>](../../programming-guide/concepts/threading/index.md)
- [<span data-ttu-id="ade36-130">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="ade36-130">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="ade36-131">Mots clés d’instructions</span><span class="sxs-lookup"><span data-stu-id="ade36-131">Statement Keywords</span></span>](statement-keywords.md)
- [<span data-ttu-id="ade36-132">Opérations verrouillées</span><span class="sxs-lookup"><span data-stu-id="ade36-132">Interlocked Operations</span></span>](../../../standard/threading/interlocked-operations.md)
- [<span data-ttu-id="ade36-133">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="ade36-133">AutoResetEvent</span></span>](../../../standard/threading/autoresetevent.md)
- [<span data-ttu-id="ade36-134">Synchronisation des threads</span><span class="sxs-lookup"><span data-stu-id="ade36-134">Thread Synchronization</span></span>](../../programming-guide/concepts/threading/thread-synchronization.md)