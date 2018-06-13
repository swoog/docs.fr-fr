---
title: "Comment : créer un effet de substitution à l'aide d'événements"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors of elements [WPF], changing
- rollover effect [WPF]
- element colors [WPF], changing
ms.assetid: 3b20d028-6f1c-4b25-95d2-fa68cefbdb4c
ms.openlocfilehash: d458d87586614093b35fcd73969dea04fe620351
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543008"
---
# <a name="how-to-create-a-rollover-effect-using-events"></a>Comment : créer un effet de substitution à l'aide d'événements
Cet exemple montre comment modifier la couleur d’un élément que le pointeur de la souris entre et sort de la zone occupée par l’élément.  
  
 Cet exemple se compose d’un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier et un fichier code-behind.  
  
> [!NOTE]
>  Cet exemple montre comment utiliser des événements, mais la méthode recommandée pour parvenir à ce même effet consiste à utiliser un <xref:System.Windows.Trigger> dans un style. Pour plus d’informations, consultez [Application d’un style et création de modèles](../../../../docs/framework/wpf/controls/styling-and-templating.md).  
  
## <a name="example"></a>Exemple  
 Les éléments suivants [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crée l’interface utilisateur, qui se compose de <xref:System.Windows.Controls.Border> autour un <xref:System.Windows.Controls.TextBlock>et l’attache le <xref:System.Windows.Input.Mouse.MouseEnter> et <xref:System.Windows.UIElement.MouseLeave> gestionnaires d’événements pour le <xref:System.Windows.Controls.Border>.  
  
 [!code-xaml[mouseenterMouseleave#MouseEnterLeaveSampleXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/mouseenterMouseleave/CSharp/Window1.xaml#mouseenterleavesamplexaml)]  
  
 Le code-behind suivant crée le <xref:System.Windows.UIElement.MouseEnter> et <xref:System.Windows.UIElement.MouseLeave> gestionnaires d’événements.  Lorsque le pointeur de la souris entre dans le <xref:System.Windows.Controls.Border>, l’arrière-plan de la <xref:System.Windows.Controls.Border> est modifié en rouge.  Lorsque le pointeur de la souris quitte le <xref:System.Windows.Controls.Border>, l’arrière-plan de la <xref:System.Windows.Controls.Border> repasse au blanc.  
  
 [!code-csharp[mouseenterMouseleave#MouseEnterLeaveSampleEventHandlers](../../../../samples/snippets/csharp/VS_Snippets_Wpf/mouseenterMouseleave/CSharp/Window1.xaml.cs#mouseenterleavesampleeventhandlers)]
 [!code-vb[mouseenterMouseleave#MouseEnterLeaveSampleEventHandlers](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/mouseenterMouseleave/VisualBasic/Window1.xaml.vb#mouseenterleavesampleeventhandlers)]
