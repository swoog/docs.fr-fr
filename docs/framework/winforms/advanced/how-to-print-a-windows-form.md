---
title: 'Procédure : Imprimer un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, printing
- printing [Windows Forms]
- printing a form
- printing [Windows Forms], printing a form
ms.assetid: c8dff5f8-f56a-4c07-ae31-64643b31f8fc
ms.openlocfilehash: 5e672f40797a90111daefed0be74c941d4cc37b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628134"
---
# <a name="how-to-print-a-windows-form"></a>Procédure : Imprimer un formulaire Windows
Dans le cadre du processus de développement, vous généralement intérêt à imprimer une copie de votre formulaire Windows. L’exemple de code suivant montre comment imprimer une copie de l’écran actuel à l’aide de la <xref:System.Drawing.Graphics.CopyFromScreen%2A> (méthode).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Drawing.Graphics.CopyFromScreen#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Graphics.CopyFromScreen/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Graphics.CopyFromScreen#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Graphics.CopyFromScreen/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Il s’agit d’un exemple de code complet qui contient un `Main` (méthode).  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Vous n’êtes pas autorisé à accéder à l’imprimante.  
  
-   Aucune imprimante n’est installée.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Pour exécuter cet exemple de code, vous devez être autorisé à accéder à l’imprimante que vous utilisez avec votre ordinateur.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Printing.PrintDocument>
- [Guide pratique pour Rendre des Images avec GDI +](../../../../docs/framework/winforms/advanced/how-to-render-images-with-gdi.md)
- [Guide pratique pour Imprimer des graphiques dans les Windows Forms](../../../../docs/framework/winforms/advanced/how-to-print-graphics-in-windows-forms.md)
