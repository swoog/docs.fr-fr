---
title: 'Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], populating
- list views [Windows Forms], adding list items
- ListView control [Windows Forms], adding list items
ms.assetid: 1b35a80a-edd8-495f-a807-a28c4aae52c6
ms.openlocfilehash: 8a97d73b9b2c46d02ae0794ad66b20a04db58af6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011123"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control"></a><span data-ttu-id="23644-102">Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="23644-102">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>
<span data-ttu-id="23644-103">Le processus d’ajout d’un élément à un formulaire Windows <xref:System.Windows.Forms.ListView> contrôle se compose principalement de la spécification de l’élément et lui assigner des propriétés.</span><span class="sxs-lookup"><span data-stu-id="23644-103">The process of adding an item to a Windows Forms <xref:System.Windows.Forms.ListView> control consists primarily of specifying the item and assigning properties to it.</span></span> <span data-ttu-id="23644-104">Ajouter ou supprimer des éléments de liste peut être effectuée à tout moment.</span><span class="sxs-lookup"><span data-stu-id="23644-104">Adding or removing list items can be done at any time.</span></span>  
  
### <a name="to-add-items-programmatically"></a><span data-ttu-id="23644-105">Pour ajouter des éléments par programmation</span><span class="sxs-lookup"><span data-stu-id="23644-105">To add items programmatically</span></span>  
  
1. <span data-ttu-id="23644-106">Utilisez le <xref:System.Windows.Forms.ListView.ListViewItemCollection.Add%2A> méthode de la <xref:System.Windows.Forms.ListView.Items%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="23644-106">Use the <xref:System.Windows.Forms.ListView.ListViewItemCollection.Add%2A> method of the <xref:System.Windows.Forms.ListView.Items%2A> property.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#11)]  
  
### <a name="to-remove-items-programmatically"></a><span data-ttu-id="23644-107">Pour supprimer des éléments par programmation</span><span class="sxs-lookup"><span data-stu-id="23644-107">To remove items programmatically</span></span>  
  
1. <span data-ttu-id="23644-108">Utilisez le <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> ou <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> méthode de la <xref:System.Windows.Forms.ListView.Items%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="23644-108">Use the <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> or <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> method of the <xref:System.Windows.Forms.ListView.Items%2A> property.</span></span> <span data-ttu-id="23644-109">Le <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> méthode supprime un élément unique ; le <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> méthode supprime tous les éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="23644-109">The <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> method removes a single item; the <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> method removes all items from the list.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a><span data-ttu-id="23644-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23644-110">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- [<span data-ttu-id="23644-111">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="23644-111">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="23644-112">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="23644-112">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
