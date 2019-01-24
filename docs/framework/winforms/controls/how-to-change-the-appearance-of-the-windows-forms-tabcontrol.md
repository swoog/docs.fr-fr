---
title: 'Procédure : Modifier l’apparence du contrôle TabControl Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- icons [Windows Forms], displaying on tabs
- TabControl control [Windows Forms], changing page appearance
- tabs [Windows Forms], controlling appearance
- buttons [Windows Forms], displaying tabs as
ms.assetid: 7c6cc443-ed62-4d26-b94d-b8913b44f773
ms.openlocfilehash: 1ed062b3991d7738269d30a6ff13cda3c80927c2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630318"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-tabcontrol"></a><span data-ttu-id="51a75-102">Procédure : Modifier l’apparence du contrôle TabControl Windows Forms</span><span class="sxs-lookup"><span data-stu-id="51a75-102">How to: Change the Appearance of the Windows Forms TabControl</span></span>
<span data-ttu-id="51a75-103">Vous pouvez modifier l’apparence des onglets dans les Windows Forms à l’aide des propriétés de la <xref:System.Windows.Forms.TabControl> et <xref:System.Windows.Forms.TabPage> objets qui composent les différents onglets du contrôle.</span><span class="sxs-lookup"><span data-stu-id="51a75-103">You can change the appearance of tabs in Windows Forms by using properties of the <xref:System.Windows.Forms.TabControl> and the <xref:System.Windows.Forms.TabPage> objects that make up the individual tabs on the control.</span></span> <span data-ttu-id="51a75-104">En définissant ces propriétés, vous pouvez afficher des images sur les onglets, afficher des onglets verticalement plutôt qu’horizontalement, afficher plusieurs lignes d’onglets et activer ou désactiver les onglets par programmation.</span><span class="sxs-lookup"><span data-stu-id="51a75-104">By setting these properties, you can display images on tabs, display tabs vertically instead of horizontally, display multiple rows of tabs, and enable or disable tabs programmatically.</span></span>  
  
### <a name="to-display-an-icon-on-the-label-part-of-a-tab"></a><span data-ttu-id="51a75-105">Pour afficher une icône sur la partie de l’étiquette d’un onglet</span><span class="sxs-lookup"><span data-stu-id="51a75-105">To display an icon on the label part of a tab</span></span>  
  
1.  <span data-ttu-id="51a75-106">Ajouter un <xref:System.Windows.Forms.ImageList> contrôle au formulaire.</span><span class="sxs-lookup"><span data-stu-id="51a75-106">Add an <xref:System.Windows.Forms.ImageList> control to the form.</span></span>  
  
2.  <span data-ttu-id="51a75-107">Ajouter des images à la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="51a75-107">Add images to the image list.</span></span>  
  
     <span data-ttu-id="51a75-108">Pour plus d’informations sur les listes d’images, consultez [composant ImageList](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md) et [Comment : Ajouter ou supprimer des Images avec les Windows Forms composant ImageList](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span><span class="sxs-lookup"><span data-stu-id="51a75-108">For more information about image lists, see [ImageList Component](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md) and [How to: Add or Remove Images with the Windows Forms ImageList Component](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span>  
  
3.  <span data-ttu-id="51a75-109">Définir le <xref:System.Windows.Forms.TabControl.ImageList%2A> propriété de la <xref:System.Windows.Forms.TabControl> à la <xref:System.Windows.Forms.ImageList> contrôle.</span><span class="sxs-lookup"><span data-stu-id="51a75-109">Set the <xref:System.Windows.Forms.TabControl.ImageList%2A> property of the <xref:System.Windows.Forms.TabControl> to the <xref:System.Windows.Forms.ImageList> control.</span></span>  
  
4.  <span data-ttu-id="51a75-110">Définir le <xref:System.Windows.Forms.TabPage.ImageIndex%2A> propriété de la <xref:System.Windows.Forms.TabPage> à l’index d’une image appropriée dans la liste.</span><span class="sxs-lookup"><span data-stu-id="51a75-110">Set the <xref:System.Windows.Forms.TabPage.ImageIndex%2A> property of the <xref:System.Windows.Forms.TabPage> to the index of an appropriate image in the list.</span></span>  
  
### <a name="to-create-multiple-rows-of-tabs"></a><span data-ttu-id="51a75-111">Pour créer plusieurs lignes d’onglets</span><span class="sxs-lookup"><span data-stu-id="51a75-111">To create multiple rows of tabs</span></span>  
  
1.  <span data-ttu-id="51a75-112">Ajoutez le nombre de pages d’onglets.</span><span class="sxs-lookup"><span data-stu-id="51a75-112">Add the number of tab pages you want.</span></span>  
  
2.  <span data-ttu-id="51a75-113">Définir le <xref:System.Windows.Forms.TabControl.Multiline%2A> propriété de la <xref:System.Windows.Forms.TabControl> à `true`.</span><span class="sxs-lookup"><span data-stu-id="51a75-113">Set the <xref:System.Windows.Forms.TabControl.Multiline%2A> property of the <xref:System.Windows.Forms.TabControl> to `true`.</span></span>  
  
3.  <span data-ttu-id="51a75-114">Si les onglets n’apparaissent pas déjà dans plusieurs lignes, définissez la <xref:System.Windows.Forms.Control.Width%2A> propriété de la <xref:System.Windows.Forms.TabControl> à être plus restrictif que tous les onglets.</span><span class="sxs-lookup"><span data-stu-id="51a75-114">If the tabs do not already appear in multiple rows, set the <xref:System.Windows.Forms.Control.Width%2A> property of the <xref:System.Windows.Forms.TabControl> to be narrower than all the tabs.</span></span>  
  
### <a name="to-arrange-tabs-on-the-side-of-the-control"></a><span data-ttu-id="51a75-115">Pour réorganiser les onglets sur le côté du contrôle</span><span class="sxs-lookup"><span data-stu-id="51a75-115">To arrange tabs on the side of the control</span></span>  
  
-   <span data-ttu-id="51a75-116">Définir le <xref:System.Windows.Forms.TabControl.Alignment%2A> propriété de la <xref:System.Windows.Forms.TabControl> à <xref:System.Windows.Forms.TabAlignment.Left> ou <xref:System.Windows.Forms.TabAlignment.Right>.</span><span class="sxs-lookup"><span data-stu-id="51a75-116">Set the <xref:System.Windows.Forms.TabControl.Alignment%2A> property of the <xref:System.Windows.Forms.TabControl> to <xref:System.Windows.Forms.TabAlignment.Left> or <xref:System.Windows.Forms.TabAlignment.Right>.</span></span>  
  
### <a name="to-programmatically-enable-or-disable-all-controls-on-a-tab"></a><span data-ttu-id="51a75-117">Pour activer ou désactiver tous les contrôles sur un onglet par programme</span><span class="sxs-lookup"><span data-stu-id="51a75-117">To programmatically enable or disable all controls on a tab</span></span>  
  
1.  <span data-ttu-id="51a75-118">Définir le <xref:System.Windows.Forms.TabPage.Enabled%2A> propriété de la <xref:System.Windows.Forms.TabPage> à `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="51a75-118">Set the <xref:System.Windows.Forms.TabPage.Enabled%2A> property of the <xref:System.Windows.Forms.TabPage> to `true` or `false`.</span></span>  
  
    ```vb  
    TabPage1.Enabled = False  
    ```  
  
    ```csharp  
    tabPage1.Enabled = false;  
    ```  
  
    ```cpp  
    tabPage1->Enabled = false;  
    ```  
  
### <a name="to-display-tabs-as-buttons"></a><span data-ttu-id="51a75-119">Pour afficher les onglets sous forme de boutons</span><span class="sxs-lookup"><span data-stu-id="51a75-119">To display tabs as buttons</span></span>  
  
-   <span data-ttu-id="51a75-120">Définir le <xref:System.Windows.Forms.TabControl.Appearance%2A> propriété de la <xref:System.Windows.Forms.TabControl> à <xref:System.Windows.Forms.TabAppearance.Buttons> ou <xref:System.Windows.Forms.TabAppearance.FlatButtons>.</span><span class="sxs-lookup"><span data-stu-id="51a75-120">Set the <xref:System.Windows.Forms.TabControl.Appearance%2A> property of the <xref:System.Windows.Forms.TabControl> to <xref:System.Windows.Forms.TabAppearance.Buttons> or <xref:System.Windows.Forms.TabAppearance.FlatButtons>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51a75-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51a75-121">See also</span></span>
- [<span data-ttu-id="51a75-122">TabControl, contrôle</span><span class="sxs-lookup"><span data-stu-id="51a75-122">TabControl Control</span></span>](../../../../docs/framework/winforms/controls/tabcontrol-control-windows-forms.md)
- [<span data-ttu-id="51a75-123">Vue d’ensemble du contrôle TabControl</span><span class="sxs-lookup"><span data-stu-id="51a75-123">TabControl Control Overview</span></span>](../../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)
- [<span data-ttu-id="51a75-124">Guide pratique pour Ajouter un contrôle à une Page d’onglets</span><span class="sxs-lookup"><span data-stu-id="51a75-124">How to: Add a Control to a Tab Page</span></span>](../../../../docs/framework/winforms/controls/how-to-add-a-control-to-a-tab-page.md)
- [<span data-ttu-id="51a75-125">Guide pratique pour Désactiver les Pages d’onglets</span><span class="sxs-lookup"><span data-stu-id="51a75-125">How to: Disable Tab Pages</span></span>](../../../../docs/framework/winforms/controls/how-to-disable-tab-pages.md)
- [<span data-ttu-id="51a75-126">Guide pratique pour Ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="51a75-126">How to: Add and Remove Tabs with the Windows Forms TabControl</span></span>](../../../../docs/framework/winforms/controls/how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
