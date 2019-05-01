---
title: 'Procédure : Retourner un résultat de boîte de dialogue'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dialog boxes [WPF], returning results
ms.assetid: 4c5cf286-746b-4052-934d-d80cbf8acba3
ms.openlocfilehash: b574a5bbc08d947371837116915c2fc8c13ec81d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62006706"
---
# <a name="how-to-return-a-dialog-box-result"></a>Procédure : Retourner un résultat de boîte de dialogue
Cet exemple montre comment récupérer le résultat de la boîte de dialogue pour une fenêtre est ouverte en appelant <xref:System.Windows.Window.ShowDialog%2A>.  
  
## <a name="example"></a>Exemple  
 Avant qu’une boîte de dialogue se ferme, son <xref:System.Windows.Window.DialogResult%2A> propriété doit être définie avec un <xref:System.Nullable%601> <xref:System.Boolean> qui indique la façon dont l’utilisateur a fermé la boîte de dialogue. Cette valeur est retournée par <xref:System.Windows.Window.ShowDialog%2A> pour permettre au code client déterminer comment la boîte de dialogue a été fermée et, par conséquent, comment traiter le résultat.  
  
> [!NOTE]
>  <xref:System.Windows.Window.DialogResult%2A> peut être défini uniquement si une fenêtre a été ouverte en appelant <xref:System.Windows.Window.ShowDialog%2A>.  
  
 [!code-csharp[HOWTOWindowManagementSnippets#GetDialogResultCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#getdialogresultcode)]
 [!code-vb[HOWTOWindowManagementSnippets#GetDialogResultCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#getdialogresultcode)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Appel <xref:System.Windows.Window.ShowDialog%2A> nécessite l’autorisation d’utiliser toutes les fenêtres et événements d’entrée d’utilisateur sans restriction.
