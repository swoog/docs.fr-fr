---
title: 'Comment : créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripPanel control [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: 64992ed9-44af-4baf-b45f-863e6ab35711
ms.openlocfilehash: badbf316c769f60001b2ca2a4cacbf268f600e8d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a>Comment : créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip
L'espace de noms <xref:System.Windows.Forms?displayProperty=nameWithType> prend en charge plusieurs applications MDI (Multiple Document Interface) et le contrôle <xref:System.Windows.Forms.MenuStrip> prend en charge la fusion de menus. Les formulaires MDI peuvent également contenir des contrôles <xref:System.Windows.Forms.ToolStrip>.  
  
 Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.  
  
 Consultez également [Procédure pas à pas : création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](http://msdn.microsoft.com/library/ms233676\(v=vs.110\)).  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment utiliser des contrôles <xref:System.Windows.Forms.ToolStripPanel> avec un formulaire MDI. Le formulaire prend également en charge la fusion de menus avec les menus enfants.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple de code nécessite :  
  
-   Références aux assemblys System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également la page [Comment : compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi  
 [Contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
