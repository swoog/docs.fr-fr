---
title: 'Procédure : construire des familles de polices et des polices'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- font families [Windows Forms], constructing
- fonts [Windows Forms], constructing
ms.assetid: d3a4a223-9492-4b54-9afd-db1c31c3cefd
ms.openlocfilehash: 0a9dcd00d4bc3e64ae4fc9a1d4884fac18521825
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181218"
---
# <a name="how-to-construct-font-families-and-fonts"></a>Procédure : construire des familles de polices et des polices
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] regroupe les polices avec le même type de caractère, mais des styles différents dans des familles de polices. Par exemple, la famille de polices Arial contient les polices suivantes :  
  
-   Arial normal  
  
-   Arial gras  
  
-   Arial italique  
  
-   Arial gras italique  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] utilise quatre styles pour former des familles : normal, gras, italique et gras italique. Adjectifs comme *affiner* et *arrondi* ne sont pas considérés comme des styles ; au lieu de cela ils font partie du nom de famille. Par exemple, Arial Narrow est une famille de polices avec les membres suivants :  
  
-   Arial Regular étroit  
  
-   Arial Condensé en gras  
  
-   Arial italique étroit  
  
-   Arial gras italique étroit  
  
 Vous pouvez dessiner du texte avec [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], vous devez construire un <xref:System.Drawing.FontFamily> objet et un <xref:System.Drawing.Font> objet. Le <xref:System.Drawing.FontFamily> objet spécifie le type de caractères (par exemple, Arial) et le <xref:System.Drawing.Font> objet spécifie la taille, style et les unités.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant construit un style régulière police Arial, avec une taille de 16 pixels. Dans le code suivant, le premier argument passé à la <xref:System.Drawing.Font.%23ctor%2A> constructeur est le <xref:System.Drawing.FontFamily> objet. Le deuxième argument spécifie la taille de la police mesurée en unités identifiées par le quatrième argument. Le troisième argument identifie le style.  
  
 <xref:System.Drawing.GraphicsUnit.Pixel> est un membre de la <xref:System.Drawing.GraphicsUnit> énumération, et <xref:System.Drawing.FontStyle.Regular> est un membre de la <xref:System.Drawing.FontStyle> énumération.  
  
 [!code-csharp[System.Drawing.FontsAndText#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.FontsAndText#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de polices et de texte](using-fonts-and-text.md)
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
