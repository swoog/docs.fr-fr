---
title: "Procédure : Obtenir une copie en écriture d'un Freezable en lecture seule"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cloning Freezable objects [WPF]
- Freezable objects [WPF], modifiable clones
ms.assetid: d028de61-bbe9-4d62-b656-8fe3b1b2ca24
ms.openlocfilehash: 2853b1e02e1223cbb2b6dff4acbddb0a41d882cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629954"
---
# <a name="how-to-obtain-a-writable-copy-of-a-read-only-freezable"></a>Procédure : Obtenir une copie en écriture d'un Freezable en lecture seule
Cet exemple montre comment utiliser le <xref:System.Windows.Freezable.Clone%2A> méthode pour créer une copie accessible en écriture en lecture seule <xref:System.Windows.Freezable>.  
  
 Après un <xref:System.Windows.Freezable> objet est marqué comme en lecture seule (« figé »), vous ne pouvez pas le modifier. Toutefois, vous pouvez utiliser la <xref:System.Windows.Freezable.Clone%2A> méthode pour créer un clone modifiable de l’objet figé.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un clone modifiable de figé <xref:System.Windows.Media.SolidColorBrush> objet.  
  
 [!code-csharp[freezablesample_procedural#CloneExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#cloneexample)]
 [!code-vb[freezablesample_procedural#CloneExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#cloneexample)]  
  
 Pour plus d’informations sur <xref:System.Windows.Freezable> , voir la [vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CloneCurrentValue%2A>
- [Vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)
- [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
