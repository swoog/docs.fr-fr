---
title: 'Procédure : Définir l’ordre Z de contrôles ToolStrip ancrés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], specifying z-order
- z-order
ms.assetid: 8b595429-ba9f-46af-9c55-3d5cc53f7fff
ms.openlocfilehash: 170aca57a30ca89d8f7a50397ebf61cb1b0b60e4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629629"
---
# <a name="how-to-define-z-ordering-of-docked-toolstrip-controls"></a>Procédure : Définir l’ordre Z de contrôles ToolStrip ancrés
Pour positionner un contrôle <xref:System.Windows.Forms.ToolStrip> correctement avec l'ancrage, vous devez positionner le contrôle correctement dans l'ordre de plan du formulaire.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment organiser un contrôle <xref:System.Windows.Forms.ToolStrip> et un contrôle <xref:System.Windows.Forms.MenuStrip> ancré en spécifiant l'ordre de plan.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#21](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#21)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#21](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#21)]  
  
 L'ordre de plan est déterminé par l'ordre dans lequel les contrôles <xref:System.Windows.Forms.ToolStrip> et <xref:System.Windows.Forms.MenuStrip>  
  
 sont ajoutés à la collection <xref:System.Windows.Forms.Control.Controls%2A> du formulaire.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#23](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#23)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#23](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#23)]  
  
 Inversez l'ordre de ces appels à la méthode <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> et observez l'effet sur la disposition.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également la page [Comment : Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.Control.ControlCollection.Add%2A>
- <xref:System.Windows.Forms.Control.Controls%2A>
- <xref:System.Windows.Forms.Control.Dock%2A>
- [Contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
