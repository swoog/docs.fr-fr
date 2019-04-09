---
title: 'Procédure : Redimensionner un canevas à l’aide d’un curseur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- resizing Canvas control [WPF]
- controls [WPF], Thumb
- controls [WPF], Canvas
- Thumb control [WPF]
- Canvas control [WPF]
ms.assetid: 7dc9f435-726c-4d4d-be41-eb24cfe17bef
ms.openlocfilehash: 14942157429b029147d47e2f88428c56e66523d1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59146352"
---
# <a name="how-to-resize-a-canvas-by-using-a-thumb"></a>Procédure : Redimensionner un canevas à l’aide d’un curseur
Cet exemple montre comment utiliser un <xref:System.Windows.Controls.Primitives.Thumb> contrôle pour redimensionner un <xref:System.Windows.Controls.Canvas> contrôle.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Controls.Primitives.Thumb> contrôle fournit des fonctionnalités de glissement qui peuvent être utilisée pour déplacer ou redimensionner des contrôles en surveillant le <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>, <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> et <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> événements de la <xref:System.Windows.Controls.Primitives.Thumb>.  
  
 L’utilisateur commence une opération glisser en appuyant sur le bouton gauche de la souris lorsque le pointeur de la souris est en pause sur le <xref:System.Windows.Controls.Primitives.Thumb> contrôle. L’opération glisser se poursuit aussi longtemps que le bouton gauche de la souris est enfoncé. Pendant l’opération glisser, la <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> peut se produire plusieurs fois. Chaque fois qu’il se produit, le <xref:System.Windows.Controls.Primitives.DragDeltaEventArgs> classe fournit la modification de la position qui correspond à la modification de la position de la souris. Lorsque l’utilisateur relâche le bouton gauche de la souris, l’opération glisser est terminée. L’opération glisser fournit uniquement les nouvelles coordonnées ; elle ne repositionne pas automatiquement le <xref:System.Windows.Controls.Primitives.Thumb>.  
  
 L’exemple suivant montre un <xref:System.Windows.Controls.Primitives.Thumb> contrôle qui est l’élément enfant d’un <xref:System.Windows.Controls.Canvas> contrôle. Le Gestionnaire d’événements pour son <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> événement fournit la logique pour déplacer le <xref:System.Windows.Controls.Primitives.Thumb> et redimensionner le <xref:System.Windows.Controls.Canvas>. Les gestionnaires d’événements pour le <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> et <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> événement modifier la couleur de la <xref:System.Windows.Controls.Primitives.Thumb> pendant une opération glisser. L’exemple suivant définit la <xref:System.Windows.Controls.Primitives.Thumb>.  
  
 [!code-xaml[Thumb#thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml#thumb)]  
  
 L’exemple suivant montre le <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> Gestionnaire d’événements qui déplace les <xref:System.Windows.Controls.Primitives.Thumb> et redimensionne le <xref:System.Windows.Controls.Canvas> en réponse à un mouvement de souris.  
  
 [!code-csharp[Thumb#2](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#2)]  
  
 L’exemple suivant montre le <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> Gestionnaire d’événements.  
  
 [!code-csharp[Thumb#DragStartedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragstartedhandler)]
 [!code-vb[Thumb#DragStartedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragstartedhandler)]  
  
 L’exemple suivant montre le <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Gestionnaire d’événements.  
  
 [!code-csharp[Thumb#DragCompletedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragcompletedhandler)]
 [!code-vb[Thumb#DragCompletedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragcompletedhandler)]  
  
 Pour obtenir un exemple complet, consultez [exemple de fonctionnalité de glisser Thumb](https://go.microsoft.com/fwlink/?LinkID=160042).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Primitives.Thumb>
- <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>
- <xref:System.Windows.Controls.Primitives.Thumb.DragDelta>
- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted>
