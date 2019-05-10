---
title: 'Procédure : définir le renderer ToolStrip pour une application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Renderer property [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], customizing
ms.assetid: 46acef3e-9844-4ae8-9a2e-3006fe99cadf
ms.openlocfilehash: 22f9276a3fa7fcecf6b4667f5aaba489c6ed296e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64630583"
---
# <a name="how-to-set-the-toolstrip-renderer-for-an-application"></a>Procédure : définir le renderer ToolStrip pour une application
Vous pouvez personnaliser l'apparence de vos contrôles <xref:System.Windows.Forms.ToolStrip> individuellement ou pour tous les contrôles <xref:System.Windows.Forms.ToolStrip> de votre application.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment appliquer de manière sélective un convertisseur personnalisé à un contrôle <xref:System.Windows.Forms.ToolStrip> et à un contrôle <xref:System.Windows.Forms.MenuStrip>.  
  
 Pour utiliser cet exemple de code, compilez et exécutez l'application, puis sélectionnez la portée du rendu personnalisé à partir du contrôle <xref:System.Windows.Forms.ComboBox>. Cliquez sur **Appliquer** pour définir le convertisseur.  
  
 Pour afficher le rendu d’élément de menu personnalisé, sélectionnez le <xref:System.Windows.Forms.MenuStrip> option à partir de la <xref:System.Windows.Forms.ComboBox> contrôler, cliquez sur **appliquer**, puis ouvrez le **fichier** élément de menu.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#70](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#70)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#70](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#70)]  
  
 Définissez la propriété <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> pour appliquer un convertisseur personnalisé à tous les contrôles <xref:System.Windows.Forms.ToolStrip> de votre application.  
  
 Définissez la propriété <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> pour appliquer un convertisseur personnalisé à un contrôle <xref:System.Windows.Forms.ToolStrip> spécifique.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
- [Contrôle ToolStrip](toolstrip-control-windows-forms.md)
