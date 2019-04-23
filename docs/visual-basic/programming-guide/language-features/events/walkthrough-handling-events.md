---
title: Gestion des événements (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- event handling [Visual Basic], walkthroughs
- walkthroughs [Visual Basic], event handling
- variables [Visual Basic], WithEvents
- events [Visual Basic], walkthroughs
- WithEvents keyword [Visual Basic], walkthroughs
- event handlers [Visual Basic], walkthroughs
ms.assetid: f145b3fc-5ae0-4509-a2aa-1ff6934706bd
ms.openlocfilehash: 2ae32f0ac31c504e86d5cf39ed6a36cc5523a4a0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59308560"
---
# <a name="walkthrough-handling-events-visual-basic"></a>Procédure pas à pas : Gestion des événements (Visual Basic)
Il s’agit de la deuxième des deux rubriques qui montrent comment utiliser des événements. La première rubrique [procédure pas à pas : Déclaration et déclenchement des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-declaring-and-raising-events.md), montre comment déclarer et déclencher des événements. Cette section utilise le formulaire et la classe à partir de cette procédure pas à pas pour montrer comment gérer des événements lorsqu’elles ont lieu.  
  
 Le `Widget` exemple de classe utilise des instructions de gestion des événements traditionnelles. Visual Basic fournit d’autres techniques pour l’utilisation des événements. En guise d’exercice, vous pouvez modifier cet exemple montre comment utiliser le `AddHandler` et `Handles` instructions.  
  
### <a name="to-handle-the-percentdone-event-of-the-widget-class"></a>Pour gérer l’événement PercentDone de la classe Widget  
  
1. Placez le code suivant dans `Form1`:  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnWalkthroughDeclaringAndRaisingEvents/VB/Form1.vb#4)]  
  
     Le `WithEvents` mot clé spécifie que la variable `mWidget` est utilisée pour gérer les événements d’un objet. Vous spécifiez le type d’objet en fournissant le nom de la classe à partir duquel l’objet sera créé.  
  
     La variable `mWidget` est déclarée dans `Form1` car `WithEvents` variables doivent être de niveau classe. Cela est vrai quel que soit le type de classe que vous les placez dans.  
  
     La variable `mblnCancel` est utilisée pour annuler le `LongTask` (méthode).  
  
## <a name="writing-code-to-handle-an-event"></a>Écriture de Code pour gérer un événement  
 Dès que vous déclarez une variable à l’aide `WithEvents`, le nom de variable s’affiche dans la liste déroulante de gauche de la classe **éditeur de Code**. Lorsque vous sélectionnez `mWidget`, le `Widget` événements de la classe apparaissent dans la liste déroulante droite. Si un événement est sélectionnée, la procédure d’événement correspondante, avec le préfixe `mWidget` et un trait de soulignement. Toutes les procédures d’événement associés à un `WithEvents` variable reçoivent le nom de variable en tant que préfixe.  
  
#### <a name="to-handle-an-event"></a>Pour gérer un événement  
  
1. Sélectionnez `mWidget` dans la liste déroulante de gauche dans le **éditeur de Code**.  
  
2. Sélectionnez le `PercentDone` événement dans la liste déroulante droite. Le **éditeur de Code** ouvre le `mWidget_PercentDone` procédure événementielle.  
  
    > [!NOTE]
    >  Le **éditeur de Code** est utile, mais pas obligatoire, pour l’insertion de nouveaux gestionnaires d’événements. Dans cette procédure pas à pas, il est plus rapide de copier simplement les gestionnaires d’événements directement dans votre code.  
  
3. Ajoutez le code suivant au gestionnaire d'événements `mWidget_PercentDone` :  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnWalkthroughDeclaringAndRaisingEvents/VB/Form1.vb#5)]  
  
     Chaque fois que le `PercentDone` événement est déclenché, la procédure événementielle affiche le pourcentage d’achèvement dans un `Label` contrôle. Le `DoEvents` méthode permet de l’étiquette à repeindre et donne également à l’utilisateur la possibilité de cliquer sur le **Annuler** bouton.  
  
4. Ajoutez le code suivant pour le `Button2_Click` Gestionnaire d’événements :  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnWalkthroughDeclaringAndRaisingEvents/VB/Form1.vb#6)]  
  
 Si l’utilisateur clique sur le **Annuler** bouton lors de la `LongTask` est en cours d’exécution, le `Button2_Click` événement est exécuté dès que le `DoEvents` instruction permet le traitement de l’événement. La variable de niveau classe `mblnCancel` a la valeur `True`et le `mWidget_PercentDone` événement, puis le teste et définit le `ByRef Cancel` argument `True`.  
  
## <a name="connecting-a-withevents-variable-to-an-object"></a>Connexion d’une Variable WithEvents à un objet  
 `Form1` est désormais configuré pour gérer un `Widget` événements d’objet. Ne reste qu’à trouver un `Widget` quelque part.  
  
 Lorsque vous déclarez une variable `WithEvents` au moment du design, aucun objet lui n’est associé. A `WithEvents` variable s’apparente à toute autre variable d’objet. Vous devez créer un objet et lui assigner une référence à l’aide du `WithEvents` variable.  
  
#### <a name="to-create-an-object-and-assign-a-reference-to-it"></a>Pour créer un objet et affecter une référence à celui-ci  
  
1. Sélectionnez **(Form1 Events)** dans la liste déroulante de gauche dans le **éditeur de Code**.  
  
2. Sélectionnez le `Load` événement dans la liste déroulante droite. Le **éditeur de Code** ouvre le `Form1_Load` procédure événementielle.  
  
3. Ajoutez le code suivant pour le `Form1_Load` procédure événementielle à créer le `Widget`:  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnWalkthroughDeclaringAndRaisingEvents/VB/Form1.vb#7)]  
  
 Lorsque ce code s’exécute, Visual Basic crée un `Widget` de l’objet et se connecte ses événements pour les procédures d’événement associées `mWidget`. Partir de ce point, chaque fois que le `Widget` déclenche son `PercentDone` événement, le `mWidget_PercentDone` procédure événementielle est exécutée.  
  
#### <a name="to-call-the-longtask-method"></a>Pour appeler la méthode LongTask  
  
-   Ajoutez le code suivant au gestionnaire d'événements `Button1_Click` :  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnWalkthroughDeclaringAndRaisingEvents/VB/Form1.vb#8)]  
  
 Avant du `LongTask` méthode est appelée, l’étiquette qu’affiche le pourcentage d’achèvement doit être initialisé et niveau de la classe `Boolean` indicateur pour l’annulation de la méthode doit être définie sur `False`.  
  
 `LongTask` est appelée avec une durée de la tâche de 12,2 secondes. Le `PercentDone` événement est déclenché une fois tous les tiers de seconde. Chaque fois que l’événement est déclenché, le `mWidget_PercentDone` procédure événementielle est exécutée.  
  
 Lorsque `LongTask` est terminé, `mblnCancel` est testé pour voir si `LongTask` s’est terminée normalement, ou si elle s’est arrêté, car `mblnCancel` a été défini sur `True`. Le pourcentage d’achèvement est mis à jour uniquement dans le premier cas.  
  
#### <a name="to-run-the-program"></a>Pour exécuter le programme  
  
1. Appuyez sur F5 pour configurer le projet en mode exécution.  
  
2. Cliquez sur le **démarrer une tâche** bouton. Chaque fois que le `PercentDone` événement est déclenché, l’étiquette est mise à jour avec le pourcentage de la tâche est terminée.  
  
3. Cliquez sur le **Annuler** bouton Arrêter la tâche. Notez que l’apparence de la **Annuler** bouton ne change pas immédiatement lorsque vous cliquez dessus. Le `Click` événement ne peut pas se produire jusqu'à ce que le `My.Application.DoEvents` instruction permet le traitement des événements.  
  
    > [!NOTE]
    >  Le `My.Application.DoEvents` méthode ne traite pas les événements de la même façon que le formulaire. Par exemple, dans cette procédure pas à pas, vous devez cliquer sur le **Annuler** bouton à deux reprises. Pour permettre au formulaire gérer les événements directement, vous pouvez utiliser le multithreading. Pour plus d’informations, consultez [Managed Threading](../../../../standard/threading/index.md).
  
 Il peut s’avérer intéressant d’exécuter le programme en appuyant sur F11 pour parcourir le code une ligne à la fois. Vous pouvez voir clairement comment l’exécution passe `LongTask`et puis repasse brièvement dans `Form1` chaque fois que le `PercentDone` événement est déclenché.  
  
 Que se passerait-il si, alors que l’exécution a été dans le code de `Form1`, le `LongTask` méthode était de nouveau appelée ? Au pire des cas, un débordement de pile peut se produire si `LongTask` appelées chaque fois que l’événement a été déclenché.  
  
 Vous pouvez provoquer la variable `mWidget` pour gérer les événements pour un autre `Widget` objet en assignant une référence au nouveau `Widget` à `mWidget`. En fait, vous pouvez rendre le code dans `Button1_Click` cette opération chaque fois que vous cliquez sur le bouton.  
  
#### <a name="to-handle-events-for-a-different-widget"></a>Pour gérer les événements pour un autre widget  
  
-   Ajoutez la ligne suivante de code pour le `Button1_Click` procédure, juste avant la ligne qui lit `mWidget.LongTask(12.2, 0.33)`:  
  
     [!code-vb[VbVbcnWalkthroughDeclaringAndRaisingEvents#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnWalkthroughDeclaringAndRaisingEvents/VB/Form1.vb#9)]  
  
 Le code ci-dessus crée un nouveau `Widget` chaque fois que le bouton est activé. Dès que le `LongTask` méthode se termine, la référence à la `Widget` est libéré et le `Widget` est détruit.  
  
 A `WithEvents` variable peut contenir uniquement une référence d’objet à la fois, donc si vous affectez une autre `Widget` objet `mWidget`, précédent `Widget` événements de l’objet seront n’est plus gérées. Si `mWidget` est la seule variable objet qui contient une référence à l’ancien `Widget`, l’objet est détruit. Si vous souhaitez gérer les événements à partir de plusieurs `Widget` objets, utilisez la `AddHandler` instruction pour traiter les événements de chaque objet séparément.  
  
> [!NOTE]
>  Vous pouvez déclarer autant `WithEvents` variables en tant que vous avez besoin, mais les tableaux de `WithEvents` variables ne sont pas prises en charge.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure pas à pas : Déclaration et déclenchement des événements](../../../../visual-basic/programming-guide/language-features/events/walkthrough-declaring-and-raising-events.md)
- [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)
