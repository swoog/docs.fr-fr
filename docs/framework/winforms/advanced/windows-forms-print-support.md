---
title: Prise en charge de l'impression dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, printing
- printing [Windows Forms]
- forms [Windows Forms], printing (using designer)
- printing [Windows Forms], Windows Forms, support
- printing [Windows Forms], print support
ms.assetid: a4a2960c-eb70-48e2-b641-cfb222704e46
ms.openlocfilehash: 8e008f2cb4b2f32cdba676e68d9fd790530e2b06
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011846"
---
# <a name="windows-forms-print-support"></a><span data-ttu-id="ee764-102">Prise en charge de l'impression dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ee764-102">Windows Forms Print Support</span></span>
<span data-ttu-id="ee764-103">L’impression dans Windows Forms consiste principalement à l’aide de la [du composant PrintDocument](../controls/printdocument-component-windows-forms.md) composant pour permettre aux utilisateurs d’imprimer et le [du contrôle PrintPreviewDialog](../controls/printpreviewdialog-control-windows-forms.md) contrôle, [PrintDialog Composant](../controls/printdialog-component-windows-forms.md) et [du composant PageSetupDialog](../controls/pagesetupdialog-component-windows-forms.md) composants pour fournir une interface graphique familière aux utilisateurs habitués au système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="ee764-103">Printing in Windows Forms consists primarily of using the [PrintDocument Component](../controls/printdocument-component-windows-forms.md) component to enable the user to print, and the [PrintPreviewDialog Control](../controls/printpreviewdialog-control-windows-forms.md) control, [PrintDialog Component](../controls/printdialog-component-windows-forms.md) and [PageSetupDialog Component](../controls/pagesetupdialog-component-windows-forms.md) components to provide a familiar graphical interface to users accustomed to the Windows operating system.</span></span>  
  
 <span data-ttu-id="ee764-104">En général, vous créez une nouvelle instance de la <xref:System.Drawing.Printing.PrintDocument> composant, définir les propriétés qui décrivent les éléments à imprimer à l’aide de la <xref:System.Drawing.Printing.PrinterSettings> et <xref:System.Drawing.Printing.PageSettings> classes, puis appelez le <xref:System.Drawing.Printing.PrintDocument.Print%2A> méthode réellement imprimer le document.</span><span class="sxs-lookup"><span data-stu-id="ee764-104">Typically, you create a new instance of the <xref:System.Drawing.Printing.PrintDocument> component, set the properties that describe what to print using the <xref:System.Drawing.Printing.PrinterSettings> and <xref:System.Drawing.Printing.PageSettings> classes, and call the <xref:System.Drawing.Printing.PrintDocument.Print%2A> method to actually print the document.</span></span>  
  
 <span data-ttu-id="ee764-105">Au cours de l’impression à partir d’une application Windows, le <xref:System.Drawing.Printing.PrintDocument> composant affiche une boîte de dialogue d’impression d’annulation pour alerter les utilisateurs au fait que l’impression est en cours et pour permettre le travail d’impression doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="ee764-105">During the course of printing from a Windows-based application, the <xref:System.Drawing.Printing.PrintDocument> component will show an abort print dialog box to alert users to the fact that printing is occurring and to allow the print job to be canceled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ee764-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ee764-106">In This Section</span></span>  
 [<span data-ttu-id="ee764-107">Guide pratique pour Créer des travaux d’impression Standard de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ee764-107">How to: Create Standard Windows Forms Print Jobs</span></span>](how-to-create-standard-windows-forms-print-jobs.md)  
 <span data-ttu-id="ee764-108">Explique comment utiliser le <xref:System.Drawing.Printing.PrintDocument> composant pour imprimer à partir d’un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="ee764-108">Explains how to use the <xref:System.Drawing.Printing.PrintDocument> component to print from a Windows Form.</span></span>  
  
 [<span data-ttu-id="ee764-109">Guide pratique pour Capturer des entrées utilisateur à partir d’un composant PrintDialog au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="ee764-109">How to: Capture User Input from a PrintDialog at Run Time</span></span>](how-to-capture-user-input-from-a-printdialog-at-run-time.md)  
 <span data-ttu-id="ee764-110">Explique comment modifier les options d’impression sélectionnées par programmation en utilisant le <xref:System.Windows.Forms.PrintDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="ee764-110">Explains how to modify selected print options programmatically using the <xref:System.Windows.Forms.PrintDialog> component.</span></span>  
  
 [<span data-ttu-id="ee764-111">Guide pratique pour Choisir les imprimantes connectées à l’ordinateur d’un utilisateur dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ee764-111">How to: Choose the Printers Attached to a User's Computer in Windows Forms</span></span>](how-to-choose-the-printers-attached-to-user-computer-in-windows-forms.md)  
 <span data-ttu-id="ee764-112">Décrit la modification de l’imprimante pour imprimer à l’utilisation de la <xref:System.Windows.Forms.PrintDialog> composant en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ee764-112">Describes changing the printer to print to using the <xref:System.Windows.Forms.PrintDialog> component at run time.</span></span>  
  
 [<span data-ttu-id="ee764-113">Guide pratique pour Imprimer des graphiques dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ee764-113">How to: Print Graphics in Windows Forms</span></span>](how-to-print-graphics-in-windows-forms.md)  
 <span data-ttu-id="ee764-114">Décrit l’envoi de graphismes à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ee764-114">Describes sending graphics to the printer.</span></span>  
  
 [<span data-ttu-id="ee764-115">Guide pratique pour Imprimer un fichier texte de plusieurs pages dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ee764-115">How to: Print a Multi-Page Text File in Windows Forms</span></span>](how-to-print-a-multi-page-text-file-in-windows-forms.md)  
 <span data-ttu-id="ee764-116">Décrit l’envoi de texte à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ee764-116">Describes sending text to the printer.</span></span>  
  
 [<span data-ttu-id="ee764-117">Guide pratique pour Travaux d’impression de complète Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ee764-117">How to: Complete Windows Forms Print Jobs</span></span>](how-to-complete-windows-forms-print-jobs.md)  
 <span data-ttu-id="ee764-118">Explique comment avertir les utilisateurs de l’achèvement d’un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="ee764-118">Explains how to alert users to the completion of a print job.</span></span>  
  
 [<span data-ttu-id="ee764-119">Guide pratique pour Imprimer un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="ee764-119">How to: Print a Windows Form</span></span>](how-to-print-a-windows-form.md)  
 <span data-ttu-id="ee764-120">Montre comment imprimer une copie de l’écran actuel.</span><span class="sxs-lookup"><span data-stu-id="ee764-120">Shows how to print a copy of the current form.</span></span>  
  
 [<span data-ttu-id="ee764-121">Guide pratique pour Imprimer dans les formulaires de Windows à l’aide de l’aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="ee764-121">How to: Print in Windows Forms Using Print Preview</span></span>](how-to-print-in-windows-forms-using-print-preview.md)  
 <span data-ttu-id="ee764-122">Montre comment utiliser un <xref:System.Windows.Forms.PrintPreviewDialog> pour imprimer un document.</span><span class="sxs-lookup"><span data-stu-id="ee764-122">Shows how to use a <xref:System.Windows.Forms.PrintPreviewDialog> for printing a document.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="ee764-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee764-123">Related Sections</span></span>  
 [<span data-ttu-id="ee764-124">Composant PrintDocument</span><span class="sxs-lookup"><span data-stu-id="ee764-124">PrintDocument Component</span></span>](../controls/printdocument-component-windows-forms.md)  
 <span data-ttu-id="ee764-125">Explique comment utiliser le <xref:System.Drawing.Printing.PrintDocument> composant.</span><span class="sxs-lookup"><span data-stu-id="ee764-125">Explains usage of the <xref:System.Drawing.Printing.PrintDocument> component.</span></span>  
  
 [<span data-ttu-id="ee764-126">PrintDialog, composant</span><span class="sxs-lookup"><span data-stu-id="ee764-126">PrintDialog Component</span></span>](../controls/printdialog-component-windows-forms.md)  
 <span data-ttu-id="ee764-127">Explique comment utiliser le <xref:System.Windows.Forms.PrintDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="ee764-127">Explains usage of the <xref:System.Windows.Forms.PrintDialog> component.</span></span>  
  
 [<span data-ttu-id="ee764-128">PrintPreviewDialog, contrôle</span><span class="sxs-lookup"><span data-stu-id="ee764-128">PrintPreviewDialog Control</span></span>](../controls/printpreviewdialog-control-windows-forms.md)  
 <span data-ttu-id="ee764-129">Explique comment utiliser le <xref:System.Windows.Forms.PrintPreviewDialog> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ee764-129">Explains usage of the <xref:System.Windows.Forms.PrintPreviewDialog> control.</span></span>  
  
 [<span data-ttu-id="ee764-130">PageSetupDialog, composant</span><span class="sxs-lookup"><span data-stu-id="ee764-130">PageSetupDialog Component</span></span>](../controls/pagesetupdialog-component-windows-forms.md)  
 <span data-ttu-id="ee764-131">Explique comment utiliser le <xref:System.Windows.Forms.PageSetupDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="ee764-131">Explains usage of the <xref:System.Windows.Forms.PageSetupDialog> component.</span></span>  
  
 <xref:System.Drawing.Printing>  
 <span data-ttu-id="ee764-132">Décrit les classes dans le <xref:System.Drawing.Printing> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ee764-132">Describes the classes in the <xref:System.Drawing.Printing> namespace.</span></span>
