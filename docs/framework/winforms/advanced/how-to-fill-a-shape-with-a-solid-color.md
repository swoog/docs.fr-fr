---
title: 'Procédure : Remplir une forme avec une couleur unie'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], adding to shapes
- shapes [Windows Forms], filling
ms.assetid: 06088b31-bac9-4ef3-9ebe-06c2c764d6df
ms.openlocfilehash: d6fe7a252029ff80f21d99f7342fabb1d29fbe24
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59211671"
---
# <a name="how-to-fill-a-shape-with-a-solid-color"></a>Procédure : Remplir une forme avec une couleur unie
Pour remplir une forme avec une couleur unie, créez un <xref:System.Drawing.SolidBrush> de l’objet et la transmettre puis <xref:System.Drawing.SolidBrush> objet en tant qu’argument à une des méthodes de remplissage de la <xref:System.Drawing.Graphics> classe. L’exemple suivant montre comment remplir une ellipse avec la couleur rouge.  
  
## <a name="example"></a>Exemple  
 Dans le code suivant, le <xref:System.Drawing.SolidBrush.%23ctor%2A> constructeur accepte un <xref:System.Drawing.Color> objet comme seul argument. Les valeurs utilisées par le <xref:System.Drawing.Color.FromArgb%2A> méthode représentent les composants alphabétiques, rouges, vert et bleus de la couleur. Chacune de ces valeurs doit être comprise entre 0 et 255. Le premier 255 indique que la couleur est complètement opaque, et le deuxième 255 indique que le composant rouge est à intensité complète. Les deux zéros indiquent que les composants verts et bleus ont une intensité de 0.  
  
 Les quatre nombres (0, 0, 100, 60) passé à la <xref:System.Drawing.Graphics.FillEllipse%2A> méthode spécifier l’emplacement et la taille du rectangle englobant de l’ellipse. Le rectangle a un coin supérieur gauche de (0, 0), une largeur de 100 et une hauteur de 60.  
  
 [!code-csharp[System.Drawing.UsingABrush#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingABrush#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d'un pinceau pour remplir des formes](using-a-brush-to-fill-shapes.md)
