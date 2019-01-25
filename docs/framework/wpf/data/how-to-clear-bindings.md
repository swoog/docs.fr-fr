---
title: 'Procédure : Supprimer des liaisons'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
ms.openlocfilehash: bd0f42b868c316cb9a6344134d4aaf01930519ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508429"
---
# <a name="how-to-clear-bindings"></a>Procédure : Supprimer des liaisons
Cet exemple montre comment supprimer des liaisons d’un objet.  
  
## <a name="example"></a>Exemple  
 Pour supprimer une liaison à partir d’une propriété individuelle sur un objet, appelez <xref:System.Windows.Data.BindingOperations.ClearBinding%2A> comme indiqué dans l’exemple suivant. L’exemple suivant supprime la liaison à partir de la <xref:System.Windows.Controls.TextBlock.TextProperty> de *mytext*, un <xref:System.Windows.Controls.TextBlock> objet.  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 La suppression de liaison a pour effet de supprimer la liaison de sorte que la valeur de la propriété de dépendance est modifiée pour apparaître telle qu’elle aurait été sans la liaison. Cette valeur peut être une valeur par défaut, une valeur héritée ou une valeur dérivée d’une liaison de modèle de données.  
  
 Pour effacer les liaisons à partir de toutes les propriétés possibles sur un objet, utilisez <xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Data.BindingOperations>
- [Vue d’ensemble de la liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [Rubriques de guide pratique](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
