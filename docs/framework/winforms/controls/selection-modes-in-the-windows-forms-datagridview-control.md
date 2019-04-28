---
title: Modes de sélection dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- selection [Windows Forms], modes in DataGridView control
- DataGridView control [Windows Forms], selection mode
ms.assetid: a3ebfd3d-0525-479d-9d96-d9e017289b36
ms.openlocfilehash: 79e13e65938252015e43b59a962d40f20963a5df
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61902666"
---
# <a name="selection-modes-in-the-windows-forms-datagridview-control"></a>Modes de sélection dans le contrôle DataGridView Windows Forms
Parfois vous souhaitez que votre application pour effectuer des actions en fonction des sélections d’utilisateur dans un <xref:System.Windows.Forms.DataGridView> contrôle. Selon les actions, vous voudrez limiter les types de sélection qui ne sont possibles. Par exemple, supposons que votre application peut imprimer un rapport pour l’enregistrement actuellement sélectionné. Dans ce cas, vous souhaitez configurer le <xref:System.Windows.Forms.DataGridView> contrôle afin que toujours de cliquer n’importe où dans une ligne sélectionne la ligne entière, et par conséquent, ce qu’une seule ligne à la fois peut être sélectionnée.  
  
 Vous pouvez spécifier les sélections autorisées en définissant le <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType> propriété à une des opérations suivantes <xref:System.Windows.Forms.DataGridViewSelectionMode> valeurs d’énumération.  
  
|DataGridViewSelectionMode value|Description|  
|-------------------------------------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewSelectionMode.CellSelect>|En cliquant sur une cellule sélectionne. En-têtes de ligne et de colonne ne peut pas être utilisés pour la sélection.|  
|<xref:System.Windows.Forms.DataGridViewSelectionMode.ColumnHeaderSelect>|En cliquant sur une cellule sélectionne. En cliquant sur un en-tête de colonne sélectionne la colonne entière. En-têtes de colonne ne peut pas être utilisés pour le tri.|  
|<xref:System.Windows.Forms.DataGridViewSelectionMode.FullColumnSelect>|En cliquant sur une cellule ou un en-tête de colonne sélectionne la colonne entière. En-têtes de colonne ne peut pas être utilisés pour le tri.|  
|<xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect>|En cliquant sur une cellule ou un en-tête de ligne sélectionne la ligne entière.|  
|<xref:System.Windows.Forms.DataGridViewSelectionMode.RowHeaderSelect>|Mode de sélection par défaut. En cliquant sur une cellule sélectionne. En cliquant sur un en-tête de ligne sélectionne la ligne entière.|  
  
> [!NOTE]
>  Modifier le mode de sélection en cours d’exécution automatiquement efface la sélection actuelle.  
  
 Par défaut, les utilisateurs peuvent sélectionner plusieurs lignes, colonnes ou cellules en faisant glisser avec la souris, en appuyant sur CTRL ou MAJ ENFONCÉE tout en sélectionnant pour étendre ou modifier une sélection, ou en cliquant sur la cellule d’en-tête de l’angle supérieur gauche pour sélectionner toutes les cellules dans le contrôle. Pour empêcher ce comportement, affectez la <xref:System.Windows.Forms.DataGridView.MultiSelect%2A> propriété `false`.  
  
 Le <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect> et <xref:System.Windows.Forms.DataGridViewSelectionMode.RowHeaderSelect> modes permettent aux utilisateurs de supprimer des lignes en les sélectionnant et en appuyant sur la touche SUPPR. Les utilisateurs peuvent supprimer des lignes uniquement lorsque la cellule active n’est pas en mode édition, le <xref:System.Windows.Forms.DataGridView.AllowUserToDeleteRows%2A> propriété est définie sur `true`, et la source de données sous-jacente prend en charge la suppression de ligne pilotée par l’utilisateur. Notez que ces paramètres n’empêchent pas la suppression de ligne par programmation.  
  
## <a name="programmatic-selection"></a>Sélection par programmation  
 Le mode de sélection actuel restreint le comportement de sélection par programmation ainsi que la sélection de l’utilisateur. Vous pouvez modifier la sélection actuelle par programme en définissant le `Selected` propriété des cellules, lignes ou colonnes présentes dans le <xref:System.Windows.Forms.DataGridView> contrôle. Vous pouvez également sélectionner toutes les cellules dans le contrôle via le <xref:System.Windows.Forms.DataGridView.SelectAll%2A> (méthode), selon le mode de sélection. Pour effacer la sélection, utilisez le <xref:System.Windows.Forms.DataGridView.ClearSelection%2A> (méthode).  
  
 Si le <xref:System.Windows.Forms.DataGridView.MultiSelect%2A> propriété est définie sur `true`, vous pouvez ajouter <xref:System.Windows.Forms.DataGridView> éléments à ou supprimez-les de la sélection en modifiant le `Selected` propriété de l’élément. Sinon, la définition de la `Selected` propriété `true` pour un élément supprime automatiquement les autres éléments de la sélection.  
  
 Notez que si vous modifiez la valeur de la <xref:System.Windows.Forms.DataGridView.CurrentCell%2A> propriété ne modifie pas la sélection actuelle.  
  
 Vous pouvez récupérer une collection de cellules sélectionnées actuellement, de lignes ou de colonnes à travers le <xref:System.Windows.Forms.DataGridView.SelectedCells%2A>, <xref:System.Windows.Forms.DataGridView.SelectedRows%2A>, et <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> propriétés de la <xref:System.Windows.Forms.DataGridView> contrôle. L’accès à ces propriétés est inefficace lorsque chaque cellule dans le contrôle est sélectionné. Pour éviter une altération des performances dans ce cas, utilisez le <xref:System.Windows.Forms.DataGridView.AreAllCellsSelected%2A> méthode première. En outre, l’accès à ces collections pour déterminer le nombre de cellules sélectionnées, lignes ou colonnes peuvent être inefficace. Au lieu de cela, vous devez utiliser le <xref:System.Windows.Forms.DataGridView.GetCellCount%2A>, <xref:System.Windows.Forms.DataGridViewRowCollection.GetRowCount%2A>, ou <xref:System.Windows.Forms.DataGridViewColumnCollection.GetColumnCount%2A> méthode, en passant le <xref:System.Windows.Forms.DataGridViewElementStates.Selected> valeur.  
  
> [!TIP]
>  Vous trouverez des exemples de code qui illustre l’utilisation par programmation des cellules sélectionnées dans le <xref:System.Windows.Forms.DataGridView> vue d’ensemble de la classe.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.MultiSelect%2A>
- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A>
- <xref:System.Windows.Forms.DataGridViewSelectionMode>
- [Sélection et utilisation du Presse-papiers avec le contrôle DataGridView Windows Forms](selection-and-clipboard-use-with-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Définir le Mode de sélection du contrôle DataGridView Windows Forms](how-to-set-the-selection-mode-of-the-windows-forms-datagridview-control.md)
