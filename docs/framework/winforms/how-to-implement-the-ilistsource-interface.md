---
title: 'Procédure : implémenter l’interface IListSource'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [Windows Forms], implementing
- IListSource interface
ms.assetid: 63ce27aa-2e23-4fbd-8228-0c1726f6c421
ms.openlocfilehash: bd4e554b7e4be51847496307b50be3084d0115d5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59159781"
---
# <a name="how-to-implement-the-ilistsource-interface"></a><span data-ttu-id="913d4-102">Procédure : implémenter l’interface IListSource</span><span class="sxs-lookup"><span data-stu-id="913d4-102">How to: Implement the IListSource Interface</span></span>
<span data-ttu-id="913d4-103">Implémenter le <xref:System.ComponentModel.IListSource> interface permettant de créer une classe pouvant être liée qui n’implémente pas <xref:System.Collections.IList> mais plutôt une liste à partir d’un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="913d4-103">Implement the <xref:System.ComponentModel.IListSource> interface to create a bindable class that does not implement <xref:System.Collections.IList> but instead provides a list from another location.</span></span>  
  
## <a name="example"></a><span data-ttu-id="913d4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="913d4-104">Example</span></span>  
 <span data-ttu-id="913d4-105">L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.IListSource> interface.</span><span class="sxs-lookup"><span data-stu-id="913d4-105">The following code example demonstrates how to implement the <xref:System.ComponentModel.IListSource> interface.</span></span> <span data-ttu-id="913d4-106">Un composant nommé `EmployeeListSource` expose un <xref:System.Collections.IList> pour la liaison de données en implémentant le <xref:System.ComponentModel.IListSource.GetList%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="913d4-106">A component named `EmployeeListSource` exposes an <xref:System.Collections.IList> for data binding by implementing the <xref:System.ComponentModel.IListSource.GetList%2A> method.</span></span>  
  
 [!code-csharp[System.ComponentModel.IListSource#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/EmployeeListSource.cs#1)]
 [!code-vb[System.ComponentModel.IListSource#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/EmployeeListSource.vb#1)]  
  
 [!code-csharp[System.ComponentModel.IListSource#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/Employee.cs#10)]
 [!code-vb[System.ComponentModel.IListSource#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/Employee.vb#10)]  
  
 [!code-csharp[System.ComponentModel.IListSource#100](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/BusinessObjectBase.cs#100)]
 [!code-vb[System.ComponentModel.IListSource#100](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/BusinessObjectBase.vb#100)]  
  
 [!code-csharp[System.ComponentModel.IListSource#1000](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/Form1.cs#1000)]
 [!code-vb[System.ComponentModel.IListSource#1000](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/Form1.vb#1000)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="913d4-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="913d4-107">Compiling the Code</span></span>  
 <span data-ttu-id="913d4-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="913d4-108">This example requires:</span></span>  
  
-   <span data-ttu-id="913d4-109">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="913d4-109">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="913d4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="913d4-110">See also</span></span>

- <xref:System.ComponentModel.IListSource>
- <xref:System.ComponentModel.ITypedList>
- <xref:System.ComponentModel.BindingList%601>
- <xref:System.ComponentModel.IBindingList>
- [<span data-ttu-id="913d4-111">Liaison de données et Windows Forms</span><span class="sxs-lookup"><span data-stu-id="913d4-111">Data Binding and Windows Forms</span></span>](data-binding-and-windows-forms.md)
