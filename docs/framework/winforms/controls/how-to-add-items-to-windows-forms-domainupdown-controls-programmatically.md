---
title: 'Procédure : Ajouter des éléments à des contrôles DomainUpDown Windows Forms par programmation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- spin button control [Windows Forms], adding items
- DomainUpDown control [Windows Forms], adding items to
ms.assetid: fd31d314-33eb-4181-90f8-d32ed0c4e072
ms.openlocfilehash: 865f569da561ec5883b0a0f08fcedb34fc84820c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738558"
---
# <a name="how-to-add-items-to-windows-forms-domainupdown-controls-programmatically"></a>Procédure : Ajouter des éléments à des contrôles DomainUpDown Windows Forms par programmation
Vous pouvez ajouter des éléments pour les formulaires Windows <xref:System.Windows.Forms.DomainUpDown> contrôle dans le code. Appelez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> ou <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> méthode de la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe pour ajouter des éléments du contrôle <xref:System.Windows.Forms.DomainUpDown.Items%2A> propriété. Le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> méthode ajoute un élément à la fin d’une collection, tandis que le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> méthode ajoute un élément à une position spécifiée.  
  
### <a name="to-add-a-new-item"></a>Pour ajouter un nouvel élément  
  
1.  Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A> pour ajouter un élément à la fin de la liste des éléments.  
  
    ```vb  
    DomainUpDown1.Items.Add("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Add("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Add("noodles");  
    ```  
  
     ou  
  
2.  Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A> méthode pour insérer un élément dans la liste à une position spécifiée.  
  
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
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DomainUpDown>
- <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A?displayProperty=nameWithType>
- <xref:System.Collections.ArrayList.Insert%2A?displayProperty=nameWithType>
- [DomainUpDown, contrôle](../../../../docs/framework/winforms/controls/domainupdown-control-windows-forms.md)
- [Vue d’ensemble du contrôle DomainUpDown](../../../../docs/framework/winforms/controls/domainupdown-control-overview-windows-forms.md)
