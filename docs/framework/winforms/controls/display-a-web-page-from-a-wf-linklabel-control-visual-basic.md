---
title: 'Comment : afficher une page web à partir d’un contrôle LinkLabel Windows Forms (Visual Basic)'
ms.date: 03/30/2017
dev_langs:
- vb
f1_keywords:
- LinkLabel1_LinkClicked
helpviewer_keywords:
- examples [Windows Forms], LinkLabel control
- Web pages [Windows Forms], displaying
- linking [Windows Forms], to Web pages from forms
- Windows Forms, linking to Web pages
- LinkLabel control [Windows Forms], examples
ms.assetid: 477a7398-5971-4de3-b24c-f49f32bdb28a
ms.openlocfilehash: a9964c8d333ea87dd995ec9111acc1a8ac1e79b0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524181"
---
# <a name="how-to-display-a-web-page-from-a-windows-forms-linklabel-control-visual-basic"></a>Comment : afficher une page web à partir d’un contrôle LinkLabel Windows Forms (Visual Basic)
Cet exemple affiche une page Web dans le navigateur par défaut lorsqu’un utilisateur clique sur un Windows Form <xref:System.Windows.Forms.LinkLabel> contrôle.  
  
## <a name="example"></a>Exemple  
  
```vb  
Private Sub Form1_Load(ByVal sender As System.Object, ByVal e _  
As System.EventArgs) Handles MyBase.Load  
    LinkLabel1.Text = "Click here to get more info."  
    LinkLabel1.Links.Add(6, 4, "www.microsoft.com")  
End Sub  
Private Sub LinkLabel1_LinkClicked(ByVal sender As System.Object, ByVal _  
e As System.Windows.Forms.LinkLabelLinkClickedEventArgs) Handles _  
LinkLabel1.LinkClicked  
    System.Diagnostics.Process.Start(e.Link.LinkData.ToString())  
End Sub  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Un Windows Form nommé `Form1`.  
  
-   un contrôle <xref:System.Windows.Forms.LinkLabel> nommé `LinkLabel1` ;  
  
-   Une connexion Internet active.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 L’appel à la <xref:System.Diagnostics.Process.Start%2A> méthode requiert une confiance totale. Pour plus d'informations, consultez <xref:System.Security.SecurityException>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.LinkLabel>  
 [LinkLabel, contrôle](../../../../docs/framework/winforms/controls/linklabel-control-windows-forms.md)
