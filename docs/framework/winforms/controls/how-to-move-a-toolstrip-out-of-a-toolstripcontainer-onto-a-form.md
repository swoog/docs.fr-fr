---
title: 'Procédure : déplacer un ToolStrip hors d’un ToolStripContainer dans un formulaire'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStrip control [Windows Forms], parenting to forms
- Windows Forms, parenting ToolStrip controls
ms.assetid: a1c94a7f-6fc5-4e4c-84cf-ff11dc573d33
ms.openlocfilehash: 9106a69ea9f28442da6e3270f7cf5abb9374b62d
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59335262"
---
# <a name="how-to-move-a-toolstrip-out-of-a-toolstripcontainer-onto-a-form"></a><span data-ttu-id="b5c4f-102">Procédure : déplacer un ToolStrip hors d’un ToolStripContainer dans un formulaire</span><span class="sxs-lookup"><span data-stu-id="b5c4f-102">How to: Move a ToolStrip Out of a ToolStripContainer onto a Form</span></span>
<span data-ttu-id="b5c4f-103">Utilisez la procédure suivante pour déplacer un <xref:System.Windows.Forms.ToolStrip> d’un <xref:System.Windows.Forms.ToolStripContainer> sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-103">Use the following procedure to move a <xref:System.Windows.Forms.ToolStrip> out of a <xref:System.Windows.Forms.ToolStripContainer> onto a form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b5c4f-104">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="b5c4f-105">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="b5c4f-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="b5c4f-106">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="b5c4f-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-move-a-toolstrip-out-of-a-toolstripcontainer-onto-a-form"></a><span data-ttu-id="b5c4f-107">Pour déplacer un ToolStrip hors d’un ToolStripContainer dans un formulaire</span><span class="sxs-lookup"><span data-stu-id="b5c4f-107">To move a ToolStrip out of a ToolStripContainer onto a form</span></span>  
  
1. <span data-ttu-id="b5c4f-108">Sélectionnez le contrôle <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-108">Select the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
2. <span data-ttu-id="b5c4f-109">Couper la <xref:System.Windows.Forms.ToolStrip> en appuyant sur CTRL + X, ou cliquez sur le <xref:System.Windows.Forms.ToolStrip> et choisissez **couper** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-109">Cut the <xref:System.Windows.Forms.ToolStrip> by pressing CTRL+X, or right-click the <xref:System.Windows.Forms.ToolStrip> and choose **Cut** from the context menu.</span></span>  
  
3. <span data-ttu-id="b5c4f-110">Sélectionnez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-110">Select the form.</span></span>  
  
4. <span data-ttu-id="b5c4f-111">Coller le <xref:System.Windows.Forms.ToolStrip> en appuyant sur CTRL + V, ou choisissez **coller** à partir de la **modifier** menu.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-111">Paste the <xref:System.Windows.Forms.ToolStrip> by pressing CTRL+V, or choose **Paste** from the **Edit** menu.</span></span>  
  
5. <span data-ttu-id="b5c4f-112">Définir le <xref:System.Windows.Forms.ToolStrip.Dock%2A> propriété de la <xref:System.Windows.Forms.ToolStrip> à **haut**.</span><span class="sxs-lookup"><span data-stu-id="b5c4f-112">Set the <xref:System.Windows.Forms.ToolStrip.Dock%2A> property of the <xref:System.Windows.Forms.ToolStrip> to **Top**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5c4f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5c4f-113">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripContainer>
- [<span data-ttu-id="b5c4f-114">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="b5c4f-114">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
