---
title: 'Procédure : Effectuer un test de positionnement dans un Viewport3D'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 3-D visuals [WPF], hit-testing for
- hit tests [WPF], for 3-D visuals
- Viewport3D [WPF]
ms.assetid: 42bfbd99-c7c6-43f1-940b-90448faa412e
ms.openlocfilehash: 0906fc0da363f9b4022eea863ec1140c8eeb2da2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54494238"
---
# <a name="how-to-hit-test-in-a-viewport3d"></a>Procédure : Effectuer un test de positionnement dans un Viewport3D
Cet exemple montre comment le test de positionnement pour les objets visuels 3D dans un <xref:System.Windows.Controls.Viewport3D>.  
  
 Étant donné que <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> retourne des informations 2D et 3D, il est possible d’effectuer une itération dans les résultats des tests pour lire les résultats uniquement 3D.  
  
 [!code-csharp[HitTest3D#HitTest3D3DN4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HitTest3D/CSharp/Window1.xaml.cs#hittest3d3dn4)]
 [!code-vb[HitTest3D#HitTest3D3DN4](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HitTest3D/visualbasic/window1.xaml.vb#hittest3d3dn4)]  
  
 Le <xref:System.Windows.Media.HitTestResultBehavior> dans le code suivant détermine comment les résultats de test de positionnement sont traités.  `UpdateResultInfo` et `UpdateMaterial` sont des méthodes définies localement.  
  
 [!code-csharp[HitTest3D#HitTest3D3DN5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HitTest3D/CSharp/Window1.xaml.cs#hittest3d3dn5)]
 [!code-vb[HitTest3D#HitTest3D3DN5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HitTest3D/visualbasic/window1.xaml.vb#hittest3d3dn5)]  
  
## <a name="see-also"></a>Voir aussi
- [Exemple de test de positionnement 3D](https://go.microsoft.com/fwlink/?LinkID=159959)
