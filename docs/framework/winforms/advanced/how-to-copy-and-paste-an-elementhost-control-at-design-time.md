---
title: 'Procédure : copier et coller un contrôle ElementHost au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
ms.openlocfilehash: 0f3367deaaec04744a3f812d7f2d08047d7eb588
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211387"
---
# <a name="how-to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="9d6fe-102">Procédure : copier et coller un contrôle ElementHost au moment du design</span><span class="sxs-lookup"><span data-stu-id="9d6fe-102">How to: Copy and Paste an ElementHost Control at Design Time</span></span>

<span data-ttu-id="9d6fe-103">Cette procédure vous montre comment copier un contrôle Windows Presentation Foundation (WPF) sur un formulaire Windows dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-103">This procedure shows you how to copy a Windows Presentation Foundation (WPF) control on a Windows Form in Visual Studio.</span></span>

## <a name="copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="9d6fe-104">Copiez et collez un contrôle ElementHost au moment du design</span><span class="sxs-lookup"><span data-stu-id="9d6fe-104">Copy and paste an ElementHost control at design time</span></span>

1. <span data-ttu-id="9d6fe-105">Ajoutez un nouveau WPF <xref:System.Windows.Controls.UserControl> à votre projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-105">Add a new WPF <xref:System.Windows.Controls.UserControl> to your Windows Forms project.</span></span> <span data-ttu-id="9d6fe-106">Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-106">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="9d6fe-107">Pour plus d’informations, consultez [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="9d6fe-107">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>

2. <span data-ttu-id="9d6fe-108">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés de `UserControl1` à `200`.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-108">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties of `UserControl1` to `200`.</span></span>

3. <span data-ttu-id="9d6fe-109">Affectez à la propriété <xref:System.Windows.Controls.Control.Background%2A> la valeur `Blue`.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-109">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Blue`.</span></span>

4. <span data-ttu-id="9d6fe-110">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-110">Build the project.</span></span>

5. <span data-ttu-id="9d6fe-111">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-111">Open `Form1` in the Windows Forms Designer.</span></span>

6. <span data-ttu-id="9d6fe-112">À partir de la **boîte à outils**, faites glisser une instance de `UserControl1` vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-112">From the **Toolbox**, drag an instance of `UserControl1` onto the form.</span></span>

   <span data-ttu-id="9d6fe-113">Une instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-113">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>

7. <span data-ttu-id="9d6fe-114">`elementHost1` étant sélectionné, appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-114">With `elementHost1` selected, press CTRL+C to copy it to the clipboard.</span></span>

8. <span data-ttu-id="9d6fe-115">Appuyez sur CTRL + V pour coller le contrôle copié vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-115">Press CTRL+V to paste the copied control onto the form.</span></span>

   <span data-ttu-id="9d6fe-116">Un nouveau <xref:System.Windows.Forms.Integration.ElementHost> contrôle nommé `elementHost2` est créé sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9d6fe-116">A new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost2` is created on the form.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d6fe-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6fe-117">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="9d6fe-118">Migration et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="9d6fe-118">Migration and Interoperability</span></span>](../../wpf/advanced/migration-and-interoperability.md)
- [<span data-ttu-id="9d6fe-119">Utilisation de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="9d6fe-119">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="9d6fe-120">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9d6fe-120">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
