---
title: 'Procédure : Rechercher des données dans un contrôle DataRepeater (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, implementing search
- DataRepeater, searching data
ms.assetid: a8ab5d17-b94f-43c4-8dd7-d0450226d73f
ms.openlocfilehash: 514e72afc9570071f57e385574456ff7d716bad7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654384"
---
# <a name="how-to-search-data-in-a-datarepeater-control-visual-studio"></a><span data-ttu-id="c292f-102">Procédure : Rechercher des données dans un contrôle DataRepeater (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="c292f-102">How to: Search Data in a DataRepeater Control (Visual Studio)</span></span>
<span data-ttu-id="c292f-103">Lorsque vous utilisez un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle qui contient de nombreux enregistrements, vous souhaiterez peut-être permettre aux utilisateurs, recherchez un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="c292f-103">When you are using a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control that contains many records, you may want to let users search for a specific record.</span></span> <span data-ttu-id="c292f-104">Au lieu de rechercher les données dans le contrôle lui-même, vous pouvez implémenter une recherche en interrogeant sous-jacent <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="c292f-104">Rather than searching the data in the control itself, you can implement a search by querying the underlying <xref:System.Windows.Forms.BindingSource>.</span></span> <span data-ttu-id="c292f-105">Si l’élément est trouvé, vous pouvez ensuite utiliser le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A> propriété pour sélectionner l’élément et de faire défiler dans la vue.</span><span class="sxs-lookup"><span data-stu-id="c292f-105">If the item is found, you can then use the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A> property to select the item and scroll it into view.</span></span>  
  
### <a name="to-implement-search"></a><span data-ttu-id="c292f-106">Pour implémenter la recherche</span><span class="sxs-lookup"><span data-stu-id="c292f-106">To implement search</span></span>  
  
1.  <span data-ttu-id="c292f-107">Faites glisser un contrôle <xref:System.Windows.Forms.TextBox> de la **Boîte à outils** vers le formulaire qui contient le contrôle <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> .</span><span class="sxs-lookup"><span data-stu-id="c292f-107">Drag a <xref:System.Windows.Forms.TextBox> control from the **Toolbox** onto the form that contains the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
2.  <span data-ttu-id="c292f-108">Dans la fenêtre Propriétés, attribuez à la propriété **Name** la valeur **SearchTextBox**.</span><span class="sxs-lookup"><span data-stu-id="c292f-108">In the Properties window, change the **Name** property to **SearchTextBox**.</span></span>  
  
3.  <span data-ttu-id="c292f-109">Faites glisser un contrôle <xref:System.Windows.Forms.Button> de la **Boîte à outils** vers le formulaire qui contient le contrôle <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> .</span><span class="sxs-lookup"><span data-stu-id="c292f-109">Drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** onto the form that contains the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
4.  <span data-ttu-id="c292f-110">Dans la fenêtre Propriétés, attribuez à la propriété **Name** la valeur **SearchButton**.</span><span class="sxs-lookup"><span data-stu-id="c292f-110">In the Properties window, change the **Name** property to **SearchButton**.</span></span> <span data-ttu-id="c292f-111">Affectez à la propriété **Text** la valeur **Search**.</span><span class="sxs-lookup"><span data-stu-id="c292f-111">Change the **Text** property to **Search**.</span></span>  
  
5.  <span data-ttu-id="c292f-112">Double-cliquez sur le contrôle <xref:System.Windows.Forms.Button> pour ouvrir l’éditeur de code et ajoutez le code suivant au gestionnaire d’événements `SearchButton_Click` .</span><span class="sxs-lookup"><span data-stu-id="c292f-112">Double-click the <xref:System.Windows.Forms.Button> control to open the Code Editor, and add the following code to the `SearchButton_Click` event handler.</span></span>  
  
     [!code-vb[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-search-data-in-a-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-search-data-in-a-datarepeater-control-visual-studio_1.cs)]  
  
     <span data-ttu-id="c292f-113">Remplacez *ProductsBindingSource* par le nom de la <xref:System.Windows.Forms.BindingSource> pour votre <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>et remplacez *ProductID* avec le nom du champ que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="c292f-113">Replace *ProductsBindingSource* with the name of the <xref:System.Windows.Forms.BindingSource> for your <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>, and replace *ProductID* with the name of the field that you want to search.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c292f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c292f-114">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [<span data-ttu-id="c292f-115">Introduction au contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="c292f-115">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="c292f-116">Dépannage des problèmes liés au contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="c292f-116">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="c292f-117">Guide pratique pour Modifier l’apparence d’un contrôle DataRepeater</span><span class="sxs-lookup"><span data-stu-id="c292f-117">How to: Change the Appearance of a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
