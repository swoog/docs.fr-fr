---
title: AddHandler, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AddHandlerMethod
- addhandler
- vb.addhandler
helpviewer_keywords:
- AddHandler statement [Visual Basic]
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
ms.openlocfilehash: f731ff150bd901e325726fca5aa682ff1770f979
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43502948"
---
# <a name="addhandler-statement"></a><span data-ttu-id="03eda-102">AddHandler, instruction</span><span class="sxs-lookup"><span data-stu-id="03eda-102">AddHandler Statement</span></span>
<span data-ttu-id="03eda-103">Associe un événement à un gestionnaire d’événements en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="03eda-103">Associates an event with an event handler at run time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03eda-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03eda-104">Syntax</span></span>  
  
```  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a><span data-ttu-id="03eda-105">Composants</span><span class="sxs-lookup"><span data-stu-id="03eda-105">Parts</span></span>  
|||
|---|---|
|<span data-ttu-id="03eda-106">événement</span><span class="sxs-lookup"><span data-stu-id="03eda-106">event</span></span>|<span data-ttu-id="03eda-107">Le nom de l’événement à gérer.</span><span class="sxs-lookup"><span data-stu-id="03eda-107">The name of the event to handle.</span></span>|  
|`eventhandler`|<span data-ttu-id="03eda-108">Le nom d’une procédure qui gère l’événement.</span><span class="sxs-lookup"><span data-stu-id="03eda-108">The name of a procedure that handles the event.</span></span>|
|||
  
## <a name="remarks"></a><span data-ttu-id="03eda-109">Notes</span><span class="sxs-lookup"><span data-stu-id="03eda-109">Remarks</span></span>  
 <span data-ttu-id="03eda-110">Le `AddHandler` et `RemoveHandler` vous permettent de démarrer et arrêter la gestion des événements à tout moment pendant l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="03eda-110">The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling at any time during program execution.</span></span>  
  
 <span data-ttu-id="03eda-111">La signature de la `eventhandler` procédure doit correspondre à la signature de l’événement `event`.</span><span class="sxs-lookup"><span data-stu-id="03eda-111">The signature of the `eventhandler` procedure must match the signature of the event `event`.</span></span>  
  
 <span data-ttu-id="03eda-112">Le mot clé `Handles` et l'instruction `AddHandler` vous permettent de spécifier que des procédures particulières gèrent des événements particuliers, mais il existe des différences.</span><span class="sxs-lookup"><span data-stu-id="03eda-112">The `Handles` keyword and the `AddHandler` statement both allow you to specify that particular procedures handle particular events, but there are differences.</span></span> <span data-ttu-id="03eda-113">L'instruction `AddHandler` connecte les procédures aux événements au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="03eda-113">The `AddHandler` statement connects procedures to events at run time.</span></span> <span data-ttu-id="03eda-114">Utilisez le mot clé `Handles` quand vous définissez une procédure pour indiquer qu'elle gère un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="03eda-114">Use the `Handles` keyword when defining a procedure to specify that it handles a particular event.</span></span> <span data-ttu-id="03eda-115">Pour plus d’informations, consultez [gère](../../../visual-basic/language-reference/statements/handles-clause.md).</span><span class="sxs-lookup"><span data-stu-id="03eda-115">For more information, see [Handles](../../../visual-basic/language-reference/statements/handles-clause.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="03eda-116">Pour les événements personnalisés, le `AddHandler` instruction appelle de l’événement `AddHandler` accesseur.</span><span class="sxs-lookup"><span data-stu-id="03eda-116">For custom events, the `AddHandler` statement invokes the event's `AddHandler` accessor.</span></span> <span data-ttu-id="03eda-117">Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="03eda-117">For more information on custom events, see [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="03eda-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="03eda-118">Example</span></span>  
 [!code-vb[VbVbalrEvents#17](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/addhandler-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="03eda-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03eda-119">See Also</span></span>  
 [<span data-ttu-id="03eda-120">RemoveHandler (instruction)</span><span class="sxs-lookup"><span data-stu-id="03eda-120">RemoveHandler Statement</span></span>](../../../visual-basic/language-reference/statements/removehandler-statement.md)  
 [<span data-ttu-id="03eda-121">Handles</span><span class="sxs-lookup"><span data-stu-id="03eda-121">Handles</span></span>](../../../visual-basic/language-reference/statements/handles-clause.md)  
 [<span data-ttu-id="03eda-122">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="03eda-122">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
 [<span data-ttu-id="03eda-123">Événements</span><span class="sxs-lookup"><span data-stu-id="03eda-123">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
