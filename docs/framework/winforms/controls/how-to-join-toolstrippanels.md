---
title: 'Procédure : joindre des contrôles ToolStripPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], joining together
- ToolStripPanel control [Windows Forms], joining together
ms.assetid: 4eadda6d-e3b8-4151-aaf2-a8d564fbe6b3
ms.openlocfilehash: f73c13c4aac1abef70a2ceb0a30c3e46d8664748
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59161003"
---
# <a name="how-to-join-toolstrippanels"></a>Procédure : joindre des contrôles ToolStripPanel
Vous pouvez joindre des contrôles <xref:System.Windows.Forms.ToolStrip> à un <xref:System.Windows.Forms.ToolStripPanel> au moment de l'exécution pour bénéficier de la souplesse des applications MDI (Multiple-Document Interface).  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment joindre des contrôles <xref:System.Windows.Forms.ToolStrip> à un <xref:System.Windows.Forms.ToolStripPanel>.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#11)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripPanel>
- [Guide pratique pour Utiliser des contrôles ToolStripPanel pour MDI](how-to-use-toolstrippanels-for-mdi.md)
