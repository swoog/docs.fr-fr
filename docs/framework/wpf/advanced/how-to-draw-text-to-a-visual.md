---
title: 'Procédure : Ajouter du texte à un visuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], drawing text to visuals
- visuals [WPF], drawing text to
- text [WPF], drawing to visuals
- drawing [WPF], text to visuals
ms.assetid: fee4003c-e8a6-46ec-babd-2c7f4231a101
ms.openlocfilehash: 1ea31540ad59ab419e209e4133bcb88640cc01fe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776166"
---
# <a name="how-to-draw-text-to-a-visual"></a>Procédure : Ajouter du texte à un visuel
L’exemple suivant montre comment dessiner du texte à un <xref:System.Windows.Media.DrawingVisual> à l’aide un <xref:System.Windows.Media.DrawingContext> objet. Un contexte de dessin est retourné en appelant le <xref:System.Windows.Media.DrawingVisual.RenderOpen%2A> méthode d’un <xref:System.Windows.Media.DrawingVisual> objet. Vous pouvez dessiner des graphiques et du texte dans un contexte de dessin.  
  
 Pour dessiner du texte dans le contexte de dessin, utilisez la <xref:System.Windows.Media.DrawingContext.DrawText%2A> méthode d’un <xref:System.Windows.Media.DrawingContext> objet. Lorsque vous avez terminé de dessiner le contenu dans le contexte de dessin, appelez le <xref:System.Windows.Media.DrawingContext.Close%2A> méthode pour fermer le contexte de dessin et de conserver le contenu.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[DrawingVisualSample#110](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingVisualSample/CSharp/Window1.xaml.cs#110)]
 [!code-vb[DrawingVisualSample#110](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DrawingVisualSample/visualbasic/window1.xaml.vb#110)]  
  
> [!NOTE]
>  Pour consulter l’intégralité de l’exemple de code duquel l’exemple de code précédent a été extrait, référez-vous à la section [Hit Test Using DrawingVisuals Sample](https://go.microsoft.com/fwlink/?LinkID=159994) (Test de positionnement à l’aide d’exemples de DrawingVisuals).
