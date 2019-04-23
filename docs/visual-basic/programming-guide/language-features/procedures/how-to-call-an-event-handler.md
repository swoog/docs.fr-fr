---
title: 'Procédure : Appeler un gestionnaire d’événements en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- event handlers [Visual Basic], calling
- event handlers
- procedures [Visual Basic], event handlers
- procedures [Visual Basic], calling
ms.assetid: 72e18ef8-144e-40df-a1f4-066a57271e28
ms.openlocfilehash: 3690d1c2eb8ece9059b8b25b5a14bef2021bc8f6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59320169"
---
# <a name="how-to-call-an-event-handler-in-visual-basic"></a>Procédure : Appeler un gestionnaire d’événements en Visual Basic
Un *événement* est une action ou une occurrence, comme une souris, cliquez ou une limite de crédit dépassé, qui est reconnue par un composant de programme, et pour lequel vous pouvez écrire du code pour répondre. Un *Gestionnaire d’événements* est le code que vous écrivez pour répondre à un événement.  
  
 Un gestionnaire d’événements en Visual Basic est un `Sub` procédure. Toutefois, vous ne normalement l’appelez pas la même façon que les autres `Sub` procédures. Au lieu de cela, vous identifiez la procédure en tant que gestionnaire pour l’événement. Cela avec une [gère](../../../../visual-basic/language-reference/statements/handles-clause.md) clause et un [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md) variable, ou avec un [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md). À l’aide un `Handles` clause constitue la méthode par défaut pour déclarer un gestionnaire d’événements en Visual Basic. Il s’agit de la manière dont les gestionnaires d’événements sont écrits par les concepteurs lorsque vous programmez dans l’environnement de développement intégré (IDE). La `AddHandler` instruction convient pour déclencher des événements dynamiquement au moment de l’exécution.  
  
 Lorsque l’événement se produit, Visual Basic appelle automatiquement la procédure de gestionnaire d’événements. Tout code qui a accès à l’événement peut déclencher celui-ci en exécutant une [RaiseEvent, instruction](../../../../visual-basic/language-reference/statements/raiseevent-statement.md).  
  
 Vous pouvez associer plusieurs gestionnaires d’événements avec le même événement. Dans certains cas, vous pouvez dissocier un gestionnaire d’un événement. Pour plus d'informations, consultez [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md).  
  
### <a name="to-call-an-event-handler-using-handles-and-withevents"></a>Pour appeler un gestionnaire d’événements à l’aide de Handles et WithEvents  
  
1. Assurez-vous que l’événement est déclaré avec un [Event, instruction](../../../../visual-basic/language-reference/statements/event-statement.md).  
  
2. Déclarez une variable d’objet au module ou de la classe de niveau, à l’aide de la [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md) mot clé. Le `As` clause pour cette variable doit spécifier la classe qui déclenche l’événement.  
  
3. Dans la déclaration de la gestion des événements `Sub` procédure, ajoutez un [gère](../../../../visual-basic/language-reference/statements/handles-clause.md) clause qui spécifie le `WithEvents` variable et le nom de l’événement.  
  
4. Lorsque l’événement se produit, Visual Basic appelle automatiquement la `Sub` procédure. Votre code peut utiliser un `RaiseEvent` instruction pour rendre l’événement se produit.  
  
     L’exemple suivant définit un événement et un `WithEvents` variable qui fait référence à la classe qui déclenche l’événement. La gestion des événements `Sub` procédure utilise un `Handles` clause pour spécifier la classe et l’événement qu’elle gère.  
  
     [!code-vb[VbVbcnProcedures#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#4)]  
  
### <a name="to-call-an-event-handler-using-addhandler"></a>Pour appeler un gestionnaire d’événements à l’aide de AddHandler  
  
1. Assurez-vous que l’événement est déclaré avec un `Event` instruction.  
  
2. Exécuter un [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md) connecter dynamiquement la gestion des événements `Sub` procédure avec l’événement.  
  
3. Lorsque l’événement se produit, Visual Basic appelle automatiquement la `Sub` procédure. Votre code peut utiliser un `RaiseEvent` instruction pour rendre l’événement se produit.  
  
     L’exemple suivant définit un `Sub` procédure gère le <xref:System.Windows.Forms.Form.Closing> événement d’un formulaire. Il utilise ensuite le [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md) pour associer le `catchClose` procédure comme gestionnaire d’événements pour <xref:System.Windows.Forms.Form.Closing>.  
  
     [!code-vb[VbVbcnProcedures#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#5)]  
  
     Vous pouvez dissocier un gestionnaire d’événements à partir d’un événement en exécutant la [RemoveHandler, instruction](../../../../visual-basic/language-reference/statements/removehandler-statement.md).  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Sub (instruction)](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [AddressOf (opérateur)](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Guide pratique pour Créer une procédure](./how-to-create-a-procedure.md)
- [Guide pratique pour Appeler une procédure qui ne retourne pas de valeur](./how-to-call-a-procedure-that-does-not-return-a-value.md)
