---
title: "Comment : imprimer des zones clientes et non clientes d'un formulaire (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- title bar [Visual Basic], printing
- printing
- borders [Visual Basic], printing
- entire form
- non-client area [Visual Basic], printing
ms.assetid: 856bb0e4-dbc3-47e2-81cd-4b376cf07757
ms.openlocfilehash: 5109993146a8d53d5cbeebcc52c018a6f0f57ed5
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43856736"
---
# <a name="how-to-print-client-and-non-client-areas-of-a-form-visual-basic"></a><span data-ttu-id="9a053-102">Comment : imprimer des zones clientes et non clientes d'un formulaire (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9a053-102">How to: Print Client and Non-Client Areas of a Form (Visual Basic)</span></span>
<span data-ttu-id="9a053-103">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> vous permet d’imprimer rapidement une image d’un formulaire tel qu’il apparaît à l’écran sans utiliser un composant <xref:System.Drawing.Printing.PrintDocument> .</span><span class="sxs-lookup"><span data-stu-id="9a053-103">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component enables you to quickly print an image of a form exactly as it appears on screen without using a <xref:System.Drawing.Printing.PrintDocument> component.</span></span> <span data-ttu-id="9a053-104">La procédure suivante montre comment imprimer un formulaire, y compris la zone cliente et la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="9a053-104">The following procedure shows how to print a form, including both the client area and the non-client area.</span></span> <span data-ttu-id="9a053-105">La zone non cliente comprend la barre de titre, les bordures et les barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="9a053-105">The non-client area includes the title bar, borders, and scroll bars.</span></span>  
  
 <span data-ttu-id="9a053-106">Les contrôles PowerPack ne sont plus inclus dans Visual Studio, mais vous pouvez les télécharger à partir de la [centre de téléchargement](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span><span class="sxs-lookup"><span data-stu-id="9a053-106">The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span></span>  
  
### <a name="to-print-both-the-client-and-the-non-client-areas-of-a-form"></a><span data-ttu-id="9a053-107">Pour imprimer à la fois les zones clientes et les zones non clientes d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="9a053-107">To print both the client and the non-client areas of a form</span></span>  
  
1.  <span data-ttu-id="9a053-108">Dans la **Boîte à outils**, cliquez sur l’onglet **Visual Basic PowerPacks** , puis faites glisser le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9a053-108">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="9a053-109">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> est ajouté à la barre d’état des composants.</span><span class="sxs-lookup"><span data-stu-id="9a053-109">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="9a053-110">Dans la fenêtre **Propriétés** , définissez la propriété <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> sur <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span><span class="sxs-lookup"><span data-stu-id="9a053-110">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span></span>  
  
3.  <span data-ttu-id="9a053-111">Ajoutez le code suivant dans le gestionnaire d’événements approprié (par exemple, dans le  gestionnaire d’événements `Click` pour un `Button`Imprimer).</span><span class="sxs-lookup"><span data-stu-id="9a053-111">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a Print `Button`).</span></span>  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.FullWindow)  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="9a053-112">Sur certains systèmes d’exploitation, le texte ou les graphiques dessinés par des méthodes <xref:System.Drawing.Graphics> peuvent ne pas s’imprimer correctement.</span><span class="sxs-lookup"><span data-stu-id="9a053-112">On some operating systems, text or graphics drawn by <xref:System.Drawing.Graphics> methods may not print correctly.</span></span> <span data-ttu-id="9a053-113">Dans ce cas, utilisez la méthode d’impression compatible : `PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.CompatibleModeFullWindow`).</span><span class="sxs-lookup"><span data-stu-id="9a053-113">In this case, use the compatible printing method: `PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.CompatibleModeFullWindow`).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a053-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a053-114">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print%2A>  
 [<span data-ttu-id="9a053-115">PrintForm, composant</span><span class="sxs-lookup"><span data-stu-id="9a053-115">PrintForm Component</span></span>](../../../visual-basic/developing-apps/printing/printform-component.md)  
 [<span data-ttu-id="9a053-116">Guide pratique : imprimer un formulaire à défilement variable</span><span class="sxs-lookup"><span data-stu-id="9a053-116">How to: Print a Scrollable Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-a-scrollable-form.md)
