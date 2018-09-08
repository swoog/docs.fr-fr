---
title: 'Comment : copier et coller un contrôle ElementHost au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
ms.openlocfilehash: 43ebe50497df97511925bd2e413ab5b5988b7f57
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44210917"
---
# <a name="how-to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="5aea8-102">Comment : copier et coller un contrôle ElementHost au moment du design</span><span class="sxs-lookup"><span data-stu-id="5aea8-102">How to: Copy and Paste an ElementHost Control at Design Time</span></span>
<span data-ttu-id="5aea8-103">Cette procédure vous indique comment copier un contrôle Windows Presentation Foundation (WPF) sur un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="5aea8-103">This procedure shows you how to copy a Windows Presentation Foundation (WPF) control on a Windows Form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5aea8-104">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="5aea8-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="5aea8-105">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="5aea8-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="5aea8-106">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="5aea8-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="5aea8-107">Pour copier et coller un contrôle ElementHost au moment du design</span><span class="sxs-lookup"><span data-stu-id="5aea8-107">To copy and paste an ElementHost control at design time</span></span>  
  
1.  <span data-ttu-id="5aea8-108">Ajoutez un nouveau WPF <xref:System.Windows.Controls.UserControl> à votre projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="5aea8-108">Add a new WPF <xref:System.Windows.Controls.UserControl> to your Windows Forms project.</span></span> <span data-ttu-id="5aea8-109">Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`.</span><span class="sxs-lookup"><span data-stu-id="5aea8-109">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="5aea8-110">Pour plus d’informations, consultez [procédure pas à pas : création de nouveau contenu WPF sur les formulaires Windows au moment du Design](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="5aea8-110">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>  
  
2.  <span data-ttu-id="5aea8-111">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés de `UserControl1` à `200`.</span><span class="sxs-lookup"><span data-stu-id="5aea8-111">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties of `UserControl1` to `200`.</span></span>  
  
3.  <span data-ttu-id="5aea8-112">Affectez à la propriété <xref:System.Windows.Controls.Control.Background%2A> la valeur `Blue`.</span><span class="sxs-lookup"><span data-stu-id="5aea8-112">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Blue`.</span></span>  
  
4.  <span data-ttu-id="5aea8-113">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="5aea8-113">Build the project.</span></span>  
  
5.  <span data-ttu-id="5aea8-114">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="5aea8-114">Open `Form1` in the Windows Forms Designer.</span></span>  
  
6.  <span data-ttu-id="5aea8-115">À partir de la **boîte à outils**, faites glisser une instance de `UserControl1` vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="5aea8-115">From the **Toolbox**, drag an instance of `UserControl1` onto the form.</span></span>  
  
     <span data-ttu-id="5aea8-116">Une instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="5aea8-116">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>  
  
7.  <span data-ttu-id="5aea8-117">`elementHost1` étant sélectionné, appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="5aea8-117">With `elementHost1` selected, press CTRL+C to copy it to the clipboard.</span></span>  
  
8.  <span data-ttu-id="5aea8-118">Appuyez sur CTRL + V pour coller le contrôle copié vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="5aea8-118">Press CTRL+V to paste the copied control onto the form.</span></span>  
  
     <span data-ttu-id="5aea8-119">Un nouveau <xref:System.Windows.Forms.Integration.ElementHost> contrôle nommé `elementHost2` est créé sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="5aea8-119">A new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost2` is created on the form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5aea8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aea8-120">See Also</span></span>  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [<span data-ttu-id="5aea8-121">Procédure pas à pas : copier-coller d'un contrôle ElementHost dans d'autres Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5aea8-121">Walkthrough: Copying and Pasting an ElementHost Control into Separate Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/copy--paste-an-elementhost-control-into-forms.md)  
 [<span data-ttu-id="5aea8-122">Migration et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="5aea8-122">Migration and Interoperability</span></span>](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)  
 [<span data-ttu-id="5aea8-123">Utilisation de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="5aea8-123">Using WPF Controls</span></span>](../../../../docs/framework/winforms/advanced/using-wpf-controls.md)  
 [<span data-ttu-id="5aea8-124">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5aea8-124">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
