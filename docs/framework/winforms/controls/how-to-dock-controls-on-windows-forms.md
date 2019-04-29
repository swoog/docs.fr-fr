---
title: 'Procédure : arrimer des contrôles dans des Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], docking
- Explorer-style applications [Windows Forms], creating
- Windows Forms controls, filling client area
ms.assetid: bc11f2e4-e90a-4830-b0e2-f43b6e2b8bec
ms.openlocfilehash: d015dce7307bec092f6da1dc5ee31691a6baf1f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941494"
---
# <a name="how-to-dock-controls-on-windows-forms"></a>Procédure : arrimer des contrôles dans des Windows Forms
Vous pouvez ancrer des contrôles sur les bords de votre formulaire ou demander qu’ils remplissent le conteneur du contrôle (un formulaire ou un contrôle conteneur). Par exemple, l’Explorateur Windows ancre son <xref:System.Windows.Forms.TreeView> contrôle vers le côté gauche de la fenêtre et son <xref:System.Windows.Forms.ListView> contrôle sur le côté droit de la fenêtre. Utilisez le <xref:System.Windows.Forms.Control.Dock%2A> propriété pour tous les contrôles Windows Forms visibles définir le mode d’ancrage.  
  
> [!NOTE]
>  Les contrôles sont ancrés dans l’ordre inverse.  
  
 Le <xref:System.Windows.Forms.Control.Dock%2A> propriété interagit avec le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété. Pour plus d’informations, consultez [vue d’ensemble de la propriété AutoSize](autosize-property-overview.md).  
  
### <a name="to-dock-a-control"></a>Pour ancrer un contrôle  
  
1. Sélectionnez le contrôle que vous souhaitez ancrer.  
  
2. Dans la fenêtre Propriétés, cliquez sur la flèche à droite de la <xref:System.Windows.Forms.Control.Dock%2A> propriété.  
  
     Un éditeur s’affiche qui présente une série de zones représentant les bords et le centre du formulaire.  
  
3. Cliquez sur le bouton qui représente le bord de l’écran où vous souhaitez ancrer le contrôle. Pour remplir le formulaire du contrôle ou le contrôle conteneur, cliquez sur la zone centrale. Cliquez sur **(aucun)** pour désactiver l’ancrage.  
  
     Le contrôle est redimensionné automatiquement pour ajuster les limites du bord ancré.  
  
    > [!NOTE]
    >  Les contrôles hérités doivent être `Protected` pour pouvoir être ancrée. Pour modifier le niveau d’accès d’un contrôle, définissez son **modificateur** propriété dans la fenêtre Propriétés.  
  
## <a name="see-also"></a>Voir aussi

- [Contrôles Windows Forms](index.md)
- [Disposition des contrôles dans les Windows Forms](arranging-controls-on-windows-forms.md)
- [Création d'étiquettes et de raccourcis pour les contrôles Windows Forms](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
- [Classement par fonction des contrôles Windows Forms](windows-forms-controls-by-function.md)
- [Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle FlowLayoutPanel](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [Vue d’ensemble de la propriété AutoSize](autosize-property-overview.md)
- [Guide pratique pour Ancrer les contrôles aux Windows Forms](how-to-anchor-controls-on-windows-forms.md)
