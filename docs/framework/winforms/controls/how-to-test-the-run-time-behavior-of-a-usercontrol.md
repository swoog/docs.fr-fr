---
title: 'Procédure : Tester le comportement au moment de l’exécution d’un UserControl'
ms.date: 03/30/2017
helpviewer_keywords:
- UserControl class [Windows Forms], testing
- user controls [Windows Forms], testing
- composite controls [Windows Forms], testing
- UserControl Test Container
- UserControl class [Windows Forms], run-time behavior
ms.assetid: 4e4d5c49-1346-40ac-9d96-40211b573583
ms.openlocfilehash: 0b87034487ef0f2cabed786354682f394500cafc
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707883"
---
# <a name="how-to-test-the-run-time-behavior-of-a-usercontrol"></a>Procédure : Tester le comportement au moment de l’exécution d’un UserControl
Lorsque vous développez un <xref:System.Windows.Forms.UserControl>, vous devez tester son comportement au moment de l’exécution. Vous pouvez créer un projet d’application Windows séparé et placer votre contrôle sur un formulaire de test, mais cette procédure n’est pas pratique. Un moyen plus rapide et plus facile consiste à utiliser le **conteneur de Test UserControl** fournis par Visual Studio. Ce conteneur de test démarre directement à partir de votre projet de bibliothèque de contrôles Windows.  
  
> [!IMPORTANT]
>  Le conteneur de test charger votre <xref:System.Windows.Forms.UserControl>, le contrôle doit avoir au moins un constructeur public.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
> [!NOTE]
>  Un contrôle Visual C++ ne peuvent pas être testé à l’aide de la **conteneur de Test UserControl**.  
  
### <a name="to-test-the-run-time-behavior-of-a-usercontrol"></a>Pour tester le comportement au moment de l’exécution d’un UserControl  
  
1.  Créer un projet de bibliothèque de contrôles Windows appelé **TestContainerExample**. Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).  
  
2.  Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.Label> contrôle depuis la **boîte à outils** aire de conception du contrôle.  
  
3.  Appuyez sur F5 pour générer le projet et exécuter le **conteneur de Test UserControl**. Le conteneur de test s’affiche avec votre <xref:System.Windows.Forms.UserControl> dans le **aperçu** volet.  
  
4.  Sélectionnez le <xref:System.Windows.Forms.Control.BackColor%2A> propriété affichée dans le <xref:System.Windows.Forms.PropertyGrid> contrôle situé à droite de la **aperçu** volet. Modifiez sa valeur en `ControlDark`. Observez que le contrôle passe à une couleur plus sombre. Essayez de modifier d’autres valeurs de propriété et observer l’effet sur votre contrôle.  
  
5.  Cliquez sur le **ancrer le contrôle utilisateur remplir** case à cocher ci-dessous le **aperçu** volet. Observez que le contrôle est redimensionné pour remplir le volet. Redimensionner le conteneur de test et observez que le contrôle est redimensionné avec le volet.  
  
6.  Fermez le conteneur de test.  
  
7.  Ajoutez un autre contrôle utilisateur à la **TestContainerExample** projet. Pour plus d’informations, consultez [Guide pratique pour Ajouter des éléments existants à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).  
  
8.  Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.Button> contrôle depuis la **boîte à outils** aire de conception du contrôle.  
  
9. Appuyez sur F5 pour générer le projet et exécuter le conteneur de test.  
  
10. Cliquez sur le **sélectionner un contrôle utilisateur** <xref:System.Windows.Forms.ComboBox> pour basculer entre les deux contrôles utilisateur.  
  
## <a name="testing-user-controls-from-another-project"></a>Test des contrôles utilisateur à partir d’un autre projet  
 Vous pouvez tester les contrôles utilisateur à partir d’autres projets dans le conteneur de test de votre projet actuel.  
  
#### <a name="to-test-user-controls-from-another-project"></a>Pour tester les contrôles utilisateur à partir d’un autre projet  
  
1.  Créer un projet de bibliothèque de contrôles Windows appelé **TestContainerExample2**. Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).  
  
2.  Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.RadioButton> contrôle depuis la **boîte à outils** aire de conception du contrôle.  
  
3.  Appuyez sur F5 pour générer le projet et exécuter le conteneur de test. Le conteneur de test s’affiche avec votre <xref:System.Windows.Forms.UserControl> dans le **aperçu** volet.  
  
4.  Cliquez sur le **charge** bouton.  
  
5.  Dans le **Open** boîte de dialogue, accédez à **TestContainerExample**.dll que vous avez créé dans la procédure précédente. Sélectionnez **TestContainerExample**.dll et cliquez sur le **Open** bouton pour charger les contrôles utilisateur  
  
6.  Utilisez le **sélectionner un contrôle utilisateur** <xref:System.Windows.Forms.ComboBox> pour basculer entre les deux contrôles utilisateur à partir de la **TestContainerExample** projet.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.UserControl>
- [Guide pratique pour Créer des contrôles composites](how-to-author-composite-controls.md)
- [Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic](walkthrough-authoring-a-composite-control-with-visual-basic.md)
- [Procédure pas à pas : Création d’un contrôle Composite avec VisualC#](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- [Concepteur de contrôles utilisateur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))
