---
title: 'Procédure : Déterminer si un format de données est présent dans un objet de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataFormats class [WPF]
- drag-and-drop [WPF], data formats present
- data formats [WPF], determining if present
ms.assetid: e487a454-c9fc-4e53-aeaa-c458d059ad4c
ms.openlocfilehash: 4cec733490e2a9dc5d54b3b253ac38a5090ac885
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207966"
---
# <a name="how-to-determine-if-a-data-format-is-present-in-a-data-object"></a>Procédure : Déterminer si un format de données est présent dans un objet de données
Les exemples suivants montrent comment utiliser les différentes <xref:System.Windows.DataObject.GetDataPresent%2A> surcharges de méthode de requête si un format de données particulier est présent dans un objet de données.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> surcharge pour interroger la présence d’un format de données particulier par chaîne de descripteur.  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_String](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_querydataformats_string)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_String](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_querydataformats_string)]  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetDataPresent%28System.Type%29> surcharge pour interroger la présence d’un format de données particulier par type.  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Type](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_querydataformats_type)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Type](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_querydataformats_type)]  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple de code suivant utilise la <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> surcharger pour rechercher les données en chaîne de descripteur et en spécifiant comment traiter des formats de données convertibles automatiquement.  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Autoconvert](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_querydataformats_autoconvert)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Autoconvert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_querydataformats_autoconvert)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.IDataObject>
