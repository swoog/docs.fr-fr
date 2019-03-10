---
title: 'Procédure : Désigner un contrôle Button Windows Forms comme bouton accepter à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], default on Windows Forms
- Accept button on Windows Forms
- Button control [Windows Forms], designating as default
- Windows Forms controls, default button on form
ms.assetid: a1da0590-755f-49f2-aca7-609fac6351bf
ms.openlocfilehash: 61f0c99560d008cc10c94403ac936e5b97267d3a
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707649"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-accept-button-using-the-designer"></a><span data-ttu-id="ad6bf-102">Procédure : Désigner un contrôle Button Windows Forms comme bouton accepter à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="ad6bf-102">How to: Designate a Windows Forms Button as the Accept Button Using the Designer</span></span>
<span data-ttu-id="ad6bf-103">Sur n’importe quel formulaire Windows, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle de bouton Accepter, également connu sous le bouton par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-103">On any Windows Form, you can designate a <xref:System.Windows.Forms.Button> control to be the accept button, also known as the default button.</span></span> <span data-ttu-id="ad6bf-104">Chaque fois que l’utilisateur appuie sur la touche entrée, le bouton par défaut un clic sur quel autre contrôle sur le formulaire a le focus.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-104">Whenever the user presses the ENTER key, the default button is clicked regardless of which other control on the form has the focus.</span></span> <span data-ttu-id="ad6bf-105">Les exceptions sont lorsque le contrôle ayant le focus est un autre bouton, dans ce cas, un clic sur le bouton qui a le focus, ou une zone de texte multiligne ou un contrôle personnalisé qui intercepte la touche ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-105">The exceptions to this are when the control with focus is another button — in that case, the button with the focus will be clicked — or a multiline text box, or a custom control that traps the ENTER key.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ad6bf-106">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="ad6bf-107">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="ad6bf-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="ad6bf-108">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="ad6bf-108">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-designate-the-accept-button"></a><span data-ttu-id="ad6bf-109">Pour désigner le bouton Accepter</span><span class="sxs-lookup"><span data-stu-id="ad6bf-109">To designate the accept button</span></span>  
  
1.  <span data-ttu-id="ad6bf-110">Sélectionnez le formulaire sur lequel réside le bouton.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-110">Select the form on which the button resides.</span></span>  
  
2.  <span data-ttu-id="ad6bf-111">Dans le **propriétés** fenêtre, définissez le formulaire <xref:System.Windows.Forms.Form.AcceptButton%2A> propriété le <xref:System.Windows.Forms.Button> nom du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-111">In the **Properties** window, set the form's <xref:System.Windows.Forms.Form.AcceptButton%2A> property to the <xref:System.Windows.Forms.Button> control's name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad6bf-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad6bf-112">See also</span></span>
- <xref:System.Windows.Forms.Form.AcceptButton%2A>
- [<span data-ttu-id="ad6bf-113">Vue d'ensemble du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="ad6bf-113">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="ad6bf-114">Méthodes de sélection du contrôle Button Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ad6bf-114">Ways to Select a Windows Forms Button Control</span></span>](ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="ad6bf-115">Guide pratique pour Répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ad6bf-115">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="ad6bf-116">Guide pratique pour Désigner un contrôle Button Windows Forms comme bouton Annuler à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="ad6bf-116">How to: Designate a Windows Forms Button as the Cancel Button Using the Designer</span></span>](designate-a-wf-button-as-the-cancel-button-using-the-designer.md)
- [<span data-ttu-id="ad6bf-117">Button, contrôle</span><span class="sxs-lookup"><span data-stu-id="ad6bf-117">Button Control</span></span>](button-control-windows-forms.md)
