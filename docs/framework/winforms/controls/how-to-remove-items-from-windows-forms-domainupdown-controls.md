---
title: 'Comment : supprimer des éléments des contrôles DomainUpDown Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DomainUpDown control [Windows Forms], removing items from
- spin button control [Windows Forms], removing items
ms.assetid: e70f5cbc-b497-41a9-975a-344c00e56ed2
ms.openlocfilehash: 702e5e2180148758c4b3775a5cc96a1365703166
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33532159"
---
# <a name="how-to-remove-items-from-windows-forms-domainupdown-controls"></a>Comment : supprimer des éléments des contrôles DomainUpDown Windows Forms
Vous pouvez supprimer des éléments à partir de Windows Forms <xref:System.Windows.Forms.DomainUpDown> contrôle en appelant le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> ou <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> méthode de la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe. Le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> méthode supprime un élément spécifique, tandis que le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> méthode supprime un élément par sa position.  
  
### <a name="to-remove-an-item"></a>Pour supprimer un élément  
  
-   Utilisez le <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> méthode de la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe pour supprimer un élément par son nom.  
  
    ```vb  
    DomainUpDown1.Items.Remove("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Remove("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Remove("noodles");  
    ```  
  
     - ou -  
  
-   Utilisez la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> méthode pour supprimer un élément par sa position.  
  
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
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.DomainUpDown>  
 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A?displayProperty=nameWithType>  
 [DomainUpDown, contrôle](../../../../docs/framework/winforms/controls/domainupdown-control-windows-forms.md)  
 [Vue d’ensemble du contrôle DomainUpDown](../../../../docs/framework/winforms/controls/domainupdown-control-overview-windows-forms.md)
