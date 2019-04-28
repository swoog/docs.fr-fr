---
title: Itérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Iterator
helpviewer_keywords:
- Iterator keyword [Visual Basic]
ms.assetid: 69cb0b04-ac87-49d0-bcfe-810c0d60daff
ms.openlocfilehash: 499949d1f4c20e1f465355bd076ba39f1496779b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61920716"
---
# <a name="iterator-visual-basic"></a><span data-ttu-id="33990-102">Itérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="33990-102">Iterator (Visual Basic)</span></span>
<span data-ttu-id="33990-103">Spécifie qu’une fonction ou `Get` accesseur est un itérateur.</span><span class="sxs-lookup"><span data-stu-id="33990-103">Specifies that a function or `Get` accessor is an iterator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="33990-104">Notes</span><span class="sxs-lookup"><span data-stu-id="33990-104">Remarks</span></span>  
 <span data-ttu-id="33990-105">Un *itérateur* effectue une itération personnalisée sur une collection.</span><span class="sxs-lookup"><span data-stu-id="33990-105">An *iterator* performs a custom iteration over a collection.</span></span> <span data-ttu-id="33990-106">Un itérateur utilise le [Yield](../../../visual-basic/language-reference/statements/yield-statement.md) instruction pour retourner chaque élément dans la collection un à la fois.</span><span class="sxs-lookup"><span data-stu-id="33990-106">An iterator uses the [Yield](../../../visual-basic/language-reference/statements/yield-statement.md) statement to return each element in the collection one at a time.</span></span> <span data-ttu-id="33990-107">Quand un `Yield` instruction est atteinte, l’emplacement actuel dans le code est conservé.</span><span class="sxs-lookup"><span data-stu-id="33990-107">When a `Yield` statement is reached, the current location in code is retained.</span></span> <span data-ttu-id="33990-108">L'exécution redémarrera à partir de cet emplacement la prochaine fois que la fonction d'itérateur sera appelée.</span><span class="sxs-lookup"><span data-stu-id="33990-108">Execution is restarted from that location the next time that the iterator function is called.</span></span>  
  
 <span data-ttu-id="33990-109">Un itérateur peut être implémenté sous la forme d’une fonction ou un `Get` accesseur d’une définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="33990-109">An iterator can be implemented as a function or as a `Get` accessor of a property definition.</span></span> <span data-ttu-id="33990-110">Le `Iterator` modificateur apparaît dans la déclaration de la fonction d’itérateur ou `Get` accesseur.</span><span class="sxs-lookup"><span data-stu-id="33990-110">The `Iterator` modifier appears in the declaration of the iterator function or `Get` accessor.</span></span>  
  
 <span data-ttu-id="33990-111">Vous appelez un itérateur depuis le code client en utilisant un [For Each... L’instruction suivante](../../../visual-basic/language-reference/statements/for-each-next-statement.md).</span><span class="sxs-lookup"><span data-stu-id="33990-111">You call an iterator from client code by using a [For Each...Next Statement](../../../visual-basic/language-reference/statements/for-each-next-statement.md).</span></span>  
  
 <span data-ttu-id="33990-112">Le type de retour d’une fonction d’itérateur ou `Get` accesseur peut être <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator>, ou <xref:System.Collections.Generic.IEnumerator%601>.</span><span class="sxs-lookup"><span data-stu-id="33990-112">The return type of an iterator function or `Get` accessor can be <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator>, or <xref:System.Collections.Generic.IEnumerator%601>.</span></span>  
  
 <span data-ttu-id="33990-113">Un itérateur ne peut avoir aucun `ByRef` paramètres.</span><span class="sxs-lookup"><span data-stu-id="33990-113">An iterator cannot have any `ByRef` parameters.</span></span>  
  
 <span data-ttu-id="33990-114">Un itérateur ne peut pas être présent dans un événement, un constructeur d’instance, un constructeur statique ou un destructeur statique.</span><span class="sxs-lookup"><span data-stu-id="33990-114">An iterator cannot occur in an event, instance constructor, static constructor, or static destructor.</span></span>  
  
 <span data-ttu-id="33990-115">Un itérateur peut être une fonction anonyme.</span><span class="sxs-lookup"><span data-stu-id="33990-115">An iterator can be an anonymous function.</span></span> <span data-ttu-id="33990-116">Pour plus d'informations, consultez [Itérateurs](../../programming-guide/concepts/iterators.md).</span><span class="sxs-lookup"><span data-stu-id="33990-116">For more information, see [Iterators](../../programming-guide/concepts/iterators.md).</span></span>  
  
## <a name="usage"></a><span data-ttu-id="33990-117">Utilisation</span><span class="sxs-lookup"><span data-stu-id="33990-117">Usage</span></span>  
 <span data-ttu-id="33990-118">Le modificateur `Iterator` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="33990-118">The `Iterator` modifier can be used in these contexts:</span></span>  
  
- [<span data-ttu-id="33990-119">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="33990-119">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
- [<span data-ttu-id="33990-120">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="33990-120">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="example"></a><span data-ttu-id="33990-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="33990-121">Example</span></span>  
 <span data-ttu-id="33990-122">L’exemple suivant montre une fonction d’itérateur.</span><span class="sxs-lookup"><span data-stu-id="33990-122">The following example demonstrates an iterator function.</span></span> <span data-ttu-id="33990-123">La fonction d’itérateur a un `Yield` instruction qui se trouve dans un [pour... Suivant](../../../visual-basic/language-reference/statements/for-next-statement.md) boucle.</span><span class="sxs-lookup"><span data-stu-id="33990-123">The iterator function has a `Yield` statement that is inside a [For…Next](../../../visual-basic/language-reference/statements/for-next-statement.md) loop.</span></span> <span data-ttu-id="33990-124">Chaque itération de la [pour chaque](../../../visual-basic/language-reference/statements/for-each-next-statement.md) corps d’instruction dans `Main` crée un appel à la `Power` fonction d’itérateur.</span><span class="sxs-lookup"><span data-stu-id="33990-124">Each iteration of the [For Each](../../../visual-basic/language-reference/statements/for-each-next-statement.md) statement body in `Main` creates a call to the `Power` iterator function.</span></span> <span data-ttu-id="33990-125">Chaque appel à la fonction d'itérateur continue vers l'exécution suivante de l'instruction `Yield`, qui se produit pendant l'itération suivante de la boucle `For…Next`.</span><span class="sxs-lookup"><span data-stu-id="33990-125">Each call to the iterator function proceeds to the next execution of the `Yield` statement, which occurs during the next iteration of the `For…Next` loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#98](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class2.vb#98)]  
  
## <a name="example"></a><span data-ttu-id="33990-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="33990-126">Example</span></span>  
 <span data-ttu-id="33990-127">L'exemple suivant illustre un accesseur `Get` qui est un itérateur.</span><span class="sxs-lookup"><span data-stu-id="33990-127">The following example demonstrates a `Get` accessor that is an iterator.</span></span> <span data-ttu-id="33990-128">Le `Iterator` modificateur est dans la déclaration de propriété.</span><span class="sxs-lookup"><span data-stu-id="33990-128">The `Iterator` modifier is in the property declaration.</span></span>  
  
 [!code-vb[VbVbalrStatements#99](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class2.vb#99)]  
  
 <span data-ttu-id="33990-129">Pour obtenir des exemples supplémentaires, consultez [itérateurs](../../programming-guide/concepts/iterators.md).</span><span class="sxs-lookup"><span data-stu-id="33990-129">For additional examples, see [Iterators](../../programming-guide/concepts/iterators.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33990-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33990-130">See also</span></span>

- <xref:System.Runtime.CompilerServices.IteratorStateMachineAttribute>
- [<span data-ttu-id="33990-131">Itérateurs</span><span class="sxs-lookup"><span data-stu-id="33990-131">Iterators</span></span>](../../programming-guide/concepts/iterators.md)
- [<span data-ttu-id="33990-132">Yield (instruction)</span><span class="sxs-lookup"><span data-stu-id="33990-132">Yield Statement</span></span>](../../../visual-basic/language-reference/statements/yield-statement.md)
