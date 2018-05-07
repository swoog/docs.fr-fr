---
title: Vue d'ensemble du contrôle PrintPreviewControl (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PrintPreviewControl
helpviewer_keywords:
- print preview
- PrintPreviewControl control
ms.assetid: 4513c6c7-5e9b-4f4c-82ca-00f993a26955
ms.openlocfilehash: 330172a2ccf285cb75432572a558363e71de7ab1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="printpreviewcontrol-control-overview-windows-forms"></a>Vue d'ensemble du contrôle PrintPreviewControl (Windows Forms)
Windows Forms <xref:System.Windows.Forms.PrintPreviewControl> est utilisé pour afficher un [PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md) tel qu’il apparaîtra une fois imprimé. Ce contrôle n'ayant aucun bouton ni élément d'interface utilisateur, vous utilisez généralement <xref:System.Windows.Forms.PrintPreviewControl> uniquement si vous souhaitez écrire votre propre interface utilisateur d'aperçu avant impression. Si vous souhaitez que l’interface utilisateur standard, utilisez un <xref:System.Windows.Forms.PrintPreviewDialog> contrôle ; consultez [vue d’ensemble du contrôle PrintPreviewDialog](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md) pour une vue d’ensemble.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Propriété de clé du contrôle <xref:System.Windows.Forms.PrintPreviewControl.Document%2A>, qui définit le document à afficher. Le document doit être un <xref:System.Drawing.Printing.PrintDocument> objet. Pour une vue d’ensemble de la création de documents pour l’impression, consultez [vue d’ensemble du composant PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-overview-windows-forms.md) et [prise en charge de Windows Forms impression](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md). Le <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> et <xref:System.Windows.Forms.PrintPreviewControl.Rows%2A> propriétés déterminent le nombre de pages affichées horizontalement et verticalement sur le contrôle. L’anticrénelage peut lisser le texte, mais il peut également apporter de ralentir l’affichage ; pour l’utiliser, définissez la <xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A> propriété `true`.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.PrintPreviewControl>  
 [Vue d’ensemble du contrôle PrintPreviewDialog](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md)  
 [PrintPreviewControl, contrôle](../../../../docs/framework/winforms/controls/printpreviewcontrol-control-windows-forms.md)  
 [Contrôles et composants de boîte de dialogue](../../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md)
