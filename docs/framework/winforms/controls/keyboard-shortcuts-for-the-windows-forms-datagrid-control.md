---
title: Raccourcis clavier du contrôle DataGrid Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- keyboard shortcuts [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], navigation keys
ms.assetid: a01780f9-20d5-4f5f-808f-c790c9a007a5
ms.openlocfilehash: c04340cf2d2c8e318ea7348c978ef943563c24da
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711770"
---
# <a name="keyboard-shortcuts-for-the-windows-forms-datagrid-control"></a>Raccourcis clavier du contrôle DataGrid Windows Forms
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Le tableau suivant répertorie les raccourcis clavier qui peuvent être utilisées pour la navigation dans les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle :  
  
|Action|Raccourci|  
|------------|--------------|  
|Terminer une entrée de cellule et Descendre pour la cellule suivante.<br /><br /> Si le focus est sur un lien de la table enfant, accédez à cette table.|ENTRÉE|  
|Annuler la modification de la cellule en mode de modification de cellule.<br /><br /> En cas de sélection de texte défilant, annuler la modification de la ligne.|Échap|  
|Supprimer le caractère avant le point d’insertion lors de la modification d’une cellule.|RETOUR ARRIÈRE|  
|Supprimer le caractère après le point d’insertion lors de la modification d’une cellule.|SUPPR|  
|Déplacer vers la première cellule de la ligne actuelle.|ORIGINE|  
|Déplacer vers la dernière cellule dans la ligne actuelle.|FIN|  
|Mettez en surbrillance les caractères dans la cellule active et positionner le point d’insertion à la fin de la ligne. Même comportement en double-cliquant sur une cellule.|F2|  
|Si le focus est sur une cellule, déplacer vers la cellule suivante dans la ligne.<br /><br /> Si le focus se trouve sur la dernière cellule dans une ligne, déplacer vers le premier lien de table enfant de la ligne et développez-le.<br /><br /> Si le focus est sur un lien enfant, déplacer vers le lien enfant suivant.<br /><br /> Si le focus se trouve sur le dernier lien enfant, déplacer vers la première cellule de la ligne suivante.|TAB|  
|Si le focus est sur une cellule, déplacer vers la cellule précédente dans la ligne.<br /><br /> Si le focus se trouve sur la première cellule dans une ligne, déplacer vers le dernier lien de table enfant étendues de la ligne précédente ou les déplacer vers la dernière cellule de la ligne précédente.<br /><br /> Si le focus est sur un lien enfant, déplacez vers le lien enfant précédent.<br /><br /> Si le focus se trouve sur le premier lien enfant, déplacer vers la dernière cellule de la ligne précédente.|MAJ+TAB|  
|Déplacer vers le contrôle suivant dans l’ordre de tabulation.|CTRL+TAB|  
|Déplacer vers le contrôle précédent dans l’ordre de tabulation.|CTRL+MAJ+TAB|  
|Déplacer vers le haut à la table parent si dans une table enfant. Comportement de même qu’un clic sur le bouton précédent.|ALT + FLÈCHE GAUCHE|  
|Développez les liens de la table enfant. ALT + flèche bas développe tous les liens, pas seulement ceux sélectionnés.|ALT + flèche bas ou CTRL + signe plus|  
|Réduire les liens de la table enfant. ALT + flèche haut réduit tous les liens, pas seulement ceux sélectionnés.|ALT + flèche haut ou CTRL + signe moins|  
|Déplacer vers la cellule plus lointain non vide dans la direction de la flèche.|CTRL + TOUCHE DE DIRECTION|  
|Étendre la sélection d’une ligne dans la direction de la flèche (à l’exception des liens de la table enfant).|MAJ + FLÈCHE HAUT/BAS|  
|Étendre la sélection à une ligne plus lointain non vide dans la direction de la flèche (à l’exception des liens de la table enfant).|CTRL + MAJ + HAUT/FLÈCHE VERS LE BAS|  
|Déplacer vers la cellule supérieure gauche.|CTRL + ORIGINE|  
|Déplacer vers la cellule inférieure droite.|CTRL + FIN|  
|Étendre la sélection à la ligne du haut.|CTRL + MAJ + ORIGINE|  
|Étendre la sélection vers la ligne inférieure.|CTRL + MAJ + FIN|  
|Sélectionnez la ligne actuelle (à l’exception des liens de la table enfant).|MAJ + ESPACE|  
|Sélectionnez l’intégralité de la grille (à l’exception des liens de la table enfant).|CTRL+A|  
|Afficher la ligne parente dans une table enfant.|CTRL+PAGE SUIVANTE|  
|Masquer la ligne parente dans une table enfant.|CTRL+PG.PRÉC|  
|Étendre la sélection à l’écran (à l’exception des liens de la table enfant).|MAJ+PG.SUIV|  
|Étendre la sélection d’une page (à l’exception des liens de la table enfant).|MAJ+PG.PRÉC|  
|Appelez le <xref:System.Windows.Forms.DataGrid.EndEdit%2A> méthode pour la ligne actuelle.|CTRL+ENTRÉE|  
|Entrez un <xref:System.DBNull.Value?displayProperty=nameWithType> valeur dans une cellule en mode édition.|CTRL+0|  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble du contrôle DataGrid](datagrid-control-overview-windows-forms.md)
- [DataGrid, contrôle](datagrid-control-windows-forms.md)
