---
title: 'Procédure : ajouter des éléments à des contrôles DomainUpDown Windows Forms par programmation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- spin button control [Windows Forms], adding items
- DomainUpDown control [Windows Forms], adding items to
ms.assetid: fd31d314-33eb-4181-90f8-d32ed0c4e072
ms.openlocfilehash: ef44a9e68b8007d57fc7442a178ae98322747c99
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59343673"
---
# <a name="how-to-add-items-to-windows-forms-domainupdown-controls-programmatically"></a><span data-ttu-id="4e5ef-102">Procédure : ajouter des éléments à des contrôles DomainUpDown Windows Forms par programmation</span><span class="sxs-lookup"><span data-stu-id="4e5ef-102">How to: Add Items to Windows Forms DomainUpDown Controls Programmatically</span></span>
<span data-ttu-id="4e5ef-103">Vous pouvez ajouter des éléments pour les formulaires Windows <xref:System.Windows.Forms.DomainUpDown> contrôle dans le code.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-103">You can add items to the Windows Forms <xref:System.Windows.Forms.DomainUpDown> control in code.</span></span> <span data-ttu-id="4e5ef-104">Appelez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> ou <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> méthode de la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe pour ajouter des éléments du contrôle <xref:System.Windows.Forms.DomainUpDown.Items%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-104">Call the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> or <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> method of the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> class to add items to the control's <xref:System.Windows.Forms.DomainUpDown.Items%2A> property.</span></span> <span data-ttu-id="4e5ef-105">Le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> méthode ajoute un élément à la fin d’une collection, tandis que le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> méthode ajoute un élément à une position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-105">The <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> method adds an item to the end of a collection, while the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> method adds an item at a specified position.</span></span>  
  
### <a name="to-add-a-new-item"></a><span data-ttu-id="4e5ef-106">Pour ajouter un nouvel élément</span><span class="sxs-lookup"><span data-stu-id="4e5ef-106">To add a new item</span></span>  
  
1. <span data-ttu-id="4e5ef-107">Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> pour ajouter un élément à la fin de la liste des éléments.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-107">Use the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> method to add an item to the end of the list of items.</span></span>  
  
    ```vb  
    DomainUpDown1.Items.Add("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Add("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Add("noodles");  
    ```  
  
     <span data-ttu-id="4e5ef-108">- ou -</span><span class="sxs-lookup"><span data-stu-id="4e5ef-108">-or-</span></span>  
  
2. <span data-ttu-id="4e5ef-109">Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> méthode pour insérer un élément dans la liste à une position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-109">Use the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> method to insert an item into the list at a specified position.</span></span>  
  
    ```vb  
    ' Inserts an item at the third position in the list  
    DomainUpDown1.Items.Insert(2, "rice")  
    ```  
  
    ```csharp  
    // Inserts an item at the third position in the list  
    domainUpDown1.Items.Insert(2, "rice");  
    ```  
  
    ```cpp  
    // Inserts an item at the third position in the list  
    domainUpDown1->Items->Insert(2, "rice");  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="4e5ef-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e5ef-110">See also</span></span>

- <xref:System.Windows.Forms.DomainUpDown>
- <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A?displayProperty=nameWithType>
- <xref:System.Collections.ArrayList.Insert%2A?displayProperty=nameWithType>
- [<span data-ttu-id="4e5ef-111">DomainUpDown, contrôle</span><span class="sxs-lookup"><span data-stu-id="4e5ef-111">DomainUpDown Control</span></span>](domainupdown-control-windows-forms.md)
- [<span data-ttu-id="4e5ef-112">Vue d’ensemble du contrôle DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="4e5ef-112">DomainUpDown Control Overview</span></span>](domainupdown-control-overview-windows-forms.md)
