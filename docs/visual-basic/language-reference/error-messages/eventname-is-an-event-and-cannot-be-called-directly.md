---
title: "'<eventname>' est un événement. Il ne peut donc pas être appelé directement"
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: bf900566bdb4ecf8d8961a12b5dd67ba426caf27
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59305596"
---
# <a name="eventname-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="4c4a8-102">'\<nom_événement >' est un événement et ne peut pas être appelée directement</span><span class="sxs-lookup"><span data-stu-id="4c4a8-102">'\<eventname>' is an event, and cannot be called directly</span></span>
<span data-ttu-id="4c4a8-103">' <`eventname`>' est un événement et ne peut donc pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="4c4a8-103">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="4c4a8-104">Utilisez un `RaiseEvent` instruction pour déclencher un événement.</span><span class="sxs-lookup"><span data-stu-id="4c4a8-104">Use a `RaiseEvent` statement to raise an event.</span></span>  
  
 <span data-ttu-id="4c4a8-105">Un appel de procédure spécifie un événement pour le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="4c4a8-105">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="4c4a8-106">Un gestionnaire d’événements est une procédure, mais l’événement lui-même est un dispositif de signalisation, qui doit être déclenché et géré.</span><span class="sxs-lookup"><span data-stu-id="4c4a8-106">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>  
  
 <span data-ttu-id="4c4a8-107">**ID d’erreur :** BC32022</span><span class="sxs-lookup"><span data-stu-id="4c4a8-107">**Error ID:** BC32022</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4c4a8-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="4c4a8-108">To correct this error</span></span>  
  
1. <span data-ttu-id="4c4a8-109">Utilisez un `RaiseEvent` instruction pour signaler un événement et appeler les procédures qui le gèrent.</span><span class="sxs-lookup"><span data-stu-id="4c4a8-109">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c4a8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c4a8-110">See also</span></span>

- [<span data-ttu-id="4c4a8-111">RaiseEvent, instruction</span><span class="sxs-lookup"><span data-stu-id="4c4a8-111">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
