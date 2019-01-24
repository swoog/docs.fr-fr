---
title: 'Procédure : Créer une Interface de Style Explorateur Windows sur un formulaire Windows'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Explorer [Windows Forms], creating with Windows Forms
- SplitContainer control [Windows Forms], Explorer-style interface
- forms [Windows Forms], Windows Explorer type
ms.assetid: 9a3d5f4f-5dda-4350-9ad5-57ce5976dc47
ms.openlocfilehash: 0b61961aff04a089ce12f4b96637e3f05023e929
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511096"
---
# <a name="how-to-create-a-windows-explorerstyle-interface-on-a-windows-form"></a><span data-ttu-id="cec0e-102">Procédure : Créer une Interface de Style Explorateur Windows sur un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="cec0e-102">How to: Create a Windows Explorer–Style Interface on a Windows Form</span></span>
<span data-ttu-id="cec0e-103">L’Explorateur Windows est un choix d’interface utilisateur commune pour les applications en raison de son caractère familier.</span><span class="sxs-lookup"><span data-stu-id="cec0e-103">Windows Explorer is a common user-interface choice for applications because of its ready familiarity.</span></span>  
  
 <span data-ttu-id="cec0e-104">L’Explorateur Windows est, fondamentalement, un <xref:System.Windows.Forms.TreeView> contrôle et un <xref:System.Windows.Forms.ListView> contrôle sur des panneaux séparés.</span><span class="sxs-lookup"><span data-stu-id="cec0e-104">Windows Explorer is, essentially, a <xref:System.Windows.Forms.TreeView> control and a <xref:System.Windows.Forms.ListView> control on separate panels.</span></span> <span data-ttu-id="cec0e-105">Les panneaux sont rendus redimensionnables par un séparateur.</span><span class="sxs-lookup"><span data-stu-id="cec0e-105">The panels are made resizable by a splitter.</span></span> <span data-ttu-id="cec0e-106">Cette disposition de contrôles est très efficace pour afficher et parcourir des informations.</span><span class="sxs-lookup"><span data-stu-id="cec0e-106">This arrangement of controls is very effective for displaying and browsing information.</span></span>  
  
 <span data-ttu-id="cec0e-107">Les étapes suivantes montrent comment disposer les contrôles dans un formulaire de type Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cec0e-107">The following steps show how to arrange controls in a Windows Explorer-like form.</span></span> <span data-ttu-id="cec0e-108">Ils ne plus afficher comment ajouter la fonctionnalité d’exploration des fichiers de l’application de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cec0e-108">They do not show how to add the file-browsing functionality of the Windows Explorer application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cec0e-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="cec0e-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="cec0e-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="cec0e-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="cec0e-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="cec0e-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-a-windows-explorer-style-windows-form"></a><span data-ttu-id="cec0e-112">Pour créer un formulaire Windows de style Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="cec0e-112">To create a Windows Explorer-style Windows Form</span></span>  
  
1.  <span data-ttu-id="cec0e-113">Créer un nouveau projet d’Application de Windows (**fichier** > **New** > **projet** > **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="cec0e-113">Create a new Windows Application project (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2.  <span data-ttu-id="cec0e-114">À partir de la **boîte à outils**:</span><span class="sxs-lookup"><span data-stu-id="cec0e-114">From the **Toolbox**:</span></span>  
  
    1.  <span data-ttu-id="cec0e-115">Faites glisser un <xref:System.Windows.Forms.SplitContainer> contrôle vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="cec0e-115">Drag a <xref:System.Windows.Forms.SplitContainer> control onto your form.</span></span>  
  
    2.  <span data-ttu-id="cec0e-116">Faites glisser un <xref:System.Windows.Forms.TreeView> contrôler en **SplitterPanel1** (le panneau de la <xref:System.Windows.Forms.SplitContainer> contrôle marqué **Panel1**).</span><span class="sxs-lookup"><span data-stu-id="cec0e-116">Drag a <xref:System.Windows.Forms.TreeView> control into **SplitterPanel1** (the panel of the <xref:System.Windows.Forms.SplitContainer> control marked **Panel1**).</span></span>  
  
    3.  <span data-ttu-id="cec0e-117">Faites glisser un <xref:System.Windows.Forms.ListView> contrôler en **SplitterPanel2** (le panneau de la <xref:System.Windows.Forms.SplitContainer> contrôle marqué **Panel2**).</span><span class="sxs-lookup"><span data-stu-id="cec0e-117">Drag a <xref:System.Windows.Forms.ListView> control into **SplitterPanel2** (the panel of the <xref:System.Windows.Forms.SplitContainer> control marked **Panel2**).</span></span>  
  
3.  <span data-ttu-id="cec0e-118">Sélectionnez tous les trois contrôles en appuyant sur la touche CTRL enfoncée et en cliquant dessus à son tour.</span><span class="sxs-lookup"><span data-stu-id="cec0e-118">Select all three controls by pressing the CTRL key and clicking them in turn.</span></span> <span data-ttu-id="cec0e-119">Lorsque vous sélectionnez le <xref:System.Windows.Forms.SplitContainer> contrôler, cliquez sur la barre de fractionnement, plutôt que les panneaux.</span><span class="sxs-lookup"><span data-stu-id="cec0e-119">When you select the <xref:System.Windows.Forms.SplitContainer> control, click the splitter bar, rather than the panels.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="cec0e-120">N’utilisez pas le **sélectionner tout** commande sur le **modifier** menu.</span><span class="sxs-lookup"><span data-stu-id="cec0e-120">Do not use the **Select All** command on the **Edit** menu.</span></span> <span data-ttu-id="cec0e-121">Si vous procédez ainsi, la propriété nécessaire à l’étape suivante n’apparaîtra pas dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cec0e-121">If you do so, the property needed in the next step will not appear in the **Properties** window.</span></span>  
  
4.  <span data-ttu-id="cec0e-122">Dans la fenêtre **Propriétés** , définissez la propriété <xref:System.Windows.Forms.SplitContainer.Dock%2A> sur <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="cec0e-122">In the **Properties** window, set the <xref:System.Windows.Forms.SplitContainer.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>  
  
5.  <span data-ttu-id="cec0e-123">Appuyez sur F5 pour exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="cec0e-123">Press F5 to run the application.</span></span>  
  
     <span data-ttu-id="cec0e-124">Le formulaire affiche une interface utilisateur de deux parties, similaire à celle de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cec0e-124">The form displays a two-part user interface, similar to that of the Windows Explorer.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="cec0e-125">Lorsque vous faites glisser le séparateur, les panneaux se redimensionnent.</span><span class="sxs-lookup"><span data-stu-id="cec0e-125">When you drag the splitter, the panels resize themselves.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cec0e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cec0e-126">See also</span></span>
- <xref:System.Windows.Forms.SplitContainer>
- [<span data-ttu-id="cec0e-127">Guide pratique pour Créer une Interface utilisateur à plusieurs volets avec des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cec0e-127">How to: Create a Multipane User Interface with Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-create-a-multipane-user-interface-with-windows-forms.md)
- [<span data-ttu-id="cec0e-128">Guide pratique pour Définir le redimensionnement et le positionnement du comportement dans une fenêtre fractionnée</span><span class="sxs-lookup"><span data-stu-id="cec0e-128">How to: Define Resize and Positioning Behavior in a Split Window</span></span>](../../../../docs/framework/winforms/controls/how-to-define-resize-and-positioning-behavior-in-a-split-window.md)
- [<span data-ttu-id="cec0e-129">Guide pratique pour Fractionner une fenêtre horizontalement</span><span class="sxs-lookup"><span data-stu-id="cec0e-129">How to: Split a Window Horizontally</span></span>](../../../../docs/framework/winforms/controls/how-to-split-a-window-horizontally.md)
- [<span data-ttu-id="cec0e-130">SplitContainer, contrôle</span><span class="sxs-lookup"><span data-stu-id="cec0e-130">SplitContainer Control</span></span>](../../../../docs/framework/winforms/controls/splitcontainer-control-windows-forms.md)
