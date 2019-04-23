---
title: Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], sizing rows and columns
- columns [Windows Forms], resizing in grids
- data grids [Windows Forms], resizing columns and rows
ms.assetid: 7532764d-e5c1-4943-a08b-6377a722d3b6
ms.openlocfilehash: e1fa2d57cfb2cd374d691fe03a0e0bdbd3ad7141
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138110"
---
# <a name="resizing-columns-and-rows-in-the-windows-forms-datagridview-control"></a>Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms
Le `DataGridView` contrôle fournit de nombreuses options permettant de personnaliser le comportement de dimensionnement de ses colonnes et de lignes. En règle générale, `DataGridView` cellules ne se redimensionnent pas en fonction de leur contenu. Au lieu de cela, elles tronquent toute valeur d’affichage qui est supérieure à la cellule. Si le contenu peut être affiché sous forme de chaîne, la cellule l’affiche dans une info-bulle.  
  
 Par défaut, les utilisateurs peuvent faire glisser de ligne, colonne et les séparateurs d’en-têtes avec la souris pour afficher plus d’informations. Les utilisateurs peuvent également double-cliquer sur un séparateur pour redimensionner automatiquement la bande de ligne, colonne ou en-tête associée, en fonction de son contenu.  
  
 Le `DataGridView` contrôle fournit des propriétés, méthodes et événements qui vous permettent de personnaliser ou de désactiver tous ces comportements dirigé par l’utilisateur. En outre, vous pouvez redimensionner par programme les lignes, colonnes et en-têtes en fonction de leur contenu, ou vous pouvez les configurer pour se redimensionnent automatiquement lorsque leur contenu change. Vous pouvez également configurer des colonnes pour diviser automatiquement la largeur disponible du contrôle dans des proportions que vous spécifiez.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Options de dimensionnement dans le contrôle DataGridView Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md)  
 Décrit les options de dimensionnement de lignes, des colonnes et des en-têtes. Également fournit des détails sur les méthodes et propriétés relatives au dimensionnement et décrit les scénarios d’utilisation courants.  
  
 [Mode Remplissage des colonnes dans le contrôle DataGridView Windows Forms](column-fill-mode-in-the-windows-forms-datagridview-control.md)  
 Décrit le mode de remplissage de colonne en détail et fournit du code de démonstration qui vous permettent de faire des essais avec le mode de remplissage de colonne et les autres modes.  
  
 [Guide pratique pour Définir les Modes de redimensionnement du contrôle DataGridView Windows Forms](how-to-set-the-sizing-modes-of-the-windows-forms-datagridview-control.md)  
 Décrit comment configurer les modes de dimensionnement pour des objectifs communs.  
  
 [Guide pratique pour Redimensionner par programme les cellules en fonction du contenu dans le contrôle de DataGridView Windows Forms](programmatically-resize-cells-to-fit-content-in-the-datagrid.md)  
 Fournit du code de démonstration que vous pouvez utiliser pour expérimenter le redimensionnement par programmation.  
  
 [Guide pratique pour Redimensionner automatiquement des cellules lorsque le contenu change dans le contrôle de DataGridView Windows Forms](automatically-resize-cells-when-content-changes-in-the-datagrid.md)  
 Fournit du code de démonstration qui vous permettent de faire des essais avec les modes de dimensionnement automatique.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.DataGridView>  
 Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.  
  
## <a name="see-also"></a>Voir aussi

- [DataGridView, contrôle](datagridview-control-windows-forms.md)
