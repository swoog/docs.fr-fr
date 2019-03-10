---
title: Méthodes de sélection du contrôle Button Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Button control [Windows Forms], selecting
ms.assetid: fe2fc058-5118-4f70-b264-6147d64a7a8d
ms.openlocfilehash: 86ef0da37ec35b991557af97a97bc9ca3da2d68c
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717256"
---
# <a name="ways-to-select-a-windows-forms-button-control"></a><span data-ttu-id="1d98e-102">Méthodes de sélection du contrôle Button Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1d98e-102">Ways to Select a Windows Forms Button Control</span></span>
<span data-ttu-id="1d98e-103">Un contrôle button Windows Forms peut être sélectionné comme suit :</span><span class="sxs-lookup"><span data-stu-id="1d98e-103">A Windows Forms button can be selected in the following ways:</span></span>  
  
-   <span data-ttu-id="1d98e-104">Utilisez une souris pour cliquer sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="1d98e-104">Use a mouse to click the button.</span></span>  
  
-   <span data-ttu-id="1d98e-105">Appeler le bouton <xref:System.Windows.Forms.Control.Click> événement dans le code.</span><span class="sxs-lookup"><span data-stu-id="1d98e-105">Invoke the button's <xref:System.Windows.Forms.Control.Click> event in code.</span></span>  
  
-   <span data-ttu-id="1d98e-106">Déplacer le focus sur le bouton en appuyant sur la touche TAB, puis choisissez le bouton en appuyant sur la touche espace ou entrée.</span><span class="sxs-lookup"><span data-stu-id="1d98e-106">Move the focus to the button by pressing the TAB key, and then choose the button by pressing the SPACEBAR or ENTER.</span></span>  
  
-   <span data-ttu-id="1d98e-107">Appuyez sur la touche d’accès rapide (ALT + la lettre soulignée) pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="1d98e-107">Press the access key (ALT + the underlined letter) for the button.</span></span> <span data-ttu-id="1d98e-108">Pour plus d’informations sur les clés d’accès, consultez [Comment : Créer des clés d’accès pour les contrôles de Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1d98e-108">For more information about access keys, see [How to: Create Access Keys for Windows Forms Controls](how-to-create-access-keys-for-windows-forms-controls.md).</span></span>  
  
-   <span data-ttu-id="1d98e-109">Si le bouton est le bouton « accepter » du formulaire, en appuyant sur entrée choisit le bouton, même si un autre contrôle a le focus, sauf si ce contrôle est un autre bouton, une zone de texte multiligne ou un contrôle personnalisé qui intercepte la touche ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="1d98e-109">If the button is the "accept" button of the form, pressing ENTER chooses the button, even if another control has the focus — except if that other control is another button, a multi-line text box, or a custom control that traps the enter key.</span></span>  
  
-   <span data-ttu-id="1d98e-110">Si le bouton est le bouton « cancel » du formulaire, en appuyant sur ÉCHAP choisit le bouton, même si un autre contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="1d98e-110">If the button is the "cancel" button of the form, pressing ESC chooses the button, even if another control has the focus.</span></span>  
  
-   <span data-ttu-id="1d98e-111">Appelez le <xref:System.Windows.Forms.Button.PerformClick%2A> méthode afin de sélectionner le bouton par programme.</span><span class="sxs-lookup"><span data-stu-id="1d98e-111">Call the <xref:System.Windows.Forms.Button.PerformClick%2A> method to select the button programmatically.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d98e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d98e-112">See also</span></span>
- [<span data-ttu-id="1d98e-113">Vue d'ensemble du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="1d98e-113">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="1d98e-114">Guide pratique pour Répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1d98e-114">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="1d98e-115">Button, contrôle</span><span class="sxs-lookup"><span data-stu-id="1d98e-115">Button Control</span></span>](button-control-windows-forms.md)
