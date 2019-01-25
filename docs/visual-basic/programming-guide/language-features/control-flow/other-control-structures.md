---
title: Autres structures de contrôle (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- statements [Visual Basic], control flow
- control structures [Visual Basic]
ms.assetid: 24b811f7-98ba-40ec-8dd3-4d528cfa4574
ms.openlocfilehash: a383d0c95de5286cce722c05bd8888d5acffb173
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589998"
---
# <a name="other-control-structures-visual-basic"></a><span data-ttu-id="c1c8d-102">Autres structures de contrôle (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c1c8d-102">Other Control Structures (Visual Basic)</span></span>
<span data-ttu-id="c1c8d-103">Visual Basic fournit des structures de contrôle qui vous aident à supprimer une ressource ou réduisent le nombre de fois où que vous devez répéter une référence d’objet.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-103">Visual Basic provides control structures that help you dispose of a resource or reduce the number of times you have to repeat an object reference.</span></span>  
  
## <a name="usingend-using-construction"></a><span data-ttu-id="c1c8d-104">À l’aide de... À l’aide de la Construction de fin</span><span class="sxs-lookup"><span data-stu-id="c1c8d-104">Using...End Using Construction</span></span>  
 <span data-ttu-id="c1c8d-105">Le `Using...End Using` construction établit un bloc d’instruction dans lequel vous utilisez une ressource telle qu’une connexion SQL.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-105">The `Using...End Using` construction establishes a statement block within which you make use of a resource such as a SQL connection.</span></span> <span data-ttu-id="c1c8d-106">Vous pouvez éventuellement acquérir la ressource avec le `Using` instruction.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-106">You can optionally acquire the resource with the `Using` statement.</span></span> <span data-ttu-id="c1c8d-107">Lorsque vous quittez le `Using` bloc, Visual Basic supprime automatiquement la ressource afin qu’il soit disponible pour tout autre code à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-107">When you exit the `Using` block, Visual Basic automatically disposes of the resource so that it is available for other code to use.</span></span> <span data-ttu-id="c1c8d-108">La ressource doit être locale et supprimable.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-108">The resource must be local and disposable.</span></span> <span data-ttu-id="c1c8d-109">Pour plus d’informations, consultez [using, instruction](../../../../visual-basic/language-reference/statements/using-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c1c8d-109">For more information, see [Using Statement](../../../../visual-basic/language-reference/statements/using-statement.md).</span></span>  
  
## <a name="withend-with-construction"></a><span data-ttu-id="c1c8d-110">Avec... Se terminer par Construction</span><span class="sxs-lookup"><span data-stu-id="c1c8d-110">With...End With Construction</span></span>  
 <span data-ttu-id="c1c8d-111">Le `With...End With` vous permet de spécifier une référence d’objet une seule fois, puis exécutez une série d’instructions qui accèdent à ses membres.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-111">The `With...End With` construction lets you specify an object reference once and then run a series of statements that access its members.</span></span> <span data-ttu-id="c1c8d-112">Cela peut simplifier votre code et améliorer les performances, car Visual Basic n’est pas obligé de rétablir la référence pour chaque instruction qui y accède.</span><span class="sxs-lookup"><span data-stu-id="c1c8d-112">This can simplify your code and improve performance because Visual Basic does not have to re-establish the reference for each statement that accesses it.</span></span> <span data-ttu-id="c1c8d-113">Pour plus d’informations, consultez [avec... End With, instruction](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c1c8d-113">For more information, see [With...End With Statement](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1c8d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1c8d-114">See also</span></span>
- [<span data-ttu-id="c1c8d-115">Flux de contrôle</span><span class="sxs-lookup"><span data-stu-id="c1c8d-115">Control Flow</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)
- [<span data-ttu-id="c1c8d-116">Structures de décision</span><span class="sxs-lookup"><span data-stu-id="c1c8d-116">Decision Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [<span data-ttu-id="c1c8d-117">Structures de boucle</span><span class="sxs-lookup"><span data-stu-id="c1c8d-117">Loop Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [<span data-ttu-id="c1c8d-118">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="c1c8d-118">Nested Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="c1c8d-119">Using (instruction)</span><span class="sxs-lookup"><span data-stu-id="c1c8d-119">Using Statement</span></span>](../../../../visual-basic/language-reference/statements/using-statement.md)
- [<span data-ttu-id="c1c8d-120">With...End With (instruction)</span><span class="sxs-lookup"><span data-stu-id="c1c8d-120">With...End With Statement</span></span>](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
