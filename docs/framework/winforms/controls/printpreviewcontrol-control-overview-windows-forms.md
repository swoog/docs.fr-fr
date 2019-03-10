---
title: Vue d'ensemble du contrôle PrintPreviewControl (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PrintPreviewControl
helpviewer_keywords:
- print preview
- PrintPreviewControl control
ms.assetid: 4513c6c7-5e9b-4f4c-82ca-00f993a26955
ms.openlocfilehash: 045141fc1860cd194f96cea106ff1ff444587418
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708540"
---
# <a name="printpreviewcontrol-control-overview-windows-forms"></a>Vue d'ensemble du contrôle PrintPreviewControl (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.PrintPreviewControl> est utilisé pour afficher un [PrintDocument](printdocument-component-windows-forms.md) tel qu’il apparaîtra une fois imprimé. Ce contrôle n'ayant aucun bouton ni élément d'interface utilisateur, vous utilisez généralement <xref:System.Windows.Forms.PrintPreviewControl> uniquement si vous souhaitez écrire votre propre interface utilisateur d'aperçu avant impression. Si vous souhaitez l’interface utilisateur standard, utilisez un <xref:System.Windows.Forms.PrintPreviewDialog> contrôler ; consultez [vue d’ensemble du contrôle PrintPreviewDialog](printpreviewdialog-control-overview-windows-forms.md) pour une vue d’ensemble.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Propriété de clé du contrôle est <xref:System.Windows.Forms.PrintPreviewControl.Document%2A>, qui définit le document à afficher. Le document doit être un <xref:System.Drawing.Printing.PrintDocument> objet. Pour une vue d’ensemble de la création de documents pour l’impression, consultez [vue d’ensemble du composant PrintDocument](printdocument-component-overview-windows-forms.md) et [prise en charge de Windows Forms Print](../advanced/windows-forms-print-support.md). Le <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> et <xref:System.Windows.Forms.PrintPreviewControl.Rows%2A> propriétés déterminent le nombre de pages affichées horizontalement et verticalement sur le contrôle. L’anticrénelage peut lisser le texte, mais il peut également apporter de ralentir l’affichage ; pour l’utiliser, définissez la <xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A> propriété `true`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.PrintPreviewControl>
- [Vue d’ensemble du contrôle PrintPreviewDialog](printpreviewdialog-control-overview-windows-forms.md)
- [PrintPreviewControl, contrôle](printpreviewcontrol-control-windows-forms.md)
- [Contrôles et composants de boîte de dialogue](dialog-box-controls-and-components-windows-forms.md)
