---
title: 'Procédure : appliquer une correction gamma à un dégradé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- gradient brushes [Windows Forms], gamma correction
- gradients [Windows Forms], gamma correction
ms.assetid: da4690e7-5fac-4fd2-b3f0-5cb35c165b92
ms.openlocfilehash: 066ccc649105018d20cb86b6e576a1a238e0dc62
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59973264"
---
# <a name="how-to-apply-gamma-correction-to-a-gradient"></a>Procédure : appliquer une correction gamma à un dégradé
Vous pouvez activer la correction gamma pour un pinceau dégradé linéaire en définissant le pinceau <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> propriété `true`. Vous pouvez désactiver la correction gamma en définissant le <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> propriété `false`. La correction du gamma est désactivée par défaut.  
  
## <a name="example"></a>Exemple  

L’exemple suivant est une méthode qui est appelée à partir d’un contrôle <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements. L’exemple crée un pinceau dégradé linéaire et utilise ce pinceau pour remplir les deux rectangles. Le premier est rempli sans correction gamma, et le deuxième rectangle est rempli avec une correction gamma.  
  
 L’illustration suivante montre les deux rectangles remplis. Le rectangle supérieur, ce qui n’a pas de correction gamma, apparaît foncé au milieu. Le rectangle en bas, ce qui a une correction gamma, semble intensité plus régulière.  
  
 ![Gradient](./media/gammagradient1.png "gammagradient1")  
  
 [!code-csharp[System.Drawing.UsingaGradientBrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingaGradientBrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>
- [Utilisation d'un pinceau à dégradé pour remplir des formes](using-a-gradient-brush-to-fill-shapes.md)
