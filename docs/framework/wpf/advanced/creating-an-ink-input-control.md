---
title: Création d'un contrôle d'entrée d'encre
ms.date: 03/30/2017
helpviewer_keywords:
- ink strokes [WPF], managing
- managing ink strokes [WPF]
- ink input control [WPF]
- input from mouse [WPF], accepting
- mouse input [WPF], accepting
- ink [WPF], rendering
- ink strokes [WPF], collecting
- rendering ink [WPF]
- collecting ink strokes [WPF]
- DynamicRenderer objects [WPF]
- StylusPlugIn objects [WPF]
ms.assetid: c31f3a67-cb3f-4ded-af9e-ed21f6575b26
ms.openlocfilehash: 105a44f90c1c654a21fc8920a149ad63b2dabc99
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61928708"
---
# <a name="creating-an-ink-input-control"></a>Création d'un contrôle d'entrée d'encre
Vous pouvez créer un contrôle personnalisé qui dynamiquement et restitue l’encre de manière statique. Autrement dit, afficher l’encre lorsqu’un utilisateur trace un trait, à l’origine de l’encre semble « couler » du stylet et d’afficher l’encre après lui est ajouté au contrôle, soit via le stylet, collé à partir du Presse-papiers ou chargé à partir d’un fichier. Pour restituer l’encre de manière dynamique, votre contrôle doit utiliser un <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer>. Pour restituer l’encre de façon statique, vous devez substituer les méthodes d’événement de stylet (<xref:System.Windows.UIElement.OnStylusDown%2A>, <xref:System.Windows.UIElement.OnStylusMove%2A>, et <xref:System.Windows.UIElement.OnStylusUp%2A>) pour collecter <xref:System.Windows.Input.StylusPoint> données, créer des traits et les ajouter à un <xref:System.Windows.Controls.InkPresenter> (qui restitue l’encre sur le contrôle).  
  
 Cette rubrique contient les sous-sections suivantes :  
  
- [Guide pratique pour Collecter des données de Point de stylet et créer des traits d’encre](#CollectingStylusPointDataAndCreatingInkStrokes)  
  
- [Guide pratique pour Activer votre contrôle d’accepter l’entrée à partir de la souris](#EnablingYourControlToAcceptInputTromTheMouse)  
  
- [Assemblage](#PuttingItTogether)  
  
- [À l’aide de Plug-ins supplémentaires et DynamicRenderers](#UsingAdditionalPluginsAndDynamicRenderers)  
  
- [Conclusion](#AdvancedInkHandling_Conclusion)  
  
<a name="CollectingStylusPointDataAndCreatingInkStrokes"></a>   
## <a name="how-to-collect-stylus-point-data-and-create-ink-strokes"></a>Procédure : Collecter des données de Point de stylet et créer des traits d’encre  
 Pour créer un contrôle qui collecte et gère l’encre traits les opérations suivantes :  
  
1. Dérivez une classe de <xref:System.Windows.Controls.Control> ou une des classes dérivées de <xref:System.Windows.Controls.Control>, tel que <xref:System.Windows.Controls.Label>.  
  
     [!code-csharp[AdvancedInkTopicsSamples#20](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#20)]  
    [!code-csharp[AdvancedInkTopicsSamples#14](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#14)]  
    [!code-csharp[AdvancedInkTopicsSamples#15](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#15)]  
  
2. Ajouter un <xref:System.Windows.Controls.InkPresenter> à la classe et définissez la <xref:System.Windows.Controls.ContentControl.Content%2A> à la nouvelle propriété <xref:System.Windows.Controls.InkPresenter>.  
  
     [!code-csharp[AdvancedInkTopicsSamples#16](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#16)]  
  
3. Attacher le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> de la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> à la <xref:System.Windows.Controls.InkPresenter> en appelant le <xref:System.Windows.Controls.InkPresenter.AttachVisuals%2A> (méthode) et ajoutez le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> à la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection. Cela permet la <xref:System.Windows.Controls.InkPresenter> pour afficher l’encre comme les données de point de stylet sont collectées par votre contrôle.  
  
     [!code-csharp[AdvancedInkTopicsSamples#17](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#17)]  
    [!code-csharp[AdvancedInkTopicsSamples#18](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#18)]  
  
4. Remplacez la méthode <xref:System.Windows.UIElement.OnStylusDown%2A> .  Dans cette méthode, capturez le stylet avec un appel à <xref:System.Windows.Input.Stylus.Capture%2A>. En capturant le stylet, votre contrôle sera pour continuer à recevoir <xref:System.Windows.UIElement.StylusMove> et <xref:System.Windows.UIElement.StylusUp> événements même si le stylet quitte les limites du contrôle. Cela n’est pas strictement obligatoire, mais il est presque toujours souhaité pour une expérience utilisateur optimale. Créer un nouveau <xref:System.Windows.Input.StylusPointCollection> pour rassembler <xref:System.Windows.Input.StylusPoint> données. Enfin, ajoutez l’ensemble initial de <xref:System.Windows.Input.StylusPoint> données à le <xref:System.Windows.Input.StylusPointCollection>.  
  
     [!code-csharp[AdvancedInkTopicsSamples#7](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#7)]  
  
5. Remplacer le <xref:System.Windows.UIElement.OnStylusMove%2A> méthode et ajoutez le <xref:System.Windows.Input.StylusPoint> données à la <xref:System.Windows.Input.StylusPointCollection> objet que vous avez créé précédemment.  
  
     [!code-csharp[AdvancedInkTopicsSamples#8](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#8)]  
  
6. Remplacer le <xref:System.Windows.UIElement.OnStylusUp%2A> (méthode) et créez un nouveau <xref:System.Windows.Ink.Stroke> avec la <xref:System.Windows.Input.StylusPointCollection> données. Ajoutez la nouvelle <xref:System.Windows.Ink.Stroke> que vous avez créé à le <xref:System.Windows.Controls.InkPresenter.Strokes%2A> collection de la <xref:System.Windows.Controls.InkPresenter> et la capture du stylet.  
  
     [!code-csharp[AdvancedInkTopicsSamples#10](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#10)]  
  
<a name="EnablingYourControlToAcceptInputTromTheMouse"></a>   
## <a name="how-to-enable-your-control-to-accept-input-from-the-mouse"></a>Procédure : Activer votre contrôle d’accepter l’entrée à partir de la souris  
 Si vous ajoutez le contrôle précédent à votre application, exécutez, puis utilisez la souris comme périphérique d’entrée, vous remarquerez que les traits ne sont pas conservées. Pour conserver les traits lorsque la souris est utilisée en tant que le périphérique d’entrée les opérations suivantes :  
  
1. Remplacer le <xref:System.Windows.UIElement.OnMouseLeftButtonDown%2A> et créez un nouveau <xref:System.Windows.Input.StylusPointCollection> obtenir la position de la souris lorsque l’événement s’est produite et créer un <xref:System.Windows.Input.StylusPoint> les données du point et ajoutez le <xref:System.Windows.Input.StylusPoint> à la <xref:System.Windows.Input.StylusPointCollection>.  
  
     [!code-csharp[AdvancedInkTopicsSamples#11](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#11)]  
  
2. Remplacez la méthode <xref:System.Windows.UIElement.OnMouseMove%2A> . Obtient la position de la souris lorsque l’événement s’est produite et créer un <xref:System.Windows.Input.StylusPoint> en utilisant les données de point.  Ajouter le <xref:System.Windows.Input.StylusPoint> à la <xref:System.Windows.Input.StylusPointCollection> objet que vous avez créé précédemment.  
  
     [!code-csharp[AdvancedInkTopicsSamples#12](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#12)]  
  
3. Remplacez la méthode <xref:System.Windows.UIElement.OnMouseLeftButtonUp%2A> .  Créer un nouveau <xref:System.Windows.Ink.Stroke> avec la <xref:System.Windows.Input.StylusPointCollection> données et ajoutez la nouvelle <xref:System.Windows.Ink.Stroke> que vous avez créé à le <xref:System.Windows.Controls.InkPresenter.Strokes%2A> collection de la <xref:System.Windows.Controls.InkPresenter>.  
  
     [!code-csharp[AdvancedInkTopicsSamples#13](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#13)]  
  
<a name="PuttingItTogether"></a>   
## <a name="putting-it-together"></a>Assemblage  
 L’exemple suivant est un contrôle personnalisé qui collecte d’encre lorsque l’utilisateur utilise la souris ou le stylet.  
  
 [!code-csharp[AdvancedInkTopicsSamples#20](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#20)]  
[!code-csharp[AdvancedInkTopicsSamples#6](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#6)]  
  
<a name="UsingAdditionalPluginsAndDynamicRenderers"></a>   
## <a name="using-additional-plug-ins-and-dynamicrenderers"></a>À l’aide de Plug-ins supplémentaires et DynamicRenderers  
 Tout comme l’InkCanvas, votre contrôle personnalisé peut avoir personnalisé <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> et d’autres <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> objets. Ajouter à la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection. L’ordre de la <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> des objets dans le <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> affecte l’apparence de l’encre lorsqu’il est restitué. Supposons que vous ayez un <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> appelé `dynamicRenderer` et personnalisé <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> appelée `translatePlugin` qui décale l’encre du stylet. Si `translatePlugin` est le premier <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> dans le <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection>, et `dynamicRenderer` est le deuxième, l’encre qui « coule » sera décalée quand l’utilisateur déplace le stylet. Si `dynamicRenderer` est tout d’abord, et `translatePlugin` est en second lieu, l’encre ne sera pas décalée jusqu'à ce que l’utilisateur soulève le stylet.  
  
<a name="AdvancedInkHandling_Conclusion"></a>   
## <a name="conclusion"></a>Conclusion  
 Vous pouvez créer un contrôle qui collecte et restitue l’encre en substituant les méthodes d’événement de stylet. En créant votre propre contrôle, en dérivant vos propres <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> classes et en les insérant le dans <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection>, vous pouvez implémenter virtuellement tout comportement imaginable avec l’encre numérique. Vous avez accès à la <xref:System.Windows.Input.StylusPoint> données tel qu’il sont générées, ce qui vous donne la possibilité de personnaliser <xref:System.Windows.Input.Stylus> d’entrée et de restituer sur l’écran en fonction de votre application. Étant donné que vous avez un accès de bas niveau pour le <xref:System.Windows.Input.StylusPoint> données, vous pouvez implémenter la collecte d’encre et restituer avec des performances optimales pour votre application.  
  
## <a name="see-also"></a>Voir aussi

- [Gestion avancée de l’encre](advanced-ink-handling.md)
- [Accéder et manipuler l’entrée du stylet](https://go.microsoft.com/fwlink/?LinkId=50752&clcid=0x409)
