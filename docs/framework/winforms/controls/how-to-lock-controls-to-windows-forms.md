---
title: 'Procédure : Verrouiller les contrôles aux Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, locking
- controls [Windows Forms], locking
ms.assetid: 94efe0d2-c14e-4d14-b903-63ea9b07e290
ms.openlocfilehash: cff3b0a3ba547c15e7b1c896bde49931a6a3c742
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702644"
---
# <a name="how-to-lock-controls-to-windows-forms"></a><span data-ttu-id="04101-102">Procédure : Verrouiller les contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04101-102">How to: Lock Controls to Windows Forms</span></span>
<span data-ttu-id="04101-103">Lorsque vous concevez l’interface utilisateur (IU) de votre application Windows, vous pouvez verrouiller les contrôles une fois qu’ils sont correctement placés, afin que vous ne pas par inadvertance de déplacer ou de les redimensionner lors de la définition d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="04101-103">When you design the user interface (UI) of your Windows application, you can lock the controls once they are positioned correctly, so that you do not inadvertently move or resize them when setting other properties.</span></span>  
  
 <span data-ttu-id="04101-104">En outre, vous pouvez verrouiller et déverrouiller tous les contrôles sur le formulaire à la fois, ce qui est utile pour les formulaires avec de nombreux contrôles, ou vous pouvez déverrouiller des contrôles individuels.</span><span class="sxs-lookup"><span data-stu-id="04101-104">Additionally, you can lock and unlock all the controls on the form at once, which is helpful for forms with many controls, or you can unlock individual controls.</span></span> <span data-ttu-id="04101-105">Une fois que vous avez passé tous les contrôles où vous le souhaitez sur le formulaire, les verrouiller tout en place pour empêcher un mouvement erroné.</span><span class="sxs-lookup"><span data-stu-id="04101-105">Once you have placed all the controls where you want them on the form, lock them all in place to prevent erroneous movement.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="04101-106">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="04101-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="04101-107">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="04101-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="04101-108">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="04101-108">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-lock-a-control"></a><span data-ttu-id="04101-109">Pour verrouiller un contrôle</span><span class="sxs-lookup"><span data-stu-id="04101-109">To lock a control</span></span>  
  
1.  <span data-ttu-id="04101-110">Dans le **propriétés** fenêtre, cliquez sur le **verrouillé** propriété et sélectionnez `true`.</span><span class="sxs-lookup"><span data-stu-id="04101-110">In the **Properties** window, click the **Locked** property and select `true`.</span></span> <span data-ttu-id="04101-111">(Double-cliquez sur le nom Active ou désactive le paramètre de propriété.)</span><span class="sxs-lookup"><span data-stu-id="04101-111">(Double-clicking the name toggles the property setting.)</span></span>  
  
     <span data-ttu-id="04101-112">Ou bien, cliquez sur le contrôle et choisissez **verrouille les contrôles**.</span><span class="sxs-lookup"><span data-stu-id="04101-112">Alternatively, right-click the control and choose **Lock Controls**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="04101-113">Contrôles de verrouillage empêche les glissé vers une nouvelle taille ou l’emplacement sur l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="04101-113">Locking controls prevents them from being dragged to a new size or location on the design surface.</span></span> <span data-ttu-id="04101-114">Toutefois, vous pouvez toujours modifier la taille ou l’emplacement des contrôles au moyen de la **propriétés** fenêtre ou dans le code.</span><span class="sxs-lookup"><span data-stu-id="04101-114">However, you can still change the size or location of controls by means of the **Properties** window or in code.</span></span>  
  
### <a name="to-lock-all-the-controls-on-a-form"></a><span data-ttu-id="04101-115">Pour verrouiller tous les contrôles sur un formulaire</span><span class="sxs-lookup"><span data-stu-id="04101-115">To lock all the controls on a form</span></span>  
  
1.  <span data-ttu-id="04101-116">À partir de la **Format** menu, choisissez **verrouille les contrôles**.</span><span class="sxs-lookup"><span data-stu-id="04101-116">From the **Format** menu, choose **Lock Controls**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="04101-117">Cette commande verrouille la taille du formulaire, car un formulaire est un contrôle.</span><span class="sxs-lookup"><span data-stu-id="04101-117">This command locks the form's size as well, because a form is a control.</span></span>  
  
### <a name="to-unlock-all-locked-controls-on-a-form"></a><span data-ttu-id="04101-118">Pour déverrouiller verrouillés tous les contrôles sur un formulaire</span><span class="sxs-lookup"><span data-stu-id="04101-118">To unlock all locked controls on a form</span></span>  
  
1.  <span data-ttu-id="04101-119">À partir de la **Format** menu, choisissez **verrouille les contrôles**.</span><span class="sxs-lookup"><span data-stu-id="04101-119">From the **Format** menu, choose **Lock Controls**.</span></span>  
  
     <span data-ttu-id="04101-120">Tous les contrôles précédemment verrouillés sur le formulaire sont maintenant déverrouillée.</span><span class="sxs-lookup"><span data-stu-id="04101-120">All previously locked controls on the form are now unlocked.</span></span>  
  
### <a name="to-unlock-locked-controls-individually"></a><span data-ttu-id="04101-121">Pour déverrouiller les contrôles verrouillés individuellement</span><span class="sxs-lookup"><span data-stu-id="04101-121">To unlock locked controls individually</span></span>  
  
1.  <span data-ttu-id="04101-122">Dans le **propriétés** fenêtre, cliquez sur le **verrouillé** propriété et sélectionnez `false`.</span><span class="sxs-lookup"><span data-stu-id="04101-122">In the **Properties** window, click the **Locked** property and select `false`.</span></span> <span data-ttu-id="04101-123">(Double-cliquez sur le nom Active ou désactive le paramètre de propriété.)</span><span class="sxs-lookup"><span data-stu-id="04101-123">(Double-clicking the name toggles the property setting.)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04101-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04101-124">See also</span></span>
- [<span data-ttu-id="04101-125">Contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04101-125">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="04101-126">Disposition des contrôles dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04101-126">Arranging Controls on Windows Forms</span></span>](arranging-controls-on-windows-forms.md)
- [<span data-ttu-id="04101-127">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04101-127">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="04101-128">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04101-128">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="04101-129">Classement par fonction des contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04101-129">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
