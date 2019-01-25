---
title: 'Procédure : Implémenter l’Interface ITypedList'
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
ms.openlocfilehash: 3d12c0b82d9475981d0c72f082665b11135d8bb0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54562166"
---
# <a name="how-to-implement-the-itypedlist-interface"></a><span data-ttu-id="edfff-102">Procédure : Implémenter l’Interface ITypedList</span><span class="sxs-lookup"><span data-stu-id="edfff-102">How to: Implement the ITypedList Interface</span></span>
<span data-ttu-id="edfff-103">Implémentez le <xref:System.ComponentModel.ITypedList> interface pour activer la découverte du schéma pour une liste pouvant être liée.</span><span class="sxs-lookup"><span data-stu-id="edfff-103">Implement the <xref:System.ComponentModel.ITypedList> interface to enable discovery of the schema for a bindable list.</span></span>  
  
## <a name="example"></a><span data-ttu-id="edfff-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="edfff-104">Example</span></span>  
 <span data-ttu-id="edfff-105">L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.ITypedList> interface.</span><span class="sxs-lookup"><span data-stu-id="edfff-105">The following code example demonstrates how to implement the <xref:System.ComponentModel.ITypedList> interface.</span></span> <span data-ttu-id="edfff-106">Un type générique nommé `SortableBindingList` dérive le <xref:System.ComponentModel.BindingList%601> classe et implémente la <xref:System.ComponentModel.ITypedList> interface.</span><span class="sxs-lookup"><span data-stu-id="edfff-106">A generic type named `SortableBindingList` derives from the <xref:System.ComponentModel.BindingList%601> class and implements the <xref:System.ComponentModel.ITypedList> interface.</span></span> <span data-ttu-id="edfff-107">Une classe simple nommée `Customer` fournit des données, qui sont liées à l’en-tête d’un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="edfff-107">A simple class named `Customer` provides data, which is bound to the header of a <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 [!code-csharp[System.ComponentModel.ITypedList#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/SortableBindingList.cs#1)]
 [!code-vb[System.ComponentModel.ITypedList#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/SortableBindingList.vb#1)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#10](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Customer.cs#10)]
 [!code-vb[System.ComponentModel.ITypedList#10](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Customer.vb#10)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#100](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Form1.cs#100)]
 [!code-vb[System.ComponentModel.ITypedList#100](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Form1.vb#100)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="edfff-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="edfff-108">Compiling the Code</span></span>  
 <span data-ttu-id="edfff-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="edfff-109">This example requires:</span></span>  
  
-   <span data-ttu-id="edfff-110">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="edfff-110">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="edfff-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edfff-111">See also</span></span>
- <xref:System.ComponentModel.ITypedList>
- <xref:System.ComponentModel.BindingList%601>
- <xref:System.ComponentModel.IBindingList>
- [<span data-ttu-id="edfff-112">Liaison de données et Windows Forms</span><span class="sxs-lookup"><span data-stu-id="edfff-112">Data Binding and Windows Forms</span></span>](../../../docs/framework/winforms/data-binding-and-windows-forms.md)
