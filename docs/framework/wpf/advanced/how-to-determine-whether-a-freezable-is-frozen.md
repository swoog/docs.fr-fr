---
title: 'Comment : déterminer si un Freezable est gelé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], determining if frozen
ms.assetid: 92e58baa-ee12-4a9e-ac3a-ca458807a8b2
ms.openlocfilehash: f6d20025d59a702357b12da9f5dc0f5887968143
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33542751"
---
# <a name="how-to-determine-whether-a-freezable-is-frozen"></a>Comment : déterminer si un Freezable est gelé
Cet exemple montre comment déterminer si un <xref:System.Windows.Freezable> objet est figé. Si vous essayez de modifier un objet figé <xref:System.Windows.Freezable> de l’objet, elle lève une <xref:System.InvalidOperationException>. Pour éviter de lever cette exception, utilisez la <xref:System.Windows.Freezable.IsFrozen%2A> propriété de la <xref:System.Windows.Freezable> objet afin de déterminer si elle est figée.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant gèle un <xref:System.Windows.Media.SolidColorBrush> , puis le teste à l’aide de la <xref:System.Windows.Freezable.IsFrozen%2A> propriété pour déterminer si elle est figée.  
  
 [!code-csharp[freezablesample_procedural#CheckIsFrozenExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#checkisfrozenexample)]
 [!code-vb[freezablesample_procedural#CheckIsFrozenExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#checkisfrozenexample)]  
  
 Pour plus d’informations sur <xref:System.Windows.Freezable> , consultez la [vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Freezable>  
 <xref:System.Windows.Freezable.IsFrozen%2A>  
 [Vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
