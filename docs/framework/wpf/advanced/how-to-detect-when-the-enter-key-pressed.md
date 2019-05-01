---
title: 'Procédure : Détecter quand la touche enfoncée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Enter key [WPF], detecting
- keys [WPF], Enter
ms.assetid: a66f39d2-ef4a-43a5-b454-a4ea0fe88655
ms.openlocfilehash: a99da5804bbc31897198b9b6d9e21da9f17dfe26
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051414"
---
# <a name="how-to-detect-when-the-enter-key-pressed"></a>Procédure : Détecter quand la touche enfoncée
Cet exemple montre comment détecter lorsque le <xref:System.Windows.Input.Key.Enter> touche du clavier.  
  
 Cet exemple se compose d’un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier et un fichier code-behind.  
  
## <a name="example"></a>Exemple  
 Lorsque l’utilisateur appuie sur la touche <xref:System.Windows.Input.Key.Enter> dans la <xref:System.Windows.Controls.TextBox>, le texte entré s’affiche dans une autre zone de la [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)].    
  
 Ce qui suit [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crée l’interface utilisateur, qui se compose d’un <xref:System.Windows.Controls.StackPanel>, un <xref:System.Windows.Controls.TextBlock>et un <xref:System.Windows.Controls.TextBox>.  
  
 [!code-xaml[keydown#KeyDownUI](~/samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml#keydownui)]  
  
 Le code-behind suivant crée le <xref:System.Windows.UIElement.KeyDown> Gestionnaire d’événements.  Si la touche enfoncée est la touche <xref:System.Windows.Input.Key.Enter>, un message s’affiche dans le <xref:System.Windows.Controls.TextBlock>.   
  
 [!code-csharp[keydown#KeyDownSample](~/samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml.cs#keydownsample)]
 [!code-vb[keydown#KeyDownSample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/KeyDown/VisualBasic/Window1.xaml.vb#keydownsample)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des entrées](input-overview.md)
- [Vue d’ensemble des événements routés](routed-events-overview.md)
