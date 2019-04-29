---
title: Procédures récursives (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], that call themselves
- procedures [Visual Basic], recursive
- procedures [Visual Basic], calling
- recursive procedures
- functions [Visual Basic], calling recursively
- recursion
ms.assetid: ba1d3962-b4c3-48d3-875e-96fdb4198327
ms.openlocfilehash: de9a2af9fc3cd78879b6525245727a6f52d51c63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791844"
---
# <a name="recursive-procedures-visual-basic"></a><span data-ttu-id="ef2f0-102">Procédures récursives (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ef2f0-102">Recursive Procedures (Visual Basic)</span></span>
<span data-ttu-id="ef2f0-103">Un *récursive* procédure est une qui s’appelle elle-même.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-103">A *recursive* procedure is one that calls itself.</span></span> <span data-ttu-id="ef2f0-104">En règle générale, cela n’est pas le moyen le plus efficace pour écrire du code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-104">In general, this is not the most effective way to write Visual Basic code.</span></span>  
  
 <span data-ttu-id="ef2f0-105">La procédure suivante utilise la récursivité pour calculer la factorielle de son argument d’origine.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-105">The following procedure uses recursion to calculate the factorial of its original argument.</span></span>  
  
 [!code-vb[VbVbcnProcedures#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#51)]  
  
## <a name="considerations-with-recursive-procedures"></a><span data-ttu-id="ef2f0-106">Considérations sur les procédures récursives</span><span class="sxs-lookup"><span data-stu-id="ef2f0-106">Considerations with Recursive Procedures</span></span>  
 <span data-ttu-id="ef2f0-107">**Conditions de limitation**.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-107">**Limiting Conditions**.</span></span> <span data-ttu-id="ef2f0-108">Vous devez concevoir une procédure récursive à tester pour au moins une condition qui peut s’arrêter la récursivité, et vous devez également gérer le cas où aucune de ces conditions n’est satisfaite au sein d’un nombre raisonnable d’appels récurrents.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-108">You must design a recursive procedure to test for at least one condition that can terminate the recursion, and you must also handle the case where no such condition is satisfied within a reasonable number of recursive calls.</span></span> <span data-ttu-id="ef2f0-109">Au moins une condition qui peut être satisfaite sans erreur, votre procédure s’exécute à un risque élevé de l’exécution dans une boucle infinie.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-109">Without at least one condition that can be met without fail, your procedure runs a high risk of executing in an infinite loop.</span></span>  
  
 <span data-ttu-id="ef2f0-110">**Utilisation de la mémoire**.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-110">**Memory Usage**.</span></span> <span data-ttu-id="ef2f0-111">Votre application dispose d’une quantité limitée d’espace pour les variables locales.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-111">Your application has a limited amount of space for local variables.</span></span> <span data-ttu-id="ef2f0-112">Chaque fois qu’une procédure appelle lui-même, il utilise des davantage d’espace pour les copies supplémentaires de ses variables locales.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-112">Each time a procedure calls itself, it uses more of that space for additional copies of its local variables.</span></span> <span data-ttu-id="ef2f0-113">Si ce processus se poursuit indéfiniment, il finit par provoque un <xref:System.StackOverflowException> erreur.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-113">If this process continues indefinitely, it eventually causes a <xref:System.StackOverflowException> error.</span></span>  
  
 <span data-ttu-id="ef2f0-114">**L’efficacité**.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-114">**Efficiency**.</span></span> <span data-ttu-id="ef2f0-115">Vous pouvez presque toujours remplacer une boucle de récursivité.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-115">You can almost always substitute a loop for recursion.</span></span> <span data-ttu-id="ef2f0-116">Une boucle n’a pas la surcharge de passage des arguments, l’initialisation du stockage supplémentaire et retourner des valeurs.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-116">A loop does not have the overhead of passing arguments, initializing additional storage, and returning values.</span></span> <span data-ttu-id="ef2f0-117">Vos performances peuvent être considérablement améliorée sans appels récurrents.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-117">Your performance can be much better without recursive calls.</span></span>  
  
 <span data-ttu-id="ef2f0-118">**Récurrence mutuelle**.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-118">**Mutual Recursion**.</span></span> <span data-ttu-id="ef2f0-119">Vous pouvez observer des performances très médiocres, ou même une boucle infinie, si deux procédures s’appellent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-119">You might observe very poor performance, or even an infinite loop, if two procedures call each other.</span></span> <span data-ttu-id="ef2f0-120">Ce type de conception présente les mêmes problèmes qu’une procédure récursive simple, mais il peut être difficile à détecter et à déboguer.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-120">Such a design presents the same problems as a single recursive procedure, but can be harder to detect and debug.</span></span>  
  
 <span data-ttu-id="ef2f0-121">**Appel avec parenthèses**.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-121">**Calling with Parentheses**.</span></span> <span data-ttu-id="ef2f0-122">Quand un `Function` procédure appelle de manière récursive, vous devez suivre le nom de la procédure avec des parenthèses, même s’il n’existe aucune liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-122">When a `Function` procedure calls itself recursively, you must follow the procedure name with parentheses, even if there is no argument list.</span></span> <span data-ttu-id="ef2f0-123">Sinon, le nom de fonction est utilisé en tant que représentant la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-123">Otherwise, the function name is taken as representing the return value of the function.</span></span>  
  
 <span data-ttu-id="ef2f0-124">**Test**.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-124">**Testing**.</span></span> <span data-ttu-id="ef2f0-125">Si vous écrivez une procédure récursive, vous devez la tester soigneusement pour vous assurer qu’il répond toujours à certaines conditions de limitation.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-125">If you write a recursive procedure, you should test it very carefully to make sure it always meets some limiting condition.</span></span> <span data-ttu-id="ef2f0-126">Vous devez également vous assurer que vous ne pouvez pas suffisamment de mémoire en raison d’un trop grand nombre d’appels récursifs.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-126">You should also ensure that you cannot run out of memory due to having too many recursive calls.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef2f0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef2f0-127">See also</span></span>

- <xref:System.StackOverflowException>
- [<span data-ttu-id="ef2f0-128">Procédures</span><span class="sxs-lookup"><span data-stu-id="ef2f0-128">Procedures</span></span>](./index.md)
- [<span data-ttu-id="ef2f0-129">Procédures Sub</span><span class="sxs-lookup"><span data-stu-id="ef2f0-129">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="ef2f0-130">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="ef2f0-130">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="ef2f0-131">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="ef2f0-131">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="ef2f0-132">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="ef2f0-132">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="ef2f0-133">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="ef2f0-133">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="ef2f0-134">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="ef2f0-134">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="ef2f0-135">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="ef2f0-135">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)
- [<span data-ttu-id="ef2f0-136">Structures de boucle</span><span class="sxs-lookup"><span data-stu-id="ef2f0-136">Loop Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
