---
title: 'Procédure : afficher l’aide contextuelle'
ms.date: 03/30/2017
helpviewer_keywords:
- pop-up Help
- Help [Windows Forms], pop-up Help
- Windows Forms, displaying Help
- forms [Windows Forms], displaying Help
- modal dialog boxes [Windows Forms], pop-up Help
- F1 Help [Windows Forms], in dialog boxes
- HelpProvider component [Windows Forms]
- Help [Windows Forms], adding to dialog boxes
ms.assetid: 218aa81e-e87e-4d67-af05-11627bbdce3b
ms.openlocfilehash: bf3bcbff0cd6f3bbf71e96e748cb170d5ce68dfc
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211399"
---
# <a name="how-to-display-pop-up-help"></a><span data-ttu-id="a6d4a-102">Procédure : Afficher l’aide contextuelle</span><span class="sxs-lookup"><span data-stu-id="a6d4a-102">How to: Display pop-up Help</span></span>

<span data-ttu-id="a6d4a-103">Pour afficher l’aide dans les Windows Forms offre un moyen du **aide** bouton situé sur le côté droit de la barre de titre, accessible via la <xref:System.Windows.Forms.Form.HelpButton%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-103">One way to display Help on Windows Forms is through the **Help** button, located on the right side of the title bar, accessible through the <xref:System.Windows.Forms.Form.HelpButton%2A> property.</span></span> <span data-ttu-id="a6d4a-104">Ce type d’affichage de l’aide convient parfaitement aux boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-104">This type of Help display is well-suited for use with dialog boxes.</span></span> <span data-ttu-id="a6d4a-105">Les boîtes de dialogue modales (affichées avec la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A>) ont des difficultés à afficher les systèmes d'aide externes, car elles doivent être fermées pour que le focus puisse basculer vers une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-105">Dialog boxes shown modally (with the <xref:System.Windows.Forms.Form.ShowDialog%2A> method) have trouble bringing up external Help systems, because modal dialog boxes need to be closed before focus can shift to another window.</span></span> <span data-ttu-id="a6d4a-106">En outre, à l’aide de la **aide** bouton requiert l’existence aucun **réduire** bouton ou **agrandir** affiché dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-106">Additionally, using the **Help** button requires that there is no **Minimize** button or **Maximize** button shown in the title bar.</span></span> <span data-ttu-id="a6d4a-107">Il s’agit une convention de boîte de dialogue standard, tandis que les formulaires possèdent généralement **réduire** et **agrandir** boutons.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-107">This is a standard dialog-box convention, whereas forms usually have **Minimize** and **Maximize** buttons.</span></span>

<span data-ttu-id="a6d4a-108">Vous pouvez également utiliser le <xref:System.Windows.Forms.HelpProvider> composant pour lier des contrôles aux fichiers dans un système d’aide, même si vous avez implémenté l’aide contextuelle.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-108">You can also use the <xref:System.Windows.Forms.HelpProvider> component to link controls to files in a Help system, even if you have implemented pop-up Help.</span></span> <span data-ttu-id="a6d4a-109">Pour plus d’informations, consultez [fourniture d’aide dans une Application Windows](how-to-provide-help-in-a-windows-application.md).</span><span class="sxs-lookup"><span data-stu-id="a6d4a-109">For more information, see [Providing Help in a Windows Application](how-to-provide-help-in-a-windows-application.md).</span></span>

## <a name="display-pop-up-help"></a><span data-ttu-id="a6d4a-110">Afficher l’aide contextuelle</span><span class="sxs-lookup"><span data-stu-id="a6d4a-110">Display pop-up Help</span></span>

1. <span data-ttu-id="a6d4a-111">Dans Visual Studio, faites glisser un [HelpProvider](../controls/helpprovider-component-windows-forms.md) composant à partir de la boîte à outils à votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-111">In Visual Studio, drag a [HelpProvider](../controls/helpprovider-component-windows-forms.md) component from the Toolbox to your form.</span></span>

   <span data-ttu-id="a6d4a-112">Il sera placé dans la barre d'état en bas du Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-112">It will sit in the tray at the bottom of the Windows Forms Designer.</span></span>

2. <span data-ttu-id="a6d4a-113">Dans la fenêtre Propriétés, affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Form.HelpButton%2A>.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-113">In the Properties window, set the <xref:System.Windows.Forms.Form.HelpButton%2A> property to `true`.</span></span> <span data-ttu-id="a6d4a-114">Ceci affichera un bouton avec un point d'interrogation sur le côté droit de la barre de titre du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-114">This will display a button with a question mark in it on the right side of the title bar of the form.</span></span>

3. <span data-ttu-id="a6d4a-115">Pour que le <xref:System.Windows.Forms.Form.HelpButton%2A> soit affiché, il faut que les propriétés <xref:System.Windows.Forms.Form.MinimizeBox%2A> et <xref:System.Windows.Forms.Form.MaximizeBox%2A>  du formulaire aient la valeur `false`, que la propriété <xref:System.Windows.Forms.Form.ControlBox%2A> ait la valeur `true` et que la propriété <xref:System.Windows.Forms.Form.FormBorderStyle%2A> ait l'une des valeurs suivantes : <xref:System.Windows.Forms.FormBorderStyle.FixedSingle>, <xref:System.Windows.Forms.FormBorderStyle.Fixed3D>, <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> ou <xref:System.Windows.Forms.FormBorderStyle.Sizable>.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-115">In order for the <xref:System.Windows.Forms.Form.HelpButton%2A> to display, the form's <xref:System.Windows.Forms.Form.MinimizeBox%2A> and <xref:System.Windows.Forms.Form.MaximizeBox%2A> properties must be set to `false`, the <xref:System.Windows.Forms.Form.ControlBox%2A> property set to `true`, and the <xref:System.Windows.Forms.Form.FormBorderStyle%2A> property to one of the following values: <xref:System.Windows.Forms.FormBorderStyle.FixedSingle>, <xref:System.Windows.Forms.FormBorderStyle.Fixed3D>, <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> or <xref:System.Windows.Forms.FormBorderStyle.Sizable>.</span></span>

4. <span data-ttu-id="a6d4a-116">Sélectionnez le contrôle pour lequel vous souhaitez afficher l'aide sur votre formulaire et définissez la chaîne d'aide dans la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-116">Select the control for which you want to show help on your form and set the Help string in the Properties window.</span></span> <span data-ttu-id="a6d4a-117">C’est la chaîne de texte qui s’affichera dans une fenêtre similaire à un [info-bulle](../controls/tooltip-component-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="a6d4a-117">This is the string of text that will be displayed in a window similar to a [ToolTip](../controls/tooltip-component-windows-forms.md).</span></span>

5. <span data-ttu-id="a6d4a-118">Appuyez sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-118">Press **F5**.</span></span>

6. <span data-ttu-id="a6d4a-119">Appuyez sur la **aide** sur la barre de titre, puis cliquez sur le contrôle sur lequel vous avez défini la chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="a6d4a-119">Press the **Help** button on the title bar and click the control on which you set the Help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6d4a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6d4a-120">See also</span></span>

- [<span data-ttu-id="a6d4a-121">Affichage sous forme d’info-bulles de l’aide relative aux contrôles</span><span class="sxs-lookup"><span data-stu-id="a6d4a-121">Control Help Using ToolTips</span></span>](control-help-using-tooltips.md)
- [<span data-ttu-id="a6d4a-122">Intégration de l’aide d’utilisateur dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a6d4a-122">Integrating User Help in Windows Forms</span></span>](integrating-user-help-in-windows-forms.md)
- [<span data-ttu-id="a6d4a-123">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a6d4a-123">Windows Forms</span></span>](../index.md)
