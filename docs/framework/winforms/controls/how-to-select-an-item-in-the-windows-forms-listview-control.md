---
title: 'Comment : sélectionner un élément dans le contrôle ListView Windows Forms'
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
ms.openlocfilehash: 8256eaeddf98c5a0dd80357bcd562e8f66db85b3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33532819"
---
# <a name="how-to-select-an-item-in-the-windows-forms-listview-control"></a>Comment : sélectionner un élément dans le contrôle ListView Windows Forms
Cet exemple montre comment sélectionner par programme un élément dans un Windows Forms <xref:System.Windows.Forms.ListView> contrôle. Sélection d’un élément par programme ne change pas automatiquement le focus vers le <xref:System.Windows.Forms.ListView> contrôle. Pour cette raison, vous serez généralement également définir l’élément comme ayant le focus lors de la sélection d’un élément.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.ListView.Misc#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Misc#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   A <xref:System.Windows.Forms.ListView> contrôle nommé `listView1` qui contient au moins un élément.  
  
-   Références aux espaces de noms <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.ListView>  
 <xref:System.Windows.Forms.ListViewItem.Selected%2A?displayProperty=nameWithType>
