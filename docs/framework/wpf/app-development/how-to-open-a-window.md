---
title: 'Procédure : Ouvrez une fenêtre'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- windows [WPF], opening
- opening windows [WPF]
ms.assetid: 6b91b2bb-fda7-491d-a72e-139dd630a5b0
ms.openlocfilehash: 9ce7ffb3f46dd869fda7893745b531bd02d18ee1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373567"
---
# <a name="how-to-open-a-window"></a><span data-ttu-id="004a2-102">Procédure : Ouvrez une fenêtre</span><span class="sxs-lookup"><span data-stu-id="004a2-102">How to: Open a Window</span></span>
<span data-ttu-id="004a2-103">Cet exemple montre comment ouvrir une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="004a2-103">This example shows how to open a window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="004a2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="004a2-104">Example</span></span>  
 <span data-ttu-id="004a2-105">Une fenêtre est ouverte en instanciant <xref:System.Windows.Window> et en appelant le <xref:System.Windows.Window.Show%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="004a2-105">A window is opened by instantiating <xref:System.Windows.Window> and calling the <xref:System.Windows.Window.Show%2A> method.</span></span> <span data-ttu-id="004a2-106"><xref:System.Windows.Window.Show%2A> Ouvre une fenêtre et retourne immédiatement sans attendre que la nouvelle fenêtre à fermer.</span><span class="sxs-lookup"><span data-stu-id="004a2-106"><xref:System.Windows.Window.Show%2A> opens a window and returns immediately without waiting for the new window to close.</span></span> <span data-ttu-id="004a2-107">Ce type de fenêtre est également appelé un *non modale* fenêtre et ne restreint pas l’entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="004a2-107">This type of window is also known as a *modeless* window, and doesn't restrict user input.</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewwindowcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewwindowcode)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="004a2-108">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="004a2-108">.NET Framework Security</span></span>  
 <span data-ttu-id="004a2-109">L’instanciation <xref:System.Windows.Window> nécessite l’autorisation d’appeler des méthodes natives non sécurisées (voir <xref:System.Windows.Window.%23ctor%2A>).</span><span class="sxs-lookup"><span data-stu-id="004a2-109">Instantiating <xref:System.Windows.Window> requires permission to call unsafe native methods (see <xref:System.Windows.Window.%23ctor%2A>).</span></span>
