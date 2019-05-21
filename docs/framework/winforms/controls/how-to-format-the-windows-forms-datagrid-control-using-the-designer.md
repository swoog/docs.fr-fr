---
title: 'Procédure : mettre en forme le contrôle DataGrid Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- columns [Windows Forms], DataGrid controls
- colors [Windows Forms], applying to DataGrid controls
- DataGrid control [Windows Forms], formatting
- DataGrid control [Windows Forms], default styles
- tables [Windows Forms], formatting in DataGrid control
- formatting [Windows Forms]
ms.assetid: 533b9814-6124-49dc-9fda-085f1502609f
ms.openlocfilehash: 1cdafa14d5b25d6cef92a48e4f460975a2076303
ms.sourcegitcommit: ffd7dd79468a81bbb0d6449f6d65513e050c04c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2019
ms.locfileid: "65960194"
---
# <a name="how-to-format-the-windows-forms-datagrid-control-using-the-designer"></a>Procédure : mettre en forme le contrôle DataGrid Windows Forms à l’aide du concepteur

> [!NOTE]
> Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).

Appliquant différentes couleurs aux différentes parties d’un <xref:System.Windows.Forms.DataGrid> contrôle peut contribuer aux informations qu’il contient plus facile à lire et à interpréter. Couleur peut être appliquée aux lignes et colonnes. Lignes et colonnes peuvent également être masquées ou affichées à votre entière discrétion.

Il existe trois aspects essentiels de la mise en forme le <xref:System.Windows.Forms.DataGrid> contrôle :

- Vous pouvez définir des propriétés pour établir un style par défaut dans lequel les données sont affichées.

- À partir de cette base, vous pouvez ensuite personnaliser la façon de que certaines tables sont affichées au moment de l’exécution.

- Enfin, vous pouvez modifier les colonnes qui sont affichées dans la grille de données, ainsi que les couleurs et autres mises en forme qui s’affiche.

Comme étape initiale de mise en forme d’une grille de données, vous pouvez définir les propriétés de la <xref:System.Windows.Forms.DataGrid> lui-même. Ces choix de couleur et format forme une base à partir de laquelle vous pouvez ensuite modifier selon les tables et les colonnes affichées.

La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGrid> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md). Dans Visual Studio 2005, le <xref:System.Windows.Forms.DataGrid> contrôle n’est pas dans le **boîte à outils** par défaut. Pour plus d'informations, voir [Procédure : Ajouter des éléments à la boîte à outils](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms165355(v=vs.100)).

> [!NOTE]
> Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).

### <a name="to-establish-a-default-style-for-the-datagrid-control"></a>Pour établir un style par défaut pour le contrôle DataGrid

1. Sélectionnez le contrôle <xref:System.Windows.Forms.DataGrid>.

2. Dans le **propriétés** fenêtre, définissez les propriétés suivantes, comme il convient.

    |Propriété|Description|
    |--------------|-----------------|
    |<xref:System.Windows.Forms.DataGrid.AlternatingBackColor%2A>|Le `BackColor` propriété définit la couleur des lignes paires de la grille. Lorsque vous définissez le <xref:System.Windows.Forms.DataGrid.AlternatingBackColor%2A> propriété sur une couleur différente, toutes les autres lignes est définie sur cette nouvelle couleur (lignes 1, 3, 5 et ainsi de suite).|
    |<xref:System.Windows.Forms.DataGrid.BackColor%2A>|La couleur d’arrière-plan des lignes paires de la grille (lignes 0, 2, 4, 6 et ainsi de suite).|
    |<xref:System.Windows.Forms.DataGrid.BackgroundColor%2A>|Tandis que le <xref:System.Windows.Forms.DataGrid.BackColor%2A> et <xref:System.Windows.Forms.DataGrid.AlternatingBackColor%2A> propriétés détermine la couleur des lignes dans la grille, le <xref:System.Windows.Forms.DataGrid.BackgroundColor%2A> propriété détermine la couleur de la zone en dehors de la zone de lignes, qui est uniquement visible lorsque vous faites défiler la grille vers le bas, ou si seules quelques lignes sont figurant dans la grille.|
    |<xref:System.Windows.Forms.DataGrid.BorderStyle%2A>|Style de bordure de la grille, parmi les <xref:System.Windows.Forms.BorderStyle> valeurs d’énumération.|
    |<xref:System.Windows.Forms.DataGrid.CaptionBackColor%2A>|La couleur d’arrière-plan de légende de la fenêtre de la grille qui s’affiche juste au-dessus de la grille.|
    |<xref:System.Windows.Forms.DataGrid.CaptionFont%2A>|La police de la légende en haut de la grille.|
    |<xref:System.Windows.Forms.DataGrid.CaptionForeColor%2A>|La couleur d’arrière-plan de légende de la fenêtre de la grille.|
    |<xref:System.Windows.Forms.Control.Font%2A>|La police utilisée pour afficher le texte dans la grille.|
    |<xref:System.Windows.Forms.DataGrid.ForeColor%2A>|La couleur de la police affichée par les données dans les lignes de la grille de données.|
    |<xref:System.Windows.Forms.DataGrid.GridLineColor%2A>|La couleur du quadrillage de la grille de données.|
    |<xref:System.Windows.Forms.DataGrid.GridLineStyle%2A>|Le style des lignes séparant les cellules de la grille, parmi les <xref:System.Windows.Forms.DataGridLineStyle> valeurs d’énumération.|
    |<xref:System.Windows.Forms.DataGrid.HeaderBackColor%2A>|La couleur d’arrière-plan des en-têtes de ligne et colonne.|
    |<xref:System.Windows.Forms.DataGrid.HeaderFont%2A>|La police utilisée pour les en-têtes de colonne.|
    |<xref:System.Windows.Forms.DataGrid.HeaderForeColor%2A>|La couleur de premier plan des en-têtes de colonnes de la grille, y compris le texte d’en-tête de colonne et le signe plus (+) et le signe moins (-) glyphes que développer et réduire les lignes lorsque plusieurs tables connexes sont affichés.|
    |<xref:System.Windows.Forms.DataGrid.LinkColor%2A>|La couleur du texte de tous les liens dans la grille de données, notamment des liens vers les tables enfants, le nom de la relation et ainsi de suite.|
    |<xref:System.Windows.Forms.DataGrid.ParentRowsBackColor%2A>|Dans une table enfant, il s’agit de la couleur d’arrière-plan des lignes parentes.|
    |<xref:System.Windows.Forms.DataGrid.ParentRowsForeColor%2A>|Dans une table enfant, il s’agit de la couleur de premier plan des lignes parentes.|
    |<xref:System.Windows.Forms.DataGrid.ParentRowsLabelStyle%2A>|Détermine si les noms de table et de colonne sont affichées dans la ligne parente, par le biais de la <xref:System.Windows.Forms.DataGridParentRowsLabelStyle> énumération.|
    |<xref:System.Windows.Forms.DataGrid.PreferredColumnWidth%2A>|Largeur par défaut (en pixels) des colonnes de la grille. Définissez cette propriété avant de réinitialiser le <xref:System.Windows.Forms.DataGrid.DataSource%2A> et <xref:System.Windows.Forms.DataGrid.DataMember%2A> propriétés (soit séparément, ou via le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> méthode), ou la propriété n’a aucun effet.<br /><br /> La propriété ne peut pas être définie sur une valeur inférieure à 0.|
    |<xref:System.Windows.Forms.DataGrid.PreferredRowHeight%2A>|La hauteur de ligne (en pixels) de lignes dans la grille. Définissez cette propriété avant de réinitialiser le <xref:System.Windows.Forms.DataGrid.DataSource%2A> et <xref:System.Windows.Forms.DataGrid.DataMember%2A> propriétés (soit séparément, ou via le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> méthode), ou la propriété n’a aucun effet.<br /><br /> La propriété ne peut pas être définie sur une valeur inférieure à 0.|
    |<xref:System.Windows.Forms.DataGrid.RowHeaderWidth%2A>|La largeur des en-têtes de lignes de la grille.|
    |<xref:System.Windows.Forms.DataGrid.SelectionBackColor%2A>|Lorsqu’une ligne ou une cellule est sélectionnée, il s’agit de la couleur d’arrière-plan.|
    |<xref:System.Windows.Forms.DataGrid.SelectionForeColor%2A>|Lorsqu’une ligne ou une cellule est sélectionnée, il s’agit de la couleur de premier plan.|

    > [!NOTE]
    > Lorsque vous personnalisez les couleurs des contrôles, il est possible de rendre le contrôle inaccessible en raison du choix d’une mauvaise couleur (par exemple, rouge et vert). Utiliser les couleurs disponibles sur le **couleurs système** palette pour éviter ce problème.

    La procédure suivante nécessite un <xref:System.Windows.Forms.DataGrid> contrôle lié à une table de données. Pour plus d'informations, voir [Procédure : Lier le contrôle DataGrid Windows Forms à une Source de données](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md).

### <a name="to-set-the-table-and-column-style-of-a-data-table-at-design-time"></a>Pour définir le style de table et de colonne d’une table de données au moment du design

1. Sélectionnez le <xref:System.Windows.Forms.DataGrid> contrôle sur votre formulaire.

2. Dans le **propriétés** fenêtre, sélectionnez le <xref:System.Windows.Forms.DataGrid.TableStyles%2A> propriété et cliquez sur le **points de suspension** (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) bouton.

3. Dans le **éditeur de collections DataGridTableStyle** boîte de dialogue, cliquez sur **ajouter** pour ajouter un style de table à la collection.

     Avec le **éditeur de collections DataGridTableStyle**, vous pouvez ajouter et supprimer les styles de table, définir l’affichage des propriétés de disposition et des ensemble le mappage de noms pour les styles de table.

4. Définir le <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> propriété le nom de mappage pour chaque style de table.

     Le nom de mappage est utilisé pour spécifier le style de tableau doit être utilisé avec quelle table.

5. Dans le **éditeur de collections DataGridTableStyle**, sélectionnez le <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A> propriété et cliquez sur le bouton de sélection (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)).

6. Dans le **éditeur de collections DataGridColumnStyle** boîte de dialogue zone, ajouter des styles de colonne pour le style de table que vous avez créé.

     Avec le **éditeur de collections DataGridColumnStyle**, vous pouvez ajouter et supprimer des styles de colonne, définir les propriétés d’affichage et la disposition et définissez le nom de mappage et les chaînes de mise en forme des colonnes de données.

    > [!NOTE]
    > Pour plus d’informations sur la mise en forme de chaînes, consultez [mise en forme des Types](../../../standard/base-types/formatting-types.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.GridTableStylesCollection>
- <xref:System.Windows.Forms.GridColumnStylesCollection>
- <xref:System.Windows.Forms.DataGrid>
- [Guide pratique pour Supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms](how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control.md)
- [DataGrid, contrôle](datagrid-control-windows-forms.md)
