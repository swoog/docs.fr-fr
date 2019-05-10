---
title: Interception d'entrée à partir du stylet
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 'architecture [WPF], '
- ', '
- ', '
- ', '
ms.assetid: 791bb2f0-4e5c-4569-ac3c-211996808d44
ms.openlocfilehash: 76976f1599ecbbaf7405d7941f66aa2c5f955565
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64598951"
---
# <a name="intercepting-input-from-the-stylus"></a>Interception d'entrée à partir du stylet
Le <xref:System.Windows.Input.StylusPlugIns> architecture fournit un mécanisme pour l’implémentation du contrôle de bas niveau sur <xref:System.Windows.Input.Stylus> d’entrée et de la création de l’encre numérique <xref:System.Windows.Ink.Stroke> objets. Le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> classe fournit un mécanisme pour vous permettre d’implémenter un comportement personnalisé et l’appliquer au flux de données provenant du périphérique de stylet pour des performances optimales.  
  
 Cette rubrique contient les sous-sections suivantes :  
  
- [Architecture](#Architecture)  
  
- [Implémentation de Plug-ins du stylet](#ImplementingStylusPlugins)  
  
- [Ajout de votre plug-in à un InkCanvas](#AddingYourPluginToAnInkCanvas)  
  
- [Conclusion](#Conclusion)  
  
<a name="Architecture"></a>   
## <a name="architecture"></a>Architecture  
 Le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> est l’évolution de la [StylusInput](https://go.microsoft.com/fwlink/?LinkId=50753&clcid=0x409) API, décrites dans [l’accès et la manipulation de Pen Input](https://go.microsoft.com/fwlink/?LinkId=50752&clcid=0x409), dans le [logiciel de Microsoft Windows XP Tablet PC Edition Kit de développement 1.7](https://go.microsoft.com/fwlink/?linkid=11782&clcid=0x409).  
  
 Chaque <xref:System.Windows.UIElement> a un <xref:System.Windows.UIElement.StylusPlugIns%2A> propriété qui est un <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection>. Vous pouvez ajouter un <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> à d’un élément <xref:System.Windows.UIElement.StylusPlugIns%2A> propriété manipuler <xref:System.Windows.Input.StylusPoint> données tel qu’il sont générées. <xref:System.Windows.Input.StylusPoint> données se composent de toutes les propriétés prises en charge par le digitaliseur de système, y compris le <xref:System.Windows.Input.StylusPoint.X%2A> et <xref:System.Windows.Input.StylusPoint.Y%2A> point de données, ainsi que <xref:System.Windows.Input.StylusPoint.PressureFactor%2A> données.  
  
 Votre <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> objets sont insérés directement dans le flux de données provenant de la <xref:System.Windows.Input.Stylus> appareil lorsque vous ajoutez le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> à la <xref:System.Windows.UIElement.StylusPlugIns%2A> propriété. L’ordre dans lequel les plug-ins sont ajoutés à la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection détermine l’ordre dans lequel ils recevront <xref:System.Windows.Input.StylusPoint> données. Par exemple, si vous ajoutez un plug-in de filtre qui restreint l’entrée à une région particulière, puis ajoutez un plug-in qui reconnaît les gestes car ils sont écrits, le plug-in qui reconnaît les gestes recevra filtré <xref:System.Windows.Input.StylusPoint> données.  
  
<a name="ImplementingStylusPlugins"></a>   
## <a name="implementing-stylus-plug-ins"></a>Implémentation de Plug-ins du stylet  
 Pour implémenter un plug-in, dérivez une classe de <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn>. Cette classe est appliquée au flux de données lorsqu’il provient le <xref:System.Windows.Input.Stylus>. Dans cette classe, vous pouvez modifier les valeurs de la <xref:System.Windows.Input.StylusPoint> données.  
  
> [!CAUTION]
>  Si un <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> lève ou provoque une exception, l’application se ferme. Vous devez tester rigoureusement les contrôles qui consomment un <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> et utiliser uniquement un contrôle si vous êtes certain que le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> pas lève une exception.  
  
 L’exemple suivant illustre un plug-in qui restreint l’entrée du stylet en modifiant le <xref:System.Windows.Input.StylusPoint.X%2A> et <xref:System.Windows.Input.StylusPoint.Y%2A> des valeurs dans le <xref:System.Windows.Input.StylusPoint> données lorsqu’elles proviennent de la <xref:System.Windows.Input.Stylus> appareil.  
  
 [!code-csharp[AdvancedInkTopicsSamples#19](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/DynamicRenderer.cs#19)]
 [!code-vb[AdvancedInkTopicsSamples#19](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdvancedInkTopicsSamples/VisualBasic/DynamicRenderer.vb#19)]  
[!code-csharp[AdvancedInkTopicsSamples#3](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/DynamicRenderer.cs#3)]
[!code-vb[AdvancedInkTopicsSamples#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdvancedInkTopicsSamples/VisualBasic/DynamicRenderer.vb#3)]  
  
<a name="AddingYourPluginToAnInkCanvas"></a>   
## <a name="adding-your-plug-in-to-an-inkcanvas"></a>Ajout de votre plug-in à un InkCanvas  
 Le moyen le plus simple d’utiliser votre plug-in personnalisé consiste à implémenter une classe qui dérive d’InkCanvas et ajoutez-la à la <xref:System.Windows.UIElement.StylusPlugIns%2A> propriété.  
  
 L’exemple suivant montre un personnalisé <xref:System.Windows.Controls.InkCanvas> qui filtre l’encre.  
  
 [!code-csharp[AdvancedInkTopicsSamples#4](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/Window1.xaml.cs#4)]  
  
 Si vous ajoutez un `FilterInkCanvas` à votre application et l’exécutez, vous remarquerez que l’encre n’est pas restreinte à une région jusqu'à ce que l’utilisateur après un trait. Il s’agit, car le <xref:System.Windows.Controls.InkCanvas> a un <xref:System.Windows.Controls.InkCanvas.DynamicRenderer%2A> propriété, qui est un <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> et est déjà un membre de la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection. Personnalisé <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> que vous avez ajouté à la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection reçoit le <xref:System.Windows.Input.StylusPoint> données après <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> reçoit des données. Par conséquent, le <xref:System.Windows.Input.StylusPoint> données ne sont pas filtrées jusqu'à une fois que l’utilisateur soulève le stylet pour terminer un trait. Pour filtrer l’encre comme l’utilisateur dessine, vous devez insérer le `FilterPlugin` avant le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer>.  
  
 Le code c# suivant montre un personnalisé <xref:System.Windows.Controls.InkCanvas> qui filtre l’encre comme il est dessiné.  
  
 [!code-csharp[AdvancedInkTopicsSamples#5](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/Window1.xaml.cs#5)]  
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a>Conclusion  
 En dérivant votre propre <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> classes et en les insérant dans <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> collections, vous pouvez améliorer considérablement le comportement de votre encre numérique. Vous avez accès à la <xref:System.Windows.Input.StylusPoint> données tel qu’il sont générées, ce qui vous donne la possibilité de personnaliser le <xref:System.Windows.Input.Stylus> d’entrée. Étant donné que vous avez un accès de bas niveau pour le <xref:System.Windows.Input.StylusPoint> données, vous pouvez implémenter la collecte d’encre et de rendu avec des performances optimales pour votre application.  
  
## <a name="see-also"></a>Voir aussi

- [Gestion avancée de l’encre](advanced-ink-handling.md)
- [Accéder et manipuler l’entrée du stylet](https://go.microsoft.com/fwlink/?LinkId=50752&clcid=0x409)
