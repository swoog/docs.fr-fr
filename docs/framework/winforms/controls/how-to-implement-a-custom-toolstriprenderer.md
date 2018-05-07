---
title: 'Comment : implémenter un ToolStripRenderer personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c66fd3f7-2377-4553-8f1b-006527f08f32
ms.openlocfilehash: acf5967c015d61a0cc148e5cb509a5a7ded2152c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-implement-a-custom-toolstriprenderer"></a>Comment : implémenter un ToolStripRenderer personnalisé
Vous pouvez personnaliser l'apparence d'un contrôle <xref:System.Windows.Forms.ToolStrip> en implémentant une classe qui dérive de <xref:System.Windows.Forms.ToolStripRenderer>. Cela offre la flexibilité nécessaire pour créer une apparence qui diffère de celle fournie par les classes <xref:System.Windows.Forms.ToolStripProfessionalRenderer> et <xref:System.Windows.Forms.ToolStripSystemRenderer>.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment implémenter une classe <xref:System.Windows.Forms.ToolStripRenderer> personnalisée. Dans cet exemple, le contrôle `GridStrip` implémente un puzzle à mosaïques coulissantes qui permet à l'utilisateur de déplacer des mosaïques dans une disposition de table pour former une image. Un contrôle <xref:System.Windows.Forms.ToolStrip> personnalisé réorganise ses contrôles <xref:System.Windows.Forms.ToolStripButton> dans une disposition de grille. La disposition contient une cellule vide, dans laquelle l'utilisateur peut glisser une mosaïque adjacente à l'aide d'une opération de glisser-déplacer. Les mosaïques que l'utilisateur peut déplacer sont mises en surbrillance.  
  
 La classe `GridStripRenderer` personnalise trois aspects de l'apparence du contrôle `GridStrip` :  
  
-   la bordure `GridStrip` ;  
  
-   la bordure <xref:System.Windows.Forms.ToolStripButton> ;  
  
-   l'image <xref:System.Windows.Forms.ToolStripButton>.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.GridStrip#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/CS/GridStrip.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.GridStrip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/VB/GridStrip.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également la page [Comment : compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.ToolStripRenderer>  
 <xref:System.Windows.Forms.ToolStripProfessionalRenderer>  
 <xref:System.Windows.Forms.ToolStripSystemRenderer>  
 <xref:System.Windows.Forms.StatusStrip>  
 [Contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
