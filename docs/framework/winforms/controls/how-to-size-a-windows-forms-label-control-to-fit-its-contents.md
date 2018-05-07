---
title: 'Comment : dimensionner un contrôle Label Windows Forms en fonction de son contenu'
ms.date: 03/30/2017
helpviewer_keywords:
- captions [Windows Forms], sizing
- sizing controls
- size [Windows Forms], controls
- labels [Windows Forms], sizing to fit contents
- Label control [Windows Forms], sizing to fit contents
ms.assetid: 99648964-63b2-438c-980e-d24103ad602b
ms.openlocfilehash: e067966b606d77ceb9d11d2784c0d5f73ad332a0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-size-a-windows-forms-label-control-to-fit-its-contents"></a>Comment : dimensionner un contrôle Label Windows Forms en fonction de son contenu
Windows Forms <xref:System.Windows.Forms.Label> contrôle peut être unique ou plusieurs lignes, et il peut être soit de taille fixe ou peut redimensionner automatiquement pour adapter sa légende. Le <xref:System.Windows.Forms.Label.AutoSize%2A> propriété vous permet de dimensionner les contrôles pour s’ajuster à la taille des légendes, ce qui est particulièrement utile si la changer au moment de l’exécution.  
  
### <a name="to-make-a-label-control-resize-dynamically-to-fit-its-contents"></a>Pour rendre un contrôle label redimensionné dynamiquement pour s’adapter à son contenu.  
  
1.  Définir son <xref:System.Windows.Forms.Label.AutoSize%2A> propriété `true`.  
  
 Si <xref:System.Windows.Forms.Label.AutoSize%2A> a la valeur `false`, le texte spécifié dans le <xref:System.Windows.Forms.Label.Text%2A> propriété encapsule à la ligne suivante si possible, mais le contrôle n’augmentera pas.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour créer des touches d'accès rapide à l'aide des contrôles Label Windows Forms](../../../../docs/framework/winforms/controls/how-to-create-access-keys-with-windows-forms-label-controls.md)  
 [Vue d'ensemble du contrôle Label](../../../../docs/framework/winforms/controls/label-control-overview-windows-forms.md)  
 [Label, contrôle](../../../../docs/framework/winforms/controls/label-control-windows-forms.md)
