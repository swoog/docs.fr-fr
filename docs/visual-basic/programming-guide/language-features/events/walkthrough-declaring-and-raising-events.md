---
title: Déclaration et déclenchement des événements (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [Visual Basic], events
- events [Visual Basic], walkthroughs
- declaring events [Visual Basic], walkthroughs
- events [Visual Basic], declaring
- events [Visual Basic], raising
- raising events [Visual Basic], walkthroughs
ms.assetid: 8ffb3be8-097d-4d3c-b71e-04555ebda2a2
ms.openlocfilehash: f792109f1d1117b5b112e06da1510938e4b8a5ec
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580493"
---
# <a name="walkthrough-declaring-and-raising-events-visual-basic"></a>Procédure pas à pas : Déclaration et déclenchement des événements (Visual Basic)
Cette procédure pas à pas montre comment déclarer et déclencher des événements pour une classe nommée `Widget`. Après avoir terminé les étapes, vous souhaiterez lire la rubrique connexe, [procédure pas à pas : Gestion des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-handling-events.md), qui montre comment utiliser des événements à partir de `Widget` objets pour fournir des informations d’état dans une application.  
  
## <a name="the-widget-class"></a>La classe Widget  
 Supposons pour le moment que vous avez un `Widget` classe. Votre `Widget` classe possède une méthode qui peut prendre beaucoup de temps à exécuter, et vous souhaitez que votre application peut placer une sorte d’indicateur d’achèvement.  
  
 Bien sûr, vous pouvez apporter les `Widget` objet affiche une boîte de dialogue de pourcentage achevé, mais vous allaient être bloqués avec cette boîte de dialogue dans chaque projet dans lequel vous avez utilisé le `Widget` classe. Principe de conception de l’objet consiste à laisser l’application qui utilise un handle d’objet de l’interface utilisateur, à moins que l’objectif de l’objet consiste à gérer une formulaire ou boîte de dialogue.  
  
 L’objectif de `Widget` consiste à effectuer d’autres tâches, par conséquent, il est préférable d’ajouter un `PercentDone` événement et permettent la procédure qui appelle `Widget`de méthodes gèrent qu’événement et l’affichage état des mises à jour. Le `PercentDone` événement peut également fournir un mécanisme d’annulation de la tâche.  
  
#### <a name="to-build-the-code-example-for-this-topic"></a>Pour générer l’exemple de code pour cette rubrique  
  
1.  Ouvrez un nouveau projet d’Application Windows de Visual Basic et créez un formulaire nommé `Form1`.  
  
2.  Ajoutez deux boutons et une étiquette à `Form1`.  
  
3.  Nommez les objets de la façon indiquée dans le tableau suivant.  
  
    |Objet|Propriété|Paramètre|  
    |------------|--------------|-------------|  
    |`Button1`|`Text`|Tâche de démarrage|  
    |`Button2`|`Text`|Annuler|  
    |`Label`|`(Name)`, `Text`|lblPercentDone, 0|  
  
4.  Sur le **projet** menu, choisissez **ajouter une classe** pour ajouter une classe nommée `Widget.vb` au projet.  
  
#### <a name="to-declare-an-event-for-the-widget-class"></a>Pour déclarer un événement pour la classe Widget  
  
-   Utilisez le `Event` mot clé pour déclarer un événement dans le `Widget` classe. Notez qu’un événement peut avoir `ByVal` et `ByRef` arguments, comme `Widget`de `PercentDone` illustre l’événement :  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#1](../../../../visual-basic/programming-guide/language-features/events/codesnippet/VisualBasic/walkthrough-declaring-and-raising-events_1.vb)]  
  
 Lorsque l’objet appelant reçoit un `PercentDone` événement, le `Percent` argument contient le pourcentage de la tâche est terminée. Le `Cancel` argument peut être défini sur `True` pour annuler la méthode qui a déclenché l’événement.  
  
> [!NOTE]
>  Vous pouvez déclarer des arguments d’événement comme arguments de procédures, avec les exceptions suivantes : Les événements ne peut pas avoir `Optional` ou `ParamArray` arguments et les événements n’ont pas de valeurs de retour.  
  
 Le `PercentDone` événement est déclenché par le `LongTask` méthode de la `Widget` classe. `LongTask` accepte deux arguments : la durée pendant laquelle la méthode prétend être active et l’intervalle de temps minimale avant `LongTask` suspendue pour déclencher le `PercentDone` événement.  
  
#### <a name="to-raise-the-percentdone-event"></a>Pour déclencher l’événement PercentDone  
  
1.  Pour simplifier l’accès à la `Timer` propriété utilisée par cette classe, ajoutez un `Imports` instruction au début de la section des déclarations de votre module de classe, au-dessus de la `Class Widget` instruction.  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#2](../../../../visual-basic/programming-guide/language-features/events/codesnippet/VisualBasic/walkthrough-declaring-and-raising-events_2.vb)]  
  
2.  Ajoutez le code suivant à la classe `Widget` :  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#3](../../../../visual-basic/programming-guide/language-features/events/codesnippet/VisualBasic/walkthrough-declaring-and-raising-events_3.vb)]  
  
 Lorsque votre application appelle la `LongTask` (méthode), le `Widget` classe lève la `PercentDone` événements chaque `MinimumInterval` secondes. Lorsque l’événement est retournée, `LongTask` vérifie si le `Cancel` argument a la valeur `True`.  
  
 Certaines exclusions sont nécessaires. Par souci de simplicité, le `LongTask` procédure suppose que vous connaissez à l’avance prendra la durée pendant laquelle la tâche. C’est presque jamais le cas. Peut être difficile de diviser les tâches en segments de taille égale, et souvent ce qui est le plus important pour les utilisateurs est simplement la quantité de temps qui s’écoule avant qu’ils soient une indication que quelque chose qui se passe.  
  
 Dans cet exemple, vous avez remarqué une autre faille. Le `Timer` propriété retourne le nombre de secondes qui se sont écoulées depuis minuit ; par conséquent, l’application se bloque si elle est démarrée juste avant minuit. Une approche plus prudente pour mesurer le temps voulez-vous prendre en compte des conditions de limite telle que celle-ci ou les éviter, à l’aide des propriétés telles que `Now`.  
  
 Maintenant que le `Widget` classe peut déclencher des événements, vous pouvez passer à la procédure suivante. [Procédure pas à pas : Gestion des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-handling-events.md) montre comment utiliser `WithEvents` pour associer un gestionnaire d’événements avec le `PercentDone` événement.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.DateAndTime.Timer%2A>
- <xref:Microsoft.VisualBasic.DateAndTime.Now%2A>
- [Procédure pas à pas : Gestion des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-handling-events.md)
- [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)
