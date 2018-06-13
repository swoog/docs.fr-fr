---
title: AddHandler, instruction
ms.date: 07/20/2015
f1_keywords:
- vb.AddHandlerMethod
- addhandler
- vb.addhandler
helpviewer_keywords:
- AddHandler statement [Visual Basic]
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
ms.openlocfilehash: db8131dc82aed40e725c9375efef274fb6917d41
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603650"
---
# <a name="addhandler-statement"></a><span data-ttu-id="781d5-102">AddHandler, instruction</span><span class="sxs-lookup"><span data-stu-id="781d5-102">AddHandler Statement</span></span>
<span data-ttu-id="781d5-103">Associe un événement à un gestionnaire d’événements au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="781d5-103">Associates an event with an event handler at run time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="781d5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="781d5-104">Syntax</span></span>  
  
```  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a><span data-ttu-id="781d5-105">Composants</span><span class="sxs-lookup"><span data-stu-id="781d5-105">Parts</span></span>  
 `event`  
 <span data-ttu-id="781d5-106">Le nom de l’événement à gérer.</span><span class="sxs-lookup"><span data-stu-id="781d5-106">The name of the event to handle.</span></span>  
  
 `eventhandler`  
 <span data-ttu-id="781d5-107">Le nom d’une procédure qui gère l’événement.</span><span class="sxs-lookup"><span data-stu-id="781d5-107">The name of a procedure that handles the event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="781d5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="781d5-108">Remarks</span></span>  
 <span data-ttu-id="781d5-109">Le `AddHandler` et `RemoveHandler` vous permettent de démarrer et arrêter la gestion des événements à tout moment pendant l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="781d5-109">The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling at any time during program execution.</span></span>  
  
 <span data-ttu-id="781d5-110">La signature de la `eventhandler` procédure doit correspondre à la signature de l’événement `event`.</span><span class="sxs-lookup"><span data-stu-id="781d5-110">The signature of the `eventhandler` procedure must match the signature of the event `event`.</span></span>  
  
 <span data-ttu-id="781d5-111">Le mot clé `Handles` et l'instruction `AddHandler` vous permettent de spécifier que des procédures particulières gèrent des événements particuliers, mais il existe des différences.</span><span class="sxs-lookup"><span data-stu-id="781d5-111">The `Handles` keyword and the `AddHandler` statement both allow you to specify that particular procedures handle particular events, but there are differences.</span></span> <span data-ttu-id="781d5-112">L'instruction `AddHandler` connecte les procédures aux événements au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="781d5-112">The `AddHandler` statement connects procedures to events at run time.</span></span> <span data-ttu-id="781d5-113">Utilisez le mot clé `Handles` quand vous définissez une procédure pour indiquer qu'elle gère un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="781d5-113">Use the `Handles` keyword when defining a procedure to specify that it handles a particular event.</span></span> <span data-ttu-id="781d5-114">Pour plus d’informations, consultez [gère](../../../visual-basic/language-reference/statements/handles-clause.md).</span><span class="sxs-lookup"><span data-stu-id="781d5-114">For more information, see [Handles](../../../visual-basic/language-reference/statements/handles-clause.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="781d5-115">Pour les événements personnalisés, les `AddHandler` instruction appelle l’événement `AddHandler` accesseur.</span><span class="sxs-lookup"><span data-stu-id="781d5-115">For custom events, the `AddHandler` statement invokes the event's `AddHandler` accessor.</span></span> <span data-ttu-id="781d5-116">Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="781d5-116">For more information on custom events, see [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="781d5-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="781d5-117">Example</span></span>  
 [!code-vb[VbVbalrEvents#17](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/addhandler-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="781d5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="781d5-118">See Also</span></span>  
 [<span data-ttu-id="781d5-119">RemoveHandler (instruction)</span><span class="sxs-lookup"><span data-stu-id="781d5-119">RemoveHandler Statement</span></span>](../../../visual-basic/language-reference/statements/removehandler-statement.md)  
 [<span data-ttu-id="781d5-120">Handles</span><span class="sxs-lookup"><span data-stu-id="781d5-120">Handles</span></span>](../../../visual-basic/language-reference/statements/handles-clause.md)  
 [<span data-ttu-id="781d5-121">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="781d5-121">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
 [<span data-ttu-id="781d5-122">Événements</span><span class="sxs-lookup"><span data-stu-id="781d5-122">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
