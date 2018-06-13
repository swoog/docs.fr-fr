---
title: 'Comment : utiliser une classe de rendu des contrôles'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- professional appearance [Windows Forms], rendering Windows Forms controls
- visual themes [Windows Forms], applying to Windows Forms controls
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: c0125e34-cd74-4c35-818c-3e40f462b0a3
ms.openlocfilehash: e5b82c3317d2d162fbd5a182166a9e0061fd770e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33534103"
---
# <a name="how-to-use-a-control-rendering-class"></a>Comment : utiliser une classe de rendu des contrôles
Cet exemple montre comment utiliser la <xref:System.Windows.Forms.ComboBoxRenderer> classe pour restituer la flèche de déroulement d’une zone de liste déroulante contrôle de zone. L’exemple se compose de la <xref:System.Windows.Forms.Control.OnPaint%2A> méthode d’un contrôle personnalisé simple. Le <xref:System.Windows.Forms.ComboBoxRenderer.IsSupported%2A?displayProperty=nameWithType> propriété est utilisée pour déterminer si les styles visuels sont activés dans la zone cliente des fenêtres d’application. Si les styles visuels sont actifs, puis le <xref:System.Windows.Forms.ComboBoxRenderer.DrawDropDownButton%2A?displayProperty=nameWithType> méthode restituera la flèche de déroulement avec les styles visuels ; sinon, le <xref:System.Windows.Forms.ControlPaint.DrawComboButton%2A?displayProperty=nameWithType> méthode restituera la flèche de déroulement dans le style Windows classique.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Windows.Forms_ControlRenderer#10](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/cpp/form1.cpp#10)]
 [!code-csharp[System.Windows.Forms_ControlRenderer#10](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/CS/form1.cs#10)]
 [!code-vb[System.Windows.Forms_ControlRenderer#10](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/VB/form1.vb#10)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Un contrôle personnalisé dérivé de la <xref:System.Windows.Forms.Control> classe.  
  
-   Un <xref:System.Windows.Forms.Form> qui héberge le contrôle personnalisé.  
  
-   Les références à la <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, et <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> espaces de noms.  
  
## <a name="see-also"></a>Voir aussi  
 [Rendu des contrôles avec les styles visuels](../../../../docs/framework/winforms/controls/rendering-controls-with-visual-styles.md)
