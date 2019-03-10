---
title: 'Procédure : Copiez et collez un contrôle ElementHost au moment du Design'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
ms.openlocfilehash: 203a01ef82554bf4104f3000c0821cceeafac9f7
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57710418"
---
# <a name="how-to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="df1ce-102">Procédure : Copiez et collez un contrôle ElementHost au moment du Design</span><span class="sxs-lookup"><span data-stu-id="df1ce-102">How to: Copy and Paste an ElementHost Control at Design Time</span></span>
<span data-ttu-id="df1ce-103">Cette procédure vous indique comment copier un contrôle Windows Presentation Foundation (WPF) sur un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="df1ce-103">This procedure shows you how to copy a Windows Presentation Foundation (WPF) control on a Windows Form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="df1ce-104">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="df1ce-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="df1ce-105">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="df1ce-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="df1ce-106">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="df1ce-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="df1ce-107">Pour copier et coller un contrôle ElementHost au moment du design</span><span class="sxs-lookup"><span data-stu-id="df1ce-107">To copy and paste an ElementHost control at design time</span></span>  
  
1.  <span data-ttu-id="df1ce-108">Ajoutez un nouveau WPF <xref:System.Windows.Controls.UserControl> à votre projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="df1ce-108">Add a new WPF <xref:System.Windows.Controls.UserControl> to your Windows Forms project.</span></span> <span data-ttu-id="df1ce-109">Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`.</span><span class="sxs-lookup"><span data-stu-id="df1ce-109">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="df1ce-110">Pour plus d’informations, consultez [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="df1ce-110">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>  
  
2.  <span data-ttu-id="df1ce-111">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés de `UserControl1` à `200`.</span><span class="sxs-lookup"><span data-stu-id="df1ce-111">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties of `UserControl1` to `200`.</span></span>  
  
3.  <span data-ttu-id="df1ce-112">Affectez à la propriété <xref:System.Windows.Controls.Control.Background%2A> la valeur `Blue`.</span><span class="sxs-lookup"><span data-stu-id="df1ce-112">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Blue`.</span></span>  
  
4.  <span data-ttu-id="df1ce-113">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="df1ce-113">Build the project.</span></span>  
  
5.  <span data-ttu-id="df1ce-114">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="df1ce-114">Open `Form1` in the Windows Forms Designer.</span></span>  
  
6.  <span data-ttu-id="df1ce-115">À partir de la **boîte à outils**, faites glisser une instance de `UserControl1` vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="df1ce-115">From the **Toolbox**, drag an instance of `UserControl1` onto the form.</span></span>  
  
     <span data-ttu-id="df1ce-116">Une instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="df1ce-116">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>  
  
7.  <span data-ttu-id="df1ce-117">
  `elementHost1\` étant sélectionné, appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="df1ce-117">With `elementHost1` selected, press CTRL+C to copy it to the clipboard.</span></span>  
  
8.  <span data-ttu-id="df1ce-118">Appuyez sur CTRL + V pour coller le contrôle copié vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="df1ce-118">Press CTRL+V to paste the copied control onto the form.</span></span>  
  
     <span data-ttu-id="df1ce-119">Un nouveau <xref:System.Windows.Forms.Integration.ElementHost> contrôle nommé `elementHost2` est créé sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="df1ce-119">A new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost2` is created on the form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df1ce-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df1ce-120">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="df1ce-121">Migration et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="df1ce-121">Migration and Interoperability</span></span>](../../wpf/advanced/migration-and-interoperability.md)
- [<span data-ttu-id="df1ce-122">Utilisation de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="df1ce-122">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="df1ce-123">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="df1ce-123">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
