---
title: 'Procédure : Utiliser la propriété BetweenShowDelay'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolTip control [WPF], BetweenShowDelay time property
- BetweenShowDelay time property [WPF]
ms.assetid: 984ea76d-f2a2-4326-a02e-f97ec3d036d6
ms.openlocfilehash: b6d55c72c8264546949833fc086937a8b1fe2540
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61696052"
---
# <a name="how-to-use-the-betweenshowdelay-property"></a>Procédure : Utiliser la propriété BetweenShowDelay
Cet exemple montre comment utiliser le <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> moment propriété afin que les info-bulles s’affichent rapidement, avec peu ou pas de délai, lorsqu’un utilisateur déplace le pointeur de la souris à partir d’une info-bulle directement vers un autre.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, le <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> propriété est définie sur une seconde (1000 millisecondes) et le <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> est défini à deux secondes (2 000 millisecondes) pour les info-bulles des deux <xref:System.Windows.Shapes.Ellipse> contrôles. Si vous afficher l’info-bulle pour l’une des ellipses et puis déplacez le pointeur de la souris à un autre ellipse dans les deux secondes et pause dessus, l’info-bulle de la deuxième ellipse s’affiche immédiatement.  
  
 Dans un des scénarios suivants, le <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> s’applique, ce qui entraîne l’info-bulle pour la seconde à attendre une seconde avant d’apparaître :  
  
- Si le temps nécessaire pour déplacer vers le deuxième bouton est plus de deux secondes.  
  
- Si l’info-bulle n’est pas visible au début de l’intervalle de temps pour la première ellipse.  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
[!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [Rubriques de guide pratique](tooltip-how-to-topics.md)
- [Vue d’ensemble de l’info-bulle](tooltip-overview.md)
