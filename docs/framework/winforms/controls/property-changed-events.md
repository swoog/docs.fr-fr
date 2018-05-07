---
title: Événements de modification de propriété
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property changes (using code)
- properties [Windows Forms], changes
ms.assetid: 268039ec-5aaa-4d76-b902-acccb036c850
ms.openlocfilehash: f4e6a6267df88cdd33a58093f276c6005209f38d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="property-changed-events"></a>Événements de modification de propriété
Si vous souhaitez que votre contrôle envoie des notifications lorsqu’une propriété nommée *PropertyName* change, définissez un événement nommé *PropertyName* `Changed` et une méthode nommée `On` *PropertyName* `Changed` qui déclenche l’événement. La convention d’affectation de noms dans les Windows Forms consiste à ajouter le mot *Changed* au nom de la propriété. Le type de délégué d’événement associé pour les événements de modification de propriété est <xref:System.EventHandler>, et le type de données d’événement est <xref:System.EventArgs>. La classe de base <xref:System.Windows.Forms.Control> définit de nombreux événements de modification de propriété, telle que <xref:System.Windows.Forms.Control.BackColorChanged>, <xref:System.Windows.Forms.Control.BackgroundImageChanged>, <xref:System.Windows.Forms.Control.FontChanged>, <xref:System.Windows.Forms.Control.LocationChanged>et d’autres. Pour des informations générales sur les événements, consultez [événements](../../../../docs/standard/events/index.md) et [événements dans les contrôles Windows Forms](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md).  
  
 Événements de modification de propriété sont utiles car ils permettent aux consommateurs d’un contrôle attacher des gestionnaires d’événements qui répondent à la modification. Si votre contrôle doit répondre à un événement de modification de propriété qu’il déclenche, substituez correspondant `On` *PropertyName* `Changed` méthode au lieu d’attacher un délégué à l’événement. En général, un contrôle répond à un événement de modification de propriété en mettant à jour d’autres propriétés ou en être redessiné tout ou partie de sa surface de dessin.  
  
 L’exemple suivant montre comment la `FlashTrackBar` contrôle personnalisé répond à certains événements de modification de propriété qu’il hérite de <xref:System.Windows.Forms.Control>. Pour obtenir un exemple complet, consultez [Comment : créer un Windows Forms que montre progression du contrôle](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#2)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#2)]  
  
## <a name="see-also"></a>Voir aussi  
 [Événements](../../../../docs/standard/events/index.md)  
 [Événements dans les contrôles Windows Forms](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)  
 [Propriétés dans les contrôles Windows Forms](../../../../docs/framework/winforms/controls/properties-in-windows-forms-controls.md)
