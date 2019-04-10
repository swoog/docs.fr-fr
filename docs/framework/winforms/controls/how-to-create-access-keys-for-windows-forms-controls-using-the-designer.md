---
title: 'Procédure : créer des clés d’accès pour les contrôles Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], access keys
- Button control [Windows Forms], access keys
- dialog box controls [Windows Forms], mnemonics
- access keys [Windows Forms], creating for controls
- mnemonics [Windows Forms], adding to dialog box controls
- ampersand character in shortcut key
- Windows Forms controls, access keys
- examples [Windows Forms], controls
- Text property [Windows Forms], specifying access keys for controls
- keyboard shortcuts [Windows Forms], creating for controls
- access keys [Windows Forms], Windows Forms
- ALT key
ms.assetid: 4c374c4c-4ca9-4a68-ac96-9dc3ab0f518a
ms.openlocfilehash: 410fc0134046c5fa7e05bfcd38ce6818244a0a54
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59307871"
---
# <a name="how-to-create-access-keys-for-windows-forms-controls-using-the-designer"></a><span data-ttu-id="826a5-102">Procédure : créer des clés d’accès pour les contrôles Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="826a5-102">How to: Create Access Keys for Windows Forms Controls Using the Designer</span></span>
<span data-ttu-id="826a5-103">Un *clé d’accès* est un caractère souligné dans le texte d’un menu, un élément de menu ou l’étiquette d’un contrôle tel qu’un bouton.</span><span class="sxs-lookup"><span data-stu-id="826a5-103">An *access key* is an underlined character in the text of a menu, menu item, or the label of a control such as a button.</span></span> <span data-ttu-id="826a5-104">Il permet à l’utilisateur « cliquer » sur un bouton en appuyant sur la touche ALT conjointement avec la clé d’accès prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="826a5-104">It enables the user to "click" a button by pressing the ALT key in combination with the predefined access key.</span></span> <span data-ttu-id="826a5-105">Par exemple, si un bouton exécute une procédure pour imprimer un formulaire et par conséquent son `Text` propriété est définie sur « Imprimer », ajoutant une esperluette (&) devant la lettre « P » a « P » être soulignées dans le texte du bouton au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="826a5-105">For example, if a button runs a procedure to print a form, and therefore its `Text` property is set to "Print," adding an ampersand (&) before the letter "P" causes the letter "P" to be underlined in the button text at run time.</span></span> <span data-ttu-id="826a5-106">L’utilisateur peut exécuter la commande associée au bouton en appuyant sur ALT + P.</span><span class="sxs-lookup"><span data-stu-id="826a5-106">The user can run the command associated with the button by pressing ALT+P.</span></span> <span data-ttu-id="826a5-107">Vous ne pouvez avoir une clé d’accès pour un contrôle qui ne peut pas recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="826a5-107">You cannot have an access key for a control that cannot receive focus.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="826a5-108">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="826a5-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="826a5-109">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="826a5-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="826a5-110">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="826a5-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-an-access-key-for-a-control"></a><span data-ttu-id="826a5-111">Pour créer une clé d’accès pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="826a5-111">To create an access key for a control</span></span>  
  
1. <span data-ttu-id="826a5-112">Dans le **propriétés** fenêtre, définissez le `Text` propriété à une chaîne qui inclut une esperluette (&) avant la lettre qui sera la clé d’accès.</span><span class="sxs-lookup"><span data-stu-id="826a5-112">In the **Properties** window, set the `Text` property to a string that includes an ampersand (&) before the letter that will be the access key.</span></span> <span data-ttu-id="826a5-113">Par exemple, pour définir la lettre « P » comme touche d’accès, tapez **& impression** dans la grille.</span><span class="sxs-lookup"><span data-stu-id="826a5-113">For example, to set the letter "P" as the access key, type **&Print** into the grid.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="826a5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="826a5-114">See also</span></span>

- <xref:System.Windows.Forms.Button>
- [<span data-ttu-id="826a5-115">Procédure : répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="826a5-115">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="826a5-116">Procédure : définir le texte affiché par un contrôle Windows Forms</span><span class="sxs-lookup"><span data-stu-id="826a5-116">How to: Set the Text Displayed by a Windows Forms Control</span></span>](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [<span data-ttu-id="826a5-117">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="826a5-117">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
