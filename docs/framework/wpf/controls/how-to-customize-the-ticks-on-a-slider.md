---
title: 'Procédure : Personnaliser les graduations sur un curseur'
ms.date: 03/30/2017
helpviewer_keywords:
- TickBar [WPF]
- Slider control [WPF], creating with TickBar
ms.assetid: 4fa694f2-a620-4b15-be78-5f4286f89361
ms.openlocfilehash: 3b32bbedb5f654ce75e90a827eb0c4dba1d4d345
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910687"
---
# <a name="how-to-customize-the-ticks-on-a-slider"></a>Procédure : Personnaliser les graduations sur un curseur
Cet exemple montre comment créer un <xref:System.Windows.Controls.Slider> contrôle qui a des graduations.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Controls.Primitives.TickBar> s’affiche lorsque vous définissez la <xref:System.Windows.Controls.Slider.TickPlacement%2A> propriété une valeur autre que <xref:System.Windows.Controls.Primitives.TickPlacement.None>, qui est la valeur par défaut.  
  
 L’exemple suivant montre comment créer un <xref:System.Windows.Controls.Slider> avec un <xref:System.Windows.Controls.Primitives.TickBar> qu’affiche les graduations. Le <xref:System.Windows.Controls.Slider.TickPlacement%2A> et <xref:System.Windows.Controls.Slider.TickFrequency%2A> propriétés définissent l’emplacement des graduations et l’intervalle entre eux. Lorsque vous déplacez le <xref:System.Windows.Controls.Primitives.Thumb>, info-bulles affichent la valeur de la <xref:System.Windows.Controls.Slider>. Le <xref:System.Windows.Controls.Slider.AutoToolTipPlacement%2A> propriété définit où les info-bulles s’affichent. Le <xref:System.Windows.Controls.Primitives.Thumb> mouvements correspondent à l’emplacement des graduations car <xref:System.Windows.Controls.Slider.IsSnapToTickEnabled%2A> est défini sur `true`.  
  
 L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.Slider.Ticks%2A> propriété pour créer des graduations le long de la <xref:System.Windows.Controls.Slider> à intervalles irréguliers.  
  
 [!code-xaml[Slider#4](~/samples/snippets/xaml/VS_Snippets_Wpf/Slider/xaml/window1.xaml#4)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Slider>
- <xref:System.Windows.Controls.Primitives.TickBar>
- <xref:System.Windows.Controls.Slider.TickPlacement%2A>
- [Guide pratique pour Lier un Slider à une valeur de propriété](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms788716(v=vs.90))
