---
title: "Comment : désactiver l'ajout et la suppression d'éléments dans un contrôle DataRepeater (Visual Studio)"
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, disabling delete
- DataRepeater, disabling add
ms.assetid: 298d8f60-ddfe-4361-ab66-cf76d0df5220
ms.openlocfilehash: e3d0d2a8d422054e269ee92df1fdfcb5acb96eac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33590797"
---
# <a name="how-to-disable-adding-and-deleting-datarepeater-items-visual-studio"></a><span data-ttu-id="14391-102">Comment : désactiver l'ajout et la suppression d'éléments dans un contrôle DataRepeater (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="14391-102">How to: Disable Adding and Deleting DataRepeater Items (Visual Studio)</span></span>
<span data-ttu-id="14391-103">Par défaut, les utilisateurs peuvent ajouter et supprimer des éléments dans un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.</span><span class="sxs-lookup"><span data-stu-id="14391-103">By default, users can add and delete items in a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span> <span data-ttu-id="14391-104">Les utilisateurs peuvent ajouter un nouvel élément en appuyant sur CTRL + N lorsqu’un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> a le focus ou en cliquant sur le **AddNewItem** bouton sur le <xref:System.Windows.Forms.BindingNavigator> contrôle.</span><span class="sxs-lookup"><span data-stu-id="14391-104">Users can add a new item by pressing CTRL+N when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> has focus or by clicking the **AddNewItem** button on the <xref:System.Windows.Forms.BindingNavigator> control.</span></span> <span data-ttu-id="14391-105">Les utilisateurs peuvent supprimer un élément en appuyant sur SUPPR lorsqu’un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> a le focus ou en cliquant sur le **DeleteItem** bouton sur le <xref:System.Windows.Forms.BindingNavigator> contrôle.</span><span class="sxs-lookup"><span data-stu-id="14391-105">Users can delete an item by pressing DELETE when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> has focus or by clicking the **DeleteItem** button on the <xref:System.Windows.Forms.BindingNavigator> control.</span></span>  
  
 <span data-ttu-id="14391-106">Vous pouvez désactiver Ajout et/ou la suppression au moment du design ou au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="14391-106">You can disable adding and/or deleting at design time or at run time.</span></span>  
  
### <a name="to-disable-adding-and-deleting-at-design-time"></a><span data-ttu-id="14391-107">Pour désactiver l’ajout et la suppression au moment du design</span><span class="sxs-lookup"><span data-stu-id="14391-107">To disable adding and deleting at design time</span></span>  
  
1.  <span data-ttu-id="14391-108">Dans le Concepteur Windows Forms, sélectionnez le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.</span><span class="sxs-lookup"><span data-stu-id="14391-108">In the Windows Forms Designer, select the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="14391-109">Vous devez sélectionner la section inférieure du contrôle.</span><span class="sxs-lookup"><span data-stu-id="14391-109">You must select the lower section of the control.</span></span> <span data-ttu-id="14391-110">Si vous sélectionnez la section de modèle d’élément, un ensemble différent de propriétés s’affichera.</span><span class="sxs-lookup"><span data-stu-id="14391-110">If you select the item template section, a different set of properties will be displayed.</span></span>  
  
2.  <span data-ttu-id="14391-111">Dans la fenêtre Propriétés, définissez la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A> propriété **False**.</span><span class="sxs-lookup"><span data-stu-id="14391-111">In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A> property to **False**.</span></span>  
  
3.  <span data-ttu-id="14391-112">Définir le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A> propriété **False**.</span><span class="sxs-lookup"><span data-stu-id="14391-112">Set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A> property to **False**.</span></span>  
  
4.  <span data-ttu-id="14391-113">Dans le Concepteur Windows Forms, sélectionnez le <xref:System.Windows.Forms.BindingNavigator> contrôler, puis cliquez sur le **AddNewItem** bouton (le bouton avec un signe plus).</span><span class="sxs-lookup"><span data-stu-id="14391-113">In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator> control, and then click the **AddNewItem** button (the button with a plus sign on it).</span></span>  
  
5.  <span data-ttu-id="14391-114">Dans la fenêtre Propriétés, définissez la <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> propriété **False**.</span><span class="sxs-lookup"><span data-stu-id="14391-114">In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property to **False**.</span></span>  
  
6.  <span data-ttu-id="14391-115">Dans le Concepteur Windows Forms, sélectionnez le <xref:System.Windows.Forms.BindingNavigator> contrôler, puis cliquez sur le **DeleteItem** bouton (le bouton avec un X rouge).</span><span class="sxs-lookup"><span data-stu-id="14391-115">In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator> control, and then click the **DeleteItem** button (the button with a red X on it).</span></span>  
  
7.  <span data-ttu-id="14391-116">Dans la fenêtre Propriétés, définissez la <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> propriété **False**.</span><span class="sxs-lookup"><span data-stu-id="14391-116">In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property to **False**.</span></span>  
  
8.  <span data-ttu-id="14391-117">Dans la barre d’état du composant, sélectionnez le <xref:System.Windows.Forms.BindingSource> auquel le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> est lié.</span><span class="sxs-lookup"><span data-stu-id="14391-117">In the Component Tray, select the <xref:System.Windows.Forms.BindingSource> to which the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> is bound.</span></span>  
  
9. <span data-ttu-id="14391-118">Dans la fenêtre Propriétés, définissez la <xref:System.Windows.Forms.BindingSource.AllowNew%2A> propriété **False**.</span><span class="sxs-lookup"><span data-stu-id="14391-118">In the Properties window, set the <xref:System.Windows.Forms.BindingSource.AllowNew%2A> property to **False**.</span></span>  
  
10. <span data-ttu-id="14391-119">Dans le Concepteur Windows Forms, double-cliquez sur le **DeleteItem** bouton pour ouvrir l’éditeur de Code.</span><span class="sxs-lookup"><span data-stu-id="14391-119">In the Windows Forms Designer, double-click the **DeleteItem** button to open the Code Editor.</span></span>  
  
11. <span data-ttu-id="14391-120">Dans la liste déroulante d’événements, sélectionnez le `BindingNavigatorDeleteItem_EnabledChanged` événement.</span><span class="sxs-lookup"><span data-stu-id="14391-120">In the Events drop-down list, select the `BindingNavigatorDeleteItem_EnabledChanged` event.</span></span>  
  
12. <span data-ttu-id="14391-121">Ajoutez le code suivant au gestionnaire d'événements `BindingNavigatorDeleteItem_EnabledChanged` :</span><span class="sxs-lookup"><span data-stu-id="14391-121">Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.vb)]  
  
    > [!NOTE]
    >  <span data-ttu-id="14391-122">Cette étape est nécessaire car <xref:System.Windows.Forms.BindingSource> active le bouton **DeleteItem** chaque fois que l’enregistrement actif est modifié.</span><span class="sxs-lookup"><span data-stu-id="14391-122">This step is necessary because the <xref:System.Windows.Forms.BindingSource> will enable the **DeleteItem** button every time that the current record changes.</span></span>  
  
### <a name="to-disable-adding-and-deleting-at-run-time"></a><span data-ttu-id="14391-123">Pour désactiver l’ajout et la suppression en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="14391-123">To disable adding and deleting at run time</span></span>  
  
1.  <span data-ttu-id="14391-124">Dans le Concepteur Windows Forms, double-cliquez sur le formulaire pour ouvrir l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="14391-124">In the Windows Forms Designer, double-click the form to open the Code Editor.</span></span>  
  
2.  <span data-ttu-id="14391-125">Ajoutez le code suivant à l’événement `Form_Load` .</span><span class="sxs-lookup"><span data-stu-id="14391-125">Add the following code to the `Form_Load` event:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_2.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_2.vb)]  
  
3.  <span data-ttu-id="14391-126">Ajoutez le code suivant au gestionnaire d'événements `BindingNavigatorDeleteItem_EnabledChanged` :</span><span class="sxs-lookup"><span data-stu-id="14391-126">Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.vb)]  
  
    > [!NOTE]
    >  <span data-ttu-id="14391-127">Cette étape est nécessaire car <xref:System.Windows.Forms.BindingSource> active le bouton **DeleteItem** chaque fois que l’enregistrement actif est modifié.</span><span class="sxs-lookup"><span data-stu-id="14391-127">This step is necessary because the <xref:System.Windows.Forms.BindingSource> will enable the **DeleteItem** button every time that the current record changes.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="14391-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14391-128">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [<span data-ttu-id="14391-129">Introduction au contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="14391-129">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="14391-130">Dépannage des problèmes liés au contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="14391-130">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
