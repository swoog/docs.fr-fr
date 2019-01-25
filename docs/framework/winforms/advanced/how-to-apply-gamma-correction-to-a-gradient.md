---
title: 'Procédure : Appliquer une Correction Gamma à un dégradé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- gradient brushes [Windows Forms], gamma correction
- gradients [Windows Forms], gamma correction
ms.assetid: da4690e7-5fac-4fd2-b3f0-5cb35c165b92
ms.openlocfilehash: b3b45c312542a3f8410bd93fcbe4e4cb70aa8516
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527157"
---
# <a name="how-to-apply-gamma-correction-to-a-gradient"></a>Procédure : Appliquer une Correction Gamma à un dégradé
Vous pouvez activer la correction gamma pour un pinceau dégradé linéaire en définissant le pinceau <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> propriété `true`. Vous pouvez désactiver la correction gamma en définissant le <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> propriété `false`. La correction du gamma est désactivée par défaut.  
  
## <a name="example"></a>Exemple  
 L’exemple crée un pinceau dégradé linéaire et utilise ce pinceau pour remplir les deux rectangles. Le premier est rempli sans correction gamma, et le deuxième rectangle est rempli avec une correction gamma.  
  
 L’illustration suivante montre les deux rectangles remplis. Le rectangle supérieur, ce qui n’a pas de correction gamma, apparaît foncé au milieu. Le rectangle en bas, ce qui a une correction gamma, semble intensité plus régulière.  
  
 ![Gradient](../../../../docs/framework/winforms/advanced/media/gammagradient1.png "gammagradient1")  
  
 [!code-csharp[System.Drawing.UsingaGradientBrush#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingaGradientBrush#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Drawing2D.LinearGradientBrush>
- [Utilisation d'un pinceau à dégradé pour remplir des formes](../../../../docs/framework/winforms/advanced/using-a-gradient-brush-to-fill-shapes.md)
