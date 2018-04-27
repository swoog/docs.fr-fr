---
title: 'Comment : créer un contrôle ToolStrip de style professionnel'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-winforms
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStripRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c208b2f6-8105-474b-9075-d582e1792870
caps.latest.revision: 9
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: e8b2d67f38f9533e60575b45df011f50e7ec091d
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="how-to-create-a-professionally-styled-toolstrip-control"></a>Comment : créer un contrôle ToolStrip de style professionnel
Vous pouvez donner aux contrôles <xref:System.Windows.Forms.ToolStrip> de votre application une apparence et un comportement professionnels en écrivant votre propre classe dérivée du type <xref:System.Windows.Forms.ToolStripProfessionalRenderer>.  
  
 Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.  
  
 Consultez [Procédure pas à pas : création d’un contrôle ToolStrip de style professionnel](../../../../docs/framework/winforms/controls/walkthrough-creating-a-professionally-styled-toolstrip-control.md).  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment utiliser <xref:System.Windows.Forms.ToolStrip> des contrôles pour créer un contrôle composite qui reproduit le **volet de Navigation** fourni par Microsoft® Outlook®.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StackView#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StackView#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez [Procédure pas à pas : création d’un contrôle ToolStrip de style professionnel](http://msdn.microsoft.com/library/ms233664\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.StatusStrip>  
 [Contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)  
 [Comment : fournir des éléments de menu standard à un formulaire](../../../../docs/framework/winforms/controls/how-to-provide-standard-menu-items-to-a-form.md)
