---
title: "Procédure : Faire pivoter l'entrée manuscrite"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ink [WPF], rotating
- rotating ink [WPF]
ms.assetid: fac36cc9-dd01-41ca-9bde-9d33e3790bbe
ms.openlocfilehash: 31f5d0ffb6f0fdcdaef13bc44653f8c7938ac7f3
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378794"
---
# <a name="how-to-rotate-ink"></a><span data-ttu-id="eb758-102">Procédure : Faire pivoter l'entrée manuscrite</span><span class="sxs-lookup"><span data-stu-id="eb758-102">How to: Rotate Ink</span></span>
## <a name="example"></a><span data-ttu-id="eb758-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb758-103">Example</span></span>  
 <span data-ttu-id="eb758-104">L’exemple suivant copie l’encre à partir d’un <xref:System.Windows.Controls.InkCanvas> à un <xref:System.Windows.Controls.Canvas> qui contient un <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="eb758-104">The following example copies the ink from an <xref:System.Windows.Controls.InkCanvas> to a <xref:System.Windows.Controls.Canvas> that contains an <xref:System.Windows.Controls.InkPresenter>.</span></span>  <span data-ttu-id="eb758-105">Lorsque l’application copie l’encre, il fait également pivoter l’encre 90 degrés dans le sens horaire.</span><span class="sxs-lookup"><span data-stu-id="eb758-105">When the application copies the ink, it also rotates the ink 90 degrees clockwise.</span></span>  
  
 [!code-xaml[HowToRotateInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToRotateInk/CSharp/Window1.xaml#1)]  
  
 [!code-csharp[HowToRotateInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToRotateInk/CSharp/Window1.xaml.cs#2)]  
  
## <a name="example"></a><span data-ttu-id="eb758-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb758-106">Example</span></span>  
 <span data-ttu-id="eb758-107">L’exemple suivant est un personnalisé <xref:System.Windows.Documents.Adorner> qui fait pivoter les traits sur un <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="eb758-107">The following example is a custom <xref:System.Windows.Documents.Adorner> that rotates the strokes on an <xref:System.Windows.Controls.InkPresenter>.</span></span>  
  
 [!code-csharp[AdornerForStrokes#1](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornerForStrokes/CSharp/RotatingAdornerForStrokes.cs#1)]
 [!code-vb[AdornerForStrokes#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornerForStrokes/VisualBasic/RotatingAdornerForStrokes.vb#1)]  
  
 <span data-ttu-id="eb758-108">L’exemple suivant est un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier qui définit un <xref:System.Windows.Controls.InkPresenter> et la remplit avec l’encre.</span><span class="sxs-lookup"><span data-stu-id="eb758-108">The following example is a [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file that defines an <xref:System.Windows.Controls.InkPresenter> and populates it with ink.</span></span> <span data-ttu-id="eb758-109">Le `Window_Loaded` Gestionnaire d’événements ajoute l’ornement personnalisé à la <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="eb758-109">The `Window_Loaded` event handler adds the custom adorner to the <xref:System.Windows.Controls.InkPresenter>.</span></span>  
  
 [!code-xaml[AdornerForStrokes#2](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornerForStrokes/CSharp/Window1.xaml#2)]  
  
 [!code-csharp[AdornerForStrokes#3](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornerForStrokes/CSharp/Window1.xaml.cs#3)]
 [!code-vb[AdornerForStrokes#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornerForStrokes/VisualBasic/Window1.xaml.vb#3)]
