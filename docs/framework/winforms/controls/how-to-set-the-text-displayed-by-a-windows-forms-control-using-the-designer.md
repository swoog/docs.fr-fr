---
title: 'Procédure : définir le texte affiché par un contrôle Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], setting caption
- Windows Forms, setting the text displayed
ms.assetid: 9d18e0e0-f17f-4074-837d-e67ceeeaa89d
ms.openlocfilehash: 37ab3823a41cca2eeea550c90e92e90bc364c759
ms.sourcegitcommit: ffd7dd79468a81bbb0d6449f6d65513e050c04c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2019
ms.locfileid: "65960349"
---
# <a name="how-to-set-the-text-displayed-by-a-windows-forms-control-using-the-designer"></a><span data-ttu-id="f9a78-102">Procédure : définir le texte affiché par un contrôle Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="f9a78-102">How to: Set the Text Displayed by a Windows Forms Control Using the Designer</span></span>

<span data-ttu-id="f9a78-103">Contrôles Windows Forms affichent généralement un texte qui est lié à la fonction principale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f9a78-103">Windows Forms controls typically display some text that is related to the primary function of the control.</span></span> <span data-ttu-id="f9a78-104">Par exemple, un <xref:System.Windows.Forms.Button> contrôle affiche habituellement une légende qui indique quelle action sera effectuée lorsque le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="f9a78-104">For example, a <xref:System.Windows.Forms.Button> control typically displays a caption that indicates what action will be performed when the button is clicked.</span></span> <span data-ttu-id="f9a78-105">Pour tous les contrôles, vous pouvez définir ou retourner le texte à l'aide de la propriété <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="f9a78-105">For all controls, you can set or return the text by using the <xref:System.Windows.Forms.Control.Text%2A> property.</span></span> <span data-ttu-id="f9a78-106">Vous pouvez modifier la police en utilisant la propriété <xref:System.Windows.Forms.Control.Font%2A>.</span><span class="sxs-lookup"><span data-stu-id="f9a78-106">You can change the font by using the <xref:System.Windows.Forms.Control.Font%2A> property.</span></span>

### <a name="to-set-the-text-and-font-with-the-designer"></a><span data-ttu-id="f9a78-107">Pour définir le texte et la police avec le Concepteur</span><span class="sxs-lookup"><span data-stu-id="f9a78-107">To set the text and font with the designer</span></span>

1. <span data-ttu-id="f9a78-108">Dans la fenêtre Propriétés, définissez la <xref:System.Windows.Forms.Control.Text%2A> propriété du contrôle à une chaîne appropriée.</span><span class="sxs-lookup"><span data-stu-id="f9a78-108">In the Properties window, set the <xref:System.Windows.Forms.Control.Text%2A> property of the control to an appropriate string.</span></span>

     <span data-ttu-id="f9a78-109">Pour créer une touche de raccourci soulignée, incluez une esperluette (&) avant la lettre qui sera la touche de raccourci.</span><span class="sxs-lookup"><span data-stu-id="f9a78-109">To create an underlined shortcut key, includes an ampersand (&) before the letter that will be the shortcut key.</span></span>

2. <span data-ttu-id="f9a78-110">Dans la fenêtre Propriétés, cliquez sur le bouton de sélection (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) à côté du <xref:System.Windows.Forms.Control.Font%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f9a78-110">In the Properties window, click the ellipsis button (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) next to the <xref:System.Windows.Forms.Control.Font%2A> property.</span></span>

     <span data-ttu-id="f9a78-111">Dans la boîte de dialogue Police standard, sélectionnez la police, le style de police, taille, effets (tels que barré ou soulignement) et script que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f9a78-111">In the standard font dialog box, select the font, font style, size, effects (such as strikeout or underline), and script that you want.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9a78-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9a78-112">See also</span></span>

- [<span data-ttu-id="f9a78-113">Guide pratique pour Définir le texte affiché par un Windows Forms de contrôle</span><span class="sxs-lookup"><span data-stu-id="f9a78-113">How to: Set the Text Displayed by a Windows Forms Control</span></span>](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [<span data-ttu-id="f9a78-114">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="f9a78-114">Using Fonts and Text</span></span>](../advanced/using-fonts-and-text.md)
- [<span data-ttu-id="f9a78-115">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f9a78-115">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
