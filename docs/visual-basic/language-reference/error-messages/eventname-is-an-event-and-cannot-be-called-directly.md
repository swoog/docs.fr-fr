---
title: "'<eventname>' est un événement. Il ne peut donc pas être appelé directement"
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: eb0b40a80d37788bcab32791d7ed701a77505371
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58831428"
---
# <a name="eventname-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="d5d1f-102">'\<nom_événement >' est un événement et ne peut pas être appelée directement</span><span class="sxs-lookup"><span data-stu-id="d5d1f-102">'\<eventname>' is an event, and cannot be called directly</span></span>
<span data-ttu-id="d5d1f-103">' <`eventname`>' est un événement et ne peut donc pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="d5d1f-103">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="d5d1f-104">Utilisez un `RaiseEvent` instruction pour déclencher un événement.</span><span class="sxs-lookup"><span data-stu-id="d5d1f-104">Use a `RaiseEvent` statement to raise an event.</span></span>  
  
 <span data-ttu-id="d5d1f-105">Un appel de procédure spécifie un événement pour le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="d5d1f-105">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="d5d1f-106">Un gestionnaire d’événements est une procédure, mais l’événement lui-même est un dispositif de signalisation, qui doit être déclenché et géré.</span><span class="sxs-lookup"><span data-stu-id="d5d1f-106">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>  
  
 <span data-ttu-id="d5d1f-107">**ID d’erreur :** BC32022</span><span class="sxs-lookup"><span data-stu-id="d5d1f-107">**Error ID:** BC32022</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d5d1f-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="d5d1f-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="d5d1f-109">Utilisez un `RaiseEvent` instruction pour signaler un événement et appeler les procédures qui le gèrent.</span><span class="sxs-lookup"><span data-stu-id="d5d1f-109">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5d1f-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d1f-110">See also</span></span>

- [<span data-ttu-id="d5d1f-111">RaiseEvent (instruction)</span><span class="sxs-lookup"><span data-stu-id="d5d1f-111">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
