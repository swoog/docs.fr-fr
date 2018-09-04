---
title: "Comment : définir l'arrière-plan d'un contrôle Panel Windows Forms à l'aide du concepteur"
ms.date: 03/30/2017
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: db83cf54-3c69-4b08-ac6c-25b9b5abb1b0
ms.openlocfilehash: 86ab8bc979765fe79ccc76db9a0566459fde6e46
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43499911"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel-using-the-designer"></a><span data-ttu-id="f8ede-102">Comment : définir l'arrière-plan d'un contrôle Panel Windows Forms à l'aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="f8ede-102">How to: Set the Background of a Windows Forms Panel Using the Designer</span></span>
<span data-ttu-id="f8ede-103">Un formulaire Windows <xref:System.Windows.Forms.Panel> contrôle peut afficher une couleur d’arrière-plan et une image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f8ede-103">A Windows Forms <xref:System.Windows.Forms.Panel> control can display both a background color and a background image.</span></span> <span data-ttu-id="f8ede-104">Le <xref:System.Windows.Forms.Control.BackColor%2A> propriété définit la couleur d’arrière-plan pour les contrôles qui sont contenus dans le panneau de configuration, tels que des étiquettes et cases d’option.</span><span class="sxs-lookup"><span data-stu-id="f8ede-104">The <xref:System.Windows.Forms.Control.BackColor%2A> property sets the background color for controls that are contained in the panel, such as labels and radio buttons.</span></span> <span data-ttu-id="f8ede-105">Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété n’est pas définie, le <xref:System.Windows.Forms.Control.BackColor%2A> sélectionnée remplit tout le panneau.</span><span class="sxs-lookup"><span data-stu-id="f8ede-105">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is not set, the <xref:System.Windows.Forms.Control.BackColor%2A> selection will fill all of the panel.</span></span> <span data-ttu-id="f8ede-106">Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété est définie, l’image est affichée derrière les contrôles qui sont contenus dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="f8ede-106">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is set, the image will be displayed behind the controls that are contained in the panel.</span></span>  
  
 <span data-ttu-id="f8ede-107">La procédure suivante nécessite un **Windows Application** projet avec un formulaire qui contient un <xref:System.Windows.Forms.Panel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8ede-107">The following procedure requires a **Windows Application** project with a form that contains a <xref:System.Windows.Forms.Panel> control.</span></span> <span data-ttu-id="f8ede-108">Pour plus d’informations sur la façon de configurer un tel projet, consultez [Comment : créer un projet d’Application Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) et [Comment : ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="f8ede-108">For information about how to set up such a project, see [How to: Create a Windows Application Project](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) and [How to: Add Controls to Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f8ede-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8ede-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="f8ede-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="f8ede-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="f8ede-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="f8ede-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-set-the-background-in-the-windows-forms-designer"></a><span data-ttu-id="f8ede-112">Pour définir l’arrière-plan dans le Concepteur de formulaires Windows</span><span class="sxs-lookup"><span data-stu-id="f8ede-112">To set the background in the Windows Forms Designer</span></span>  
  
1.  <span data-ttu-id="f8ede-113">Sélectionnez le contrôle <xref:System.Windows.Forms.Panel>.</span><span class="sxs-lookup"><span data-stu-id="f8ede-113">Select the <xref:System.Windows.Forms.Panel> control.</span></span>  
  
2.  <span data-ttu-id="f8ede-114">Dans le **propriétés** fenêtre, cliquez sur la flèche située en regard du <xref:System.Windows.Forms.Control.BackColor%2A> propriété pour afficher une fenêtre avec trois onglets.</span><span class="sxs-lookup"><span data-stu-id="f8ede-114">In the **Properties** window, click the arrow button next to the <xref:System.Windows.Forms.Control.BackColor%2A> property to display a window with three tabs.</span></span>  
  
3.  <span data-ttu-id="f8ede-115">Sélectionnez le **personnalisé** onglet pour afficher une palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f8ede-115">Select the **Custom** tab to display a palette of colors.</span></span>  
  
4.  <span data-ttu-id="f8ede-116">Sélectionnez le **Web** ou **système** onglet pour afficher une liste de noms de couleurs prédéfinis, puis sélectionnez une couleur.</span><span class="sxs-lookup"><span data-stu-id="f8ede-116">Select the **Web** or **System** tab to display a list of predefined names for colors, and then select a color.</span></span>  
  
5.  <span data-ttu-id="f8ede-117">Dans le **propriétés** fenêtre, cliquez sur la flèche située en regard du <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f8ede-117">In the **Properties** window, click the arrow button next to the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property.</span></span>  
  
6.  <span data-ttu-id="f8ede-118">Dans le **Open** boîte de dialogue, sélectionnez le fichier que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="f8ede-118">In the **Open** dialog box, select the file that you want to display.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8ede-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8ede-119">See Also</span></span>  
 <xref:System.Windows.Forms.Control.BackColor%2A>  
 <xref:System.Windows.Forms.Control.BackgroundImage%2A>  
 [<span data-ttu-id="f8ede-120">Panel, contrôle</span><span class="sxs-lookup"><span data-stu-id="f8ede-120">Panel Control</span></span>](../../../../docs/framework/winforms/controls/panel-control-windows-forms.md)  
 [<span data-ttu-id="f8ede-121">Vue d’ensemble du contrôle Panel</span><span class="sxs-lookup"><span data-stu-id="f8ede-121">Panel Control Overview</span></span>](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md)  
 [<span data-ttu-id="f8ede-122">Guide pratique pour grouper les contrôles avec le contrôle Panel Windows Forms à l'aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="f8ede-122">How to: Group Controls with the Windows Forms Panel Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/group-controls-with-wf-panel-control-using-the-designer.md)
