---
title: 'Procédure : Implémenter l’Interface IListSource'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [Windows Forms], implementing
- IListSource interface
ms.assetid: 63ce27aa-2e23-4fbd-8228-0c1726f6c421
ms.openlocfilehash: 331abebf3336d8444559c117f5747597bc3b0122
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728211"
---
# <a name="how-to-implement-the-ilistsource-interface"></a><span data-ttu-id="9c757-102">Procédure : Implémenter l’Interface IListSource</span><span class="sxs-lookup"><span data-stu-id="9c757-102">How to: Implement the IListSource Interface</span></span>
<span data-ttu-id="9c757-103">Implémenter le <xref:System.ComponentModel.IListSource> interface permettant de créer une classe pouvant être liée qui n’implémente pas <xref:System.Collections.IList> mais plutôt une liste à partir d’un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="9c757-103">Implement the <xref:System.ComponentModel.IListSource> interface to create a bindable class that does not implement <xref:System.Collections.IList> but instead provides a list from another location.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9c757-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9c757-104">Example</span></span>  
 <span data-ttu-id="9c757-105">L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.IListSource> interface.</span><span class="sxs-lookup"><span data-stu-id="9c757-105">The following code example demonstrates how to implement the <xref:System.ComponentModel.IListSource> interface.</span></span> <span data-ttu-id="9c757-106">Un composant nommé `EmployeeListSource` expose un <xref:System.Collections.IList> pour la liaison de données en implémentant le <xref:System.ComponentModel.IListSource.GetList%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="9c757-106">A component named `EmployeeListSource` exposes an <xref:System.Collections.IList> for data binding by implementing the <xref:System.ComponentModel.IListSource.GetList%2A> method.</span></span>  
  
 [!code-csharp[System.ComponentModel.IListSource#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/EmployeeListSource.cs#1)]
 [!code-vb[System.ComponentModel.IListSource#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/EmployeeListSource.vb#1)]  
  
 [!code-csharp[System.ComponentModel.IListSource#10](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/Employee.cs#10)]
 [!code-vb[System.ComponentModel.IListSource#10](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/Employee.vb#10)]  
  
 [!code-csharp[System.ComponentModel.IListSource#100](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/BusinessObjectBase.cs#100)]
 [!code-vb[System.ComponentModel.IListSource#100](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/BusinessObjectBase.vb#100)]  
  
 [!code-csharp[System.ComponentModel.IListSource#1000](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/Form1.cs#1000)]
 [!code-vb[System.ComponentModel.IListSource#1000](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/Form1.vb#1000)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9c757-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9c757-107">Compiling the Code</span></span>  
 <span data-ttu-id="9c757-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="9c757-108">This example requires:</span></span>  
  
-   <span data-ttu-id="9c757-109">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="9c757-109">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c757-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c757-110">See also</span></span>
- <xref:System.ComponentModel.IListSource>
- <xref:System.ComponentModel.ITypedList>
- <xref:System.ComponentModel.BindingList%601>
- <xref:System.ComponentModel.IBindingList>
- [<span data-ttu-id="9c757-111">Liaison de données et Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9c757-111">Data Binding and Windows Forms</span></span>](../../../docs/framework/winforms/data-binding-and-windows-forms.md)
