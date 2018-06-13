---
title: 'Comment : rechercher des données dans un contrôle DataRepeater (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, implementing search
- DataRepeater, searching data
ms.assetid: a8ab5d17-b94f-43c4-8dd7-d0450226d73f
ms.openlocfilehash: 689990ee125c85c3151a4e965b619fde068d220e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588052"
---
# <a name="how-to-search-data-in-a-datarepeater-control-visual-studio"></a><span data-ttu-id="21fc7-102">Comment : rechercher des données dans un contrôle DataRepeater (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="21fc7-102">How to: Search Data in a DataRepeater Control (Visual Studio)</span></span>
<span data-ttu-id="21fc7-103">Lorsque vous utilisez un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle qui contient plusieurs enregistrements, vous pouvez souhaiter permettre aux utilisateurs, recherchez un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="21fc7-103">When you are using a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control that contains many records, you may want to let users search for a specific record.</span></span> <span data-ttu-id="21fc7-104">Au lieu de rechercher les données dans le contrôle lui-même, vous pouvez implémenter une recherche en interrogeant sous-jacent <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="21fc7-104">Rather than searching the data in the control itself, you can implement a search by querying the underlying <xref:System.Windows.Forms.BindingSource>.</span></span> <span data-ttu-id="21fc7-105">Si l’élément est trouvé, vous pouvez ensuite utiliser le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A> propriété pour sélectionner l’élément et de faire défiler dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="21fc7-105">If the item is found, you can then use the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A> property to select the item and scroll it into view.</span></span>  
  
### <a name="to-implement-search"></a><span data-ttu-id="21fc7-106">Pour implémenter la recherche</span><span class="sxs-lookup"><span data-stu-id="21fc7-106">To implement search</span></span>  
  
1.  <span data-ttu-id="21fc7-107">Faites glisser un contrôle <xref:System.Windows.Forms.TextBox> de la **Boîte à outils** vers le formulaire qui contient le contrôle <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> .</span><span class="sxs-lookup"><span data-stu-id="21fc7-107">Drag a <xref:System.Windows.Forms.TextBox> control from the **Toolbox** onto the form that contains the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
2.  <span data-ttu-id="21fc7-108">Dans la fenêtre Propriétés, attribuez à la propriété **Name** la valeur **SearchTextBox**.</span><span class="sxs-lookup"><span data-stu-id="21fc7-108">In the Properties window, change the **Name** property to **SearchTextBox**.</span></span>  
  
3.  <span data-ttu-id="21fc7-109">Faites glisser un contrôle <xref:System.Windows.Forms.Button> de la **Boîte à outils** vers le formulaire qui contient le contrôle <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> .</span><span class="sxs-lookup"><span data-stu-id="21fc7-109">Drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** onto the form that contains the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
4.  <span data-ttu-id="21fc7-110">Dans la fenêtre Propriétés, attribuez à la propriété **Name** la valeur **SearchButton**.</span><span class="sxs-lookup"><span data-stu-id="21fc7-110">In the Properties window, change the **Name** property to **SearchButton**.</span></span> <span data-ttu-id="21fc7-111">Affectez à la propriété **Text** la valeur **Search**.</span><span class="sxs-lookup"><span data-stu-id="21fc7-111">Change the **Text** property to **Search**.</span></span>  
  
5.  <span data-ttu-id="21fc7-112">Double-cliquez sur le contrôle <xref:System.Windows.Forms.Button> pour ouvrir l’éditeur de code et ajoutez le code suivant au gestionnaire d’événements `SearchButton_Click` .</span><span class="sxs-lookup"><span data-stu-id="21fc7-112">Double-click the <xref:System.Windows.Forms.Button> control to open the Code Editor, and add the following code to the `SearchButton_Click` event handler.</span></span>  
  
     [!code-vb[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-search-data-in-a-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-search-data-in-a-datarepeater-control-visual-studio_1.cs)]  
  
     <span data-ttu-id="21fc7-113">Remplacez *ProductsBindingSource* avec le nom de la <xref:System.Windows.Forms.BindingSource> pour votre <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>et remplacez *ProductID* avec le nom du champ que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="21fc7-113">Replace *ProductsBindingSource* with the name of the <xref:System.Windows.Forms.BindingSource> for your <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>, and replace *ProductID* with the name of the field that you want to search.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21fc7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21fc7-114">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [<span data-ttu-id="21fc7-115">Introduction au contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="21fc7-115">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="21fc7-116">Dépannage des problèmes liés au contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="21fc7-116">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="21fc7-117">Guide pratique : modifier l’apparence d’un contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="21fc7-117">How to: Change the Appearance of a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
