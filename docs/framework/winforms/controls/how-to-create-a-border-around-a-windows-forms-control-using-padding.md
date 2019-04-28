---
title: 'Procédure : créer une bordure autour d’un contrôle Windows Forms à l’aide de la marge intérieure'
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
ms.openlocfilehash: e3bbf43dbe45e675df172a6c3e1db16a3ba9caa8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61746835"
---
# <a name="how-to-create-a-border-around-a-windows-forms-control-using-padding"></a>Procédure : créer une bordure autour d’un contrôle Windows Forms à l’aide de la marge intérieure
L’exemple de code suivant montre comment créer une bordure ou un cadre autour un <xref:System.Windows.Forms.RichTextBox> contrôle. L’exemple définit la valeur d’un <xref:System.Windows.Forms.Panel> du contrôle <xref:System.Windows.Forms.Padding> propriété à 5 et affecte le <xref:System.Windows.Forms.Control.Dock%2A> propriété d’un enfant <xref:System.Windows.Forms.RichTextBox> le contrôle à <xref:System.Windows.Forms.DockStyle.Fill>. Le <xref:System.Windows.Forms.Control.BackColor%2A> de la <xref:System.Windows.Forms.Panel> contrôle est défini sur <xref:System.Drawing.Color.Blue%2A>, ce qui crée une bordure bleue autour de le <xref:System.Windows.Forms.RichTextBox> contrôle.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.Padding#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Padding/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.Padding#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Padding/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Padding>
- [Marge et marge intérieure dans les contrôles Windows Forms](margin-and-padding-in-windows-forms-controls.md)
