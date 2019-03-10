---
title: 'Procédure : Définir le texte affiché par un Windows Forms à l’aide du Concepteur de contrôle'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], setting caption
- Windows Forms, setting the text displayed
ms.assetid: 9d18e0e0-f17f-4074-837d-e67ceeeaa89d
ms.openlocfilehash: 4d3f12bd2606e40b5ceeef716d8f5d264bc46622
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707376"
---
# <a name="how-to-set-the-text-displayed-by-a-windows-forms-control-using-the-designer"></a><span data-ttu-id="3a125-102">Procédure : Définir le texte affiché par un Windows Forms à l’aide du Concepteur de contrôle</span><span class="sxs-lookup"><span data-stu-id="3a125-102">How to: Set the Text Displayed by a Windows Forms Control Using the Designer</span></span>
<span data-ttu-id="3a125-103">Contrôles Windows Forms affichent généralement un texte qui est lié à la fonction principale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a125-103">Windows Forms controls typically display some text that is related to the primary function of the control.</span></span> <span data-ttu-id="3a125-104">Par exemple, un <xref:System.Windows.Forms.Button> contrôle affiche habituellement une légende qui indique quelle action sera effectuée lorsque le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="3a125-104">For example, a <xref:System.Windows.Forms.Button> control typically displays a caption that indicates what action will be performed when the button is clicked.</span></span> <span data-ttu-id="3a125-105">Pour tous les contrôles, vous pouvez définir ou retourner le texte à l'aide de la propriété <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="3a125-105">For all controls, you can set or return the text by using the <xref:System.Windows.Forms.Control.Text%2A> property.</span></span> <span data-ttu-id="3a125-106">Vous pouvez modifier la police en utilisant la propriété <xref:System.Windows.Forms.Control.Font%2A>.</span><span class="sxs-lookup"><span data-stu-id="3a125-106">You can change the font by using the <xref:System.Windows.Forms.Control.Font%2A> property.</span></span>  
  
### <a name="to-set-the-text-and-font-with-the-designer"></a><span data-ttu-id="3a125-107">Pour définir le texte et la police avec le Concepteur</span><span class="sxs-lookup"><span data-stu-id="3a125-107">To set the text and font with the designer</span></span>  
  
1.  <span data-ttu-id="3a125-108">Dans la fenêtre Propriétés, définissez la <xref:System.Windows.Forms.Control.Text%2A> propriété du contrôle à une chaîne appropriée.</span><span class="sxs-lookup"><span data-stu-id="3a125-108">In the Properties window, set the <xref:System.Windows.Forms.Control.Text%2A> property of the control to an appropriate string.</span></span>  
  
     <span data-ttu-id="3a125-109">Pour créer une touche de raccourci soulignée, incluez une esperluette (&) avant la lettre qui sera la touche de raccourci.</span><span class="sxs-lookup"><span data-stu-id="3a125-109">To create an underlined shortcut key, includes an ampersand (&) before the letter that will be the shortcut key.</span></span>  
  
2.  <span data-ttu-id="3a125-110">Dans la fenêtre Propriétés, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.Control.Font%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="3a125-110">In the Properties window, click the ellipsis button (![VisualStudioEllipsesButton screenshot](../media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.Control.Font%2A> property.</span></span>  
  
     <span data-ttu-id="3a125-111">Dans la boîte de dialogue Police standard, sélectionnez la police, le style de police, taille, effets (tels que barré ou soulignement) et script que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="3a125-111">In the standard font dialog box, select the font, font style, size, effects (such as strikeout or underline), and script that you want.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a125-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a125-112">See also</span></span>
- [<span data-ttu-id="3a125-113">Guide pratique pour Définir le texte affiché par un Windows Forms de contrôle</span><span class="sxs-lookup"><span data-stu-id="3a125-113">How to: Set the Text Displayed by a Windows Forms Control</span></span>](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [<span data-ttu-id="3a125-114">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="3a125-114">Using Fonts and Text</span></span>](../advanced/using-fonts-and-text.md)
- [<span data-ttu-id="3a125-115">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3a125-115">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
