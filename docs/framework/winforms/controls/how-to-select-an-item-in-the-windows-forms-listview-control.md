---
title: 'Procédure : Sélectionnez un élément dans le contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lists [Windows Forms], selecting items
- ListView control [Windows Forms], selecting items
- selection [Windows Forms], in list views
- list views [Windows Forms], selecting items
ms.assetid: ddea918e-1ddf-47f4-bd09-1e9b4c9d0c39
ms.openlocfilehash: ed3e68fbe77f194ed04d15f99a48657a32a13b50
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644714"
---
# <a name="how-to-select-an-item-in-the-windows-forms-listview-control"></a><span data-ttu-id="fe978-102">Procédure : Sélectionnez un élément dans le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fe978-102">How to: Select an Item in the Windows Forms ListView Control</span></span>
<span data-ttu-id="fe978-103">Cet exemple montre comment sélectionner par programme un élément dans un formulaire Windows <xref:System.Windows.Forms.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe978-103">This example demonstrates how to programmatically select an item in a Windows Forms <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="fe978-104">Sélection d’un élément par programme ne change pas automatiquement le focus à la <xref:System.Windows.Forms.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe978-104">Selecting an item programmatically does not automatically change the focus to the <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="fe978-105">Pour cette raison, vous également souhaitez généralement définir l’élément comme ayant le focus lors de la sélection d’un élément.</span><span class="sxs-lookup"><span data-stu-id="fe978-105">For this reason, you will typically also want to set the item as focused when selecting an item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fe978-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe978-106">Example</span></span>  
 [!code-csharp[System.Windows.Forms.ListView.Misc#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Misc#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fe978-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="fe978-107">Compiling the Code</span></span>  
 <span data-ttu-id="fe978-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="fe978-108">This example requires:</span></span>  
  
-   <span data-ttu-id="fe978-109">Un <xref:System.Windows.Forms.ListView> contrôle nommé `listView1` qui contient au moins un élément.</span><span class="sxs-lookup"><span data-stu-id="fe978-109">A <xref:System.Windows.Forms.ListView> control named `listView1` that contains at least one item.</span></span>  
  
-   <span data-ttu-id="fe978-110">Références aux espaces de noms <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="fe978-110">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe978-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe978-111">See also</span></span>
- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListViewItem.Selected%2A?displayProperty=nameWithType>
