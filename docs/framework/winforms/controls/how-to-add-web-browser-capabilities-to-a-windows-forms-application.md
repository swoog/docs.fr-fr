---
title: 'Procédure : ajouter des fonctionnalités de navigateur web à une application Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- WebBrowser control [Windows Forms], adding Web browser capabilities to your application
- WebBrowser control [Windows Forms], examples
- Web browsers [.NET Framework], adding to Windows Forms
- examples [Windows Forms], WebBrowser control
- Windows Forms, adding Web browser functionality
ms.assetid: 3871f072-b57a-435b-9976-e5da28df04a7
ms.openlocfilehash: 29422ad384240b017b279795d07e3c8100fae493
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208798"
---
# <a name="how-to-add-web-browser-capabilities-to-a-windows-forms-application"></a><span data-ttu-id="e7ad5-102">Procédure : ajouter des fonctionnalités de navigateur web à une application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e7ad5-102">How to: Add Web Browser Capabilities to a Windows Forms Application</span></span>
<span data-ttu-id="e7ad5-103">Avec le contrôle <xref:System.Windows.Forms.WebBrowser>, vous pouvez ajouter des fonctionnalités de navigateur web à votre application.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-103">With the <xref:System.Windows.Forms.WebBrowser> control, you can add Web browser functionality to your application.</span></span> <span data-ttu-id="e7ad5-104">Le contrôle fonctionne comme un navigateur web par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-104">The control works like a Web browser by default.</span></span> <span data-ttu-id="e7ad5-105">Après avoir chargé une URL initiale en définissant la propriété <xref:System.Windows.Forms.WebBrowser.Url%2A>, vous pouvez naviguer en cliquant sur des liens hypertexte ou en utilisant des raccourcis clavier pour parcourir l'historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-105">After you load an initial URL by setting the <xref:System.Windows.Forms.WebBrowser.Url%2A> property, you can navigate by clicking hyperlinks or by using keyboard shortcuts to move backward and forward through navigation history.</span></span> <span data-ttu-id="e7ad5-106">Par défaut, vous pouvez accéder à d'autres fonctionnalités de navigateur via le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-106">By default, you can access additional browser functionality through the right-click shortcut menu.</span></span> <span data-ttu-id="e7ad5-107">Vous pouvez aussi ouvrir de nouveaux documents en les déposant sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-107">You can also open new documents by dropping them onto the control.</span></span> <span data-ttu-id="e7ad5-108">Le contrôle <xref:System.Windows.Forms.WebBrowser> possède également plusieurs propriétés, méthodes et événements que vous pouvez utiliser pour implémenter des fonctionnalités d'interface utilisateur semblables à celles d'Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-108">The <xref:System.Windows.Forms.WebBrowser> control also has several properties, methods, and events that you can use to implement user interface features similar to those found in Internet Explorer.</span></span>  
  
 <span data-ttu-id="e7ad5-109">L’exemple de code suivant implémente une barre d’adresses, des boutons de navigateur courants, un menu **Fichier**, une barre d’état et une barre de titre qui affiche le titre de la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-109">The following code example implements an address bar, typical browser buttons, a **File** menu, a status bar, and a title bar that displays the current page title.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e7ad5-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="e7ad5-110">Example</span></span>  
 [!code-cpp[System.Windows.Forms.WebBrowser#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.WebBrowser/CPP/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.WebBrowser#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.WebBrowser/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.WebBrowser#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.WebBrowser/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e7ad5-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e7ad5-111">Compiling the Code</span></span>  
 <span data-ttu-id="e7ad5-112">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="e7ad5-112">This example requires:</span></span>  
  
-   <span data-ttu-id="e7ad5-113">des références aux assemblys `System`, `System.Drawing` et `System.Windows.Forms`.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-113">References to the `System`, `System.Drawing`, and `System.Windows.Forms` assemblies.</span></span>  
  
 <span data-ttu-id="e7ad5-114">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="e7ad5-114">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="e7ad5-115">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="e7ad5-115">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7ad5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7ad5-116">See also</span></span>

- <xref:System.Windows.Forms.WebBrowser>
- [<span data-ttu-id="e7ad5-117">WebBrowser, contrôle</span><span class="sxs-lookup"><span data-stu-id="e7ad5-117">WebBrowser Control</span></span>](webbrowser-control-windows-forms.md)
