---
title: "Procédure : Sélectionner une encre à partir d'un contrôle personnalisé"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], ink selection
- ink [WPF], selecting from custom control
- custom controls [WPF], ink selection
ms.assetid: 5f3a45c6-6d40-4017-9b47-933f134ceba3
ms.openlocfilehash: 8517041fd9a1864abfb32851314a2926ddab5a3e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57363773"
---
# <a name="how-to-select-ink-from-a-custom-control"></a>Procédure : Sélectionner une encre à partir d'un contrôle personnalisé
En ajoutant un <xref:System.Windows.Ink.IncrementalLassoHitTester> à votre contrôle personnalisé, vous pouvez activer votre contrôle afin qu’un utilisateur peut sélectionner l’encre avec un outil lasso, semblable à la façon dont le <xref:System.Windows.Controls.InkCanvas> sélectionne l’encre avec un lasso.  
  
 Cet exemple suppose que vous êtes familiarisé avec la création d’un contrôle personnalisé prenant en charge de l’encre.  Pour créer un contrôle personnalisé qui accepte l’entrée d’encre, consultez [création d’un contrôle d’entrée d’encre](creating-an-ink-input-control.md).  
  
## <a name="example"></a>Exemple  
 Lorsque l’utilisateur dessine un lasso, le <xref:System.Windows.Ink.IncrementalLassoHitTester> prédit les traits seront dans les limites du tracé du lasso une fois que l’utilisateur a terminé le lasso.  Les traits qui sont considérées comme dans les limites du tracé du lasso peuvent être considérés comme étant sélectionnée.  Traits sélectionnés peuvent également être désélectionnés.  Par exemple, si l’utilisateur inverse le sens lors du tracé du lasso, le <xref:System.Windows.Ink.IncrementalLassoHitTester> peut désélectionner certains traits.  
  
 Le <xref:System.Windows.Ink.IncrementalLassoHitTester> déclenche le <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> événement, ce qui permet à votre contrôle personnalisé de répondre pendant que l’utilisateur dessine le lasso.  Par exemple, vous pouvez modifier l’apparence des traits quand l’utilisateur sélectionne et désélectionne les.  
  
## <a name="managing-the-ink-mode"></a>Gestion du Mode de l’encre  
 Il est utile à l’utilisateur si le lasso apparaît différemment de l’encre sur votre contrôle. Pour ce faire, votre contrôle personnalisé doit suivre des si l’utilisateur est écrit ou en sélectionnant l’encre. Le moyen le plus simple pour ce faire consiste à déclarer une énumération avec deux valeurs : une pour indiquer que l’utilisateur écrit l’encre et l’autre pour indiquer que l’utilisateur sélectionne l’encre.  
  
 [!code-csharp[HowToSelectInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#2)]
 [!code-vb[HowToSelectInk#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#2)]  
  
 Ensuite, ajoutez deux <xref:System.Windows.Ink.DrawingAttributes> à la classe : l’application à utiliser lorsque l’utilisateur écrit l’encre, l’application à utiliser lorsque l’utilisateur sélectionne l’encre.  Dans le constructeur, initialisez le <xref:System.Windows.Ink.DrawingAttributes> et attachez les deux <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> événements au même gestionnaire d’événements. Définissez ensuite la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> propriété de la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> à l’encre <xref:System.Windows.Ink.DrawingAttributes>.  
  
 [!code-csharp[HowToSelectInk#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#3)]
 [!code-vb[HowToSelectInk#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#3)]  
[!code-csharp[HowToSelectInk#4](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#4)]
[!code-vb[HowToSelectInk#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#4)]  
  
 Ajouter une propriété qui expose le mode de sélection. Lorsque l’utilisateur modifie le mode de sélection, définissez la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> propriété de la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> appropriés <xref:System.Windows.Ink.DrawingAttributes> de l’objet, puis reconnectez le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> propriété le <xref:System.Windows.Controls.InkPresenter>.  
  
 [!code-csharp[HowToSelectInk#5](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#5)]
 [!code-vb[HowToSelectInk#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#5)]  
  
 Exposer le <xref:System.Windows.Ink.DrawingAttributes> comme propriétés pour que les applications peuvent déterminer l’apparence des traits d’encre et des traits de sélection.  
  
 [!code-csharp[HowToSelectInk#6](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#6)]
 [!code-vb[HowToSelectInk#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#6)]  
  
 Lorsqu’une propriété d’un <xref:System.Windows.Ink.DrawingAttributes> l’objet de modifications, la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> doivent être rattachés à la <xref:System.Windows.Controls.InkPresenter>.  Dans le Gestionnaire d’événements pour le <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> événement, rattachez la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> à la <xref:System.Windows.Controls.InkPresenter>.  
  
 [!code-csharp[HowToSelectInk#7](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#7)]
 [!code-vb[HowToSelectInk#7](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#7)]  
  
## <a name="using-the-incrementallassohittester"></a>Utilisation d’IncrementalLassoHitTester  
 Créer et initialiser un <xref:System.Windows.Ink.StrokeCollection> qui contient les traits sélectionnés.  
  
 [!code-csharp[HowToSelectInk#8](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#8)]
 [!code-vb[HowToSelectInk#8](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#8)]  
  
 Lorsque l’utilisateur commence à dessiner un trait, l’encre ou lasso, désélectionnez tous les traits sélectionnés. Ensuite, si l’utilisateur le dessine un lasso, créez un <xref:System.Windows.Ink.IncrementalLassoHitTester> en appelant <xref:System.Windows.Ink.StrokeCollection.GetIncrementalLassoHitTester%2A>, s’abonner à la <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> événements et les appels <xref:System.Windows.Ink.IncrementalHitTester.AddPoints%2A>. Ce code peut être une méthode distincte et appelé à partir de la <xref:System.Windows.UIElement.OnStylusDown%2A> et <xref:System.Windows.UIElement.OnMouseDown%2A> méthodes.  
  
 [!code-csharp[HowToSelectInk#9](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#9)]
 [!code-vb[HowToSelectInk#9](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#9)]  
  
 Ajouter les points du stylet à le <xref:System.Windows.Ink.IncrementalLassoHitTester> pendant que l’utilisateur dessine le lasso.  Appelez la méthode suivante à partir de la <xref:System.Windows.UIElement.OnStylusMove%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, <xref:System.Windows.UIElement.OnMouseMove%2A>, et <xref:System.Windows.UIElement.OnMouseLeftButtonUp%2A> méthodes.  
  
 [!code-csharp[HowToSelectInk#10](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#10)]
 [!code-vb[HowToSelectInk#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#10)]  
  
 Gérer le <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged?displayProperty=nameWithType> événement répondre quand l’utilisateur sélectionne et désélectionne des traits.  Le <xref:System.Windows.Ink.LassoSelectionChangedEventArgs> classe a le <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.SelectedStrokes%2A> et <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.DeselectedStrokes%2A> propriétés qui obtiennent les traits qui ont été sélectionnées et, respectivement.  
  
 [!code-csharp[HowToSelectInk#11](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#11)]
 [!code-vb[HowToSelectInk#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#11)]  
  
 L’utilisateur a terminé de dessiner le lasso, annuler votre abonnement à la <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> événements et les appels <xref:System.Windows.Ink.IncrementalHitTester.EndHitTesting%2A>.  
  
 [!code-csharp[HowToSelectInk#12](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#12)]
 [!code-vb[HowToSelectInk#12](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#12)]  
  
## <a name="putting-it-all-together"></a>Placer tous les éléments.  
 L’exemple suivant est un contrôle personnalisé qui permet à un utilisateur de sélectionner une encre avec un lasso.  
  
 [!code-csharp[HowToSelectInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#1)]
 [!code-vb[HowToSelectInk#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Ink.IncrementalLassoHitTester>
- <xref:System.Windows.Ink.StrokeCollection>
- <xref:System.Windows.Input.StylusPointCollection>
- [Création d'un contrôle d'entrée d'encre](creating-an-ink-input-control.md)
