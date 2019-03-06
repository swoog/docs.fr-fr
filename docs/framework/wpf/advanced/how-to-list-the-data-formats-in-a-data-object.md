---
title: 'Procédure : Répertorier les formats de données dans un objet de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], listing data formats
- DataFormats class [WPF]
- data formats [WPF], listing
ms.assetid: 18e7ba4b-ccef-4815-ae2d-3a32891010c0
ms.openlocfilehash: c8e9f24a0e991fa44ddd3f4d778cc7ba640ae9c3
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370174"
---
# <a name="how-to-list-the-data-formats-in-a-data-object"></a><span data-ttu-id="a501b-102">Procédure : Répertorier les formats de données dans un objet de données</span><span class="sxs-lookup"><span data-stu-id="a501b-102">How to: List the Data Formats in a Data Object</span></span>
<span data-ttu-id="a501b-103">Les exemples suivants montrent comment utiliser le <xref:System.Windows.DataObject.GetFormats%2A> surcharges de méthode obtient un tableau de chaînes qui dénote chaque format de données qui est disponible dans un objet de données.</span><span class="sxs-lookup"><span data-stu-id="a501b-103">The following examples show how to use the <xref:System.Windows.DataObject.GetFormats%2A> method overloads get an array of strings denoting each data format that is available in a data object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a501b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a501b-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="a501b-105">Description</span><span class="sxs-lookup"><span data-stu-id="a501b-105">Description</span></span>  
 <span data-ttu-id="a501b-106">L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetFormats%2A> surcharge pour obtenir un tableau de chaînes qui désigne tous les formats de données disponibles dans un objet de données (natif et convertibles automatiquement).</span><span class="sxs-lookup"><span data-stu-id="a501b-106">The following example code uses the <xref:System.Windows.DataObject.GetFormats%2A> overload to get an array of strings denoting all data formats available in a data object (both native and auto-convertible).</span></span>  
  
### <a name="code"></a><span data-ttu-id="a501b-107">Code</span><span class="sxs-lookup"><span data-stu-id="a501b-107">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats)]  
  
## <a name="example"></a><span data-ttu-id="a501b-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="a501b-108">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="a501b-109">Description</span><span class="sxs-lookup"><span data-stu-id="a501b-109">Description</span></span>  
 <span data-ttu-id="a501b-110">L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetFormats%2A> surcharge pour obtenir un tableau de chaînes indiquant uniquement les formats de données disponibles dans un objet de données (données convertibles automatiquement les formats sont filtrés).</span><span class="sxs-lookup"><span data-stu-id="a501b-110">The following example code uses the <xref:System.Windows.DataObject.GetFormats%2A> overload to get an array of strings denoting only data formats available in a data object (auto-convertible data formats are filtered).</span></span>  
  
### <a name="code"></a><span data-ttu-id="a501b-111">Code</span><span class="sxs-lookup"><span data-stu-id="a501b-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats_nativeonly)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats_nativeonly)]  
  
## <a name="see-also"></a><span data-ttu-id="a501b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a501b-112">See also</span></span>
- <xref:System.Windows.IDataObject>
- [<span data-ttu-id="a501b-113">Vue d'ensemble du glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="a501b-113">Drag and Drop Overview</span></span>](drag-and-drop-overview.md)
