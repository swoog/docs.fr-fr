---
title: Autres structures de contrôle (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- statements [Visual Basic], control flow
- control structures [Visual Basic]
ms.assetid: 24b811f7-98ba-40ec-8dd3-4d528cfa4574
ms.openlocfilehash: 272ebcf0639b83a51e87de5ebbf93d7e750c03a7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33654107"
---
# <a name="other-control-structures-visual-basic"></a><span data-ttu-id="726fd-102">Autres structures de contrôle (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="726fd-102">Other Control Structures (Visual Basic)</span></span>
<span data-ttu-id="726fd-103">Visual Basic fournit des structures de contrôle qui vous aident à supprimer une ressource ou de réduisent le nombre de fois où que vous devez répéter une référence d’objet.</span><span class="sxs-lookup"><span data-stu-id="726fd-103">Visual Basic provides control structures that help you dispose of a resource or reduce the number of times you have to repeat an object reference.</span></span>  
  
## <a name="usingend-using-construction"></a><span data-ttu-id="726fd-104">À l’aide de... À l’aide de la Construction de fin</span><span class="sxs-lookup"><span data-stu-id="726fd-104">Using...End Using Construction</span></span>  
 <span data-ttu-id="726fd-105">Le `Using...End Using` construction établit un bloc d’instruction dans laquelle vous utilisez une ressource telle qu’une connexion SQL.</span><span class="sxs-lookup"><span data-stu-id="726fd-105">The `Using...End Using` construction establishes a statement block within which you make use of a resource such as a SQL connection.</span></span> <span data-ttu-id="726fd-106">Vous pouvez éventuellement acquérir la ressource avec la `Using` instruction.</span><span class="sxs-lookup"><span data-stu-id="726fd-106">You can optionally acquire the resource with the `Using` statement.</span></span> <span data-ttu-id="726fd-107">Lorsque vous quittez la `Using` bloc, Visual Basic supprime automatiquement la ressource afin qu’il soit disponible pour un autre code à utiliser.</span><span class="sxs-lookup"><span data-stu-id="726fd-107">When you exit the `Using` block, Visual Basic automatically disposes of the resource so that it is available for other code to use.</span></span> <span data-ttu-id="726fd-108">La ressource doit être locale et supprimable.</span><span class="sxs-lookup"><span data-stu-id="726fd-108">The resource must be local and disposable.</span></span> <span data-ttu-id="726fd-109">Pour plus d’informations, consultez [using, instruction](../../../../visual-basic/language-reference/statements/using-statement.md).</span><span class="sxs-lookup"><span data-stu-id="726fd-109">For more information, see [Using Statement](../../../../visual-basic/language-reference/statements/using-statement.md).</span></span>  
  
## <a name="withend-with-construction"></a><span data-ttu-id="726fd-110">Avec... Se termine par la Construction</span><span class="sxs-lookup"><span data-stu-id="726fd-110">With...End With Construction</span></span>  
 <span data-ttu-id="726fd-111">Le `With...End With` vous permet de spécifier une référence d’objet une fois, puis exécutez une série d’instructions qui accèdent à ses membres.</span><span class="sxs-lookup"><span data-stu-id="726fd-111">The `With...End With` construction lets you specify an object reference once and then run a series of statements that access its members.</span></span> <span data-ttu-id="726fd-112">Cela peut simplifier votre code et améliorer les performances car Visual Basic ne dispose pas de rétablir la référence pour chaque instruction qui y accède.</span><span class="sxs-lookup"><span data-stu-id="726fd-112">This can simplify your code and improve performance because Visual Basic does not have to re-establish the reference for each statement that accesses it.</span></span> <span data-ttu-id="726fd-113">Pour plus d’informations, consultez [avec... End With, instruction](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).</span><span class="sxs-lookup"><span data-stu-id="726fd-113">For more information, see [With...End With Statement](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="726fd-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="726fd-114">See Also</span></span>  
 [<span data-ttu-id="726fd-115">Flux de contrôle</span><span class="sxs-lookup"><span data-stu-id="726fd-115">Control Flow</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)  
 [<span data-ttu-id="726fd-116">Structures de décision</span><span class="sxs-lookup"><span data-stu-id="726fd-116">Decision Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)  
 [<span data-ttu-id="726fd-117">Structures de boucle</span><span class="sxs-lookup"><span data-stu-id="726fd-117">Loop Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)  
 [<span data-ttu-id="726fd-118">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="726fd-118">Nested Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)  
 [<span data-ttu-id="726fd-119">Using (instruction)</span><span class="sxs-lookup"><span data-stu-id="726fd-119">Using Statement</span></span>](../../../../visual-basic/language-reference/statements/using-statement.md)  
 [<span data-ttu-id="726fd-120">With...End With (instruction)</span><span class="sxs-lookup"><span data-stu-id="726fd-120">With...End With Statement</span></span>](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
