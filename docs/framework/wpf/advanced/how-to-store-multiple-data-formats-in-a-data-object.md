---
title: 'Procédure : Stocker plusieurs formats de données dans un objet de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataObject class [WPF], storing multiple formats
- DataFormats class [WPF], storing multiple formats
- drag-and-drop [WPF], storing multiple formats
ms.assetid: 941ace29-29c4-4c26-b75b-ea7d06aa0d69
ms.openlocfilehash: 33415dd3cb1a05263cf9fb9ecafcbc857d364d57
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555672"
---
# <a name="how-to-store-multiple-data-formats-in-a-data-object"></a>Procédure : Stocker plusieurs formats de données dans un objet de données
L’exemple suivant montre comment utiliser le <xref:System.Windows.DataObject.SetData%28System.String%2CSystem.Object%29> méthode pour ajouter des données à un objet de données dans plusieurs formats.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_StoreMultipleFormats](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_storemultipleformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_StoreMultipleFormats](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_storemultipleformats)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.IDataObject>
- [Vue d'ensemble du glisser-déplacer](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)
