---
title: "Comment : créer un Windows Form redimensionnable pour l'entrée de données"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- layout [Windows Forms], resizing
- forms [Windows Forms], creating resizable
- Windows Forms, resizable
ms.assetid: babdf198-404c-485d-a914-ed370c6ecd99
ms.openlocfilehash: a319fba43c6735cd5552dd71d1fb614a6192da97
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44205742"
---
# <a name="how-to-create-a-resizable-windows-form-for-data-entry"></a><span data-ttu-id="fe60f-102">Comment : créer un Windows Form redimensionnable pour l'entrée de données</span><span class="sxs-lookup"><span data-stu-id="fe60f-102">How to: Create a Resizable Windows Form for Data Entry</span></span>
<span data-ttu-id="fe60f-103">Une bonne disposition répond correctement aux modifications des dimensions de son formulaire parent.</span><span class="sxs-lookup"><span data-stu-id="fe60f-103">A good layout responds well to changes in the dimensions of its parent form.</span></span> <span data-ttu-id="fe60f-104">Vous pouvez utiliser le contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour organiser la disposition de votre formulaire afin de redimensionner et de positionner vos contrôles de façon cohérente à mesure que les dimensions du formulaire changent.</span><span class="sxs-lookup"><span data-stu-id="fe60f-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to arrange the layout of your form to resize and position your controls in a consistent way as the form's dimensions change.</span></span> <span data-ttu-id="fe60f-105">Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> est également utile quand des modifications du contenu de vos contrôles entraîne une modification de la disposition.</span><span class="sxs-lookup"><span data-stu-id="fe60f-105">The <xref:System.Windows.Forms.TableLayoutPanel> control is also useful when changes in the contents of your controls cause changes in the layout.</span></span> <span data-ttu-id="fe60f-106">Vous pouvez effectuer les tâches décrites dans cette procédure dans l'environnement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fe60f-106">The process covered in this procedure can be done within the Visual Studio environment.</span></span>  <span data-ttu-id="fe60f-107">Consultez également [Procédure pas à pas : création d’un Windows Form redimensionnable pour l’entrée de données](https://msdn.microsoft.com/library/991eahec\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="fe60f-107">Also see [Walkthrough: Creating a Resizable Windows Form for Data Entry](https://msdn.microsoft.com/library/991eahec\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="fe60f-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe60f-108">Example</span></span>  
 <span data-ttu-id="fe60f-109">L'exemple suivant montre comment utiliser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour générer une disposition qui répond correctement quand l'utilisateur redimensionne le formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe60f-109">The following example demonstrates how to use a <xref:System.Windows.Forms.TableLayoutPanel> control to build a layout that responds well when the user resizes the form.</span></span> <span data-ttu-id="fe60f-110">Il illustre également une disposition qui répond correctement à la localisation.</span><span class="sxs-lookup"><span data-stu-id="fe60f-110">It also demonstrates a layout that responds well to localization.</span></span>  
  
 [!code-cpp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/cpp/basicdataentryform.cpp#1)]
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/CS/basicdataentryform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/VB/basicdataentryform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fe60f-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="fe60f-111">Compiling the Code</span></span>  
 <span data-ttu-id="fe60f-112">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="fe60f-112">This example requires:</span></span>  
  
-   <span data-ttu-id="fe60f-113">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="fe60f-113">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="fe60f-114">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="fe60f-114">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="fe60f-115">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="fe60f-115">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="fe60f-116">Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="fe60f-116">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe60f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe60f-117">See Also</span></span>  
 <xref:System.Windows.Forms.FlowLayoutPanel>  
 <xref:System.Windows.Forms.TableLayoutPanel>  
 [<span data-ttu-id="fe60f-118">Guide pratique pour ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="fe60f-118">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 [<span data-ttu-id="fe60f-119">Guide pratique pour créer une présentation Windows Forms qui répond bien à la localisation</span><span class="sxs-lookup"><span data-stu-id="fe60f-119">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>](../../../../docs/framework/winforms/controls/how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)  
 [<span data-ttu-id="fe60f-120">Expérience utilisateur Microsoft Windows, Recommandations officielles à destination des développeurs et des concepteurs d’interfaces utilisateur. Redmond, WA: Microsoft Press, 1999. (USBN : 0-7356-0566-1)</span><span class="sxs-lookup"><span data-stu-id="fe60f-120">Microsoft Windows User Experience, Official Guidelines for User Interface Developers and Designers. Redmond, WA: Microsoft Press, 1999. (USBN: 0-7356-0566-1)</span></span>](https://www.microsoft.com/mspress/southpacific/books/book11588.htm)
