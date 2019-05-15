---
title: Comment afficher le composant PrintDialog
ms.date: 03/30/2017
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], displaying
- printing [Windows Forms], displaying print dialog box
ms.assetid: 745a8db7-0526-4b21-b09d-18e13ed32014
ms.openlocfilehash: de0acc655bbcf0cfc017d594545fae56cc27f981
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65637454"
---
# <a name="how-to-display-the-printdialog-component"></a><span data-ttu-id="9bafb-102">Comment afficher le composant PrintDialog</span><span class="sxs-lookup"><span data-stu-id="9bafb-102">How to display the PrintDialog component</span></span>

<span data-ttu-id="9bafb-103">Le <xref:System.Windows.Forms.PrintDialog> composant est la boîte de dialogue d’impression Windows standard qui la plupart de vos utilisateurs seront familiers.</span><span class="sxs-lookup"><span data-stu-id="9bafb-103">The <xref:System.Windows.Forms.PrintDialog> component is the standard Windows print dialog box that many of your users will be familiar with.</span></span> <span data-ttu-id="9bafb-104">Étant donné que vos utilisateurs seront immédiatement à l’aise avec lui, il serait préférable que vous pouvez utiliser le <xref:System.Windows.Forms.PrintDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="9bafb-104">Because your users will be immediately comfortable with it, it would be beneficial for you to use the <xref:System.Windows.Forms.PrintDialog> component.</span></span>

## <a name="to-display-the-printdialog-component"></a><span data-ttu-id="9bafb-105">Pour afficher le composant PrintDialog</span><span class="sxs-lookup"><span data-stu-id="9bafb-105">To display the PrintDialog component</span></span>

- <span data-ttu-id="9bafb-106">Appelez le <xref:System.Windows.Forms.Form.ShowDialog%2A> méthode à partir du code de votre application.</span><span class="sxs-lookup"><span data-stu-id="9bafb-106">Call the <xref:System.Windows.Forms.Form.ShowDialog%2A> method from within the code of your application.</span></span>

     <span data-ttu-id="9bafb-107">Une fois le composant affiché, les utilisateurs interagissent avec lui et définissent les propriétés du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9bafb-107">Once the component is shown, users will interact with it, setting the properties of the print job.</span></span> <span data-ttu-id="9bafb-108">Celles-ci sont enregistrées dans le <xref:System.Drawing.Printing.PrinterSettings> classe (et le <xref:System.Drawing.Printing.PageSettings> classe, si l’utilisateur accède à la [du composant PageSetupDialog](pagesetupdialog-component-windows-forms.md) via la <xref:System.Windows.Forms.PrintDialog> composant) associé à ce travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9bafb-108">These are saved in the  <xref:System.Drawing.Printing.PrinterSettings> class (and the <xref:System.Drawing.Printing.PageSettings> class, if the user accesses the [PageSetupDialog Component](pagesetupdialog-component-windows-forms.md) through the <xref:System.Windows.Forms.PrintDialog> component) associated with that print job.</span></span> <span data-ttu-id="9bafb-109">Vous pouvez ensuite faire des appels aux propriétés qu’elles définissent pour déterminer les caractéristiques du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9bafb-109">You can then make calls to the properties they set to determine the specifics of the print job.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bafb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bafb-110">See also</span></span>

- [<span data-ttu-id="9bafb-111">Guide pratique pour Créer des travaux d’impression Standard de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9bafb-111">How to: Create Standard Windows Forms Print Jobs</span></span>](../advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [<span data-ttu-id="9bafb-112">Guide pratique pour Capturer des entrées utilisateur à partir d’un composant PrintDialog au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="9bafb-112">How to: Capture User Input from a PrintDialog at Run Time</span></span>](../advanced/how-to-capture-user-input-from-a-printdialog-at-run-time.md)
- [<span data-ttu-id="9bafb-113">PrintPreviewDialog, contrôle</span><span class="sxs-lookup"><span data-stu-id="9bafb-113">PrintPreviewDialog Control</span></span>](printpreviewdialog-control-windows-forms.md)
- [<span data-ttu-id="9bafb-114">PrintDialog, composant</span><span class="sxs-lookup"><span data-stu-id="9bafb-114">PrintDialog Component</span></span>](printdialog-component-windows-forms.md)
- [<span data-ttu-id="9bafb-115">Prise en charge de l’impression dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9bafb-115">Windows Forms Print Support</span></span>](../advanced/windows-forms-print-support.md)
- [<span data-ttu-id="9bafb-116">Contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9bafb-116">Windows Forms Controls</span></span>](index.md)
