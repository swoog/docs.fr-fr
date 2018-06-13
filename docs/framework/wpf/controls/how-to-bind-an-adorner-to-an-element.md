---
title: 'Comment : lier un ornement à un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UIElements [WPF], binding adorners to
- adorners [WPF], binding to specified UIElements
ms.assetid: b2101611-a0ee-4137-bdb8-9b3673d2e6b9
ms.openlocfilehash: fb419ee5a57e81e7e3bc72ae04fd200703b80cd3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552550"
---
# <a name="how-to-bind-an-adorner-to-an-element"></a>Comment : lier un ornement à un élément
Cet exemple montre comment lier par programmation un ornement spécifié <xref:System.Windows.UIElement>.  
  
## <a name="example"></a>Exemple  
 Pour lier un ornement à un emplacement donné <xref:System.Windows.UIElement>, procédez comme suit :  
  
1.  Appeler le `static` méthode <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> pour obtenir un <xref:System.Windows.Documents.AdornerLayer> de l’objet pour le <xref:System.Windows.UIElement> à orner. <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> parcourt l’arborescence d’éléments visuels, en commençant à la position spécifiée **UIElement**et retourne la première couche d’ornement qu’il trouve. (Si aucune couche d’ornement n’est trouvée, la méthode retourne Null.)  
  
2.  Appelez le <xref:System.Windows.Documents.AdornerLayer.Add%2A> méthode à laquelle lier l’ornement à la cible **UIElement**.  
  
 L’exemple suivant lie un SimpleCircleAdorner (illustré ci-dessus) pour un <xref:System.Windows.Controls.TextBox> nommé *myTextBox*.  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornSingleElement](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornsingleelement)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornSingleElement](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornsingleelement)]  
  
> [!NOTE]
>  L’utilisation du [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour lier un ornement à un autre élément n’est pas prise en charge pour l’instant.  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble des ornements](../../../../docs/framework/wpf/controls/adorners-overview.md)
