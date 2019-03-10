---
title: 'Procédure : Dessiner une ligne en pointillés personnalisée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], custom
- lines [Windows Forms], drawing
- lines [Windows Forms], dashed
ms.assetid: cd0ed96a-cce4-47b9-b58a-3bae2e3d1bee
ms.openlocfilehash: 830fa45fc88c35b8aa5f047e065ae1efc161f581
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718942"
---
# <a name="how-to-draw-a-custom-dashed-line"></a>Procédure : Dessiner une ligne en pointillés personnalisée
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] fournit plusieurs styles de ligne sont répertoriées dans le <xref:System.Drawing.Drawing2D.DashStyle> énumération. Si ces styles de tiret standard ne répondent pas à vos besoins, vous pouvez créer un modèle de tirets personnalisés.  
  
## <a name="example"></a>Exemple  
 Pour dessiner une ligne en pointillés personnalisée, placez les longueurs des tirets et des espaces dans un tableau et assignez le tableau comme valeur de la <xref:System.Drawing.Pen.DashPattern%2A> propriété d’un <xref:System.Drawing.Pen> objet. L’exemple suivant dessine une ligne en pointillés personnalisée en fonction du tableau `{5, 2, 15, 4}`. Si vous multipliez les éléments du tableau par la largeur du stylet 5, vous obtenez `{25, 10, 75, 20}`. Les tirets affichées longueur alternent entre 25 et 75, et les espaces longueur alternent entre 10 et 20.  
  
 L’illustration suivante montre la ligne en pointillés qui en résulte. Notez que le tiret final doit être inférieure à 25 unités afin que la ligne peut se terminer à (405, 5).  
  
 ![Stylets](./media/pens6.gif "pens6")  
  
 [!code-csharp[System.Drawing.UsingAPen#51](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#51)]
 [!code-vb[System.Drawing.UsingAPen#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#51)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Créer un formulaire Windows et de gérer le formulaire <xref:System.Windows.Forms.Control.Paint> événement. Collez le code précédent dans le <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation d'un stylet pour dessiner des lignes et des formes](using-a-pen-to-draw-lines-and-shapes.md)
