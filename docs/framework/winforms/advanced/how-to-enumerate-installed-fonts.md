---
title: 'Procédure : Énumérer les polices installées'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], enumerating installed
- examples [Windows Forms], fonts
ms.assetid: 26d74ef5-0f39-4eeb-8d20-00e66e014abe
ms.openlocfilehash: 0124d2bdd8b9c60dc2bf2508348044d76a2c7eb4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602232"
---
# <a name="how-to-enumerate-installed-fonts"></a>Procédure : Énumérer les polices installées
Le <xref:System.Drawing.Text.InstalledFontCollection> classe hérite de la <xref:System.Drawing.Text.FontCollection> classe de base abstraite. Vous pouvez utiliser un <xref:System.Drawing.Text.InstalledFontCollection> objet à énumérer les polices installées sur l’ordinateur. Le <xref:System.Drawing.Text.FontCollection.Families%2A> propriété d’un <xref:System.Drawing.Text.InstalledFontCollection> objet est un tableau de <xref:System.Drawing.FontFamily> objets.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant répertorie les noms de toutes les familles de polices installées sur l’ordinateur. Le code récupère le <xref:System.Drawing.FontFamily.Name%2A> propriété de chaque <xref:System.Drawing.FontFamily> objet dans le tableau retourné par la <xref:System.Drawing.Text.FontCollection.Families%2A> propriété. Comme les noms de famille sont récupérés, ils sont concaténés pour former une virgule liste. Le <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe dessine la liste séparée par des virgules dans un rectangle.  
  
 Si vous exécutez l’exemple de code, la sortie sera similaire à celle illustrée dans l’illustration suivante.  
  
 ![Polices installées](../../../../docs/framework/winforms/advanced/media/csfontstext6.png "csfontstext6")  
  
 [!code-csharp[System.Drawing.FontsAndText#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.FontsAndText#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>. En outre, vous devez importer le <xref:System.Drawing.Text> espace de noms.  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation de polices et de texte](../../../../docs/framework/winforms/advanced/using-fonts-and-text.md)
