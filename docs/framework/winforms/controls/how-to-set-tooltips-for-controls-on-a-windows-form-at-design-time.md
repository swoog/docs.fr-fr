---
title: 'Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], for controls
- examples [Windows Forms], tooltips
ms.assetid: c4b60637-4c0a-44c2-a103-f66dff887936
ms.openlocfilehash: 541e50a8ee9c5338acc7c5e347549fd03a0f6323
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57710717"
---
# <a name="how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time"></a><span data-ttu-id="f4eb6-102">Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design</span><span class="sxs-lookup"><span data-stu-id="f4eb6-102">How to: Set ToolTips for Controls on a Windows Form at Design Time</span></span>
<span data-ttu-id="f4eb6-103">Vous pouvez définir un <xref:System.Windows.Forms.ToolTip> chaîne dans le code ou dans le Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-103">You can set a <xref:System.Windows.Forms.ToolTip> string in code or in the Windows Forms Designer.</span></span> <span data-ttu-id="f4eb6-104">Pour plus d’informations sur la <xref:System.Windows.Forms.ToolTip> composant, consultez [vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="f4eb6-104">For more information about the <xref:System.Windows.Forms.ToolTip> component, see [ToolTip Component Overview](tooltip-component-overview-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f4eb6-105">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-105">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="f4eb6-106">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="f4eb6-106">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="f4eb6-107">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="f4eb6-107">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-set-a-tooltip-programmatically"></a><span data-ttu-id="f4eb6-108">Pour définir une info-bulle par programmation</span><span class="sxs-lookup"><span data-stu-id="f4eb6-108">To set a ToolTip programmatically</span></span>  
  
1.  <span data-ttu-id="f4eb6-109">Ajoutez le contrôle qui affiche l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-109">Add the control that will display the ToolTip.</span></span>  
  
2.  <span data-ttu-id="f4eb6-110">Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-110">Use the <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> method of the <xref:System.Windows.Forms.ToolTip> component.</span></span>  
  
    ```vb  
    ' In this example, Button1 is the control to display the ToolTip.  
    ToolTip1.SetToolTip(Button1, "Save changes")  
    ```  
  
    ```csharp  
    // In this example, button1 is the control to display the ToolTip.  
    toolTip1.SetToolTip(button1, "Save changes");  
    ```  
  
    ```cpp  
    // In this example, button1 is the control to display the ToolTip.  
    toolTip1->SetToolTip(button1, "Save changes");  
    ```  
  
### <a name="to-set-a-tooltip-in-the-designer"></a><span data-ttu-id="f4eb6-111">Pour définir une info-bulle dans le Concepteur</span><span class="sxs-lookup"><span data-stu-id="f4eb6-111">To set a ToolTip in the designer</span></span>  
  
1.  <span data-ttu-id="f4eb6-112">Ajoutez un composant <xref:System.Windows.Forms.ToolTip> au formulaire.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-112">Add a <xref:System.Windows.Forms.ToolTip> component to the form.</span></span>  
  
2.  <span data-ttu-id="f4eb6-113">Sélectionnez le contrôle qui affiche l’info-bulle, ou ajoutez-le au formulaire.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-113">Select the control that will display the ToolTip, or add it to the form.</span></span>  
  
3.  <span data-ttu-id="f4eb6-114">Dans le **propriétés** fenêtre, définissez la **info-bulle sur ToolTip1** valeur à une chaîne de texte appropriée.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-114">In the **Properties** window, set the **ToolTip on ToolTip1** value to an appropriate string of text.</span></span>  

### <a name="to-remove-a-tooltip-programmatically"></a><span data-ttu-id="f4eb6-115">Pour supprimer une info-bulle par programme</span><span class="sxs-lookup"><span data-stu-id="f4eb6-115">To remove a ToolTip programmatically</span></span>  
  
1.  <span data-ttu-id="f4eb6-116">Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-116">Use the <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> method of the <xref:System.Windows.Forms.ToolTip> component.</span></span>  
  
    ```vb  
    ' In this example, Button1 is the control displaying the ToolTip.  
    ToolTip1.SetToolTip(Button1, Nothing)  
    ```  
  
    ```csharp  
    // In this example, button1 is the control displaying the ToolTip.  
    toolTip1.SetToolTip(button1, null);  
    ```  
  
    ```cpp  
    // In this example, button1 is the control displaying the ToolTip.  
    toolTip1->SetToolTip(button1, NULL);  
    ```  
  
### <a name="to-remove-a-tooltip-in-the-designer"></a><span data-ttu-id="f4eb6-117">Pour supprimer une info-bulle dans le Concepteur</span><span class="sxs-lookup"><span data-stu-id="f4eb6-117">To remove a ToolTip in the designer</span></span>  
  
1.  <span data-ttu-id="f4eb6-118">Sélectionnez le contrôle qui affiche l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-118">Select the control that is displaying the ToolTip.</span></span>  
  
2.  <span data-ttu-id="f4eb6-119">Dans le **propriétés** fenêtre, supprimez le texte dans le **info-bulle sur ToolTip1**.</span><span class="sxs-lookup"><span data-stu-id="f4eb6-119">In the **Properties** window, delete the text in the **ToolTip on ToolTip1**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f4eb6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4eb6-120">See also</span></span>
- [<span data-ttu-id="f4eb6-121">Vue d’ensemble du composant ToolTip</span><span class="sxs-lookup"><span data-stu-id="f4eb6-121">ToolTip Component Overview</span></span>](tooltip-component-overview-windows-forms.md)
- [<span data-ttu-id="f4eb6-122">Guide pratique pour Modifier la durée avant affichage du composant ToolTip Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f4eb6-122">How to: Change the Delay of the Windows Forms ToolTip Component</span></span>](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
- [<span data-ttu-id="f4eb6-123">ToolTip, composant</span><span class="sxs-lookup"><span data-stu-id="f4eb6-123">ToolTip Component</span></span>](tooltip-component-windows-forms.md)
