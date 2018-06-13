---
title: SyncLock, instruction
ms.date: 07/20/2015
f1_keywords:
- vb.SyncLock
- SyncLock
helpviewer_keywords:
- threading [Visual Basic], locks
- SyncLock statement [Visual Basic]
- locks, threads
ms.assetid: 14501703-298f-4d43-b139-c4b6366af176
ms.openlocfilehash: cf2aad9ec2ba67200d175fbcddfcb49afeac6efc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604976"
---
# <a name="synclock-statement"></a><span data-ttu-id="5c253-102">SyncLock, instruction</span><span class="sxs-lookup"><span data-stu-id="5c253-102">SyncLock Statement</span></span>
<span data-ttu-id="5c253-103">Acquiert un verrou exclusif pour un bloc d’instructions avant d’exécuter le bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-103">Acquires an exclusive lock for a statement block before executing the block.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c253-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c253-104">Syntax</span></span>  
  
```  
SyncLock lockobject  
    [ block ]  
End SyncLock  
```  
  
## <a name="parts"></a><span data-ttu-id="5c253-105">Composants</span><span class="sxs-lookup"><span data-stu-id="5c253-105">Parts</span></span>  
 `lockobject`  
 <span data-ttu-id="5c253-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5c253-106">Required.</span></span> <span data-ttu-id="5c253-107">Expression qui correspond à une référence d’objet.</span><span class="sxs-lookup"><span data-stu-id="5c253-107">Expression that evaluates to an object reference.</span></span>  
  
 `block`  
 <span data-ttu-id="5c253-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="5c253-108">Optional.</span></span> <span data-ttu-id="5c253-109">Bloc d’instructions à exécuter lorsque le verrou est acquis.</span><span class="sxs-lookup"><span data-stu-id="5c253-109">Block of statements that are to execute when the lock is acquired.</span></span>  
  
 `End SyncLock`  
 <span data-ttu-id="5c253-110">Met fin à une `SyncLock` bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-110">Terminates a `SyncLock` block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5c253-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5c253-111">Remarks</span></span>  
 <span data-ttu-id="5c253-112">La `SyncLock` instruction permet de s’assurer que plusieurs threads n’exécutent pas le bloc d’instructions en même temps.</span><span class="sxs-lookup"><span data-stu-id="5c253-112">The `SyncLock` statement ensures that multiple threads do not execute the statement block at the same time.</span></span> <span data-ttu-id="5c253-113">`SyncLock` empêche chaque thread d’entrer dans le bloc jusqu'à ce qu’aucun autre thread ne l’exécute.</span><span class="sxs-lookup"><span data-stu-id="5c253-113">`SyncLock` prevents each thread from entering the block until no other thread is executing it.</span></span>  
  
 <span data-ttu-id="5c253-114">L’utilisation la plus courante de `SyncLock` consiste à protéger les données à partir de la mise à jour par plusieurs threads simultanément.</span><span class="sxs-lookup"><span data-stu-id="5c253-114">The most common use of `SyncLock` is to protect data from being updated by more than one thread simultaneously.</span></span> <span data-ttu-id="5c253-115">Si les instructions qui manipulent les données doivent être exécutées sans interruption, placez-les à l’intérieur d’un `SyncLock` bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-115">If the statements that manipulate the data must go to completion without interruption, put them inside a `SyncLock` block.</span></span>  
  
 <span data-ttu-id="5c253-116">Un bloc d’instruction protégé par un verrou exclusif est parfois appelé un *section critique*.</span><span class="sxs-lookup"><span data-stu-id="5c253-116">A statement block protected by an exclusive lock is sometimes called a *critical section*.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="5c253-117">Règles</span><span class="sxs-lookup"><span data-stu-id="5c253-117">Rules</span></span>  
  
-   <span data-ttu-id="5c253-118">Création de branche.</span><span class="sxs-lookup"><span data-stu-id="5c253-118">Branching.</span></span> <span data-ttu-id="5c253-119">Vous ne pouvez pas créer de branche dans un `SyncLock` blocage à partir de l’extérieur du bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-119">You cannot branch into a `SyncLock` block from outside the block.</span></span>  
  
-   <span data-ttu-id="5c253-120">Valeur de l’objet verrou.</span><span class="sxs-lookup"><span data-stu-id="5c253-120">Lock Object Value.</span></span> <span data-ttu-id="5c253-121">La valeur de `lockobject` ne peut pas être `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="5c253-121">The value of `lockobject` cannot be `Nothing`.</span></span> <span data-ttu-id="5c253-122">Vous devez créer l’objet lock avant de l’utiliser dans un `SyncLock` instruction.</span><span class="sxs-lookup"><span data-stu-id="5c253-122">You must create the lock object before you use it in a `SyncLock` statement.</span></span>  
  
     <span data-ttu-id="5c253-123">Vous ne pouvez pas modifier la valeur de `lockobject` lors de l’exécution une `SyncLock` bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-123">You cannot change the value of `lockobject` while executing a `SyncLock` block.</span></span> <span data-ttu-id="5c253-124">Le mécanisme exige que l’objet verrou reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="5c253-124">The mechanism requires that the lock object remain unchanged.</span></span>  
  
-   <span data-ttu-id="5c253-125">Vous ne pouvez pas utiliser le [Await](../../../visual-basic/language-reference/operators/await-operator.md) opérateur dans un `SyncLock` bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-125">You can't use the [Await](../../../visual-basic/language-reference/operators/await-operator.md) operator in a `SyncLock` block.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="5c253-126">Comportement</span><span class="sxs-lookup"><span data-stu-id="5c253-126">Behavior</span></span>  
  
-   <span data-ttu-id="5c253-127">Mécanisme.</span><span class="sxs-lookup"><span data-stu-id="5c253-127">Mechanism.</span></span> <span data-ttu-id="5c253-128">Lorsqu’un thread atteint le `SyncLock` instruction, il évalue les `lockobject` expression et suspend l’exécution jusqu'à ce qu’il acquiert un verrou exclusif sur l’objet retourné par l’expression.</span><span class="sxs-lookup"><span data-stu-id="5c253-128">When a thread reaches the `SyncLock` statement, it evaluates the `lockobject` expression and suspends execution until it acquires an exclusive lock on the object returned by the expression.</span></span> <span data-ttu-id="5c253-129">Lorsqu’un autre thread atteint le `SyncLock` instruction, il n’acquiert pas de verrou jusqu'à ce que le premier thread exécute la `End SyncLock` instruction.</span><span class="sxs-lookup"><span data-stu-id="5c253-129">When another thread reaches the `SyncLock` statement, it does not acquire a lock until the first thread executes the `End SyncLock` statement.</span></span>  
  
-   <span data-ttu-id="5c253-130">Les données protégées.</span><span class="sxs-lookup"><span data-stu-id="5c253-130">Protected Data.</span></span> <span data-ttu-id="5c253-131">Si `lockobject` est un `Shared` variable, le verrou exclusif empêche un thread dans n’importe quelle instance de la classe à partir de l’exécution de la `SyncLock` bloquer un autre thread est exécutée.</span><span class="sxs-lookup"><span data-stu-id="5c253-131">If `lockobject` is a `Shared` variable, the exclusive lock prevents a thread in any instance of the class from executing the `SyncLock` block while any other thread is executing it.</span></span> <span data-ttu-id="5c253-132">Cela protège les données qui sont partagées entre toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="5c253-132">This protects data that is shared among all the instances.</span></span>  
  
     <span data-ttu-id="5c253-133">Si `lockobject` est une variable d’instance (non `Shared`), le verrou empêche un thread en cours d’exécution dans l’instance actuelle à partir de l’exécution de la `SyncLock` bloc en même temps qu’un autre thread dans la même instance.</span><span class="sxs-lookup"><span data-stu-id="5c253-133">If `lockobject` is an instance variable (not `Shared`), the lock prevents a thread running in the current instance from executing the `SyncLock` block at the same time as another thread in the same instance.</span></span> <span data-ttu-id="5c253-134">Cela protège les données gérées par l’instance.</span><span class="sxs-lookup"><span data-stu-id="5c253-134">This protects data maintained by the individual instance.</span></span>  
  
-   <span data-ttu-id="5c253-135">Acquisition et la mise en production.</span><span class="sxs-lookup"><span data-stu-id="5c253-135">Acquisition and Release.</span></span> <span data-ttu-id="5c253-136">A `SyncLock` bloc se comporte comme un `Try...Finally` dans laquelle le `Try` bloc acquiert un verrou exclusif sur `lockobject` et `Finally` bloc le libère.</span><span class="sxs-lookup"><span data-stu-id="5c253-136">A `SyncLock` block behaves like a `Try...Finally` construction in which the `Try` block acquires an exclusive lock on `lockobject` and the `Finally` block releases it.</span></span> <span data-ttu-id="5c253-137">Pour cette raison, le `SyncLock` bloc garantit la libération du verrou, quel que soit la manière dont vous quittez le bloc.</span><span class="sxs-lookup"><span data-stu-id="5c253-137">Because of this, the `SyncLock` block guarantees release of the lock, no matter how you exit the block.</span></span> <span data-ttu-id="5c253-138">Cela est vrai même en cas d’une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="5c253-138">This is true even in the case of an unhandled exception.</span></span>  
  
-   <span data-ttu-id="5c253-139">Appels du Framework.</span><span class="sxs-lookup"><span data-stu-id="5c253-139">Framework Calls.</span></span> <span data-ttu-id="5c253-140">Le `SyncLock` bloc acquiert et libère le verrou exclusif en appelant le `Enter` et `Exit` méthodes de la `Monitor` classe dans le <xref:System.Threading> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="5c253-140">The `SyncLock` block acquires and releases the exclusive lock by calling the `Enter` and `Exit` methods of the `Monitor` class in the <xref:System.Threading> namespace.</span></span>  
  
## <a name="programming-practices"></a><span data-ttu-id="5c253-141">Méthodes de programmation</span><span class="sxs-lookup"><span data-stu-id="5c253-141">Programming Practices</span></span>  
 <span data-ttu-id="5c253-142">Le `lockobject` expression doit toujours correspondre à un objet qui appartienne exclusivement à votre classe.</span><span class="sxs-lookup"><span data-stu-id="5c253-142">The `lockobject` expression should always evaluate to an object that belongs exclusively to your class.</span></span> <span data-ttu-id="5c253-143">Vous devez déclarer un `Private` variable objet pour protéger les données appartenant à l’instance actuelle, ou un `Private Shared` variable objet pour protéger les données communes à toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="5c253-143">You should declare a `Private` object variable to protect data belonging to the current instance, or a `Private Shared` object variable to protect data common to all instances.</span></span>  
  
 <span data-ttu-id="5c253-144">Vous ne devez pas utiliser le `Me` données mot clé pour fournir un verrou d’objet pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="5c253-144">You should not use the `Me` keyword to provide a lock object for instance data.</span></span> <span data-ttu-id="5c253-145">Si le code externe à votre classe possède une référence à une instance de votre classe, il peut utiliser cette référence comme un objet lock pour un `SyncLock` bloc complètement différent du vôtre, protégeant des données différentes.</span><span class="sxs-lookup"><span data-stu-id="5c253-145">If code external to your class has a reference to an instance of your class, it could use that reference as a lock object for a `SyncLock` block completely different from yours, protecting different data.</span></span> <span data-ttu-id="5c253-146">De cette façon, votre classe et l’autre classe peuvent bloquer mutuellement à partir de l’exécution de leur relation `SyncLock` blocs.</span><span class="sxs-lookup"><span data-stu-id="5c253-146">In this way, your class and the other class could block each other from executing their unrelated `SyncLock` blocks.</span></span> <span data-ttu-id="5c253-147">Le verrouillage de la même façon sur une chaîne peut être problématique, car tout autre code dans le processus à l’aide de la même chaîne partagera le même verrou.</span><span class="sxs-lookup"><span data-stu-id="5c253-147">Similarly locking on a string can be problematic since any other code in the process using the same string will share the same lock.</span></span>  
  
 <span data-ttu-id="5c253-148">Vous devez également utiliser pas le `Me.GetType` méthode pour fournir un objet de verrouillage pour les données partagées.</span><span class="sxs-lookup"><span data-stu-id="5c253-148">You should also not use the `Me.GetType` method to provide a lock object for shared data.</span></span> <span data-ttu-id="5c253-149">C’est parce que `GetType` retourne toujours le même `Type` objet pour un nom de classe donné.</span><span class="sxs-lookup"><span data-stu-id="5c253-149">This is because `GetType` always returns the same `Type` object for a given class name.</span></span> <span data-ttu-id="5c253-150">Le code externe peut appeler `GetType` sur votre classe et obtenir le même objet lock que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="5c253-150">External code could call `GetType` on your class and obtain the same lock object you are using.</span></span> <span data-ttu-id="5c253-151">Cela entraînerait le blocage de l’autre de deux classes leurs `SyncLock` blocs.</span><span class="sxs-lookup"><span data-stu-id="5c253-151">This would result in the two classes blocking each other from their `SyncLock` blocks.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="5c253-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="5c253-152">Examples</span></span>  
  
### <a name="description"></a><span data-ttu-id="5c253-153">Description</span><span class="sxs-lookup"><span data-stu-id="5c253-153">Description</span></span>  
 <span data-ttu-id="5c253-154">L’exemple suivant montre une classe qui gère une liste simple de messages.</span><span class="sxs-lookup"><span data-stu-id="5c253-154">The following example shows a class that maintains a simple list of messages.</span></span> <span data-ttu-id="5c253-155">Il stocke les messages dans un tableau et le dernier élément utilisé de ce tableau dans une variable.</span><span class="sxs-lookup"><span data-stu-id="5c253-155">It holds the messages in an array and the last used element of that array in a variable.</span></span> <span data-ttu-id="5c253-156">Le `addAnotherMessage` procédure incrémente le dernier élément et stocke le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="5c253-156">The `addAnotherMessage` procedure increments the last element and stores the new message.</span></span> <span data-ttu-id="5c253-157">Ces deux opérations sont protégées par le `SyncLock` et `End SyncLock` instructions, car une fois que le dernier élément a été incrémenté, le nouveau message doit être stocké avant que n’importe quel autre thread puisse incrémenter le dernier élément à nouveau.</span><span class="sxs-lookup"><span data-stu-id="5c253-157">Those two operations are protected by the `SyncLock` and `End SyncLock` statements, because once the last element has been incremented, the new message must be stored before any other thread can increment the last element again.</span></span>  
  
 <span data-ttu-id="5c253-158">Si le `simpleMessageList` classe partagée d’une liste de messages entre toutes ses instances, les variables `messagesList` et `messagesLast` sont déclarées comme `Shared`.</span><span class="sxs-lookup"><span data-stu-id="5c253-158">If the `simpleMessageList` class shared one list of messages among all its instances, the variables `messagesList` and `messagesLast` would be declared as `Shared`.</span></span> <span data-ttu-id="5c253-159">Dans ce cas, la variable `messagesLock` doit également être `Shared`, afin qu’il y ait un objet lock seul utilisé par chaque instance.</span><span class="sxs-lookup"><span data-stu-id="5c253-159">In this case, the variable `messagesLock` should also be `Shared`, so that there would be a single lock object used by every instance.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5c253-160">Code</span><span class="sxs-lookup"><span data-stu-id="5c253-160">Code</span></span>  
 [!code-vb[VbVbalrThreading#1](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/synclock-statement_1.vb)]  
  
### <a name="description"></a><span data-ttu-id="5c253-161">Description</span><span class="sxs-lookup"><span data-stu-id="5c253-161">Description</span></span>  
 <span data-ttu-id="5c253-162">L’exemple suivant utilise des threads et `SyncLock`.</span><span class="sxs-lookup"><span data-stu-id="5c253-162">The following example uses threads and `SyncLock`.</span></span> <span data-ttu-id="5c253-163">Tant que le `SyncLock` instruction est présente, le bloc d’instructions est une section critique et `balance` ne devient jamais un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="5c253-163">As long as the `SyncLock` statement is present, the statement block is a critical section and `balance` never becomes a negative number.</span></span> <span data-ttu-id="5c253-164">Vous pouvez placer en commentaire la `SyncLock` et `End SyncLock` instructions pour voir l’effet de la mise la `SyncLock` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="5c253-164">You can comment out the `SyncLock` and `End SyncLock` statements to see the effect of leaving out the `SyncLock` keyword.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5c253-165">Code</span><span class="sxs-lookup"><span data-stu-id="5c253-165">Code</span></span>  
 [!code-vb[VbVbalrThreading#21](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/synclock-statement_2.vb)]  
  
### <a name="comments"></a><span data-ttu-id="5c253-166">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5c253-166">Comments</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c253-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c253-167">See Also</span></span>  
 <xref:System.Threading>  
 <xref:System.Threading.Monitor>  
 [<span data-ttu-id="5c253-168">Synchronisation des threads</span><span class="sxs-lookup"><span data-stu-id="5c253-168">Thread Synchronization</span></span>](../../programming-guide/concepts/threading/thread-synchronization.md)  
 [<span data-ttu-id="5c253-169">Thread</span><span class="sxs-lookup"><span data-stu-id="5c253-169">Threading</span></span>](../../programming-guide/concepts/threading/index.md)
