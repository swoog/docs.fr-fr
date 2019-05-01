---
title: 'Procédure : Test de positionnement à l’aide d’un conteneur hôte Win32'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], using Win32 host containers
- visual objects [WPF], hit tests on
- Win32 host containers [WPF], hit tests using
ms.assetid: 9491f7f3-d8ba-4573-a888-2f064d1349dc
ms.openlocfilehash: ac5cae5bcd94dc8bf80ff95b8971914e1fa5ba2c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62025104"
---
# <a name="how-to-hit-test-using-a-win32-host-container"></a>Procédure : Test de positionnement à l’aide d’un conteneur hôte Win32
Vous pouvez créer des objets visuels dans un [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] fenêtre en fournissant un hôte de conteneur de fenêtre pour les objets visuels. Pour assurer la gestion des événements des objets visuels du conteneur, vous devez traiter les messages transmis à la boucle de filtre de messages du conteneur de fenêtre hôte. Reportez-vous à [didacticiel : Hébergement d’objets visuels dans une Application Win32](tutorial-hosting-visual-objects-in-a-win32-application.md) pour plus d’informations sur l’hébergement d’objets visuels dans un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre.  
  
## <a name="example"></a>Exemple  
 Le code suivant montre comment définir des gestionnaires d’événements de souris pour un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre qui est utilisé comme un conteneur hôte pour des objets visuels.  
  
 [!code-csharp[VisualsHitTesting#103](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyWindow.cs#103)]
 [!code-vb[VisualsHitTesting#103](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyWindow.vb#103)]  
  
 L’exemple suivant montre comment configurer un test de positionnement en réponse à l’interception d’événements de souris spécifiques.  
  
 [!code-csharp[VisualsHitTesting#104](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyCircle.cs#104)]
 [!code-vb[VisualsHitTesting#104](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyCircle.vb#104)]  
  
 Le <xref:System.Windows.Interop.HwndSource> objet présente [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] contenu dans un [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] fenêtre. La valeur de la <xref:System.Windows.Interop.HwndSource.RootVisual%2A> propriété de la <xref:System.Windows.Interop.HwndSource> objet représente le nœud supérieur dans la hiérarchie d’arborescence d’éléments visuels.  
  
 Pour l’exemple complet sur le test de positionnement des objets à l’aide d’un conteneur hôte Win32, consultez [Test de positionnement avec interopérabilité Win32, exemple](https://go.microsoft.com/fwlink/?LinkID=159995).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Interop.HwndSource>
- [Test de positionnement dans la couche visuelle](hit-testing-in-the-visual-layer.md)
- [Tutoriel : Hébergement d’objets visuels dans une Application Win32](tutorial-hosting-visual-objects-in-a-win32-application.md)
