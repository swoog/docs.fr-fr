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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62053806"
---
# <a name="troubleshooting-inherited-event-handlers-in-visual-basic"></a>Dépannage des gestionnaires d'événements hérités dans Visual Basic
Cette rubrique répertorie les problèmes courants qui surviennent avec les gestionnaires d’événements dans les composants hérités.  
  
## <a name="procedures"></a>Procédures  
  
#### <a name="code-in-event-handler-executes-twice-for-every-call"></a>Code de gestionnaire d’événements s’exécute deux fois pour chaque appel.  
  
- Un gestionnaire d’événements hérité ne doit pas inclure un [gère](../../../../visual-basic/language-reference/statements/handles-clause.md) clause. La méthode dans la classe de base est déjà associée à l’événement et se déclenche en conséquence. Supprimer le `Handles` clause de la méthode héritée.  
  
     [!code-vb[VbVbalrEvents#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#32)]  
  
- Si la méthode héritée n’a pas un `Handles` mot clé, vérifiez que votre code ne contient pas un supplémentaire [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md) ou d’autres méthodes qui gèrent le même événement.  
  
## <a name="see-also"></a>Voir aussi

- [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)
