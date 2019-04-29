---
title: 'Optimisation des performances : Autres recommandations'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Terminal Services rendering [WPF]
- opacity [WPF]
- hit-test objects [WPF]
- ScrollBarVisibility enumeration [WPF]
- brushes [WPF], performance
ms.assetid: d028cc65-7e97-4a4f-9859-929734eaf40d
ms.openlocfilehash: 56d3e3cad09b46090a11b884f3ac590e8d4ba23a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61773098"
---
# <a name="optimizing-performance-other-recommendations"></a>Optimisation des performances : Autres recommandations
<a name="introduction"></a> Cette rubrique fournit des recommandations pour améliorer les performances en plus de celles abordées dans les rubriques de la section [Optimisation des performances des applications WPF](optimizing-wpf-application-performance.md).  
  
 Cette rubrique contient les sections suivantes :  
  
- [Opacité au niveau des pinceaux et opacité au niveau des éléments](#Opacity)  
  
- [Navigation vers un objet](#Navigation_Objects)  
  
- [Test de positionnement sur les grandes surfaces 3D](#Hit_Testing)  
  
- [Événement CompositionTarget.Rendering](#CompositionTarget_Rendering_Event)  
  
- [Éviter l’utilisation de ScrollBarVisibility=Auto](#Avoid_Using_ScrollBarVisibility)  
  
- [Configurer le service de mise en cache de polices pour réduire le temps de démarrage](#FontCache)  
  
<a name="Opacity"></a>   
## <a name="opacity-on-brushes-versus-opacity-on-elements"></a>Opacité au niveau des pinceaux et opacité au niveau des éléments  
 Lorsque vous utilisez un <xref:System.Windows.Media.Brush> pour définir le <xref:System.Windows.Shapes.Shape.Fill%2A> ou <xref:System.Windows.Shapes.Shape.Stroke%2A> d’un élément, il est préférable de définir la <xref:System.Windows.Media.Brush.Opacity%2A?displayProperty=nameWithType> valeur plutôt que le paramètre de l’élément <xref:System.Windows.UIElement.Opacity%2A> propriété. Modification d’un élément <xref:System.Windows.UIElement.Opacity%2A> propriété peut provoquer une [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pour créer une surface temporaire.  
  
<a name="Navigation_Objects"></a>   
## <a name="navigation-to-object"></a>Navigation vers un objet  
 Le <xref:System.Windows.Navigation.NavigationWindow> objet dérive <xref:System.Windows.Window> et l’étend avec prise en charge de la navigation de contenu, principalement en combinant <xref:System.Windows.Navigation.NavigationService> et le journal. Vous pouvez mettre à jour la zone cliente de <xref:System.Windows.Navigation.NavigationWindow> en spécifiant un [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)] ou un objet. L'exemple suivant illustre les deux méthodes :  
  
 [!code-csharp[Performance#PerformanceSnippet14](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/TestNavigation.xaml.cs#performancesnippet14)]
 [!code-vb[Performance#PerformanceSnippet14](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Performance/visualbasic/testnavigation.xaml.vb#performancesnippet14)]  
  
 Chaque <xref:System.Windows.Navigation.NavigationWindow> objet possède un journal qui enregistre l’historique de navigation de l’utilisateur dans cette fenêtre. Un des objectifs du journal est de permettre aux utilisateurs de retracer leurs étapes.  
  
 Quand vous naviguez à l’aide d’un [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)], le journal stocke uniquement la référence de l’[!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)]. Cela signifie que chaque fois que vous revisitez la page, elle est reconstruite dynamiquement, ce qui peut prendre beaucoup de temps selon la complexité de la page. Dans ce cas, le coût de stockage du journal est faible, mais le temps de reconstitution de la page est élevé.  
  
 Quand vous naviguez à l’aide d’un objet, le journal stocke intégralement l’arborescence de visuels de l’objet. Cela signifie que chaque fois que vous visitez la page, elle s’affiche immédiatement sans avoir à être reconstruite. Dans ce cas, le coût de stockage du journal est élevé, mais le temps de reconstitution de la page est faible.  
  
 Lorsque vous utilisez la <xref:System.Windows.Navigation.NavigationWindow> de l’objet, vous devez garder à l’esprit l’impact de la journalisation sur les performances de votre application. Pour plus d’informations, consultez [Vue d’ensemble de la navigation](../app-development/navigation-overview.md).  
  
<a name="Hit_Testing"></a>   
## <a name="hit-testing-on-large-3d-surfaces"></a>Test de positionnement sur les grandes surfaces 3D  
 Le test de positionnement sur les grandes surfaces 3D est une opération qui affecte considérablement les performances en utilisant une grande part du processeur. Cela est particulièrement vrai quand la surface 3D est animée. Si vous n’avez pas besoin de tester le positionnement sur ces surfaces, désactivez le test de positionnement. Objets qui sont dérivés de <xref:System.Windows.UIElement> peut désactiver le test de positionnement en définissant le <xref:System.Windows.UIElement.IsHitTestVisible%2A> propriété `false`.  
  
<a name="CompositionTarget_Rendering_Event"></a>   
## <a name="compositiontargetrendering-event"></a>Événement CompositionTarget.Rendering  
 Le <xref:System.Windows.Media.CompositionTarget.Rendering?displayProperty=nameWithType> événement entraîne [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pour animer en permanence. Si vous utilisez cet événement, détacher-le dès que possible.  
  
<a name="Avoid_Using_ScrollBarVisibility"></a>   
## <a name="avoid-using-scrollbarvisibilityauto"></a>Éviter l’utilisation de ScrollBarVisibility=Auto  
 Si possible, évitez d’utiliser le <xref:System.Windows.Controls.ScrollBarVisibility.Auto?displayProperty=nameWithType> valeur pour le `HorizontalScrollBarVisibility` et `VerticalScrollBarVisibility` propriétés. Ces propriétés sont définies pour <xref:System.Windows.Controls.RichTextBox>, <xref:System.Windows.Controls.ScrollViewer>, et <xref:System.Windows.Controls.TextBox> objets et en tant que propriété jointe pour le <xref:System.Windows.Controls.ListBox> objet. Au lieu de cela, définissez <xref:System.Windows.Controls.ScrollBarVisibility> à <xref:System.Windows.Controls.ScrollBarVisibility.Disabled>, <xref:System.Windows.Controls.ScrollBarVisibility.Hidden>, ou <xref:System.Windows.Controls.ScrollBarVisibility.Visible>.  
  
 Le <xref:System.Windows.Controls.ScrollBarVisibility.Auto> valeur est destinée aux cas lorsque l’espace est limité et barres de défilement doivent être affichées uniquement lorsque cela est nécessaire. Par exemple, il peut être utile d’utiliser cette <xref:System.Windows.Controls.ScrollBarVisibility> valeur avec un <xref:System.Windows.Controls.ListBox> de 30 éléments par opposition à un <xref:System.Windows.Controls.TextBox> avec des centaines de lignes de texte.  
  
<a name="FontCache"></a>   
## <a name="configure-font-cache-service-to-reduce-start-up-time"></a>Configurer le service de mise en cache de polices pour réduire le temps de démarrage  
 Le service de mise en cache de polices [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] partage les données de police entre les applications [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)]. La première application [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] que vous exécutez démarre ce service s’il n’est pas déjà en cours d’exécution. Si vous utilisez [!INCLUDE[TLA#tla_winvista](../../../../includes/tlasharptla-winvista-md.md)], vous pouvez définir le service « Windows Presentation Foundation (WPF) Font Cache 3.0.0.0 » à partir de « Manuel » (la valeur par défaut) sur « Automatique (début différé) » afin de réduire le temps de démarrage initial [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] applications.  
  
## <a name="see-also"></a>Voir aussi

- [Planification des performances des applications](planning-for-application-performance.md)
- [Tirer parti du matériel](optimizing-performance-taking-advantage-of-hardware.md)
- [Disposition et conception](optimizing-performance-layout-and-design.md)
- [Graphiques 2D et acquisition d'images](optimizing-performance-2d-graphics-and-imaging.md)
- [Comportement de l’objet](optimizing-performance-object-behavior.md)
- [Ressources d'application](optimizing-performance-application-resources.md)
- [Text](optimizing-performance-text.md)
- [Liaison de données](optimizing-performance-data-binding.md)
- [Conseils et astuces sur les animations](../graphics-multimedia/animation-tips-and-tricks.md)
