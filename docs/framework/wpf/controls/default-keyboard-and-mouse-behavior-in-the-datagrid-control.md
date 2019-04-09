---
title: Comportement par défaut du clavier et de la souris dans le contrôle DataGrid
ms.date: 03/30/2017
helpviewer_keywords:
- DataGrid [WPF], keyboard behavior
- DataGrid [WPF], mouse behavior
- keyboard behavior [WPF], DataGrid
- mouse behavior [WPF], DataGrid
ms.assetid: 563b8854-ca39-4d97-8235-17eaa0f93c8d
ms.openlocfilehash: 6be464ce85bd3ba91dd6e6cc810ec7d04edc0c3d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59083320"
---
# <a name="default-keyboard-and-mouse-behavior-in-the-datagrid-control"></a>Comportement par défaut du clavier et de la souris dans le contrôle DataGrid
Cette rubrique décrit comment les utilisateurs peuvent interagir avec le <xref:System.Windows.Controls.DataGrid> contrôle à l’aide du clavier et la souris.  
  
 Interactions standard avec le <xref:System.Windows.Controls.DataGrid> incluent la navigation, la sélection et la modification. Comportement de sélection est affecté par le <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> et <xref:System.Windows.Controls.DataGrid.SelectionUnit%2A> propriétés. Les valeurs par défaut qui provoquent le comportement décrit dans cette rubrique sont <xref:System.Windows.Controls.DataGridSelectionMode.Extended?displayProperty=nameWithType> et <xref:System.Windows.Controls.DataGridSelectionUnit.FullRow?displayProperty=nameWithType>. Modification de ces valeurs peut-être provoquer un comportement qui est différent de celle décrite. Lorsqu’une cellule est en mode édition, le contrôle d’édition peut substituer le comportement de clavier standard de la <xref:System.Windows.Controls.DataGrid>.  
  
## <a name="default-keyboard-behavior"></a>Comportement du clavier par défaut  
 Le tableau suivant répertorie le comportement de clavier par défaut pour le <xref:System.Windows.Controls.DataGrid>.  
  
|Touche ou combinaison de touches|Description|  
|----------------------------|-----------------|  
|BAS|Déplace le focus vers la cellule directement sous la cellule active. Si le focus est dans la dernière ligne, en appuyant sur la flèche vers le bas ne fait rien.|  
|HAUT|Déplace le focus vers la cellule juste au-dessus de la cellule active. Si le focus est dans la première ligne, la touche haut ne fait rien.|  
|GAUCHE|Déplace le focus vers la cellule précédente dans la ligne. Si le focus est dans la première cellule de la ligne, en appuyant sur la flèche de gauche n’a aucun effet.|  
|DROITE|Déplace le focus vers la cellule suivante dans la ligne. Si le focus est dans la dernière cellule dans la ligne, en appuyant sur la flèche de droite ne fait rien.|  
|ORIGINE|Déplace le focus vers la première cellule dans la ligne actuelle.|  
|FIN|Déplace le focus vers la dernière cellule dans la ligne actuelle.|  
|PG.SUIV|Si les lignes ne sont pas regroupées, fait défiler le contrôle vers le bas par le nombre de lignes qui sont entièrement affichés. Déplace le focus vers la dernière ligne entièrement affichée sans modifier les colonnes.<br /><br /> Si les lignes sont regroupées, déplace le focus vers la dernière ligne dans le <xref:System.Windows.Controls.DataGrid> sans modifier les colonnes.|  
|PG.PRÉC|Si les lignes ne sont pas regroupées, fait défiler le contrôle vers le haut par le nombre de lignes qui sont entièrement affichés. Déplace le focus sur la première ligne affichée sans modifier les colonnes.<br /><br /> Si les lignes sont regroupées, déplace le focus vers la première ligne dans le <xref:System.Windows.Controls.DataGrid> sans modifier les colonnes.|  
|TAB|Déplace le focus vers la cellule suivante dans la ligne actuelle. Si le focus est dans la dernière cellule de la ligne, déplace le focus vers la première cellule dans la ligne suivante. Si le focus est dans la dernière cellule dans le contrôle, déplace le focus au contrôle suivant dans l’ordre de tabulation du conteneur parent.<br /><br /> Si la cellule active est en mode édition et en appuyant sur tabulation, le focus à s’éloigner de la ligne actuelle, toutes les modifications qui ont été apportées à la ligne sont validées avant la modification de focus.|  
|MAJ+TAB|Déplace le focus vers la cellule précédente dans la ligne actuelle. Si le focus se trouve déjà dans la première cellule de la ligne, déplace le focus vers la dernière cellule de la ligne précédente. Si le focus est dans la première cellule dans le contrôle, déplace le focus au contrôle précédent dans l’ordre de tabulation du conteneur parent.<br /><br /> Si la cellule active est en mode édition et en appuyant sur tabulation, le focus à s’éloigner de la ligne actuelle, toutes les modifications qui ont été apportées à la ligne sont validées avant la modification de focus.|  
|CTRL+BAS|Déplace le focus vers la dernière cellule dans la colonne actuelle.|  
|CTRL+HAUT|Déplace le focus vers la première cellule dans la colonne actuelle.|  
|CTRL+FLECHE DROITE|Déplace le focus vers la dernière cellule dans la ligne actuelle.|  
|CTRL+FLECHE GAUCHE|Déplace le focus vers la première cellule dans la ligne actuelle.|  
|CTRL + ORIGINE|Déplace le focus vers la première cellule dans le contrôle.|  
|CTRL + FIN|Déplace le focus vers la dernière cellule dans le contrôle.|  
|CTRL+PAGE SUIVANTE|Identique à la PAGE suivante.|  
|CTRL+PG.PRÉC|Identique à la PAGE précédente.|  
|F2|Si le <xref:System.Windows.Controls.DataGrid.IsReadOnly%2A?displayProperty=nameWithType> propriété est `false` et <xref:System.Windows.Controls.DataGridColumn.IsReadOnly%2A?displayProperty=nameWithType> propriété est `false` pour la colonne actuelle, place la cellule active en mode de modification de cellule.|  
|ENTRÉE|Valide toutes les modifications à la cellule active et la ligne et déplace le focus vers la cellule directement sous la cellule active. Si le focus est dans la dernière ligne, valide toutes les modifications sans déplacer le focus.|  
|Échap|Si le contrôle est en mode édition, annule la modification et rétablit toutes les modifications qui ont été apportées dans le contrôle. Si la source de données sous-jacente implémente <xref:System.ComponentModel.IEditableObject>, en appuyant sur ÉCHAP une deuxième fois annule en mode édition pour la ligne entière.|  
|RETOUR ARRIÈRE|Supprime le caractère avant le curseur lors de la modification d’une cellule.|  
|SUPPR|Supprime le caractère situé après le curseur lors de la modification d’une cellule.|  
|CTRL+ENTRÉE|Valide toutes les modifications à la cellule active sans déplacer le focus.|  
|CTRL+A|Si <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> a la valeur <xref:System.Windows.Controls.DataGridSelectionMode.Extended>, sélectionne toutes les lignes dans le <xref:System.Windows.Controls.DataGrid>.|  
  
## <a name="selection-keys"></a>Touches de sélection  
 Si le <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> propriété est définie sur <xref:System.Windows.Controls.DataGridSelectionMode.Extended>, le comportement de navigation ne change pas, mais navigation avec le clavier tout en appuyant sur MAJ (y compris CTRL + MAJ) modifiera une sélection de plusieurs lignes. Avant le début de la navigation, le contrôle marque la ligne actuelle comme une ligne d’ancrage. Lorsque vous naviguez tout en appuyant sur MAJ, la sélection inclut toutes les lignes entre la ligne d’ancrage et de la ligne actuelle.  
  
 Les clés suivantes de la sélection modifient la sélection de plusieurs lignes.  
  
-   MAJ+BAS  
  
-   MAJ+HAUT  
  
-   MAJ+PG.SUIV  
  
-   MAJ+PG.PRÉC  
  
-   CTRL+MAJ+BAS  
  
-   CTRL+MAJ+HAUT  
  
-   CTRL + MAJ + ORIGINE  
  
-   CTRL + MAJ + FIN  
  
## <a name="default-mouse-behavior"></a>Comportement de la souris par défaut  
 Le tableau suivant répertorie le comportement de la souris par défaut pour le <xref:System.Windows.Controls.DataGrid>.  
  
|Action de la souris|Description|  
|------------------|-----------------|  
|Cliquez sur une ligne non sélectionnée|Transforme la ligne un clic sur la ligne actuelle et l’utilisateur a cliqué dessus la cellule active.|  
|Cliquez sur la cellule active|Place la cellule active en mode édition.|  
|Faites glisser une cellule d’en-tête de colonne|Si le <xref:System.Windows.Controls.DataGrid.CanUserReorderColumns%2A?displayProperty=nameWithType> propriété est `true` et <xref:System.Windows.Controls.DataGridColumn.CanUserReorder%2A?displayProperty=nameWithType> propriété est `true` pour la colonne actuelle, déplace la colonne afin qu’elle peut être placée dans une nouvelle position.|  
|Faites glisser un séparateur d’en-tête de colonne|Si le <xref:System.Windows.Controls.DataGrid.CanUserResizeColumns%2A?displayProperty=nameWithType> propriété est `true` et <xref:System.Windows.Controls.DataGridColumn.CanUserResize%2A?displayProperty=nameWithType> propriété est `true` pour la colonne actuelle, redimensionne la colonne.|  
|Double-cliquez sur un séparateur d’en-tête de colonne|Si le <xref:System.Windows.Controls.DataGrid.CanUserResizeColumns%2A?displayProperty=nameWithType> propriété est `true` et le <xref:System.Windows.Controls.DataGridColumn.CanUserResize%2A?displayProperty=nameWithType> propriété est `true` pour la colonne actuelle, auto-sizes la colonne en utilisant la <xref:System.Windows.Controls.DataGridLength.Auto%2A> mode de dimensionnement.|  
|Cliquez sur une cellule d’en-tête de colonne|Si le <xref:System.Windows.Controls.DataGrid.CanUserSortColumns%2A?displayProperty=nameWithType> propriété est `true` et <xref:System.Windows.Controls.DataGridColumn.CanUserSort%2A?displayProperty=nameWithType> propriété est `true` pour la colonne actuelle, trie la colonne.<br /><br /> Cliquez sur l’en-tête d’une colonne qui est déjà triée sera inverser le sens du tri de la colonne.<br /><br /> En appuyant sur la touche MAJ ENFONCÉE pendant que cliquez plusieurs en-têtes de colonne pour trier par plusieurs colonnes dans l’ordre que vous cliquez sur.|  
|CTRL + clic sur une ligne|Si <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> a la valeur <xref:System.Windows.Controls.DataGridSelectionMode.Extended>, modifie une sélection de plusieurs lignes non contiguës.<br /><br /> Si la ligne est déjà sélectionnée, désélectionne la ligne.|  
|MAJ + clic sur une ligne|Si <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> a la valeur <xref:System.Windows.Controls.DataGridSelectionMode.Extended>, modifie une sélection de plusieurs ligne contiguës.|  
|Cliquez sur un en-tête de groupe de lignes|Développe ou réduit le groupe.|  
|Cliquez sur le bouton Sélectionner tout dans l’angle supérieur gauche de la <xref:System.Windows.Controls.DataGrid>|Si <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> a la valeur <xref:System.Windows.Controls.DataGridSelectionMode.Extended>, sélectionne toutes les lignes dans le <xref:System.Windows.Controls.DataGrid>.|  
  
## <a name="mouse-selection"></a>Sélection de la souris  
 Si le <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> propriété est définie sur <xref:System.Windows.Controls.DataGridSelectionMode.Extended>, en cliquant sur une ligne tout en appuyant sur la touche CTRL ou MAJ modifiera une sélection de plusieurs lignes.  
  
 Lorsque vous cliquez sur une ligne en appuyant sur CTRL, la ligne modifie son état de sélection tandis que toutes les autres lignes conservent leur état de sélection actuel. Cela permet de sélectionner les lignes non adjacentes.  
  
 Lorsque vous cliquez sur une ligne en appuyant sur MAJ, la sélection inclut toutes les lignes entre la ligne actuelle et une ligne d’ancrage située à la position de la ligne actuelle avant le clic. Les clics suivants tout en appuyant sur MAJ modifient la ligne actuelle, mais pas la ligne d’ancrage. Cela permet de sélectionner une plage de lignes adjacentes.  
  
 CTRL + MAJ peuvent être combiné pour sélectionner des plages non adjacentes de lignes adjacentes. Pour ce faire, sélectionnez la première plage à l’aide de MAJ + clic, comme décrit précédemment. Une fois que la première plage de lignes est sélectionnée, utilisez CTRL + cliquez pour sélectionner la première ligne dans la plage suivante, puis cliquez sur la dernière ligne dans la plage suivante tout en appuyant sur CTRL + MAJ.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.DataGrid>
- <xref:System.Windows.Controls.DataGrid.SelectionMode%2A>
