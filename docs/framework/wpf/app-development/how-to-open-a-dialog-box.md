---
title: 'Comment : ouvrir une boîte de dialogue'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- opening dialog boxes [WPF]
- dialog boxes [WPF], opening
ms.assetid: 6b1557d2-da98-4ef4-9f68-4089f04ab9ea
ms.openlocfilehash: 29fe8b0d516f20fcc742b91099a30e368dfe4548
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33546359"
---
# <a name="how-to-open-a-dialog-box"></a>Comment : ouvrir une boîte de dialogue
Cet exemple montre comment ouvrir une boîte de dialogue.  
  
## <a name="example"></a>Exemple  
 Une boîte de dialogue est une fenêtre qui est ouvert en instanciant <xref:System.Windows.Window> et en appelant le <xref:System.Windows.Window.ShowDialog%2A> (méthode). <xref:System.Windows.Window.ShowDialog%2A> Ouvre une fenêtre et ne retourne pas jusqu'à ce que la nouvelle boîte de dialogue a été fermée. Ce type de fenêtre est également appelé un *modale* fenêtre et il restreint l’entrée d’utilisateur.  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewdialogboxcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewdialogboxcode)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Appel de <xref:System.Windows.Window.ShowDialog%2A> requiert l’autorisation d’utiliser toutes les fenêtres et événements d’entrée d’utilisateur sans restriction.  
  
## <a name="see-also"></a>Voir aussi  
 [Retourner un résultat de boîte de dialogue](../../../../docs/framework/wpf/app-development/how-to-return-a-dialog-box-result.md)
