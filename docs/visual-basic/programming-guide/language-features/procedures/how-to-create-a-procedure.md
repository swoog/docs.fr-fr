---
title: 'Procédure : Créer une procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- Visual Basic code, reusing
- procedure declarations
- procedures [Visual Basic], about procedures
ms.assetid: 4f779247-0b50-47e8-9e5c-ab5cf39ac0d2
ms.openlocfilehash: 56099d334a03e85b816cf48983cbbead0784ef5b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61665804"
---
# <a name="how-to-create-a-procedure-visual-basic"></a><span data-ttu-id="c4c62-102">Procédure : Créer une procédure (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c4c62-102">How to: Create a Procedure (Visual Basic)</span></span>
<span data-ttu-id="c4c62-103">Vous insérez une procédure entre une instruction de déclaration initiale (`Sub` ou `Function`) et une instruction de déclaration de fin (`End Sub` ou `End Function`).</span><span class="sxs-lookup"><span data-stu-id="c4c62-103">You enclose a procedure between a starting declaration statement (`Sub` or `Function`) and an ending declaration statement (`End Sub` or `End Function`).</span></span> <span data-ttu-id="c4c62-104">Code de tous les la procédure se trouve entre ces instructions.</span><span class="sxs-lookup"><span data-stu-id="c4c62-104">All the procedure's code lies between these statements.</span></span>  
  
 <span data-ttu-id="c4c62-105">Une procédure ne peut pas contenir une autre procédure, ses instructions de début et de fin doit donc être en dehors de toute autre procédure.</span><span class="sxs-lookup"><span data-stu-id="c4c62-105">A procedure cannot contain another procedure, so its starting and ending statements must be outside any other procedure.</span></span>  
  
 <span data-ttu-id="c4c62-106">Si vous avez le code qui effectue la même tâche dans des endroits différents, vous pouvez écrire la tâche une fois qu’une procédure et puis l’appeler à partir de différents endroits dans votre code.</span><span class="sxs-lookup"><span data-stu-id="c4c62-106">If you have code that performs the same task in different places, you can write the task once as a procedure and then call it from different places in your code.</span></span>  
  
### <a name="to-create-a-procedure-that-does-not-return-a-value"></a><span data-ttu-id="c4c62-107">Pour créer une procédure qui ne retourne pas de valeur</span><span class="sxs-lookup"><span data-stu-id="c4c62-107">To create a procedure that does not return a value</span></span>  
  
1. <span data-ttu-id="c4c62-108">En dehors de toute autre procédure, utilisez un `Sub` instruction, suivie d’un `End Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="c4c62-108">Outside any other procedure, use a `Sub` statement, followed by an `End Sub` statement.</span></span>  
  
2. <span data-ttu-id="c4c62-109">Dans le `Sub` instruction, suivez le `Sub` mot clé avec le nom de la procédure, puis la liste de paramètres entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="c4c62-109">In the `Sub` statement, follow the `Sub` keyword with the name of the procedure, then the parameter list in parentheses.</span></span>  
  
3. <span data-ttu-id="c4c62-110">Placez les instructions de procédure code entre la `Sub` et `End Sub` instructions.</span><span class="sxs-lookup"><span data-stu-id="c4c62-110">Place the procedure's code statements between the `Sub` and `End Sub` statements.</span></span>  
  
### <a name="to-create-a-procedure-that-returns-a-value"></a><span data-ttu-id="c4c62-111">Pour créer une procédure qui retourne une valeur</span><span class="sxs-lookup"><span data-stu-id="c4c62-111">To create a procedure that returns a value</span></span>  
  
1. <span data-ttu-id="c4c62-112">En dehors de toute autre procédure, utilisez un `Function` instruction, suivie d’un `End Function` instruction.</span><span class="sxs-lookup"><span data-stu-id="c4c62-112">Outside any other procedure, use a `Function` statement, followed by an `End Function` statement.</span></span>  
  
2. <span data-ttu-id="c4c62-113">Dans le `Function` instruction, suivez le `Function` mot clé avec le nom de la procédure, puis la liste de paramètres entre parenthèses, puis un `As` clause qui spécifie le type de données de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c4c62-113">In the `Function` statement, follow the `Function` keyword with the name of the procedure, then the parameter list in parentheses, and then an `As` clause specifying the data type of the return value.</span></span>  
  
3. <span data-ttu-id="c4c62-114">Placez les instructions de procédure code entre la `Function` et `End Function` instructions.</span><span class="sxs-lookup"><span data-stu-id="c4c62-114">Place the procedure's code statements between the `Function` and `End Function` statements.</span></span>  
  
4. <span data-ttu-id="c4c62-115">Utilisez un `Return` instruction pour retourner la valeur au code appelant.</span><span class="sxs-lookup"><span data-stu-id="c4c62-115">Use a `Return` statement to return the value to the calling code.</span></span>  
  
### <a name="to-connect-your-new-procedure-with-the-old-repetitive-blocks-of-code"></a><span data-ttu-id="c4c62-116">Pour connecter votre nouvelle procédure avec l’ancien répétitives des blocs de code</span><span class="sxs-lookup"><span data-stu-id="c4c62-116">To connect your new procedure with the old, repetitive blocks of code</span></span>  
  
1. <span data-ttu-id="c4c62-117">Assurez-vous que vous définissez la nouvelle procédure dans un endroit où l’ancien code a accès à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c4c62-117">Make sure you define the new procedure in a place where the old code has access to it.</span></span>  
  
2. <span data-ttu-id="c4c62-118">Dans votre bloc de code ancien, répétitives, remplacez les instructions qui effectuent les tâches répétitives avec une seule instruction qui appelle la `Sub` ou `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="c4c62-118">In your old, repetitive code block, replace the statements that perform the repetitive task with a single statement that calls the `Sub` or `Function` procedure.</span></span>  
  
3. <span data-ttu-id="c4c62-119">Si votre procédure est un `Function` qui retourne une valeur, assurez-vous que votre instruction appelante exécute une action avec la valeur retournée, telle que le stockage dans une variable, dans le cas contraire la valeur sera perdue.</span><span class="sxs-lookup"><span data-stu-id="c4c62-119">If your procedure is a `Function` that returns a value, ensure that your calling statement performs an action with the returned value, such as storing it in a variable, or else the value will be lost.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c4c62-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4c62-120">Example</span></span>  
 <span data-ttu-id="c4c62-121">Ce qui suit `Function` procédure calcule le côté le plus long, ou hypoténuse, d’un triangle rectangle, d’après les valeurs pour les deux côtés.</span><span class="sxs-lookup"><span data-stu-id="c4c62-121">The following `Function` procedure calculates the longest side, or hypotenuse, of a right triangle, given the values for the other two sides.</span></span>  
  
 [!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="c4c62-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4c62-122">See also</span></span>

- [<span data-ttu-id="c4c62-123">Procédures</span><span class="sxs-lookup"><span data-stu-id="c4c62-123">Procedures</span></span>](./index.md)
- [<span data-ttu-id="c4c62-124">Procédures Sub</span><span class="sxs-lookup"><span data-stu-id="c4c62-124">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="c4c62-125">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="c4c62-125">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="c4c62-126">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="c4c62-126">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="c4c62-127">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="c4c62-127">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="c4c62-128">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="c4c62-128">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="c4c62-129">Procédures récursives</span><span class="sxs-lookup"><span data-stu-id="c4c62-129">Recursive Procedures</span></span>](./recursive-procedures.md)
- [<span data-ttu-id="c4c62-130">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="c4c62-130">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="c4c62-131">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="c4c62-131">Objects and Classes</span></span>](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="c4c62-132">Programmation orientée objet (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c4c62-132">Object-Oriented Programming (Visual Basic)</span></span>](../../concepts/object-oriented-programming.md)
