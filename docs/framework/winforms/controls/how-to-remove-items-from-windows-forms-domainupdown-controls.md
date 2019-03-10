---
title: 'Procédure : Supprimer des éléments dans des contrôles DomainUpDown Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DomainUpDown control [Windows Forms], removing items from
- spin button control [Windows Forms], removing items
ms.assetid: e70f5cbc-b497-41a9-975a-344c00e56ed2
ms.openlocfilehash: 58c93f478414d24c2fdda0f9662936a8b520e381
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708962"
---
# <a name="how-to-remove-items-from-windows-forms-domainupdown-controls"></a><span data-ttu-id="01ef1-102">Procédure : Supprimer des éléments dans des contrôles DomainUpDown Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01ef1-102">How to: Remove Items from Windows Forms DomainUpDown Controls</span></span>
<span data-ttu-id="01ef1-103">Vous pouvez supprimer des éléments de formulaires Windows <xref:System.Windows.Forms.DomainUpDown> contrôle en appelant le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> ou <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> méthode de la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="01ef1-103">You can remove items from the Windows Forms <xref:System.Windows.Forms.DomainUpDown> control by calling the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> or <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> method of the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> class.</span></span> <span data-ttu-id="01ef1-104">Le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> méthode supprime un élément spécifique, tandis que le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> méthode supprime un élément par sa position.</span><span class="sxs-lookup"><span data-stu-id="01ef1-104">The <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> method removes a specific item, while the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> method removes an item by its position.</span></span>  
  
### <a name="to-remove-an-item"></a><span data-ttu-id="01ef1-105">Pour supprimer un élément</span><span class="sxs-lookup"><span data-stu-id="01ef1-105">To remove an item</span></span>  
  
-   <span data-ttu-id="01ef1-106">Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> méthode de la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe pour supprimer un élément par nom.</span><span class="sxs-lookup"><span data-stu-id="01ef1-106">Use the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> method of the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> class to remove an item by name.</span></span>  
  
    ```vb  
    DomainUpDown1.Items.Remove("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Remove("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Remove("noodles");  
    ```  
  
     <span data-ttu-id="01ef1-107">ou</span><span class="sxs-lookup"><span data-stu-id="01ef1-107">-or-</span></span>  
  
-   <span data-ttu-id="01ef1-108">Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> méthode pour supprimer un élément par sa position.</span><span class="sxs-lookup"><span data-stu-id="01ef1-108">Use the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> method to remove an item by its position.</span></span>  
  
    ```vb  
    ' Removes the first item in the list.  
    DomainUpDown1.Items.RemoveAt(0)  
    ```  
  
    ```csharp  
    // Removes the first item in the list.  
    domainUpDown1.Items.RemoveAt(0);  
    ```  
  
    ```cpp  
    // Removes the first item in the list.  
    domainUpDown1->Items->RemoveAt(0);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="01ef1-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01ef1-109">See also</span></span>
- <xref:System.Windows.Forms.DomainUpDown>
- <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A?displayProperty=nameWithType>
- [<span data-ttu-id="01ef1-110">DomainUpDown, contrôle</span><span class="sxs-lookup"><span data-stu-id="01ef1-110">DomainUpDown Control</span></span>](domainupdown-control-windows-forms.md)
- [<span data-ttu-id="01ef1-111">Vue d’ensemble du contrôle DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="01ef1-111">DomainUpDown Control Overview</span></span>](domainupdown-control-overview-windows-forms.md)
