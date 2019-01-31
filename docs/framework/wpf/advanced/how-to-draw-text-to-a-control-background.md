---
title: "Procédure : Dessiner du texte sur l'arrière-plan d'un contrôle"
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], drawing text to backgrounds
- text [WPF], drawing to control backgrounds
- drawing [WPF], text to control backgrounds
- backgrounds [WPF], drawing text to
- typography [WPF], drawing text to control backgrounds
ms.assetid: 686d8fba-f61c-4974-a871-c635d67a7f69
ms.openlocfilehash: 9be4eb92021a62baaf6b43198587616d00cc265e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259252"
---
# <a name="how-to-draw-text-to-a-controls-background"></a>Procédure : Dessiner du texte sur l'arrière-plan d'un contrôle
Vous pouvez dessiner du texte directement sur l’arrière-plan d’un contrôle en convertissant une chaîne de texte à un <xref:System.Windows.Media.FormattedText> de l’objet, puis en dessinant l’objet du contrôle <xref:System.Windows.Media.DrawingContext>. Vous pouvez également utiliser cette technique pour le dessin de l’arrière-plan des objets dérivés de <xref:System.Windows.Controls.Panel>, tel que <xref:System.Windows.Controls.Canvas> et <xref:System.Windows.Controls.StackPanel>.  
  
 ![Contrôles affichant le texte en arrière-plan](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")  
Exemple de contrôles avec des arrière-plans de texte personnalisés  
  
## <a name="example"></a>Exemple  
 Pour dessiner à l’arrière-plan d’un contrôle, créez un nouveau <xref:System.Windows.Media.DrawingBrush> de l’objet et de dessiner le texte converti à l’objet <xref:System.Windows.Media.DrawingContext>. Ensuite, assignez le nouveau <xref:System.Windows.Media.DrawingBrush> à la propriété du contrôle d’arrière-plan.  
  
 L’exemple de code suivant montre comment créer un <xref:System.Windows.Media.FormattedText> de l’objet et dessiner sur l’arrière-plan d’un <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Button> objet.  
  
 [!code-csharp[DrawTextToControlBackground#DrawTextToControlBackground1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawTextToControlBackground/CSHARP/Window1.xaml.cs#drawtexttocontrolbackground1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.FormattedText>
- [Dessin du texte mis en forme](../../../../docs/framework/wpf/advanced/drawing-formatted-text.md)
