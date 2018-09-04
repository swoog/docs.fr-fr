---
title: "Comment : gérer des événements d'entrée d'utilisateur dans les contrôles Windows Forms"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, user input
- user input [Windows Forms], Windows Forms controls
ms.assetid: 3de74dcf-fae3-42d0-92b5-bc04a61a6888
ms.openlocfilehash: 3b15edfec25282d5a0b79ef48cabd2a27c694055
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43533000"
---
# <a name="how-to-handle-user-input-events-in-windows-forms-controls"></a><span data-ttu-id="968df-102">Comment : gérer des événements d'entrée d'utilisateur dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="968df-102">How to: Handle User Input Events in Windows Forms Controls</span></span>
<span data-ttu-id="968df-103">Cet exemple montre comment gérer la plupart des événements de clavier, de souris, de focus et de validation qui peuvent se produire dans un contrôle Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="968df-103">This example demonstrates how to handle most keyboard, mouse, focus, and validation events that can occur in a Windows Forms control.</span></span> <span data-ttu-id="968df-104">La zone de texte nommée `TextBoxInput` reçoit les événements quand elle a le focus et les informations relatives à chaque événement sont écrites dans la zone de texte nommée `TextBoxOutput` dans l'ordre dans lequel les événements sont déclenchés.</span><span class="sxs-lookup"><span data-stu-id="968df-104">The text box named `TextBoxInput` receives the events when it has focus, and information about each event is written in the text box named `TextBoxOutput` in the order in which the events are raised.</span></span> <span data-ttu-id="968df-105">L'application comprend également un ensemble de cases à cocher qui peuvent servir à filtrer les événements pour lesquels établir un rapport.</span><span class="sxs-lookup"><span data-stu-id="968df-105">The application also includes a set of check boxes that can be used to filter which events to report.</span></span>  
  
## <a name="example"></a><span data-ttu-id="968df-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="968df-106">Example</span></span>  
 [!code-cpp[System.Windows.Forms.UserInputWalkthrough#0](../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/cpp/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.UserInputWalkthrough#0](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.UserInputWalkthrough#0](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="968df-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="968df-107">Compiling the Code</span></span>  
 <span data-ttu-id="968df-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="968df-108">This example requires:</span></span>  
  
-   <span data-ttu-id="968df-109">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="968df-109">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="968df-110">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="968df-110">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="968df-111">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="968df-111">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="968df-112">Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="968df-112">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="968df-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="968df-113">See Also</span></span>  
 [<span data-ttu-id="968df-114">Entrées d’utilisateur dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="968df-114">User Input in Windows Forms</span></span>](../../../docs/framework/winforms/user-input-in-windows-forms.md)
