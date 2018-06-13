---
title: 'Comment : récupérer des données dans un format de données particulier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], retrieving data
- DataFormats class [WPF], retrieving data
- DataObject class [WPF], retrieving data
ms.assetid: a625acf3-1144-44cd-add7-456aefc3859f
ms.openlocfilehash: 405fff1b586207249fbabafb28791ffa2901cf49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33545105"
---
# <a name="how-to-retrieve-data-in-a-particular-data-format"></a><span data-ttu-id="1df56-102">Comment : récupérer des données dans un format de données particulier</span><span class="sxs-lookup"><span data-stu-id="1df56-102">How to: Retrieve Data in a Particular Data Format</span></span>
<span data-ttu-id="1df56-103">Les exemples suivants montrent comment récupérer des données à partir d’un objet de données dans un format spécifié.</span><span class="sxs-lookup"><span data-stu-id="1df56-103">The following examples show how to retrieve data from a data object in a specified format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1df56-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1df56-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="1df56-105">Description</span><span class="sxs-lookup"><span data-stu-id="1df56-105">Description</span></span>  
 <span data-ttu-id="1df56-106">L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> surcharge vérifier d’abord si format de données spécifiée est disponible (en mode natif ou par conversion automatique) ; si le format spécifié est disponible, l’exemple récupère les données à l’aide de la <xref:System.Windows.DataObject.GetData%28System.String%29> (méthode).</span><span class="sxs-lookup"><span data-stu-id="1df56-106">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> overload to first check if a specified data format is available (natively or by auto-convert); if the specified format is available, the example retrieves the data by using the <xref:System.Windows.DataObject.GetData%28System.String%29> method.</span></span>  
  
### <a name="code"></a><span data-ttu-id="1df56-107">Code</span><span class="sxs-lookup"><span data-stu-id="1df56-107">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat)]  
  
## <a name="example"></a><span data-ttu-id="1df56-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="1df56-108">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="1df56-109">Description</span><span class="sxs-lookup"><span data-stu-id="1df56-109">Description</span></span>  
 <span data-ttu-id="1df56-110">L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> surcharge vérifier d’abord si un format de données spécifié est disponible en mode natif (les formats de données convertibles automatiquement sont filtrés) ; si le format spécifié est disponible, l’exemple récupère les données à l’aide de la <xref:System.Windows.DataObject.GetData%28System.String%29>(méthode).</span><span class="sxs-lookup"><span data-stu-id="1df56-110">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> overload to first check if a specified data format is available natively (auto-convertible data formats are filtered); if the specified format is available, the example retrieves the data by using the <xref:System.Windows.DataObject.GetData%28System.String%29> method.</span></span>  
  
### <a name="code"></a><span data-ttu-id="1df56-111">Code</span><span class="sxs-lookup"><span data-stu-id="1df56-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat_native)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat_native)]  
  
## <a name="see-also"></a><span data-ttu-id="1df56-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df56-112">See Also</span></span>  
 <xref:System.Windows.IDataObject>  
 [<span data-ttu-id="1df56-113">Vue d'ensemble du glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="1df56-113">Drag and Drop Overview</span></span>](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)
