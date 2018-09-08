---
title: 'Comment : imprimer un formulaire à défilement variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- entire form [Visual Basic], printing
- scrollable form [Visual Basic], printing
ms.assetid: 1196e1cf-b77f-4928-a3e4-85b51ba3787d
ms.openlocfilehash: 4a509b7c48f2bff705bc95e58fb88252cb8ca4b9
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44182030"
---
# <a name="how-to-print-a-scrollable-form-visual-basic"></a><span data-ttu-id="ebc61-102">Comment : imprimer un formulaire à défilement variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ebc61-102">How to: Print a Scrollable Form (Visual Basic)</span></span>
<span data-ttu-id="ebc61-103">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> vous permet d’imprimer rapidement une image d’un formulaire sans utiliser un composant <xref:System.Drawing.Printing.PrintDocument> .</span><span class="sxs-lookup"><span data-stu-id="ebc61-103">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component enables you to quickly print an image of a form without using a <xref:System.Drawing.Printing.PrintDocument> component.</span></span> <span data-ttu-id="ebc61-104">Par défaut, seule la partie actuellement visible du formulaire est imprimée ; si un utilisateur a redimensionné le formulaire au moment de l’exécution, l’image ne peut pas être imprimée comme prévu.</span><span class="sxs-lookup"><span data-stu-id="ebc61-104">By default, only the currently visible part of the form is printed; if a user has resized the form at run time, the image may not print as intended.</span></span> <span data-ttu-id="ebc61-105">La procédure suivante montre comment imprimer la zone cliente complète d’un formulaire avec défilement, même si le formulaire a été redimensionné.</span><span class="sxs-lookup"><span data-stu-id="ebc61-105">The following procedure shows how to print the complete client area of a scrollable form, even if the form has been resized.</span></span>  
  
 <span data-ttu-id="ebc61-106">Les contrôles PowerPack ne sont plus inclus dans Visual Studio, mais vous pouvez les télécharger à partir de la [centre de téléchargement](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span><span class="sxs-lookup"><span data-stu-id="ebc61-106">The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span></span>  
  
### <a name="to-print-the-complete-client-area-of-a-scrollable-form"></a><span data-ttu-id="ebc61-107">Pour imprimer la zone cliente complète d’un formulaire avec défilement</span><span class="sxs-lookup"><span data-stu-id="ebc61-107">To print the complete client area of a scrollable form</span></span>  
  
1.  <span data-ttu-id="ebc61-108">Dans la **Boîte à outils**, cliquez sur l’onglet **Visual Basic PowerPacks** , puis faites glisser le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ebc61-108">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="ebc61-109">Le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> va être ajouté à la barre d’état des composants.</span><span class="sxs-lookup"><span data-stu-id="ebc61-109">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component will be added to the component tray.</span></span>  
  
2.  <span data-ttu-id="ebc61-110">Dans la fenêtre **Propriétés** , définissez la propriété <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> sur <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span><span class="sxs-lookup"><span data-stu-id="ebc61-110">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span></span>  
  
3.  <span data-ttu-id="ebc61-111">Ajoutez le code suivant dans le Gestionnaire d’événements approprié (par exemple, dans le `Click` Gestionnaire d’événements pour un **impression**`Button`).</span><span class="sxs-lookup"><span data-stu-id="ebc61-111">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.Scrollable)  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="ebc61-112">Sur certains systèmes d’exploitation, le texte ou les graphiques dessinés par des méthodes <xref:System.Drawing.Graphics> peuvent ne pas s’imprimer correctement.</span><span class="sxs-lookup"><span data-stu-id="ebc61-112">On some operating systems, text or graphics drawn by <xref:System.Drawing.Graphics> methods may not print correctly.</span></span> <span data-ttu-id="ebc61-113">Dans ce cas, vous ne pourrez pas imprimer avec le paramètre `Scrollable` .</span><span class="sxs-lookup"><span data-stu-id="ebc61-113">In this case, you will not be able to print with the `Scrollable` parameter.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebc61-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc61-114">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print%2A>  
 [<span data-ttu-id="ebc61-115">PrintForm, composant</span><span class="sxs-lookup"><span data-stu-id="ebc61-115">PrintForm Component</span></span>](../../../visual-basic/developing-apps/printing/printform-component.md)  
 [<span data-ttu-id="ebc61-116">Guide pratique : imprimer la zone cliente d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="ebc61-116">How to: Print the Client Area of a Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-the-client-area-of-a-form.md)  
 [<span data-ttu-id="ebc61-117">Guide pratique : imprimer des zones clientes et non clientes d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="ebc61-117">How to: Print Client and Non-Client Areas of a Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)
