---
title: Implements, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ImplementsClause
helpviewer_keywords:
- interface implementation [Visual Basic], reimplementation
- interface members [Visual Basic], reimplementation
- interface members [Visual Basic], Implements keyword
- interface members
- members [Visual Basic], reimplementation
- interface implementation [Visual Basic], Implements keyword
- interface members [Visual Basic], implementing
- Implements keyword [Visual Basic]
- Implements statement [Visual Basic], about Implements
- members [Visual Basic], implementing
- members [Visual Basic], Implements keyword
- reimplementation
ms.assetid: 5252cdf9-964d-4fc6-af0f-0449b7126b5a
ms.openlocfilehash: 05de1d9f8966c17d84deba34f27819cce4aff3fe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58832617"
---
# <a name="implements-clause-visual-basic"></a><span data-ttu-id="c5772-102">Implements, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c5772-102">Implements Clause (Visual Basic)</span></span>
<span data-ttu-id="c5772-103">Indique qu’un membre de classe ou structure fournit l’implémentation d’un membre défini dans une interface.</span><span class="sxs-lookup"><span data-stu-id="c5772-103">Indicates that a class or structure member is providing the implementation for a member defined in an interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c5772-104">Notes</span><span class="sxs-lookup"><span data-stu-id="c5772-104">Remarks</span></span>  
<span data-ttu-id="c5772-105">Le `Implements` mot clé n’est pas le même que le [Implements, instruction](../../../visual-basic/language-reference/statements/implements-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c5772-105">The `Implements` keyword is not the same as the [Implements Statement](../../../visual-basic/language-reference/statements/implements-statement.md).</span></span> <span data-ttu-id="c5772-106">Vous utilisez le `Implements` instruction pour spécifier qu’une classe ou structure implémente une ou plusieurs interfaces, et ensuite pour chaque membre que vous utilisez le `Implements` mot clé pour spécifier quelle interface et le membre qu’il implémente.</span><span class="sxs-lookup"><span data-stu-id="c5772-106">You use the `Implements` statement to specify that a class or structure implements one or more interfaces, and then for each member you use the `Implements` keyword to specify which interface and which member it implements.</span></span>

<span data-ttu-id="c5772-107">Si une classe ou structure implémente une interface, elle doit inclure le `Implements` instruction immédiatement après le [Class, instruction](../../../visual-basic/language-reference/statements/class-statement.md) ou [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md), et il doit implémenter tous les membres définies par l’interface.</span><span class="sxs-lookup"><span data-stu-id="c5772-107">If a class or structure implements an interface, it must include the `Implements` statement immediately after the [Class Statement](../../../visual-basic/language-reference/statements/class-statement.md) or [Structure Statement](../../../visual-basic/language-reference/statements/structure-statement.md), and it must implement all the members defined by the interface.</span></span>

## <a name="reimplementation"></a><span data-ttu-id="c5772-108">Nouvelle implémentation</span><span class="sxs-lookup"><span data-stu-id="c5772-108">Reimplementation</span></span>  
<span data-ttu-id="c5772-109">Dans une classe dérivée, vous pouvez implémenter de nouveau un membre d’interface que la classe de base a déjà implémenté.</span><span class="sxs-lookup"><span data-stu-id="c5772-109">In a derived class, you can reimplement an interface member that the base class has already implemented.</span></span> <span data-ttu-id="c5772-110">Cela est différent de substituer le membre de classe de base selon les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="c5772-110">This is different from overriding the base class member in the following respects:</span></span>

- <span data-ttu-id="c5772-111">Le membre de classe de base n’a pas besoin être [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md) à être implémentées de nouveau.</span><span class="sxs-lookup"><span data-stu-id="c5772-111">The base class member does not need to be [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md) to be reimplemented.</span></span>
- <span data-ttu-id="c5772-112">Vous pouvez implémenter de nouveau le membre avec un nom différent.</span><span class="sxs-lookup"><span data-stu-id="c5772-112">You can reimplement the member with a different name.</span></span>

<span data-ttu-id="c5772-113">Le `Implements` mot clé peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="c5772-113">The `Implements` keyword can be used in the following contexts:</span></span>
- [<span data-ttu-id="c5772-114">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-114">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="c5772-115">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-115">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="c5772-116">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-116">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="c5772-117">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-117">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="c5772-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5772-118">See also</span></span>

- [<span data-ttu-id="c5772-119">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-119">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="c5772-120">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-120">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)
- [<span data-ttu-id="c5772-121">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-121">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
- [<span data-ttu-id="c5772-122">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5772-122">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
