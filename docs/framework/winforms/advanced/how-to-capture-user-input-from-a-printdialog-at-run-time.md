---
title: 'Procédure : capturer des entrées utilisateur à partir d’un PrintDialog au moment de l’exécution'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print options [Windows Forms], changing at run time
- printing [Windows Forms], options
- print options
- run time [Windows Forms], changing print options
ms.assetid: 438501d8-9a70-4fb3-aae6-e46579aba0c6
ms.openlocfilehash: c1b0a7e66a4c2050ea5b92a55a39ea46a7b762c9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59176720"
---
# <a name="how-to-capture-user-input-from-a-printdialog-at-run-time"></a><span data-ttu-id="5dd43-102">Procédure : capturer des entrées utilisateur à partir d’un PrintDialog au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="5dd43-102">How to: Capture User Input from a PrintDialog at Run Time</span></span>
<span data-ttu-id="5dd43-103">Pendant que vous pouvez définir les options relatives à l’impression au moment du design, il est parfois utile de modifier ces options en cours d’exécution, probablement en raison des choix effectués par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5dd43-103">While you can set options related to printing at design time, you will sometimes want to change these options at run time, most likely because of choices made by the user.</span></span> <span data-ttu-id="5dd43-104">Vous pouvez capturer des entrées d’utilisateur pour l’impression d’un document à l’aide de la <xref:System.Windows.Forms.PrintDialog> et <xref:System.Drawing.Printing.PrintDocument> composants.</span><span class="sxs-lookup"><span data-stu-id="5dd43-104">You can capture user input for printing a document using the <xref:System.Windows.Forms.PrintDialog> and the <xref:System.Drawing.Printing.PrintDocument> components.</span></span>  
  
### <a name="to-change-print-options-programmatically"></a><span data-ttu-id="5dd43-105">Pour modifier les options d’impression par programmation</span><span class="sxs-lookup"><span data-stu-id="5dd43-105">To change print options programmatically</span></span>  
  
1.  <span data-ttu-id="5dd43-106">Ajouter un <xref:System.Windows.Forms.PrintDialog> et une <xref:System.Drawing.Printing.PrintDocument> à votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="5dd43-106">Add a <xref:System.Windows.Forms.PrintDialog> and a <xref:System.Drawing.Printing.PrintDocument> component to your form.</span></span>  
  
2.  <span data-ttu-id="5dd43-107">Définir le <xref:System.Windows.Forms.PrintDialog.Document%2A> propriété de la <xref:System.Windows.Forms.PrintDialog> à la <xref:System.Drawing.Printing.PrintDocument> ajouté au formulaire.</span><span class="sxs-lookup"><span data-stu-id="5dd43-107">Set the <xref:System.Windows.Forms.PrintDialog.Document%2A> property of the <xref:System.Windows.Forms.PrintDialog> to the <xref:System.Drawing.Printing.PrintDocument> added to the form.</span></span>  
  
    ```vb  
    PrintDialog1.Document = PrintDocument1  
    ```  
  
    ```csharp  
    printDialog1.Document = PrintDocument1;  
    ```  
  
    ```cpp  
    printDialog1->Document = PrintDocument1;  
    ```  
  
3.  <span data-ttu-id="5dd43-108">Afficher le <xref:System.Windows.Forms.PrintDialog> composant à l’aide de la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="5dd43-108">Display the <xref:System.Windows.Forms.PrintDialog> component by using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
    ```vb  
    PrintDialog1.ShowDialog()  
    ```  
  
    ```csharp  
    printDialog1.ShowDialog();  
    ```  
  
    ```cpp  
    printDialog1->ShowDialog();  
    ```  
  
4.  <span data-ttu-id="5dd43-109">Choix de l’impression de l’utilisateur à partir de la boîte de dialogue seront copiés vers le <xref:System.Drawing.Printing.PrinterSettings> propriété de la <xref:System.Drawing.Printing.PrintDocument> composant.</span><span class="sxs-lookup"><span data-stu-id="5dd43-109">The user's printing choices from the dialog will be copied to the <xref:System.Drawing.Printing.PrinterSettings> property of the <xref:System.Drawing.Printing.PrintDocument> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5dd43-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dd43-110">See also</span></span>

- [<span data-ttu-id="5dd43-111">Procédure : imprimer un fichier texte de plusieurs pages dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5dd43-111">How to: Print a Multi-Page Text File in Windows Forms</span></span>](how-to-print-a-multi-page-text-file-in-windows-forms.md)
- [<span data-ttu-id="5dd43-112">Prise en charge de l'impression dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5dd43-112">Windows Forms Print Support</span></span>](windows-forms-print-support.md)
