---
title: Dépannage des gestionnaires d'événements hérités dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- troubleshooting events [Visual Basic]
- inherited events [Visual Basic]
- troubleshooting Visual Basic, event handlers
- event handling, troubleshooting
- event handlers, troubleshooting
ms.assetid: e1c8759f-5370-4308-8476-8c48b73509bf
ms.openlocfilehash: f6355cf7fc2e43651c1112d048220a8179968c76
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33646306"
---
# <a name="troubleshooting-inherited-event-handlers-in-visual-basic"></a><span data-ttu-id="02974-102">Dépannage des gestionnaires d'événements hérités dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="02974-102">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>
<span data-ttu-id="02974-103">Cette rubrique répertorie les problèmes courants qui surviennent avec les gestionnaires d’événements dans les composants hérités.</span><span class="sxs-lookup"><span data-stu-id="02974-103">This topic lists common issues that arise with event handlers in inherited components.</span></span>  
  
## <a name="procedures"></a><span data-ttu-id="02974-104">Procédures</span><span class="sxs-lookup"><span data-stu-id="02974-104">Procedures</span></span>  
  
#### <a name="code-in-event-handler-executes-twice-for-every-call"></a><span data-ttu-id="02974-105">Code de gestionnaire d’événements s’exécute deux fois pour chaque appel.</span><span class="sxs-lookup"><span data-stu-id="02974-105">Code in Event Handler Executes Twice for Every Call</span></span>  
  
-   <span data-ttu-id="02974-106">Un gestionnaire d’événements hérité ne doit pas inclure un [gère](../../../../visual-basic/language-reference/statements/handles-clause.md) clause.</span><span class="sxs-lookup"><span data-stu-id="02974-106">An inherited event handler must not include a [Handles](../../../../visual-basic/language-reference/statements/handles-clause.md) clause.</span></span> <span data-ttu-id="02974-107">La méthode dans la classe de base est déjà associée à l’événement et se déclenche en conséquence.</span><span class="sxs-lookup"><span data-stu-id="02974-107">The method in the base class is already associated with the event and will fire accordingly.</span></span> <span data-ttu-id="02974-108">Supprimer le `Handles` clause de la méthode héritée.</span><span class="sxs-lookup"><span data-stu-id="02974-108">Remove the `Handles` clause from the inherited method.</span></span>  
  
     [!code-vb[VbVbalrEvents#32](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/troubleshooting-inherited-event-handlers_1.vb)]  
  
-   <span data-ttu-id="02974-109">Si la méthode héritée n’a pas un `Handles` (mot clé), vérifiez que votre code ne contient pas un fichier extra [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md) ou d’autres méthodes qui gèrent le même événement.</span><span class="sxs-lookup"><span data-stu-id="02974-109">If the inherited method does not have a `Handles` keyword, verify that your code does not contain an extra [AddHandler Statement](../../../../visual-basic/language-reference/statements/addhandler-statement.md) or any additional methods that handle the same event.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02974-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02974-110">See Also</span></span>  
 [<span data-ttu-id="02974-111">Événements</span><span class="sxs-lookup"><span data-stu-id="02974-111">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)
