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
ms.openlocfilehash: dd57f63b5741822de7b11c1fafe90452a767aa34
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56965642"
---
# <a name="addhandler-statement"></a><span data-ttu-id="26239-102">AddHandler, instruction</span><span class="sxs-lookup"><span data-stu-id="26239-102">AddHandler Statement</span></span>
<span data-ttu-id="26239-103">Associe un événement à un gestionnaire d’événements en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="26239-103">Associates an event with an event handler at run time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26239-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26239-104">Syntax</span></span>  
  
```  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a><span data-ttu-id="26239-105">Composants</span><span class="sxs-lookup"><span data-stu-id="26239-105">Parts</span></span>  
|||
|---|---|
|<span data-ttu-id="26239-106">événement</span><span class="sxs-lookup"><span data-stu-id="26239-106">event</span></span>|<span data-ttu-id="26239-107">Le nom de l’événement à gérer.</span><span class="sxs-lookup"><span data-stu-id="26239-107">The name of the event to handle.</span></span>|  
|`eventhandler`|<span data-ttu-id="26239-108">Le nom d’une procédure qui gère l’événement.</span><span class="sxs-lookup"><span data-stu-id="26239-108">The name of a procedure that handles the event.</span></span>|
|||
  
## <a name="remarks"></a><span data-ttu-id="26239-109">Notes</span><span class="sxs-lookup"><span data-stu-id="26239-109">Remarks</span></span>  
 <span data-ttu-id="26239-110">Le `AddHandler` et `RemoveHandler` vous permettent de démarrer et arrêter la gestion des événements à tout moment pendant l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="26239-110">The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling at any time during program execution.</span></span>  
  
 <span data-ttu-id="26239-111">La signature de la `eventhandler` procédure doit correspondre à la signature de l’événement `event`.</span><span class="sxs-lookup"><span data-stu-id="26239-111">The signature of the `eventhandler` procedure must match the signature of the event `event`.</span></span>  
  
 <span data-ttu-id="26239-112">Le mot clé `Handles` et l'instruction `AddHandler` vous permettent de spécifier que des procédures particulières gèrent des événements particuliers, mais il existe des différences.</span><span class="sxs-lookup"><span data-stu-id="26239-112">The `Handles` keyword and the `AddHandler` statement both allow you to specify that particular procedures handle particular events, but there are differences.</span></span> <span data-ttu-id="26239-113">L'instruction `AddHandler` connecte les procédures aux événements au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="26239-113">The `AddHandler` statement connects procedures to events at run time.</span></span> <span data-ttu-id="26239-114">Utilisez le mot clé `Handles` quand vous définissez une procédure pour indiquer qu'elle gère un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="26239-114">Use the `Handles` keyword when defining a procedure to specify that it handles a particular event.</span></span> <span data-ttu-id="26239-115">Pour plus d’informations, consultez [gère](../../../visual-basic/language-reference/statements/handles-clause.md).</span><span class="sxs-lookup"><span data-stu-id="26239-115">For more information, see [Handles](../../../visual-basic/language-reference/statements/handles-clause.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="26239-116">Pour les événements personnalisés, le `AddHandler` instruction appelle de l’événement `AddHandler` accesseur.</span><span class="sxs-lookup"><span data-stu-id="26239-116">For custom events, the `AddHandler` statement invokes the event's `AddHandler` accessor.</span></span> <span data-ttu-id="26239-117">Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="26239-117">For more information on custom events, see [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="26239-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="26239-118">Example</span></span>  
 [!code-vb[VbVbalrEvents#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#17)]  
  
## <a name="see-also"></a><span data-ttu-id="26239-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26239-119">See also</span></span>
- [<span data-ttu-id="26239-120">RemoveHandler (instruction)</span><span class="sxs-lookup"><span data-stu-id="26239-120">RemoveHandler Statement</span></span>](../../../visual-basic/language-reference/statements/removehandler-statement.md)
- [<span data-ttu-id="26239-121">Handles</span><span class="sxs-lookup"><span data-stu-id="26239-121">Handles</span></span>](../../../visual-basic/language-reference/statements/handles-clause.md)
- [<span data-ttu-id="26239-122">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="26239-122">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="26239-123">Événements</span><span class="sxs-lookup"><span data-stu-id="26239-123">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
