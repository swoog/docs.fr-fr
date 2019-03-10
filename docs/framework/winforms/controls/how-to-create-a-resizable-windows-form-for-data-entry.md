---
title: 'Procédure : Créer un formulaire Windows redimensionnable pour l’entrée de données'
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
ms.openlocfilehash: 57c6d30b63b15f5e57e813c1deb90d3da5a5ba35
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57705712"
---
# <a name="how-to-create-a-resizable-windows-form-for-data-entry"></a><span data-ttu-id="f2fdd-102">Procédure : Créer un formulaire Windows redimensionnable pour l’entrée de données</span><span class="sxs-lookup"><span data-stu-id="f2fdd-102">How to: Create a Resizable Windows Form for Data Entry</span></span>
<span data-ttu-id="f2fdd-103">Une bonne disposition répond correctement aux modifications des dimensions de son formulaire parent.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-103">A good layout responds well to changes in the dimensions of its parent form.</span></span> <span data-ttu-id="f2fdd-104">Vous pouvez utiliser le contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour organiser la disposition de votre formulaire afin de redimensionner et de positionner vos contrôles de façon cohérente à mesure que les dimensions du formulaire changent.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to arrange the layout of your form to resize and position your controls in a consistent way as the form's dimensions change.</span></span> <span data-ttu-id="f2fdd-105">Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> est également utile quand des modifications du contenu de vos contrôles entraîne une modification de la disposition.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-105">The <xref:System.Windows.Forms.TableLayoutPanel> control is also useful when changes in the contents of your controls cause changes in the layout.</span></span> <span data-ttu-id="f2fdd-106">Vous pouvez effectuer les tâches décrites dans cette procédure dans l'environnement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-106">The process covered in this procedure can be done within the Visual Studio environment.</span></span>  <span data-ttu-id="f2fdd-107">Consultez également [procédure pas à pas : Création d’un formulaire Windows redimensionnable pour l’entrée de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f2fdd-107">Also see [Walkthrough: Creating a Resizable Windows Form for Data Entry](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f2fdd-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2fdd-108">Example</span></span>  
 <span data-ttu-id="f2fdd-109">L'exemple suivant montre comment utiliser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour générer une disposition qui répond correctement quand l'utilisateur redimensionne le formulaire.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-109">The following example demonstrates how to use a <xref:System.Windows.Forms.TableLayoutPanel> control to build a layout that responds well when the user resizes the form.</span></span> <span data-ttu-id="f2fdd-110">Il illustre également une disposition qui répond correctement à la localisation.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-110">It also demonstrates a layout that responds well to localization.</span></span>  
  
 [!code-cpp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/cpp/basicdataentryform.cpp#1)]
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/CS/basicdataentryform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/VB/basicdataentryform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f2fdd-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f2fdd-111">Compiling the Code</span></span>  
 <span data-ttu-id="f2fdd-112">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="f2fdd-112">This example requires:</span></span>  
  
-   <span data-ttu-id="f2fdd-113">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-113">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="f2fdd-114">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="f2fdd-114">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="f2fdd-115">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="f2fdd-115">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2fdd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2fdd-116">See also</span></span>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [<span data-ttu-id="f2fdd-117">Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="f2fdd-117">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="f2fdd-118">Guide pratique pour Créer qu'un Windows Forms de disposition qui répond bien à la localisation</span><span class="sxs-lookup"><span data-stu-id="f2fdd-118">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>](how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)
- [<span data-ttu-id="f2fdd-119">Expérience utilisateur Microsoft Windows, Recommandations officielles à destination des développeurs et des concepteurs d’interfaces utilisateur. Redmond, Washington : Microsoft Press, 1999. (USBN : 0-7356-0566-1)</span><span class="sxs-lookup"><span data-stu-id="f2fdd-119">Microsoft Windows User Experience, Official Guidelines for User Interface Developers and Designers. Redmond, WA: Microsoft Press, 1999. (USBN: 0-7356-0566-1)</span></span>](https://www.microsoft.com/mspress/southpacific/books/book11588.htm)
