---
title: "Procédure : Faire en sorte qu'un objet suive le pointeur de la souris"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- following the mouse pointer (cursor)
- mouse pointer (cursor), making objects follow
- cursor (mouse pointer), making objects follow
ms.assetid: 50b20415-14bc-405c-baf3-2fb254fffde3
ms.openlocfilehash: 3e39b9459fbc94c9b7684ffd7c597363e46ad717
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541818"
---
# <a name="how-to-make-an-object-follow-the-mouse-pointer"></a>Procédure : Faire en sorte qu'un objet suive le pointeur de la souris
Cet exemple montre comment modifier les dimensions d’un objet lorsque le pointeur de la souris se déplace sur l’écran.  
  
 L’exemple inclut un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier qui crée le [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] et un fichier code-behind qui crée le Gestionnaire d’événements.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crée le [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)], qui se compose d’un <xref:System.Windows.Shapes.Ellipse> à l’intérieur d’un <xref:System.Windows.Controls.StackPanel>et attache le Gestionnaire d’événements pour le <xref:System.Windows.UIElement.MouseMove> événement.  
  
 [!code-xaml[mouseMoveWithPointer#MouseMoveWithPointerXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml#mousemovewithpointerxaml)]  
  
 Le code-behind suivant crée le <xref:System.Windows.UIElement.MouseMove> Gestionnaire d’événements.  Lorsque le pointeur de la souris se déplace, la hauteur et la largeur de la <xref:System.Windows.Shapes.Ellipse> augmentent et diminuent.  
  
 [!code-csharp[mouseMoveWithPointer#MouseMovePointerGetPosition](../../../../samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml.cs#mousemovepointergetposition)]
 [!code-vb[mouseMoveWithPointer#MouseMovePointerGetPosition](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/mouseMoveWithPointer/VisualBasic/Window1.xaml.vb#mousemovepointergetposition)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des entrées](../../../../docs/framework/wpf/advanced/input-overview.md)
