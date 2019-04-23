---
title: 'Procédure : Lister les formats de données dans un objet de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], listing data formats
- DataFormats class [WPF]
- data formats [WPF], listing
ms.assetid: 18e7ba4b-ccef-4815-ae2d-3a32891010c0
ms.openlocfilehash: f8230eac33a18a0d99cc757d54c2b901c1afe977
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59077743"
---
# <a name="how-to-list-the-data-formats-in-a-data-object"></a><span data-ttu-id="58ca1-102">Procédure : Lister les formats de données dans un objet de données</span><span class="sxs-lookup"><span data-stu-id="58ca1-102">How to: List the Data Formats in a Data Object</span></span>
<span data-ttu-id="58ca1-103">Les exemples suivants montrent comment utiliser le <xref:System.Windows.DataObject.GetFormats%2A> surcharges de méthode obtient un tableau de chaînes qui dénote chaque format de données qui est disponible dans un objet de données.</span><span class="sxs-lookup"><span data-stu-id="58ca1-103">The following examples show how to use the <xref:System.Windows.DataObject.GetFormats%2A> method overloads get an array of strings denoting each data format that is available in a data object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="58ca1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="58ca1-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="58ca1-105">Description</span><span class="sxs-lookup"><span data-stu-id="58ca1-105">Description</span></span>  
 <span data-ttu-id="58ca1-106">L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetFormats%2A> surcharge pour obtenir un tableau de chaînes qui désigne tous les formats de données disponibles dans un objet de données (natif et convertibles automatiquement).</span><span class="sxs-lookup"><span data-stu-id="58ca1-106">The following example code uses the <xref:System.Windows.DataObject.GetFormats%2A> overload to get an array of strings denoting all data formats available in a data object (both native and auto-convertible).</span></span>  
  
### <a name="code"></a><span data-ttu-id="58ca1-107">Code</span><span class="sxs-lookup"><span data-stu-id="58ca1-107">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats)]  
  
## <a name="example"></a><span data-ttu-id="58ca1-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="58ca1-108">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="58ca1-109">Description</span><span class="sxs-lookup"><span data-stu-id="58ca1-109">Description</span></span>  
 <span data-ttu-id="58ca1-110">L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetFormats%2A> surcharge pour obtenir un tableau de chaînes indiquant uniquement les formats de données disponibles dans un objet de données (données convertibles automatiquement les formats sont filtrés).</span><span class="sxs-lookup"><span data-stu-id="58ca1-110">The following example code uses the <xref:System.Windows.DataObject.GetFormats%2A> overload to get an array of strings denoting only data formats available in a data object (auto-convertible data formats are filtered).</span></span>  
  
### <a name="code"></a><span data-ttu-id="58ca1-111">Code</span><span class="sxs-lookup"><span data-stu-id="58ca1-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats_nativeonly)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats_nativeonly)]  
  
## <a name="see-also"></a><span data-ttu-id="58ca1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ca1-112">See also</span></span>

- <xref:System.Windows.IDataObject>
- [<span data-ttu-id="58ca1-113">Vue d'ensemble du glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="58ca1-113">Drag and Drop Overview</span></span>](drag-and-drop-overview.md)
