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
ms.openlocfilehash: 704ca667a6d14ade7be0192e872f5e40791cb864
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58830186"
---
# <a name="troubleshooting-inherited-event-handlers-in-visual-basic"></a><span data-ttu-id="27fe8-102">Dépannage des gestionnaires d'événements hérités dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="27fe8-102">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>
<span data-ttu-id="27fe8-103">Cette rubrique répertorie les problèmes courants qui surviennent avec les gestionnaires d’événements dans les composants hérités.</span><span class="sxs-lookup"><span data-stu-id="27fe8-103">This topic lists common issues that arise with event handlers in inherited components.</span></span>  
  
## <a name="procedures"></a><span data-ttu-id="27fe8-104">Procédures</span><span class="sxs-lookup"><span data-stu-id="27fe8-104">Procedures</span></span>  
  
#### <a name="code-in-event-handler-executes-twice-for-every-call"></a><span data-ttu-id="27fe8-105">Code de gestionnaire d’événements s’exécute deux fois pour chaque appel.</span><span class="sxs-lookup"><span data-stu-id="27fe8-105">Code in Event Handler Executes Twice for Every Call</span></span>  
  
-   <span data-ttu-id="27fe8-106">Un gestionnaire d’événements hérité ne doit pas inclure un [gère](../../../../visual-basic/language-reference/statements/handles-clause.md) clause.</span><span class="sxs-lookup"><span data-stu-id="27fe8-106">An inherited event handler must not include a [Handles](../../../../visual-basic/language-reference/statements/handles-clause.md) clause.</span></span> <span data-ttu-id="27fe8-107">La méthode dans la classe de base est déjà associée à l’événement et se déclenche en conséquence.</span><span class="sxs-lookup"><span data-stu-id="27fe8-107">The method in the base class is already associated with the event and will fire accordingly.</span></span> <span data-ttu-id="27fe8-108">Supprimer le `Handles` clause de la méthode héritée.</span><span class="sxs-lookup"><span data-stu-id="27fe8-108">Remove the `Handles` clause from the inherited method.</span></span>  
  
     [!code-vb[VbVbalrEvents#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#32)]  
  
-   <span data-ttu-id="27fe8-109">Si la méthode héritée n’a pas un `Handles` mot clé, vérifiez que votre code ne contient pas un supplémentaire [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md) ou d’autres méthodes qui gèrent le même événement.</span><span class="sxs-lookup"><span data-stu-id="27fe8-109">If the inherited method does not have a `Handles` keyword, verify that your code does not contain an extra [AddHandler Statement](../../../../visual-basic/language-reference/statements/addhandler-statement.md) or any additional methods that handle the same event.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27fe8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27fe8-110">See also</span></span>

- [<span data-ttu-id="27fe8-111">Événements</span><span class="sxs-lookup"><span data-stu-id="27fe8-111">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)
