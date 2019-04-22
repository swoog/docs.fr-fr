---
title: RemoveHandler, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.RemoveHandlerMethod
- vb.RemoveHandler
- RemoveHandler
helpviewer_keywords:
- RemoveHandler keyword [Visual Basic]
- RemoveHandler statement [Visual Basic]
ms.assetid: 647cd825-e877-4910-b4f1-8d168beebe6a
ms.openlocfilehash: 8a9dc5874629c1687318496bd7c4016eb318c25a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58831681"
---
# <a name="removehandler-statement"></a><span data-ttu-id="ae513-102">RemoveHandler, instruction</span><span class="sxs-lookup"><span data-stu-id="ae513-102">RemoveHandler Statement</span></span>
<span data-ttu-id="ae513-103">Supprime l’association entre un événement et un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="ae513-103">Removes the association between an event and an event handler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae513-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae513-104">Syntax</span></span>  
  
```  
RemoveHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a><span data-ttu-id="ae513-105">Composants</span><span class="sxs-lookup"><span data-stu-id="ae513-105">Parts</span></span>  
  
|<span data-ttu-id="ae513-106">Terme</span><span class="sxs-lookup"><span data-stu-id="ae513-106">Term</span></span>|<span data-ttu-id="ae513-107">Définition</span><span class="sxs-lookup"><span data-stu-id="ae513-107">Definition</span></span>|  
|---|---|  
|`event`|<span data-ttu-id="ae513-108">Le nom de l’événement géré.</span><span class="sxs-lookup"><span data-stu-id="ae513-108">The name of the event being handled.</span></span>|  
|`eventhandler`|<span data-ttu-id="ae513-109">Le nom de la procédure actuellement gérant l’événement.</span><span class="sxs-lookup"><span data-stu-id="ae513-109">The name of the procedure currently handling the event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae513-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ae513-110">Remarks</span></span>  
 <span data-ttu-id="ae513-111">Le `AddHandler` et `RemoveHandler` vous permettent de démarrer et arrêter la gestion des événements pour un événement spécifique à tout moment pendant l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="ae513-111">The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling for a specific event at any time during program execution.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ae513-112">Pour les événements personnalisés, le `RemoveHandler` instruction appelle de l’événement `RemoveHandler` accesseur.</span><span class="sxs-lookup"><span data-stu-id="ae513-112">For custom events, the `RemoveHandler` statement invokes the event's `RemoveHandler` accessor.</span></span> <span data-ttu-id="ae513-113">Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ae513-113">For more information on custom events, see [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ae513-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="ae513-114">Example</span></span>  
 [!code-vb[VbVbalrEvents#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#17)]  
  
## <a name="see-also"></a><span data-ttu-id="ae513-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae513-115">See also</span></span>

- [<span data-ttu-id="ae513-116">AddHandler (instruction)</span><span class="sxs-lookup"><span data-stu-id="ae513-116">AddHandler Statement</span></span>](../../../visual-basic/language-reference/statements/addhandler-statement.md)
- [<span data-ttu-id="ae513-117">Handles</span><span class="sxs-lookup"><span data-stu-id="ae513-117">Handles</span></span>](../../../visual-basic/language-reference/statements/handles-clause.md)
- [<span data-ttu-id="ae513-118">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="ae513-118">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="ae513-119">Événements</span><span class="sxs-lookup"><span data-stu-id="ae513-119">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
