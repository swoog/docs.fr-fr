---
title: 'Procédure : implémenter l’interface ITypedList'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ITypedList interface
- BindingList(Of T) class
- data binding [Windows Forms], implementing
- IBindingList interface
ms.assetid: 834cc15c-50bc-4a8b-a610-313d6a217357
ms.openlocfilehash: 3f5a5032166087c7398d310071b3998c845e2780
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64630738"
---
# <a name="how-to-implement-the-itypedlist-interface"></a>Procédure : implémenter l’interface ITypedList
Implémentez le <xref:System.ComponentModel.ITypedList> interface pour activer la découverte du schéma pour une liste pouvant être liée.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.ITypedList> interface. Un type générique nommé `SortableBindingList` dérive le <xref:System.ComponentModel.BindingList%601> classe et implémente la <xref:System.ComponentModel.ITypedList> interface. Une classe simple nommée `Customer` fournit des données, qui sont liées à l’en-tête d’un <xref:System.Windows.Forms.DataGridView> contrôle.  
  
 [!code-csharp[System.ComponentModel.ITypedList#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/SortableBindingList.cs#1)]
 [!code-vb[System.ComponentModel.ITypedList#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/SortableBindingList.vb#1)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Customer.cs#10)]
 [!code-vb[System.ComponentModel.ITypedList#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Customer.vb#10)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#100](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Form1.cs#100)]
 [!code-vb[System.ComponentModel.ITypedList#100](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Form1.vb#100)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- Références aux assemblys System.Drawing et System.Windows.Forms.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ComponentModel.ITypedList>
- <xref:System.ComponentModel.BindingList%601>
- <xref:System.ComponentModel.IBindingList>
- [Liaison de données et Windows Forms](data-binding-and-windows-forms.md)
