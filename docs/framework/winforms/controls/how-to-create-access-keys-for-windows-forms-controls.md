---
title: 'Procédure : créer des clés d’accès pour les contrôles Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [Windows Forms], access keys
- Button control [Windows Forms], access keys
- dialog box controls [Windows Forms], mnemonics
- access keys [Windows Forms], creating for controls
- mnemonics [Windows Forms], adding to dialog box controls
- mnemonics
- ampersand character in shortcut key
- Windows Forms controls, access keys
- examples [Windows Forms], controls
- Text property [Windows Forms], specifying access keys for controls
- keyboard shortcuts [Windows Forms], creating for controls
- access keys [Windows Forms], Windows Forms
- ALT key
ms.assetid: 4faa0991-28ec-4eca-91db-51dc2cd6a7ac
ms.openlocfilehash: e6c829553163359301bad2cd896fc43562ee8069
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59334456"
---
# <a name="how-to-create-access-keys-for-windows-forms-controls"></a><span data-ttu-id="68dcb-102">Procédure : créer des clés d’accès pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="68dcb-102">How to: Create Access Keys for Windows Forms Controls</span></span>
<span data-ttu-id="68dcb-103">Un *clé d’accès* est un caractère souligné dans le texte d’un menu, un élément de menu ou l’étiquette d’un contrôle tel qu’un bouton.</span><span class="sxs-lookup"><span data-stu-id="68dcb-103">An *access key* is an underlined character in the text of a menu, menu item, or the label of a control such as a button.</span></span> <span data-ttu-id="68dcb-104">Avec une clé d’accès, l’utilisateur peut « cliquer » un bouton en appuyant sur la touche ALT conjointement avec la clé d’accès prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="68dcb-104">With an access key, the user can "click" a button by pressing the ALT key in combination with the predefined access key.</span></span> <span data-ttu-id="68dcb-105">Par exemple, si un bouton exécute une procédure pour imprimer un formulaire et par conséquent son `Text` propriété est définie à « Impression », en ajoutant une esperluette avant la lettre « P » provoque la lettre « P » être souligné dans le texte du bouton en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="68dcb-105">For example, if a button runs a procedure to print a form, and therefore its `Text` property is set to "Print," adding an ampersand before the letter "P" causes the letter "P" to be underlined in the button text at run time.</span></span> <span data-ttu-id="68dcb-106">L’utilisateur peut exécuter la commande associée au bouton en appuyant sur ALT + P.</span><span class="sxs-lookup"><span data-stu-id="68dcb-106">The user can run the command associated with the button by pressing ALT+P.</span></span> <span data-ttu-id="68dcb-107">Vous ne pouvez avoir une clé d’accès pour un contrôle qui ne peut pas recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="68dcb-107">You cannot have an access key for a control that cannot receive focus.</span></span>  
  
### <a name="to-create-an-access-key-for-a-control"></a><span data-ttu-id="68dcb-108">Pour créer une clé d’accès pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="68dcb-108">To create an access key for a control</span></span>  
  
1. <span data-ttu-id="68dcb-109">Définir le `Text` propriété à une chaîne qui inclut une esperluette (&) avant la lettre qui sera le raccourci.</span><span class="sxs-lookup"><span data-stu-id="68dcb-109">Set the `Text` property to a string that includes an ampersand (&) before the letter that will be the shortcut.</span></span>  
  
    ```vb  
    ' Set the letter "P" as an access key.  
    Button1.Text = "&Print"  
    ```  
  
    ```csharp  
    // Set the letter "P" as an access key.  
    button1.Text = "&Print";  
    ```  
  
    ```cpp  
    // Set the letter "P" as an access key.  
    button1->Text = "&Print";  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="68dcb-110">Pour inclure une esperluette dans une légende sans créer une clé d’accès, insérez deux et commerciaux (& &).</span><span class="sxs-lookup"><span data-stu-id="68dcb-110">To include an ampersand in a caption without creating an access key, include two ampersands (&&).</span></span> <span data-ttu-id="68dcb-111">Une esperluette unique s’affiche dans la légende et aucun caractère n’est soulignées.</span><span class="sxs-lookup"><span data-stu-id="68dcb-111">A single ampersand is displayed in the caption and no characters are underlined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68dcb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68dcb-112">See also</span></span>

- <xref:System.Windows.Forms.Button>
- [<span data-ttu-id="68dcb-113">Procédure : répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="68dcb-113">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="68dcb-114">Procédure : définir le texte affiché par un contrôle Windows Forms</span><span class="sxs-lookup"><span data-stu-id="68dcb-114">How to: Set the Text Displayed by a Windows Forms Control</span></span>](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [<span data-ttu-id="68dcb-115">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="68dcb-115">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
