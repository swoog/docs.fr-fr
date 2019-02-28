---
title: New, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.new
- vb.NewConstraint
helpviewer_keywords:
- constraints, Visual Basic generic types
- generics [Visual Basic], constraints
- constraints, New keyword [Visual Basic]
- New constraint
- New keyword [Visual Basic]
ms.assetid: d7d566d7-fe0e-4336-91f7-641a542de4d0
ms.openlocfilehash: dda23ef3ff49bd32474f39f5ae1807e57bdc2a62
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56980462"
---
# <a name="new-operator-visual-basic"></a><span data-ttu-id="05a1c-102">New, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="05a1c-102">New Operator (Visual Basic)</span></span>
<span data-ttu-id="05a1c-103">Introduit un `New` clause pour créer une nouvelle instance de l’objet, spécifie une contrainte de constructeur sur un paramètre de type ou identifie un `Sub` procédure en tant qu’un constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="05a1c-103">Introduces a `New` clause to create a new object instance, specifies a constructor constraint on a type parameter, or identifies a `Sub` procedure as a class constructor.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="05a1c-104">Notes</span><span class="sxs-lookup"><span data-stu-id="05a1c-104">Remarks</span></span>  
 <span data-ttu-id="05a1c-105">Dans une déclaration ou une instruction d’assignation, un `New` clause doit spécifier une classe définie à partir de laquelle l’instance peut être créée.</span><span class="sxs-lookup"><span data-stu-id="05a1c-105">In a declaration or assignment statement, a `New` clause must specify a defined class from which the instance can be created.</span></span> <span data-ttu-id="05a1c-106">Cela signifie que la classe doit exposer un ou plusieurs constructeurs le code appelant peut accéder.</span><span class="sxs-lookup"><span data-stu-id="05a1c-106">This means that the class must expose one or more constructors that the calling code can access.</span></span>  
  
 <span data-ttu-id="05a1c-107">Vous pouvez utiliser un `New` clause dans une instruction de déclaration ou une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="05a1c-107">You can use a `New` clause in a declaration statement or an assignment statement.</span></span> <span data-ttu-id="05a1c-108">Lorsque l’instruction s’exécute, il appelle le constructeur approprié de la classe spécifiée, en passant les arguments que vous avez fourni.</span><span class="sxs-lookup"><span data-stu-id="05a1c-108">When the statement runs, it calls the appropriate constructor of the specified class, passing any arguments you have supplied.</span></span> <span data-ttu-id="05a1c-109">L’exemple suivant illustre cela en créant des instances d’un `Customer` classe qui possède deux constructeurs qui n’accepte aucun paramètre et une fonction qui accepte un paramètre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="05a1c-109">The following example demonstrates this by creating instances of a `Customer` class that has two constructors, one that takes no parameters and one that takes a string parameter.</span></span>  
  
 [!code-vb[VbVbalrKeywords#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class6.vb#11)]  
  
 <span data-ttu-id="05a1c-110">Étant donné que les tableaux sont des classes, `New` peut créer une nouvelle instance de tableau, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="05a1c-110">Since arrays are classes, `New` can create a new array instance, as shown in the following examples.</span></span>  
  
 [!code-vb[VbVbalrKeywords#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class6.vb#12)]  
  
 <span data-ttu-id="05a1c-111">Le common language runtime (CLR) lève une <xref:System.OutOfMemoryException> erreur si la mémoire est insuffisante pour créer la nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="05a1c-111">The common language runtime (CLR) throws an <xref:System.OutOfMemoryException> error if there is insufficient memory to create the new instance.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05a1c-112">Le `New` mot clé est également utilisé dans les listes de paramètres de type pour spécifier que le type fourni doit exposer un constructeur sans paramètre accessible.</span><span class="sxs-lookup"><span data-stu-id="05a1c-112">The `New` keyword is also used in type parameter lists to specify that the supplied type must expose an accessible parameterless constructor.</span></span> <span data-ttu-id="05a1c-113">Pour plus d’informations sur les paramètres de type et contraintes, consultez [liste Type](../../../visual-basic/language-reference/statements/type-list.md).</span><span class="sxs-lookup"><span data-stu-id="05a1c-113">For more information about type parameters and constraints, see [Type List](../../../visual-basic/language-reference/statements/type-list.md).</span></span>  
  
 <span data-ttu-id="05a1c-114">Pour créer une procédure de constructeur pour une classe, définissez le nom d’un `Sub` procédure pour le `New` mot clé.</span><span class="sxs-lookup"><span data-stu-id="05a1c-114">To create a constructor procedure for a class, set the name of a `Sub` procedure to the `New` keyword.</span></span> <span data-ttu-id="05a1c-115">Pour plus d’informations, consultez [durée de vie : Comment les objets sont créés et détruits](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md).</span><span class="sxs-lookup"><span data-stu-id="05a1c-115">For more information, see [Object Lifetime: How Objects Are Created and Destroyed](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md).</span></span>  
  
 <span data-ttu-id="05a1c-116">Le mot clé `New` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="05a1c-116">The `New` keyword can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="05a1c-117">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="05a1c-117">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="05a1c-118">Of</span><span class="sxs-lookup"><span data-stu-id="05a1c-118">Of</span></span>](../../../visual-basic/language-reference/statements/of-clause.md)  
  
 [<span data-ttu-id="05a1c-119">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="05a1c-119">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="05a1c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05a1c-120">See also</span></span>
- <xref:System.OutOfMemoryException>
- [<span data-ttu-id="05a1c-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="05a1c-121">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="05a1c-122">Liste de types</span><span class="sxs-lookup"><span data-stu-id="05a1c-122">Type List</span></span>](../../../visual-basic/language-reference/statements/type-list.md)
- [<span data-ttu-id="05a1c-123">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="05a1c-123">Generic Types in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="05a1c-124">Durée de vie d’objet : Comment les objets sont créés et détruits</span><span class="sxs-lookup"><span data-stu-id="05a1c-124">Object Lifetime: How Objects Are Created and Destroyed</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
