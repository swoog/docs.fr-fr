---
title: 'Procédure : Imprimer un formulaire à l’aide du composant PrintForm (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Form [Visual Basic], printing
ms.assetid: df963bf6-3ee1-49f4-8b2e-1d95d1beb0be
ms.openlocfilehash: 0a1a62627390c8839625862b9d43d61fc07ebf12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521567"
---
# <a name="how-to-print-a-form-by-using-the-printform-component-visual-basic"></a><span data-ttu-id="6449e-102">Procédure : Imprimer un formulaire à l’aide du composant PrintForm (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6449e-102">How to: Print a Form by Using the PrintForm Component (Visual Basic)</span></span>
<span data-ttu-id="6449e-103">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> vous permet d’imprimer rapidement une image d’un formulaire tel qu’il apparaît à l’écran sans utiliser un composant <xref:System.Drawing.Printing.PrintDocument> .</span><span class="sxs-lookup"><span data-stu-id="6449e-103">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component enables you to quickly print an image of a form exactly as it appears on screen without using a <xref:System.Drawing.Printing.PrintDocument> component.</span></span> <span data-ttu-id="6449e-104">Les procédures suivantes montrent comment imprimer un formulaire sur une imprimante, dans une fenêtre d’aperçu avant impression et dans un fichier PostScript encapsulé.</span><span class="sxs-lookup"><span data-stu-id="6449e-104">The following procedures show how to print a form to a printer, to a print preview window, and to an Encapsulated PostScript file.</span></span>  
  
 <span data-ttu-id="6449e-105">Les contrôles PowerPack ne sont plus inclus dans Visual Studio, mais vous pouvez les télécharger à partir du [Centre de téléchargement](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span><span class="sxs-lookup"><span data-stu-id="6449e-105">The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span></span>  
  
### <a name="to-print-a-form-to-the-default-printer"></a><span data-ttu-id="6449e-106">Pour imprimer un formulaire sur l’imprimante par défaut</span><span class="sxs-lookup"><span data-stu-id="6449e-106">To print a form to the default printer</span></span>  
  
1.  <span data-ttu-id="6449e-107">Dans la **Boîte à outils**, cliquez sur l’onglet **Visual Basic PowerPacks** , puis faites glisser le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6449e-107">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="6449e-108">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> est ajouté à la barre d’état des composants.</span><span class="sxs-lookup"><span data-stu-id="6449e-108">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="6449e-109">Dans la fenêtre **Propriétés** , définissez la propriété <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> sur <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span><span class="sxs-lookup"><span data-stu-id="6449e-109">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span></span>  
  
3.  <span data-ttu-id="6449e-110">Ajoutez le code suivant dans le Gestionnaire d’événements approprié (par exemple, dans le `Click` Gestionnaire d’événements pour un **impression**`Button`).</span><span class="sxs-lookup"><span data-stu-id="6449e-110">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print()  
    ```  
  
### <a name="to-display-a-form-in-a-print-preview-window"></a><span data-ttu-id="6449e-111">Pour afficher un formulaire dans une fenêtre d’aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="6449e-111">To display a form in a print preview window</span></span>  
  
1.  <span data-ttu-id="6449e-112">Dans la **Boîte à outils**, cliquez sur l’onglet **Visual Basic PowerPacks** , puis faites glisser le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6449e-112">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="6449e-113">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> est ajouté à la barre d’état des composants.</span><span class="sxs-lookup"><span data-stu-id="6449e-113">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="6449e-114">Dans la fenêtre **Propriétés** , définissez la propriété <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> sur <xref:System.Drawing.Printing.PrintAction.PrintToPreview>.</span><span class="sxs-lookup"><span data-stu-id="6449e-114">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPreview>.</span></span>  
  
3.  <span data-ttu-id="6449e-115">Ajoutez le code suivant dans le Gestionnaire d’événements approprié (par exemple, dans le `Click` Gestionnaire d’événements pour un **impression**`Button`).</span><span class="sxs-lookup"><span data-stu-id="6449e-115">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print()  
    ```  
  
### <a name="to-print-a-form-to-a-file"></a><span data-ttu-id="6449e-116">Pour imprimer un formulaire dans un fichier</span><span class="sxs-lookup"><span data-stu-id="6449e-116">To print a form to a file</span></span>  
  
1.  <span data-ttu-id="6449e-117">Dans la **Boîte à outils**, cliquez sur l’onglet **Visual Basic PowerPacks** , puis faites glisser le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6449e-117">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="6449e-118">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> est ajouté à la barre d’état des composants.</span><span class="sxs-lookup"><span data-stu-id="6449e-118">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="6449e-119">Dans la fenêtre **Propriétés** , définissez la propriété <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> sur <xref:System.Drawing.Printing.PrintAction.PrintToFile>.</span><span class="sxs-lookup"><span data-stu-id="6449e-119">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToFile>.</span></span>  
  
3.  <span data-ttu-id="6449e-120">Si vous le souhaitez, sélectionnez la propriété <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A> , puis tapez le chemin complet et le nom de fichier du fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="6449e-120">Optionally, select the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A> property and type the full path and file name for the destination file.</span></span>  
  
     <span data-ttu-id="6449e-121">Si vous ignorez cette étape, l’utilisateur sera invité à entrer un nom de fichier lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="6449e-121">If you skip this step, the user will be prompted for a file name at run time.</span></span>  
  
4.  <span data-ttu-id="6449e-122">Ajoutez le code suivant dans le Gestionnaire d’événements approprié (par exemple, dans le `Click` Gestionnaire d’événements pour un **impression**`Button`).</span><span class="sxs-lookup"><span data-stu-id="6449e-122">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print()  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="6449e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6449e-123">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A>
- [<span data-ttu-id="6449e-124">Guide pratique pour imprimer la zone cliente d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="6449e-124">How to: Print the Client Area of a Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-the-client-area-of-a-form.md)
- [<span data-ttu-id="6449e-125">Guide pratique pour imprimer des zones clientes et non clientes d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="6449e-125">How to: Print Client and Non-Client Areas of a Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)
- [<span data-ttu-id="6449e-126">Guide pratique pour imprimer un formulaire à défilement variable</span><span class="sxs-lookup"><span data-stu-id="6449e-126">How to: Print a Scrollable Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-a-scrollable-form.md)
- [<span data-ttu-id="6449e-127">PrintForm, composant</span><span class="sxs-lookup"><span data-stu-id="6449e-127">PrintForm Component</span></span>](../../../visual-basic/developing-apps/printing/printform-component.md)
