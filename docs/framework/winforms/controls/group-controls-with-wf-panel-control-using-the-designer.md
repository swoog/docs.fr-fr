---
title: 'Procédure : regrouper des contrôles avec le contrôle Panel Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Panel control [Windows Forms], grouping controls
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
ms.assetid: 7e1cd708-fdb1-49d8-9ca2-5640b276bf2e
ms.openlocfilehash: 662343af42f72816a5a673d2cd6d839a5dca9190
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59341398"
---
# <a name="how-to-group-controls-with-the-windows-forms-panel-control-using-the-designer"></a><span data-ttu-id="ce1f6-102">Procédure : regrouper des contrôles avec le contrôle Panel Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="ce1f6-102">How to: Group Controls with the Windows Forms Panel Control Using the Designer</span></span>
<span data-ttu-id="ce1f6-103">Windows Forms <xref:System.Windows.Forms.Panel> contrôles sont utilisés pour regrouper d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-103">Windows Forms <xref:System.Windows.Forms.Panel> controls are used to group other controls.</span></span> <span data-ttu-id="ce1f6-104">Il existe trois raisons pour regrouper des contrôles.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-104">There are three reasons to group controls.</span></span> <span data-ttu-id="ce1f6-105">Regroupement d’éléments connexes pour une interface utilisateur claire ; visuel regroupement de programmation, des cases d’option, par exemple ; la dernière est pour déplacer les contrôles en tant qu’unité au moment du design.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-105">One is visual grouping of related form elements for a clear user interface; another is programmatic grouping, of radio buttons for example; the last is for moving the controls as a unit at design time.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ce1f6-106">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="ce1f6-107">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="ce1f6-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="ce1f6-108">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="ce1f6-108">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-a-group-of-controls"></a><span data-ttu-id="ce1f6-109">Pour créer un groupe de contrôles</span><span class="sxs-lookup"><span data-stu-id="ce1f6-109">To create a group of controls</span></span>  
  
1. <span data-ttu-id="ce1f6-110">Faites glisser un <xref:System.Windows.Forms.Panel> contrôle depuis la **Windows Forms** onglet de la boîte à outils sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-110">Drag a <xref:System.Windows.Forms.Panel> control from the **Windows Forms** tab of the Toolbox onto a form.</span></span>  
  
2. <span data-ttu-id="ce1f6-111">Ajoutez des contrôles pour le dessin du panneau, chacun à l’intérieur du panneau.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-111">Add other controls to the panel, drawing each inside the panel.</span></span>  
  
     <span data-ttu-id="ce1f6-112">Si vous avez des contrôles existants que vous souhaitez placer dans un panneau, vous pouvez sélectionner tous les contrôles, les couper dans le Presse-papiers, sélectionnez le <xref:System.Windows.Forms.Panel> contrôler et collez-les dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-112">If you have existing controls that you want to enclose in a panel, you can select all the controls, cut them to the Clipboard, select the <xref:System.Windows.Forms.Panel> control, and then paste them into the panel.</span></span> <span data-ttu-id="ce1f6-113">Vous pouvez également faites-les glisser dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-113">You can also drag them into the panel.</span></span>  
  
3. <span data-ttu-id="ce1f6-114">(Facultatif) Si vous souhaitez ajouter une bordure à un panneau, définissez son <xref:System.Windows.Forms.BorderStyle> propriété.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-114">(Optional) If you want to add a border to a panel, set its <xref:System.Windows.Forms.BorderStyle> property.</span></span> <span data-ttu-id="ce1f6-115">Il existe trois possibilités : <xref:System.Windows.Forms.BorderStyle.Fixed3D>, <xref:System.Windows.Forms.BorderStyle.FixedSingle>, et <xref:System.Windows.Forms.BorderStyle.None>.</span><span class="sxs-lookup"><span data-stu-id="ce1f6-115">There are three choices: <xref:System.Windows.Forms.BorderStyle.Fixed3D>, <xref:System.Windows.Forms.BorderStyle.FixedSingle>, and <xref:System.Windows.Forms.BorderStyle.None>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce1f6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce1f6-116">See also</span></span>

- [<span data-ttu-id="ce1f6-117">Panel, contrôle</span><span class="sxs-lookup"><span data-stu-id="ce1f6-117">Panel Control</span></span>](panel-control-windows-forms.md)
- [<span data-ttu-id="ce1f6-118">Vue d’ensemble du contrôle Panel</span><span class="sxs-lookup"><span data-stu-id="ce1f6-118">Panel Control Overview</span></span>](panel-control-overview-windows-forms.md)
- [<span data-ttu-id="ce1f6-119">Procédure : définir l’arrière-plan d’un panneau</span><span class="sxs-lookup"><span data-stu-id="ce1f6-119">How to: Set the Background of a Panel</span></span>](how-to-set-the-background-of-a-windows-forms-panel.md)
