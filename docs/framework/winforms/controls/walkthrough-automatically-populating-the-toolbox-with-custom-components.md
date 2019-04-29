---
title: 'Procédure pas à pas : remplissage automatique de la boîte à outils avec des composants personnalisés'
ms.date: 03/30/2017
helpviewer_keywords:
- IToolboxService interface
- Toolbox [Windows Forms], populating
- custom components [Windows Forms], adding to Toolbox
ms.assetid: 2fa1e3e8-6b9f-42b2-97c0-2be57444dba4
ms.openlocfilehash: 6ecf69350b8337dc6049b73251809192b47dc2fb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61759906"
---
# <a name="walkthrough-automatically-populating-the-toolbox-with-custom-components"></a>Procédure pas à pas : remplissage automatique de la boîte à outils avec des composants personnalisés
Si vos composants sont définis par un projet dans la solution actuellement ouverte, ils apparaissent automatiquement dans le **boîte à outils**, sans qu’aucune action requise par vous. Vous pouvez également remplir manuellement la **boîte à outils** avec vos composants personnalisés à l’aide de la [boîte à outils éléments de boîte de dialogue Choisir (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100)), mais la **boîte à outils** tient compte d’éléments dans de votre solution générer les sorties avec toutes les caractéristiques suivantes :  
  
- Implémente <xref:System.ComponentModel.IComponent>;  
  
- N’a pas <xref:System.ComponentModel.ToolboxItemAttribute> définie sur `false`;  
  
- N’a pas <xref:System.ComponentModel.DesignTimeVisibleAttribute> défini sur `false`.  
  
> [!NOTE]
>  Le **boîte à outils** ne suit pas les chaînes de référence, il n’affichera pas les éléments qui ne sont pas générés par un projet dans votre solution.  
  
 Cette procédure pas à pas montre comment un composant personnalisé apparaît automatiquement dans le **boîte à outils** une fois que le composant est généré. Cette procédure pas à pas décrit notamment les tâches suivantes :  
  
- Création d’un projet Windows Forms.  
  
- Création d’un composant personnalisé.  
  
- Création d’une instance d’un composant personnalisé.  
  
- Déchargement et rechargement d’un composant personnalisé.  
  
 Lorsque vous avez terminé, vous verrez que le **boîte à outils** est remplie avec un composant que vous avez créé.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
## <a name="creating-the-project"></a>Création du projet  
 La première étape consiste à créer le projet et à configurer le formulaire.  
  
#### <a name="to-create-the-project"></a>Pour créer le projet  
  
1. Créer un projet d’application Windows appelé `ToolboxExample` (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).  
  
2. Ajouter un nouveau composant au projet. Appelez-le `DemoComponent`.  
  
     Pour plus d'informations, voir [Procédure : Ajouter de nouveaux éléments de projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).  
  
3. Générez le projet.  
  
4. À partir de la **outils** menu, cliquez sur le **Options** élément. Cliquez sur **général** sous le **Windows Forms Designer** d’élément et vérifiez que le **AutoToolboxPopulate a** option est définie sur **True**.  
  
## <a name="creating-an-instance-of-a-custom-component"></a>Création d’une Instance d’un composant personnalisé  
 L’étape suivante consiste à créer une instance du composant personnalisé sur le formulaire. Étant donné que le **boîte à outils** automatiquement des comptes pour le nouveau composant, il s’agit aussi simple que la création de tout autre composant ou contrôle.  
  
#### <a name="to-create-an-instance-of-a-custom-component"></a>Pour créer une instance d’un composant personnalisé  
  
1. Ouvrez le formulaire du projet dans le **Concepteur Forms**.  
  
2. Dans le **boîte à outils**, cliquez sur le nouvel onglet appelé **Composants ToolboxExample**.  
  
     Une fois que vous cliquez sur l’onglet, vous verrez **DemoComponent**.  
  
    > [!NOTE]
    >  Pour des raisons de performances, les composants dans la zone rempli automatiquement de la **boîte à outils** n’affichent pas de bitmaps personnalisées et le <xref:System.Drawing.ToolboxBitmapAttribute> n’est pas pris en charge. Pour afficher une icône pour un composant personnalisé dans le **boîte à outils**, utilisez le **Choose Toolbox Items** boîte de dialogue charger votre composant.  
  
3. Faites glisser votre composant sur votre formulaire.  
  
     Une instance du composant est créée et ajoutée à la **barre d’état du composant**.  
  
## <a name="unloading-and-reloading-a-custom-component"></a>Déchargement et rechargement d’un composant personnalisé  
 Le **boîte à outils** compte des composants dans chaque chargé de projet, et lorsqu’un projet est déchargé, elle supprime les références aux composants du projet.  
  
#### <a name="to-experiment-with-the-effect-on-the-toolbox-of-unloading-and-reloading-components"></a>Pour tester l’effet sur la boîte à outils de déchargement et rechargement des composants  
  
1. Décharger le projet à partir de la solution.  
  
     Pour plus d’informations sur le déchargement de projets, consultez [Comment : Décharger et recharger des projets](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/tt479x1t(v=vs.100)). Si vous êtes invité à enregistrer, choisissez **Oui**.  
  
2. Ajouter un nouveau **Windows Application** projet à la solution. Ouvrez le formulaire dans le **concepteur**.  
  
     Le **Composants ToolboxExample** onglet à partir du projet précédent est désormais disparu.  
  
3. Recharger la `ToolboxExample` projet.  
  
     Le **Composants ToolboxExample** onglet maintenant s’affiche de nouveau.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Cette procédure pas à pas montre que la **boîte à outils** tient compte des composants d’un projet, mais la **boîte à outils** tient également compte des contrôles. Faites des essais avec vos propres contrôles personnalisés en ajoutant et supprimant des projets de contrôle à partir de votre solution.  
  
## <a name="see-also"></a>Voir aussi

- [Général, le Concepteur Windows Forms, boîte de dialogue Options](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/5aazxs78(v=vs.100))
- [Guide pratique pour Manipuler des onglets de boîte à outils](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/66kwe227(v=vs.100))
- [Choisir des éléments de boîte à outils, boîte de dialogue (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))
- [Placement de contrôles dans les Windows Forms](putting-controls-on-windows-forms.md)
