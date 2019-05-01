---
title: 'Procédure : désigner un bouton Windows Forms comme bouton Annuler à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 30e77d9c-d565-4ab5-a84a-62c043af8822
ms.openlocfilehash: f127a1a74643c975aea73b24896c098b365aa327
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972300"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button-using-the-designer"></a><span data-ttu-id="d107f-102">Procédure : désigner un bouton Windows Forms comme bouton Annuler à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="d107f-102">How to: Designate a Windows Forms Button as the Cancel Button Using the Designer</span></span>
<span data-ttu-id="d107f-103">Sur n’importe quel formulaire Windows, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle soit le bouton Annuler.</span><span class="sxs-lookup"><span data-stu-id="d107f-103">On any Windows Form, you can designate a <xref:System.Windows.Forms.Button> control to be the cancel button.</span></span> <span data-ttu-id="d107f-104">Un bouton Annuler est activé chaque fois que l’utilisateur appuie sur la touche ÉCHAP, quels que soient les autres contrôles du formulaire a le focus.</span><span class="sxs-lookup"><span data-stu-id="d107f-104">A cancel button is clicked whenever the user presses the ESC key, regardless of which other control on the form has the focus.</span></span> <span data-ttu-id="d107f-105">Ce bouton est généralement programmé pour permettre à l’utilisateur à quitter rapidement une opération sans effectuer d’action.</span><span class="sxs-lookup"><span data-stu-id="d107f-105">Such a button is usually programmed to enable the user to quickly exit an operation without committing to any action.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d107f-106">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="d107f-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="d107f-107">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="d107f-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="d107f-108">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="d107f-108">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-designate-the-cancel-button"></a><span data-ttu-id="d107f-109">Pour désigner le bouton Annuler</span><span class="sxs-lookup"><span data-stu-id="d107f-109">To designate the cancel button</span></span>  
  
1. <span data-ttu-id="d107f-110">Sélectionnez le formulaire sur lequel réside le bouton.</span><span class="sxs-lookup"><span data-stu-id="d107f-110">Select the form on which the button resides.</span></span>  
  
2. <span data-ttu-id="d107f-111">Dans le **propriétés** fenêtre, définissez le formulaire <xref:System.Windows.Forms.Form.CancelButton%2A> propriété le <xref:System.Windows.Forms.Button> nom du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d107f-111">In the **Properties** window, set the form's <xref:System.Windows.Forms.Form.CancelButton%2A> property to the <xref:System.Windows.Forms.Button> control's name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d107f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d107f-112">See also</span></span>

- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [<span data-ttu-id="d107f-113">Vue d'ensemble du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="d107f-113">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="d107f-114">Méthodes de sélection du contrôle Button Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d107f-114">Ways to Select a Windows Forms Button Control</span></span>](ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="d107f-115">Guide pratique pour Répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d107f-115">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="d107f-116">Guide pratique pour Désigner un contrôle Button Windows Forms comme bouton accepter à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="d107f-116">How to: Designate a Windows Forms Button as the Accept Button Using the Designer</span></span>](designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [<span data-ttu-id="d107f-117">Button, contrôle</span><span class="sxs-lookup"><span data-stu-id="d107f-117">Button Control</span></span>](button-control-windows-forms.md)
