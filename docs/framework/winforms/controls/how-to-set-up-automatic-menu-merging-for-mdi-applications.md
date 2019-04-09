---
title: 'Procédure : configurer la fusion automatique des menus pour des applications MDI'
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- Merging [Windows Forms], automatic menu
ms.assetid: 55e32cad-1141-4a56-aa33-d9543ca3d393
ms.openlocfilehash: 17edde6e3968823abc915eb5faed6d2751ed9393
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129349"
---
# <a name="how-to-set-up-automatic-menu-merging-for-mdi-applications"></a><span data-ttu-id="edee0-102">Procédure : configurer la fusion automatique des menus pour des applications MDI</span><span class="sxs-lookup"><span data-stu-id="edee0-102">How to: Set Up Automatic Menu Merging for MDI Applications</span></span>
<span data-ttu-id="edee0-103">La procédure suivante indique les étapes de base pour configurer la fusion automatique dans une application d’interface multidocument (MDI) avec <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="edee0-103">The following procedure gives the basic steps for setting up automatic merging in a multiple-document interface (MDI) application with <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
### <a name="to-set-up-automatic-menu-merging"></a><span data-ttu-id="edee0-104">Pour configurer la fusion de menus automatique</span><span class="sxs-lookup"><span data-stu-id="edee0-104">To set up automatic menu merging</span></span>  
  
1.  <span data-ttu-id="edee0-105">Créer un formulaire MDI parent en définissant son <xref:System.Windows.Forms.Form.IsMdiContainer%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="edee0-105">Create the MDI parent form by setting its <xref:System.Windows.Forms.Form.IsMdiContainer%2A> property to `true`.</span></span>  
  
2.  <span data-ttu-id="edee0-106">Ajouter un <xref:System.Windows.Forms.MenuStrip> le parent MDI, en définissant son <xref:System.Windows.Forms.Form.MainMenuStrip%2A> propriété qui <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="edee0-106">Add a <xref:System.Windows.Forms.MenuStrip> to the MDI parent, setting its <xref:System.Windows.Forms.Form.MainMenuStrip%2A> property to that <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
3.  <span data-ttu-id="edee0-107">Créer un formulaire enfant MDI et définir son <xref:System.Windows.Forms.Form.MdiParent%2A> propriété le nom du formulaire parent.</span><span class="sxs-lookup"><span data-stu-id="edee0-107">Create an MDI child form, and set its <xref:System.Windows.Forms.Form.MdiParent%2A> property to the name of the parent form.</span></span>  
  
4.  <span data-ttu-id="edee0-108">Ajouter un <xref:System.Windows.Forms.MenuStrip> au formulaire enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="edee0-108">Add a <xref:System.Windows.Forms.MenuStrip> to the MDI child form.</span></span>  
  
5.  <span data-ttu-id="edee0-109">Sur le formulaire enfant, définissez le <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété de la <xref:System.Windows.Forms.MenuStrip> à `false`.</span><span class="sxs-lookup"><span data-stu-id="edee0-109">On the child form, set the <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property of the <xref:System.Windows.Forms.MenuStrip> to `false`.</span></span>  
  
6.  <span data-ttu-id="edee0-110">Ajouter des éléments de menu à la forme enfant <xref:System.Windows.Forms.MenuStrip> que vous souhaitez fusionner dans le formulaire parent <xref:System.Windows.Forms.MenuStrip> lorsque le formulaire enfant est activé.</span><span class="sxs-lookup"><span data-stu-id="edee0-110">Add menu items to the child form's <xref:System.Windows.Forms.MenuStrip> that you want to merge into the parent form's <xref:System.Windows.Forms.MenuStrip> when the child form is activated.</span></span>  
  
7.  <span data-ttu-id="edee0-111">Utilisez le <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> les éléments de propriété dans le menu sous la forme enfant <xref:System.Windows.Forms.MenuStrip> pour contrôler leur fusion dans le formulaire parent.</span><span class="sxs-lookup"><span data-stu-id="edee0-111">Use the <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> property on the menu items in the child form's <xref:System.Windows.Forms.MenuStrip> to control how they merge into the parent form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="edee0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edee0-112">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [<span data-ttu-id="edee0-113">Vue d’ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="edee0-113">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
