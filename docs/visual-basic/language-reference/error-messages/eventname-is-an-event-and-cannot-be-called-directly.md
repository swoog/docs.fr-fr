---
title: '&#39;&lt;nom_événement&gt; &#39; est un événement et ne peut pas être appelée directement'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 4d8a7d716d2b7c52d1d027a1e7959d981bb0857e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587330"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="7992b-102">&#39;&lt;nom_événement&gt; &#39; est un événement et ne peut pas être appelée directement</span><span class="sxs-lookup"><span data-stu-id="7992b-102">&#39;&lt;eventname&gt;&#39; is an event, and cannot be called directly</span></span>
<span data-ttu-id="7992b-103">' <`eventname`>' est un événement et ne peut donc pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="7992b-103">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="7992b-104">Utilisez un `RaiseEvent` instruction pour déclencher un événement.</span><span class="sxs-lookup"><span data-stu-id="7992b-104">Use a `RaiseEvent` statement to raise an event.</span></span>  
  
 <span data-ttu-id="7992b-105">Un appel de procédure spécifie un événement pour le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="7992b-105">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="7992b-106">Un gestionnaire d’événements est une procédure, mais l’événement lui-même est un dispositif de signalisation qui doit être déclenché et géré.</span><span class="sxs-lookup"><span data-stu-id="7992b-106">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>  
  
 <span data-ttu-id="7992b-107">**ID d’erreur :** BC32022</span><span class="sxs-lookup"><span data-stu-id="7992b-107">**Error ID:** BC32022</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7992b-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="7992b-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="7992b-109">Utilisez un `RaiseEvent` instruction pour signaler un événement et appeler les procédures qui le gèrent.</span><span class="sxs-lookup"><span data-stu-id="7992b-109">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7992b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7992b-110">See Also</span></span>  
 [<span data-ttu-id="7992b-111">RaiseEvent (instruction)</span><span class="sxs-lookup"><span data-stu-id="7992b-111">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
