---
title: 'Procédure : Ouvrir une boîte de dialogue'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- opening dialog boxes [WPF]
- dialog boxes [WPF], opening
ms.assetid: 6b1557d2-da98-4ef4-9f68-4089f04ab9ea
ms.openlocfilehash: 70ac31285dd22244b4bd6ad0d188d182eb6e6264
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947704"
---
# <a name="how-to-open-a-dialog-box"></a><span data-ttu-id="4889b-102">Procédure : Ouvrir une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="4889b-102">How to: Open a Dialog Box</span></span>
<span data-ttu-id="4889b-103">Cet exemple montre comment ouvrir une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4889b-103">This example shows how to open a dialog box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4889b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="4889b-104">Example</span></span>  
 <span data-ttu-id="4889b-105">Une boîte de dialogue est une fenêtre est ouverte en instanciant <xref:System.Windows.Window> et en appelant le <xref:System.Windows.Window.ShowDialog%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4889b-105">A dialog box is a window that is opened by instantiating <xref:System.Windows.Window> and calling the <xref:System.Windows.Window.ShowDialog%2A> method.</span></span> <span data-ttu-id="4889b-106"><xref:System.Windows.Window.ShowDialog%2A> Ouvre une fenêtre et ne retourne pas jusqu'à ce que la nouvelle boîte de dialogue a été fermée.</span><span class="sxs-lookup"><span data-stu-id="4889b-106"><xref:System.Windows.Window.ShowDialog%2A> opens a window and doesn't return until the new dialog box has been closed.</span></span> <span data-ttu-id="4889b-107">Ce type de fenêtre est également appelé un *modale* fenêtre et restreint l’entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4889b-107">This type of window is also known as a *modal* window, and restricts user input.</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewdialogboxcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewdialogboxcode)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="4889b-108">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4889b-108">.NET Framework Security</span></span>  
 <span data-ttu-id="4889b-109">Appel <xref:System.Windows.Window.ShowDialog%2A> nécessite l’autorisation d’utiliser toutes les fenêtres et événements d’entrée d’utilisateur sans restriction.</span><span class="sxs-lookup"><span data-stu-id="4889b-109">Calling <xref:System.Windows.Window.ShowDialog%2A> requires permission to use all windows and user input events without restriction.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4889b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4889b-110">See also</span></span>

- [<span data-ttu-id="4889b-111">Retourner un résultat de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="4889b-111">Return a Dialog Box Result</span></span>](how-to-return-a-dialog-box-result.md)
