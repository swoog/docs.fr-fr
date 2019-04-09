---
title: 'Procédure : configurer les marges de sélection et d’image de MenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- margins [Windows Forms], setting in MenuStrip controls
- menus [Windows Forms], setting margins
- MenuStrip control [Windows Forms], configuring check and image margins
ms.assetid: 45a9075d-4bea-4ce2-9b2c-7619aa39f8ce
ms.openlocfilehash: 09de1a9ca4be1c4ebfb0e13e800c09753bd04f11
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134990"
---
# <a name="how-to-configure-menustrip-check-margins-and-image-margins"></a>Procédure : configurer les marges de sélection et d’image de MenuStrip
Vous pouvez personnaliser un <xref:System.Windows.Forms.MenuStrip> en définissant les propriétés <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A> et <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A> dans différentes combinaisons.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment définir et personnaliser les marges d'image et de sélection de <xref:System.Windows.Forms.ContextMenuStrip>. La procédure est identique pour <xref:System.Windows.Forms.ContextMenuStrip> et <xref:System.Windows.Forms.MenuStrip>.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#60)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#60)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [ToolStrip, contrôle](toolstrip-control-windows-forms.md)
- [Procédure : activer les marges de sélection et d’image dans les contrôles ContextMenuStrip](how-to-enable-check-margins-and-image-margins-in-contextmenustrip-controls.md)
