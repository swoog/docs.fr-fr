---
title: 'Procédure : ajouter dynamiquement des éléments ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- toolbars [Windows Forms], adding items dynamically
- ToolStrip control [Windows Forms]
ms.assetid: 0e8dea56-5f46-408b-914d-7e360341a234
ms.openlocfilehash: d84b62005554479d227778f513e72594322791a3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59124928"
---
# <a name="how-to-add-toolstrip-items-dynamically"></a>Procédure : ajouter dynamiquement des éléments ToolStrip
Vous pouvez remplir dynamiquement la collection d'éléments de menu d'un contrôle <xref:System.Windows.Forms.ToolStrip> quand le menu s’ouvre.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment ajouter dynamiquement des éléments à un contrôle <xref:System.Windows.Forms.ContextMenuStrip>. Cet exemple montre également comment réutiliser le même contrôle <xref:System.Windows.Forms.ContextMenuStrip> pour trois contrôles différents du formulaire.  
  
 Dans cet exemple, un gestionnaire d’événements <xref:System.Windows.Forms.ToolStripDropDown.Opening> remplit la collection d’éléments de menu. Le gestionnaire d'événements <xref:System.Windows.Forms.ToolStripDropDown.Opening> examine les propriétés <xref:System.Windows.Forms.ContextMenuStrip.SourceControl%2A?displayProperty=nameWithType> et <xref:System.Windows.Forms.ToolStripItem.OwnerItem%2A?displayProperty=nameWithType>, et ajoute un <xref:System.Windows.Forms.ToolStripItem> qui décrit le contrôle de code source.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#40)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#40)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripDropDownButton>
- [ToolStrip, contrôle](toolstrip-control-windows-forms.md)
