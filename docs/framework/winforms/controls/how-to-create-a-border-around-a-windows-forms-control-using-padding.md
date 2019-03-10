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
# <a name="how-to-create-a-border-around-a-windows-forms-control-using-padding"></a><span data-ttu-id="55fb5-102">Procédure : Créer une bordure autour d’un formulaire Windows contrôler à l’aide de la marge intérieure</span><span class="sxs-lookup"><span data-stu-id="55fb5-102">How to: Create a Border Around a Windows Forms Control Using Padding</span></span>
<span data-ttu-id="55fb5-103">L’exemple de code suivant montre comment créer une bordure ou un cadre autour un <xref:System.Windows.Forms.RichTextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="55fb5-103">The following code example demonstrates how to create a border or outline around a <xref:System.Windows.Forms.RichTextBox> control.</span></span> <span data-ttu-id="55fb5-104">L’exemple définit la valeur d’un <xref:System.Windows.Forms.Panel> du contrôle <xref:System.Windows.Forms.Padding> propriété à 5 et affecte le <xref:System.Windows.Forms.Control.Dock%2A> propriété d’un enfant <xref:System.Windows.Forms.RichTextBox> le contrôle à <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="55fb5-104">The example sets the value of a <xref:System.Windows.Forms.Panel> control’s <xref:System.Windows.Forms.Padding> property to 5 and sets the <xref:System.Windows.Forms.Control.Dock%2A> property of a child <xref:System.Windows.Forms.RichTextBox> control to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span> <span data-ttu-id="55fb5-105">Le <xref:System.Windows.Forms.Control.BackColor%2A> de la <xref:System.Windows.Forms.Panel> contrôle est défini sur <xref:System.Drawing.Color.Blue%2A>, ce qui crée une bordure bleue autour de le <xref:System.Windows.Forms.RichTextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="55fb5-105">The <xref:System.Windows.Forms.Control.BackColor%2A> of the <xref:System.Windows.Forms.Panel> control is set to <xref:System.Drawing.Color.Blue%2A>, which creates a blue border around the <xref:System.Windows.Forms.RichTextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55fb5-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="55fb5-106">Example</span></span>  
 [!code-csharp[System.Windows.Forms.Padding#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Padding/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.Padding#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Padding/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="55fb5-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55fb5-107">See also</span></span>
- <xref:System.Windows.Forms.Padding>
- [<span data-ttu-id="55fb5-108">Marge et marge intérieure dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="55fb5-108">Margin and Padding in Windows Forms Controls</span></span>](margin-and-padding-in-windows-forms-controls.md)
