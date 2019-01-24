---
title: 'Procédure : Dessiner des lignes opaques et translucides'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- transparency [Windows Forms], lines
- lines [Windows Forms], drawing alpha blended
- alpha blending [Windows Forms], drawing lines
ms.assetid: 8f2508af-f495-4223-b5cc-646cbbb520eb
ms.openlocfilehash: 6076ebf6cb75aa4fdb5cf5798b642597d8f84c80
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559045"
---
# <a name="how-to-draw-opaque-and-semitransparent-lines"></a>Procédure : Dessiner des lignes opaques et translucides
Quand vous dessinez une ligne, vous devez passer un objet <xref:System.Drawing.Pen> à la méthode <xref:System.Drawing.Graphics.DrawLine%2A> de la classe <xref:System.Drawing.Graphics>. L'un des paramètres du constructeur <xref:System.Drawing.Pen.%23ctor%2A> est un objet <xref:System.Drawing.Color>. Pour dessiner une ligne opaque, affectez au composant alpha de la couleur la valeur 255. Pour dessiner une ligne translucide, affectez au composant alpha n'importe quelle valeur comprise entre 1 et 254.  
  
 Quand vous dessinez une ligne translucide sur un arrière-plan, la couleur de la ligne est fusionnée avec les couleurs de l'arrière-plan. Le composant alpha spécifie comment les couleurs de ligne et de l'arrière-plan sont mélangées ; les valeurs alpha proches de 0 favorisent les couleurs d'arrière-plan, tandis que les valeurs alpha proches de 255 favorisent la couleur de ligne.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant dessine une bitmap, puis dessine trois lignes qui utilisent la bitmap comme arrière-plan. La première ligne utilise un composant alpha de 255. Elle est donc opaque. Les deuxième et troisième lignes utilisent un composant alpha de 128 et sont donc translucides. Vous pouvez voir l'image d'arrière-plan sur les lignes. L'instruction qui définit la propriété <xref:System.Drawing.Graphics.CompositingQuality%2A> fait en sorte que la fusion pour la troisième ligne s'effectue parallèlement à une correction gamma.  
  
 L'illustration suivante montre la sortie du code suivant.  
  
 ![Opaques et translucides](../../../../docs/framework/winforms/advanced/media/compqualline.png "compqualline")  
  
 [!code-csharp[System.Drawing.AlphaBlending#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.AlphaBlending#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi
- [Fusion alpha de lignes et de remplissages](../../../../docs/framework/winforms/advanced/alpha-blending-lines-and-fills.md)
- [Guide pratique pour Affecter un arrière-plan Transparent à votre contrôle](../../../../docs/framework/winforms/controls/how-to-give-your-control-a-transparent-background.md)
- [Guide pratique pour Dessiner avec des pinceaux opaques et translucides](../../../../docs/framework/winforms/advanced/how-to-draw-with-opaque-and-semitransparent-brushes.md)
