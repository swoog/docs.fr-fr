---
title: 'Procédure : créer des listes maître/détails avec le contrôle DataGrid Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- master-details lists
- DataGrid control [Windows Forms], master-details lists
- related tables [Windows Forms], displaying in DataGrid control
ms.assetid: 19438ba2-f687-4417-a2fb-ab1cd69d4ded
ms.openlocfilehash: f586572c850927ffe71566287986e6db6112c689
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61961358"
---
# <a name="how-to-create-master-details-lists-with-the-windows-forms-datagrid-control-using-the-designer"></a>Procédure : créer des listes maître/détails avec le contrôle DataGrid Windows Forms à l’aide du concepteur

> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Si votre <xref:System.Data.DataSet> contient une série de tables associées, vous pouvez utiliser deux <xref:System.Windows.Forms.DataGrid> contrôles pour afficher les données dans un format maître-détail. Un <xref:System.Windows.Forms.DataGrid> est désigné comme étant la grille principale, et la seconde peut être désignée comme la grille de détails. Lorsque vous sélectionnez une entrée dans la liste principale, toutes les entrées enfants connexes s’affichent dans la liste des détails. Par exemple, si votre <xref:System.Data.DataSet> contient une table Customers et une table connexe Orders, vous devez spécifier la table Customers pour la grille principale et la table Orders pour la grille de détails. Lorsqu’un client est sélectionné dans la grille principale, toutes les commandes associées à ce client dans la table Orders seraient affiché dans la grille de détails.  
  
 La procédure suivante nécessite un **Windows Application** projet (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-a-master-details-list-in-the-designer"></a>Pour créer une liste maître / détails dans le Concepteur  
  
1. Ajoutez deux <xref:System.Windows.Forms.DataGrid> contrôles au formulaire. Pour plus d'informations, voir [Procédure : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md). Dans Visual Studio 2005, le <xref:System.Windows.Forms.DataGrid> contrôle n’est pas dans le **boîte à outils** par défaut. Pour plus d'informations, voir [Procédure : Ajouter des éléments à la boîte à outils](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms165355(v=vs.100)).  
  
    > [!NOTE]
    >  Les étapes suivantes ne sont pas applicables à Visual Studio 2005, qui utilise le **des Sources de données** fenêtre pour la liaison de données au moment du design. Pour plus d’informations, consultez [lier des contrôles aux données dans Visual Studio](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio) et [Comment : Affichage liées à des données dans un Windows Forms Application](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/57tx3hhe(v=vs.120)).  
  
2. Faites glisser deux ou plusieurs tables à partir de **Explorateur de serveurs** au formulaire.  
  
3. À partir de la **données** menu, sélectionnez **générer le DataSet**.  
  
4. Définir les relations entre les tables à l’aide du Concepteur XML. Pour plus d’informations, consultez « Comment : Créer des relations un-à-plusieurs dans les schémas XML et des jeux de données » sur MSDN.  
  
5. Enregistrez les relations en sélectionnant **Enregistrer tout** à partir de la **fichier** menu.  
  
6. Configurer le <xref:System.Windows.Forms.DataGrid> contrôle que vous souhaitez désigner comme grille principale, comme suit :  
  
    1. Sélectionnez le <xref:System.Data.DataSet> dans la liste déroulante dans le <xref:System.Windows.Forms.DataGrid.DataSource%2A> propriété.  
  
    2. Sélectionnez la table principale (par exemple, « Customers ») dans la liste déroulante dans le <xref:System.Windows.Forms.DataGrid.DataMember%2A> propriété.  
  
7. Configurer le <xref:System.Windows.Forms.DataGrid> contrôle que vous souhaitez désigner la grille des détails, comme suit :  
  
    1. Sélectionnez le <xref:System.Data.DataSet> dans la liste déroulante dans le <xref:System.Windows.Forms.DataGrid.DataSource%2A> propriété.  
  
    2. Sélectionnez la relation (par exemple, « Customers.CustOrd ») entre les tables maître / détail dans la liste déroulante dans le <xref:System.Windows.Forms.DataGrid.DataMember%2A> propriété. Pour voir la relation, développez le nœud en cliquant sur le signe plus (**+**) en regard de la table principale dans la liste déroulante.  
  
## <a name="see-also"></a>Voir aussi

- [DataGrid, contrôle](datagrid-control-windows-forms.md)
- [Vue d’ensemble du contrôle DataGrid](datagrid-control-overview-windows-forms.md)
- [Guide pratique pour Lier le contrôle DataGrid Windows Forms à une Source de données](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md)
- [Lier des contrôles à des données dans Visual Studio](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)
