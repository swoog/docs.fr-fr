---
title: 'Procédure : Créer une activité'
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
ms.assetid: c09b1e99-21b5-4d96-9c04-ec31db3f4436
ms.openlocfilehash: 271f26888e8b140b64464f5c9c4eabb7170afe05
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57709014"
---
# <a name="how-to-create-an-activity"></a>Procédure : Créer une activité

Les activités sont l'unité principale de comportement dans [!INCLUDE[wf1](../../../includes/wf1-md.md)]. La logique d'exécution d'une activité peut être implémentée en code managé ou à l'aide d'autres activités. Cette rubrique indique comment créer deux activités. La première activité est une activité simple qui utilise le code pour implémenter la logique d'exécution. L'implémentation de la deuxième activité est définie à l'aide d'autres activités. Ces activités sont utilisées dans les procédures du didacticiel.

> [!NOTE]
> Pour télécharger une version complète du didacticiel, consultez [Windows Workflow Foundation (WF45) - Getting Started Tutorial](https://go.microsoft.com/fwlink/?LinkID=248976)(Windows Workflow Foundation (WF45) - Didacticiel de mise en route).

## <a name="create-the-activity-library-project"></a>Créer le projet de bibliothèque d’activités

1.  Ouvrez Visual Studio et choisissez **New** > **projet** à partir de la **fichier** menu.

2.  Dans le **nouveau projet** boîte de dialogue, sous le **installé** catégorie, sélectionnez **Visual C#** > **Workflow** (ou **Visual Basic** > **Workflow**).

    > [!NOTE]
    > Si vous ne voyez pas le **Workflow** catégorie du modèle, vous devrez peut-être installer le **Windows Workflow Foundation** composant de Visual Studio. Choisissez le **ouvrir Visual Studio Installer** lien sur le côté gauche de la **nouveau projet** boîte de dialogue. Dans le programme d’installation de Visual Studio, sélectionnez le **composants individuels** onglet. Ensuite, sous la **activités de développement** catégorie, sélectionnez le **Windows Workflow Foundation** composant. Choisissez **modifier** pour installer le composant.

3. Sélectionnez le **bibliothèque d’activités** modèle de projet. Type `NumberGuessWorkflowActivities` dans le **nom** , puis cliquez sur **OK**.

4.  Avec le bouton droit **Activity1.xaml** dans **l’Explorateur de solutions** et choisissez **supprimer**. Pour confirmer, cliquez sur **OK** .

## <a name="create-the-readint-activity"></a>Création de l’activité ReadInt

1.  Choisissez **ajouter un nouvel élément** à partir de la **projet** menu.

2.  Dans le **installé** > **éléments communs** nœud, sélectionnez **Workflow**. Sélectionnez **activité de Code** à partir de la **Workflow** liste.

3.  Type `ReadInt` dans le **nom** , puis cliquez sur **ajouter**.

4.  Remplacez la définition `ReadInt` existante par la définition suivante.

     [!code-csharp[CFX_WF_GettingStarted#1](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/readint.cs#1)]
     [!code-vb[CFX_WF_GettingStarted#1](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/readint.vb#1)]

    > [!NOTE]
    > L'activité `ReadInt` dérive de <xref:System.Activities.NativeActivity%601> au lieu de <xref:System.Activities.CodeActivity>, qui est la valeur par défaut pour le modèle d'activité de code. <xref:System.Activities.CodeActivity%601> peut être utilisé si l'activité fournit un résultat unique, exposé via l'argument <xref:System.Activities.Activity%601.Result%2A>, mais <xref:System.Activities.CodeActivity%601> ne prenant pas en charge l'utilisation de signets, <xref:System.Activities.NativeActivity%601> est utilisé.

## <a name="create-the-prompt-activity"></a>Créer l’activité Prompt

1.  Appuyez sur **Ctrl**+**MAJ**+**B** pour générer le projet. La génération du projet permet d'utiliser l'activité `ReadInt` dans ce projet pour générer l'activité personnalisée de cette étape.

2.  Choisissez **ajouter un nouvel élément** à partir de la **projet** menu.

3.  Dans le **installé** > **éléments communs** nœud, sélectionnez **Workflow**. Sélectionnez **activité** à partir de la **Workflow** liste.

4.  Type `Prompt` dans le **nom** , puis cliquez sur **ajouter**.

5.  Double-cliquez sur **Prompt.xaml** dans **l’Explorateur de solutions** à afficher dans le concepteur si elle n’est pas déjà affichée.

6.  Cliquez sur **Arguments** dans la partie inférieure gauche du Concepteur d’activités pour afficher le **Arguments** volet.

7.  Cliquez sur **créer un Argument**.

8.  Type `BookmarkName` dans le **nom** boîte, sélectionnez **dans** à partir de la **Direction** liste déroulante, sélectionnez **chaîne** à partir de la **Type d’argument** liste déroulante, puis appuyez sur **entrée** pour enregistrer l’argument.

9. Cliquez sur **créer un Argument**.

10. Type `Result` dans le **nom** boîte qui se trouve sous récemment ajouté `BookmarkName` argument, sélectionnez **Out** à partir de la **Direction** liste déroulante, sélectionnez **Int32** à partir de la **type d’Argument** liste déroulante, puis appuyez sur **entrée**.

11. Cliquez sur **créer un Argument**.

12. Type `Text` dans le **nom** boîte, sélectionnez **dans** à partir de la **Direction** liste déroulante, sélectionnez **chaîne** à partir de la **Type d’argument** liste déroulante, puis appuyez sur **entrée** pour enregistrer l’argument.

     Ces trois arguments sont liés aux arguments correspondants des activités <xref:System.Activities.Statements.WriteLine> et `ReadInt` ajoutées à l'activité `Prompt` dans les étapes suivantes.

13. Cliquez sur **Arguments** dans la partie inférieure gauche du Concepteur d’activités pour fermer la **Arguments** volet.

14. Faites glisser un **séquence** activité à partir de la **flux de contrôle** section de la **boîte à outils** et déposez-le sur le **déposer l’activité ici** étiquette de la **Invite** Concepteur d’activités.

    > [!TIP]
    > Si le **boîte à outils** fenêtre n’est pas affichée, sélectionnez **boîte à outils** à partir de la **vue** menu.

15. Faites glisser un **WriteLine** activité à partir de la **Primitives** section de la **boîte à outils** et déposez-le sur le **déposer l’activité ici** étiquette de la **Séquence** activité.

16. Lier le **texte** argument de la **WriteLine** activité à la **texte** argument de la **invite** activité en tapant `Text` dans le **entrer une expression c#** ou **entrer une expression VB** zone le **propriétés** fenêtre et appuyez sur la **onglet** clé de deux fois. Cela ferme la fenêtre de liste des membres IntelliSense et enregistre la valeur de propriété en déplaçant la sélection en dehors de la propriété. Cette propriété peut également être définie en tapant `Text` dans le **entrer une expression c#** ou **entrer une expression VB** boîte sur l’activité elle-même.

    > [!TIP]
    > Si le **fenêtre Propriétés** n’est pas affiché, sélectionnez **fenêtre Propriétés** à partir de la **vue** menu.

17. Faites glisser un **ReadInt** activité à partir de la **NumberGuessWorkflowActivities** section de la **boîte à outils** et déposez-le dans la **séquence** activité afin qu’elle suive le **WriteLine** activité.

18. Lier le **BookmarkName** argument de la **ReadInt** activité à la **BookmarkName** argument de la **invite** activité en tapant `BookmarkName` dans le **entrer une expression VB** zone à droite de la **BookmarkName** argument dans le **fenêtre Propriétés**, puis appuyez sur la **Onglet** deux reprises pour fermer la fenêtre de membres de liste IntelliSense et enregistrer la propriété de clé.

19. Lier le **résultat** argument de la **ReadInt** activité à la **résultat** argument de la **invite** activité en tapant `Result` dans le **entrer une expression VB** zone à droite de la **résultat** argument dans le **fenêtre Propriétés**, puis appuyez sur la **onglet** deux fois la clé.

20. Appuyez sur **Ctrl**+**MAJ**+**B** pour générer la solution.

## <a name="next-steps"></a>Étapes suivantes

Pour obtenir des instructions sur la création d’un flux de travail à l’aide de ces activités, consultez l’étape suivante du didacticiel, [Comment : Créer un flux de travail](how-to-create-a-workflow.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Activities.CodeActivity>
- <xref:System.Activities.NativeActivity%601>
- [Conception et implémentation d’activités personnalisées](designing-and-implementing-custom-activities.md)
- [Didacticiel Bien démarrer](getting-started-tutorial.md)
- [Guide pratique pour Créer un flux de travail](how-to-create-a-workflow.md)
- [Utilisation d’ExpressionTextBox dans un concepteur d’activités personnalisées](./samples/using-the-expressiontextbox-in-a-custom-activity-designer.md)