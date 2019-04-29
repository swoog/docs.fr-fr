---
title: Structure de l'interface graphique
ms.date: 03/30/2017
helpviewer_keywords:
- GDI+, using managed interface
- graphics [Windows Forms], class structure
ms.assetid: 010a1e46-656b-40a1-8d5d-87aa05ee1243
ms.openlocfilehash: 9dfffe8ea3f76d89823dfe2ef6bd0e4f3accf8f1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61956479"
---
# <a name="structure-of-the-graphics-interface"></a>Structure de l'interface graphique
L’interface de classe managée à [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] contient environ 60 classes, 50 énumérations et structures de 8. Le <xref:System.Drawing.Graphics> classe est au cœur de [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] fonctionnalité ; c’est la classe qui permet de dessiner des lignes, des courbes, des chiffres, des images et texte.  
  
## <a name="important-classes"></a>Classes importantes  
 De nombreuses classes fonctionnent avec la <xref:System.Drawing.Graphics> classe. Par exemple, le <xref:System.Drawing.Graphics.DrawLine%2A> méthode reçoit un <xref:System.Drawing.Pen> objet qui conserve les attributs (couleur, la largeur, style de ligne, etc.) de la ligne à dessiner. Le <xref:System.Drawing.Graphics.FillRectangle%2A> méthode peut recevoir un pointeur vers un <xref:System.Drawing.Drawing2D.LinearGradientBrush> objet, qui fonctionne avec le <xref:System.Drawing.Graphics> objet pour remplir un rectangle avec une couleur. <xref:System.Drawing.Font> et <xref:System.Drawing.StringFormat> objets influencent la manière dont un <xref:System.Drawing.Graphics> objet dessine du texte. Un <xref:System.Drawing.Drawing2D.Matrix> objet stocke et manipule la transformation universelle d’un <xref:System.Drawing.Graphics> objet, qui est utilisé pour faire pivoter, mettre à l’échelle et retourner des images.  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] fournit plusieurs structures (par exemple, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Point>, et <xref:System.Drawing.Size>) pour organiser les données de graphiques. En outre, certaines classes sont des types de données principalement comme structurés. Par exemple, le <xref:System.Drawing.Imaging.BitmapData> classe est une application d’assistance pour la <xref:System.Drawing.Bitmap> (classe) et le <xref:System.Drawing.Drawing2D.PathData> classe est une application d’assistance pour la <xref:System.Drawing.Drawing2D.GraphicsPath> classe.  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] définit plusieurs énumérations qui sont des collections de constantes connexes. Par exemple, le <xref:System.Drawing.Drawing2D.LineJoin> énumération contient les éléments <xref:System.Drawing.Drawing2D.LineJoin.Bevel>, <xref:System.Drawing.Drawing2D.LineJoin.Miter>, et <xref:System.Drawing.Drawing2D.LineJoin.Round>, qui spécifient les styles qui peuvent être utilisés pour joindre deux lignes.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des graphismes](graphics-overview-windows-forms.md)
- [À propos du code managé GDI+](about-gdi-managed-code.md)
- [Utilisation de classes graphiques managées](using-managed-graphics-classes.md)
