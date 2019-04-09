---
title: 'Procédure : utiliser une classe de rendu des contrôles'
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
ms.openlocfilehash: 7115c227cb24cf12a50073d0dc587524abf0cbb9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59163570"
---
# <a name="how-to-use-a-control-rendering-class"></a>Procédure : utiliser une classe de rendu des contrôles
Cet exemple montre comment utiliser le <xref:System.Windows.Forms.ComboBoxRenderer> classe pour restituer la flèche de déroulement d’une zone de liste déroulante contrôle de zone. L’exemple se compose de la <xref:System.Windows.Forms.Control.OnPaint%2A> méthode d’un contrôle personnalisé simple. Le <xref:System.Windows.Forms.ComboBoxRenderer.IsSupported%2A?displayProperty=nameWithType> propriété est utilisée pour déterminer si les styles visuels sont activés dans la zone cliente des fenêtres d’application. Si les styles visuels sont actifs, puis le <xref:System.Windows.Forms.ComboBoxRenderer.DrawDropDownButton%2A?displayProperty=nameWithType> méthode affichera la flèche de déroulement avec les styles visuels ; sinon, le <xref:System.Windows.Forms.ControlPaint.DrawComboButton%2A?displayProperty=nameWithType> méthode affichera la flèche de déroulement dans le style Windows classique.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/cpp/form1.cpp#10)]
 [!code-csharp[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/CS/form1.cs#10)]
 [!code-vb[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/VB/form1.vb#10)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Un contrôle personnalisé dérivé de la <xref:System.Windows.Forms.Control> classe.  
  
-   Un <xref:System.Windows.Forms.Form> qui héberge le contrôle personnalisé.  
  
-   Fait référence à la <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, et <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> espaces de noms.  
  
## <a name="see-also"></a>Voir aussi

- [Rendu des contrôles avec les styles visuels](rendering-controls-with-visual-styles.md)
