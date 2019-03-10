---
title: 'Procédure : Créer une bordure autour d’un formulaire Windows contrôler à l’aide de la marge intérieure'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- margins
- controls [Windows Forms], Margin property
- padding [Windows Forms], Windows Forms
- controls [Windows Forms], Padding property
- controls [Windows Forms], outlining
- Padding property [Windows Forms]
- margins [Windows Forms], Windows Forms
- Margin property [Windows Forms]
ms.assetid: bac7ed4d-a163-4259-98bd-155a36345890
ms.openlocfilehash: 66748eef299c9175814fb130a7eda359c5de0546
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57720304"
---
# <a name="how-to-create-a-border-around-a-windows-forms-control-using-padding"></a>Procédure : Créer une bordure autour d’un formulaire Windows contrôler à l’aide de la marge intérieure
L’exemple de code suivant montre comment créer une bordure ou un cadre autour un <xref:System.Windows.Forms.RichTextBox> contrôle. L’exemple définit la valeur d’un <xref:System.Windows.Forms.Panel> du contrôle <xref:System.Windows.Forms.Padding> propriété à 5 et affecte le <xref:System.Windows.Forms.Control.Dock%2A> propriété d’un enfant <xref:System.Windows.Forms.RichTextBox> le contrôle à <xref:System.Windows.Forms.DockStyle.Fill>. Le <xref:System.Windows.Forms.Control.BackColor%2A> de la <xref:System.Windows.Forms.Panel> contrôle est défini sur <xref:System.Drawing.Color.Blue%2A>, ce qui crée une bordure bleue autour de le <xref:System.Windows.Forms.RichTextBox> contrôle.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.Padding#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Padding/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.Padding#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Padding/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Padding>
- [Marge et marge intérieure dans les contrôles Windows Forms](margin-and-padding-in-windows-forms-controls.md)
