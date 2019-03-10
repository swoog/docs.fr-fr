---
title: 'Procédure pas à pas : Création d’une Interface de Style Explorateur avec les contrôles TreeView à l’aide du Concepteur de ListView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Explorer-style applications [Windows Forms], walkthroughs
- TreeView control [Windows Forms], ListView controls used with
- ListView control [Windows Forms], TreeView controls used with
- Explorer-style applications
- TreeView control [Windows Forms], using for explorer-style interface
- ListView control [Windows Forms], explorer style interface
- ListView control [Windows Forms], explorer-style interface
ms.assetid: 9e5e7721-19e2-4890-b273-a43589fe99ff
ms.openlocfilehash: a849eae086c3507bbaf7050afd2e0496ab5a970e
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716979"
---
# <a name="walkthrough-creating-an-explorer-style-interface-with-the-listview-and-treeview-controls-using-the-designer"></a>Procédure pas à pas : Création d’une Interface de Style Explorateur avec les contrôles TreeView à l’aide du Concepteur de ListView
Un des avantages de Visual Studio est la capacité de créer des applications Windows Forms de qualité professionnelle en un court laps de temps. Un scénario courant est création d’une interface utilisateur (IU) avec <xref:System.Windows.Forms.ListView> et <xref:System.Windows.Forms.TreeView> contrôles qui ressemble à la fonctionnalité de l’Explorateur Windows des systèmes d’exploitation de Windows. L’Explorateur Windows affiche une structure hiérarchique des fichiers et dossiers sur l’ordinateur d’un utilisateur.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-the-form-containing-a-listview-and-treeview-control"></a>Pour créer le formulaire contenant un contrôle ListView et TreeView  
  
1.  Dans le menu **Fichier** , pointez sur **Nouveau**, puis cliquez sur **Projet**.  
  
2.  Dans le **nouveau projet** boîte de dialogue zone, procédez comme suit :  
  
    1.  Dans les catégories, choisissez **Visual Basic** ou **Visual C#**.  
  
    2.  Dans la liste des modèles, choisissez **Windows Forms Application**.  
  
3.  Cliquez sur **OK**. Un nouveau projet Windows Forms est créé.  
  
4.  Ajouter un <xref:System.Windows.Forms.SplitContainer> au formulaire et définissez son <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>.  
  
5.  Ajouter un <xref:System.Windows.Forms.ImageList> nommé `imageList1` au formulaire et utilisez la fenêtre Propriétés pour ajouter deux images : une image de dossier et une image de document, dans cet ordre.  
  
6.  Ajouter un <xref:System.Windows.Forms.TreeView> contrôle nommé `treeview1` au formulaire et placez-le sur le côté gauche de la <xref:System.Windows.Forms.SplitContainer> contrôle. Dans la fenêtre Propriétés pour `treeView1` procédez comme suit :  
  
    1.  Affectez à la propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.  
  
    2.  Affectez à la propriété <xref:System.Windows.Forms.TreeView.ImageList%2A> la valeur `imagelist1.`  
  
7.  Ajouter un <xref:System.Windows.Forms.ListView> contrôle nommé `listView1` au formulaire et le positionner sur le côté droit de la <xref:System.Windows.Forms.SplitContainer> contrôle. Dans la fenêtre Propriétés pour `listview1` procédez comme suit :  
  
    1.  Affectez à la propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.  
  
    2.  Affectez à la propriété <xref:System.Windows.Forms.ListView.View%2A> la valeur <xref:System.Windows.Forms.View.Details>.  
  
    3.  Ouvrez l’éditeur de collections ColumnHeader en cliquant sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) dans le <xref:System.Windows.Forms.ListView.Columns%2A> propriété **.** Ajoutez trois colonnes et définissez leurs <xref:System.Windows.Forms.ColumnHeader.Text%2A> propriété `Name`, `Type`, et `Last Modified`, respectivement. Cliquez sur **OK** pour fermer la boîte de dialogue.  
  
    4.  Affectez à la propriété <xref:System.Windows.Forms.ListView.SmallImageList%2A> la valeur `imageList1.`  
  
8.  Implémentez le code pour remplir la <xref:System.Windows.Forms.TreeView> avec les nœuds et les sous-nœuds. Ajoutez ce code à la `Form1` classe.  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#1)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#1)]  
  
9. Étant donné que le code précédent utilise l’espace de noms System.IO, ajoutez l’utilisation appropriée ou importer l’instruction en haut du formulaire.  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#4)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#4)]  
  
10. Appelez la méthode de configuration de l’étape précédente dans le constructeur du formulaire ou <xref:System.Windows.Forms.Form.Load> méthode de gestion des événements. Ajoutez ce code au constructeur de formulaire.  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#2)]  
  
11. Gérer le <xref:System.Windows.Forms.TreeView.NodeMouseClick> événement pour `treeview1` **,** et implémentez le code pour remplir `listview1` avec le contenu d’un nœud lorsque l’utilisateur clique sur un nœud. Ajoutez ce code à la `Form1` classe.  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#3)]  
  
     Si vous utilisez c#, assurez-vous d’avoir le <xref:System.Windows.Forms.TreeView.NodeMouseClick> événement associé à sa méthode de gestion des événements. Ajoutez ce code au constructeur de formulaire.  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#5)]  
  
## <a name="testing-the-application"></a>Test de l'application  
 Vous pouvez maintenant tester le formulaire pour vous assurer qu’il se comporte comme prévu.  
  
#### <a name="to-test-the-form"></a>Pour tester le formulaire  
  
-   Appuyez sur F5 pour exécuter l'application.  
  
     Vous verrez un formulaire de fractionnement contenant un <xref:System.Windows.Forms.TreeView> contrôle qui affiche votre répertoire de projet sur le côté gauche, et un <xref:System.Windows.Forms.ListView> contrôle sur le côté droit avec trois colonnes. Vous pouvez parcourir le <xref:System.Windows.Forms.TreeView> en sélectionnant des nœuds de répertoire et le <xref:System.Windows.Forms.ListView> est rempli avec le contenu du répertoire sélectionné.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Cette application vous donne un exemple de la façon dont vous pouvez utiliser <xref:System.Windows.Forms.TreeView> et <xref:System.Windows.Forms.ListView> ensemble les contrôles. Pour plus d’informations sur ces contrôles, consultez les rubriques suivantes :  
  
-   [Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)  
  
-   [Guide pratique pour Ajouter des fonctionnalités de recherche à un contrôle ListView](how-to-add-search-capabilities-to-a-listview-control.md)  
  
-   [Guide pratique pour Attacher un Menu contextuel à un nœud TreeView](how-to-attach-a-shortcut-menu-to-a-treeview-node.md)  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.TreeView>
- [Contrôle ListView](listview-control-windows-forms.md)
- [Guide pratique pour Ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms](how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control.md)
- [Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
