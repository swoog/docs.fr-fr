---
title: 'Procédure : définir des info-bulles pour des contrôles dans un formulaire Windows au moment du design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], for controls
- examples [Windows Forms], tooltips
ms.assetid: c4b60637-4c0a-44c2-a103-f66dff887936
ms.openlocfilehash: 0d6725fc1a00826870e6400bffce63a1788e802c
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211685"
---
# <a name="how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time"></a><span data-ttu-id="3f135-102">Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du design</span><span class="sxs-lookup"><span data-stu-id="3f135-102">How to: Set ToolTips for controls on a Windows Form at design time</span></span>

<span data-ttu-id="3f135-103">Vous pouvez définir un <xref:System.Windows.Forms.ToolTip> chaîne dans le code ou dans le Concepteur de formulaires Windows dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3f135-103">You can set a <xref:System.Windows.Forms.ToolTip> string in code or in the Windows Forms Designer in Visual Studio.</span></span> <span data-ttu-id="3f135-104">Pour plus d’informations sur la <xref:System.Windows.Forms.ToolTip> composant, consultez [vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="3f135-104">For more information about the <xref:System.Windows.Forms.ToolTip> component, see [ToolTip Component Overview](tooltip-component-overview-windows-forms.md).</span></span>

## <a name="set-a-tooltip-programmatically"></a><span data-ttu-id="3f135-105">Définir une info-bulle par programmation</span><span class="sxs-lookup"><span data-stu-id="3f135-105">Set a ToolTip programmatically</span></span>

1. <span data-ttu-id="3f135-106">Ajoutez le contrôle qui affiche l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3f135-106">Add the control that will display the ToolTip.</span></span>

2. <span data-ttu-id="3f135-107">Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.</span><span class="sxs-lookup"><span data-stu-id="3f135-107">Use the <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> method of the <xref:System.Windows.Forms.ToolTip> component.</span></span>

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

## <a name="set-a-tooltip-in-the-designer"></a><span data-ttu-id="3f135-108">Définir une info-bulle dans le Concepteur</span><span class="sxs-lookup"><span data-stu-id="3f135-108">Set a ToolTip in the designer</span></span>

1. <span data-ttu-id="3f135-109">Dans Visual Studio, ajoutez un <xref:System.Windows.Forms.ToolTip> composant au formulaire.</span><span class="sxs-lookup"><span data-stu-id="3f135-109">In Visual Studio, add a <xref:System.Windows.Forms.ToolTip> component to the form.</span></span>

2. <span data-ttu-id="3f135-110">Sélectionnez le contrôle qui affiche l’info-bulle, ou ajoutez-le au formulaire.</span><span class="sxs-lookup"><span data-stu-id="3f135-110">Select the control that will display the ToolTip, or add it to the form.</span></span>

3. <span data-ttu-id="3f135-111">Dans le **propriétés** fenêtre, définissez la **info-bulle sur ToolTip1** valeur à une chaîne de texte appropriée.</span><span class="sxs-lookup"><span data-stu-id="3f135-111">In the **Properties** window, set the **ToolTip on ToolTip1** value to an appropriate string of text.</span></span>

### <a name="to-remove-a-tooltip-programmatically"></a><span data-ttu-id="3f135-112">Pour supprimer une info-bulle par programme</span><span class="sxs-lookup"><span data-stu-id="3f135-112">To remove a ToolTip programmatically</span></span>

1. <span data-ttu-id="3f135-113">Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.</span><span class="sxs-lookup"><span data-stu-id="3f135-113">Use the <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> method of the <xref:System.Windows.Forms.ToolTip> component.</span></span>

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

## <a name="remove-a-tooltip-in-the-designer"></a><span data-ttu-id="3f135-114">Supprimer une info-bulle dans le Concepteur</span><span class="sxs-lookup"><span data-stu-id="3f135-114">Remove a ToolTip in the designer</span></span>

1. <span data-ttu-id="3f135-115">Dans Visual Studio, sélectionnez le contrôle qui affiche l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3f135-115">In Visual Studio, select the control that is displaying the ToolTip.</span></span>

2. <span data-ttu-id="3f135-116">Dans le **propriétés** fenêtre, supprimez le texte dans le **info-bulle sur ToolTip1**.</span><span class="sxs-lookup"><span data-stu-id="3f135-116">In the **Properties** window, delete the text in the **ToolTip on ToolTip1**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f135-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f135-117">See also</span></span>

- [<span data-ttu-id="3f135-118">Vue d’ensemble du composant ToolTip</span><span class="sxs-lookup"><span data-stu-id="3f135-118">ToolTip Component Overview</span></span>](tooltip-component-overview-windows-forms.md)
- [<span data-ttu-id="3f135-119">Guide pratique pour Modifier la durée avant affichage du composant ToolTip Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3f135-119">How to: Change the Delay of the Windows Forms ToolTip Component</span></span>](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
- [<span data-ttu-id="3f135-120">ToolTip, composant</span><span class="sxs-lookup"><span data-stu-id="3f135-120">ToolTip Component</span></span>](tooltip-component-windows-forms.md)
