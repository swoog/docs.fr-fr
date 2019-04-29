---
title: Vue d'ensemble de Popup
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Popup
- Popup control [WPF], about Popup control
ms.assetid: 774f53ca-bff8-470e-9ce9-3928b4cf3d4c
ms.openlocfilehash: 370970c80221e371db5a97303ef2650d14300b14
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770563"
---
# <a name="popup-overview"></a>Vue d'ensemble de Popup
Le <xref:System.Windows.Controls.Primitives.Popup> contrôle offre un moyen pour afficher le contenu dans une fenêtre distincte qui flotte au-dessus de la fenêtre d’application actuelle par rapport à une coordonnée d’écran ou élément désignée. Cette rubrique présente la <xref:System.Windows.Controls.Primitives.Popup> contrôler et fournit des informations sur son utilisation.  

<a name="What_Is_a_Popup_"></a>   
## <a name="what-is-a-popup"></a>Qu’est-ce qu’un contrôle Popup ?  
 Un <xref:System.Windows.Controls.Primitives.Popup> contrôle affiche le contenu dans une fenêtre distincte par rapport à un élément ou un point sur l’écran. Lorsque le <xref:System.Windows.Controls.Primitives.Popup> est visible, le <xref:System.Windows.Controls.Primitives.Popup.IsOpen%2A> propriété est définie sur `true`.  
  
> [!NOTE]
>  Un <xref:System.Windows.Controls.Primitives.Popup> ne s’ouvre pas automatiquement lorsque le pointeur de la souris se déplace sur son objet parent. Si vous souhaitez un <xref:System.Windows.Controls.Primitives.Popup> pour ouvrir automatiquement, utilisez le <xref:System.Windows.Controls.ToolTip> ou <xref:System.Windows.Controls.ToolTipService> classe. Pour plus d’informations, consultez [Vue d’ensemble de l’info-bulle](tooltip-overview.md).  
  
<a name="APopupExample"></a>   
## <a name="creating-a-popup"></a>Création d'une fenêtre contextuelle  
 L’exemple suivant montre comment définir un <xref:System.Windows.Controls.Primitives.Popup> contrôle qui est l’élément enfant d’un <xref:System.Windows.Controls.Button> contrôle. Étant donné qu’un <xref:System.Windows.Controls.Button> peut avoir qu’un seul élément enfant, cet exemple place le texte pour le <xref:System.Windows.Controls.Button> et le <xref:System.Windows.Controls.Primitives.Popup> des contrôles dans un <xref:System.Windows.Controls.StackPanel>. Le contenu de la <xref:System.Windows.Controls.Primitives.Popup> s’affiche dans un <xref:System.Windows.Controls.TextBlock> contrôle, qui affiche son texte dans une fenêtre distincte qui flotte au-dessus de la fenêtre d’application près connexe <xref:System.Windows.Controls.Button> contrôle.  
  
 [!code-xaml[PopupSimple#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupSimple/CSharp/Window1.xaml#1)]  
  
 [!code-xaml[PopupSimple#CreatePopupCodeXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupSimple/CSharp/Window1.xaml#createpopupcodexaml)]  
  
<a name="PopupUses"></a>   
## <a name="controls-that-implement-a-popup"></a>Contrôles qui implémentent un contrôle Popup  
 Vous pouvez générer <xref:System.Windows.Controls.Primitives.Popup> contrôles dans d’autres contrôles. Les contrôles suivants implémentent le <xref:System.Windows.Controls.Primitives.Popup> contrôle pour des utilisations spécifiques :  
  
- <xref:System.Windows.Controls.ToolTip>. Si vous souhaitez créer une info-bulle pour un élément, utilisez la <xref:System.Windows.Controls.ToolTip> et <xref:System.Windows.Controls.ToolTipService> classes. Pour plus d’informations, consultez [Vue d’ensemble de l’info-bulle](tooltip-overview.md).  
  
- <xref:System.Windows.Controls.ContextMenu>. Si vous souhaitez créer un menu contextuel pour un élément, utilisez la <xref:System.Windows.Controls.ContextMenu> contrôle. Pour plus d’informations, consultez [Vue d’ensemble de ContextMenu](contextmenu-overview.md).  
  
- <xref:System.Windows.Controls.ComboBox>. Si vous souhaitez créer un contrôle de sélection qui possède une zone de liste déroulante qui peut être affichée ou masquée, utilisez le <xref:System.Windows.Controls.ComboBox> contrôle.  
  
- <xref:System.Windows.Controls.Expander>. Si vous souhaitez créer un contrôle qui affiche un en-tête avec une zone réductible qui affiche du contenu, utilisez le <xref:System.Windows.Controls.Expander> contrôle. Pour plus d’informations, consultez [Vue d’ensemble d’Expander](expander-overview.md).  
  
<a name="PopupBehaviorandAppearance"></a>   
## <a name="popup-behavior-and-appearance"></a>Comportement et apparence d’un contrôle Popup  
 Le <xref:System.Windows.Controls.Primitives.Popup> contrôle fournit des fonctionnalités qui vous permettent de personnaliser son comportement et son apparence. Par exemple, vous pouvez définir le comportement d’ouverture et de fermeture, des animations, des effets d’opacité et bitmap, et <xref:System.Windows.Controls.Primitives.Popup> taille et la position.  
  
<a name="OpenandCloseBehavior"></a>   
### <a name="open-and-close-behavior"></a>Comportement à l’ouverture et à la fermeture  
 Un <xref:System.Windows.Controls.Primitives.Popup> contrôle affiche son contenu lorsque le <xref:System.Windows.Controls.Primitives.Popup.IsOpen%2A> propriété est définie sur `true`. Par défaut, <xref:System.Windows.Controls.Primitives.Popup> reste ouverte jusqu'à ce que le <xref:System.Windows.Controls.Primitives.Popup.IsOpen%2A> propriété est définie sur `false`. Toutefois, vous pouvez modifier le comportement par défaut en définissant le <xref:System.Windows.Controls.Primitives.Popup.StaysOpen%2A> propriété `false`. Lorsque vous définissez cette propriété sur `false`, la <xref:System.Windows.Controls.Primitives.Popup> fenêtre de contenu possède la capture de la souris. Le <xref:System.Windows.Controls.Primitives.Popup> perd la souris capture et la fenêtre se ferme lorsqu’un événement de souris se produit en dehors de la <xref:System.Windows.Controls.Primitives.Popup> fenêtre.  
  
 Le <xref:System.Windows.Controls.Primitives.Popup.Opened> et <xref:System.Windows.Controls.Primitives.Popup.Closed> événements sont déclenchés lorsque la <xref:System.Windows.Controls.Primitives.Popup> fenêtre de contenu est ouvert ou fermé.  
  
<a name="Animation"></a>   
### <a name="animation"></a>Animation  
 Le <xref:System.Windows.Controls.Primitives.Popup> contrôle a une prise en charge intégrée des animations qui sont généralement associées à des comportements tels que l’apparition en fondu et diapositive dans. Vous pouvez activer ces animations en définissant le <xref:System.Windows.Controls.Primitives.Popup.PopupAnimation%2A> propriété un <xref:System.Windows.Controls.Primitives.PopupAnimation> valeur d’énumération. Pour <xref:System.Windows.Controls.Primitives.Popup> animations fonctionne correctement, vous devez définir le <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> propriété `true`.  
  
 Vous pouvez également appliquer des animations telles que <xref:System.Windows.Media.Animation.Storyboard> à la <xref:System.Windows.Controls.Primitives.Popup> contrôle.  
  
<a name="OpacityandBitmapEffects"></a>   
### <a name="opacity-and-bitmap-effects"></a>Effets d’opacité et bitmap  
 Le <xref:System.Windows.UIElement.Opacity%2A> propriété pour un <xref:System.Windows.Controls.Primitives.Popup> contrôle n’a aucun effet sur son contenu. Par défaut, le <xref:System.Windows.Controls.Primitives.Popup> fenêtre de contenu est opaque. Pour créer un transparent <xref:System.Windows.Controls.Primitives.Popup>, définissez le <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> propriété `true`.  
  
 Le contenu d’un <xref:System.Windows.Controls.Primitives.Popup> n’hérite pas les effets bitmap, tel que <xref:System.Windows.Media.Effects.DropShadowBitmapEffect>, que vous définissez directement sur le <xref:System.Windows.Controls.Primitives.Popup> contrôle ou sur tout autre élément dans la fenêtre parente. Pour les effets bitmap apparaissent dans le contenu d’un <xref:System.Windows.Controls.Primitives.Popup>, vous devez définir l’effet bitmap directement sur son contenu. Par exemple, si l’enfant d’un <xref:System.Windows.Controls.Primitives.Popup> est un <xref:System.Windows.Controls.StackPanel>, définissez l’effet bitmap sur le <xref:System.Windows.Controls.StackPanel>.  
  
<a name="PopupSize"></a>   
### <a name="popup-size"></a>Dimensionnement d’un contrôle Popup  
 Par défaut, un <xref:System.Windows.Controls.Primitives.Popup> est automatiquement ajusté à son contenu. En cas de redimensionnement automatique, certains effets bitmap peuvent être masqués car la taille par défaut de la zone d’écran qui est définie pour le <xref:System.Windows.Controls.Primitives.Popup> contenu ne fournit pas suffisamment d’espace pour l’affichage des effets bitmap.  
  
 <xref:System.Windows.Controls.Primitives.Popup> contenu peut également être dissimulé lorsque vous définissez un <xref:System.Windows.UIElement.RenderTransform%2A> sur le contenu. Dans ce scénario, un contenu peut être masqué si le contenu de l’élément transformé <xref:System.Windows.Controls.Primitives.Popup> s’étend au-delà de la zone d’origine <xref:System.Windows.Controls.Primitives.Popup>. Si un effet bitmap ou une transformation requiert davantage d’espace, vous pouvez définir une marge autour du <xref:System.Windows.Controls.Primitives.Popup> contenu afin de fournir plus de zone pour le contrôle.  
  
<a name="DefiningPopupPosition"></a>   
## <a name="defining-the-popup-position"></a>Définition de la position d’un contrôle Popup  
 Vous pouvez positionner un popup en définissant le <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A>, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A>, <xref:System.Windows.Controls.Primitives.Popup.Placement%2A>, <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A>, et <xref:System.Windows.Controls.Primitives.Popup.VerticalOffsetProperty> propriétés. Pour plus d’informations, consultez [Comportement de positionnement de Popup](popup-placement-behavior.md). Lorsque <xref:System.Windows.Controls.Primitives.Popup> s’affiche sur l’écran, il ne se repositionne pas si son parent est repositionné.  
  
<a name="CustomizingPopupPlacement"></a>   
### <a name="customizing-popup-placement"></a>Personnalisation du positionnement d’un contrôle Popup  
 Vous pouvez personnaliser le positionnement d’un <xref:System.Windows.Controls.Primitives.Popup> contrôle en spécifiant un jeu de coordonnées sont relatives à la <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> où vous souhaitez le <xref:System.Windows.Controls.Primitives.Popup> apparaisse.  
  
 Pour personnaliser le positionnement, définissez le <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> propriété <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>. Définissez ensuite un <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> délégué qui retourne un ensemble de points de positionnement possibles et les axes principaux (dans l’ordre de préférence) pour le <xref:System.Windows.Controls.Primitives.Popup>. Le point qui montre la plus grande partie de la <xref:System.Windows.Controls.Primitives.Popup> est automatiquement sélectionné. Pour obtenir un exemple, consultez [Spécifier une position de menu contextuel personnalisée](how-to-specify-a-custom-popup-position.md).  
  
<a name="PopupandtheVisualTree"></a>   
## <a name="popup-and-the-visual-tree"></a>Contrôle Popup et arborescence d’éléments visuels  
 Un <xref:System.Windows.Controls.Primitives.Popup> contrôle n’a pas sa propre arborescence d’éléments visuels ; il retourne à la place d’une taille de 0 (zéro) lorsque le <xref:System.Windows.Controls.Primitives.Popup.MeasureOverride%2A> méthode pour <xref:System.Windows.Controls.Primitives.Popup> est appelée. Toutefois, lorsque vous définissez la <xref:System.Windows.Controls.Primitives.Popup.IsOpen%2A> propriété du <xref:System.Windows.Controls.Primitives.Popup> à `true`, une nouvelle fenêtre avec sa propre arborescence d’éléments visuels est créée. La nouvelle fenêtre renferme le <xref:System.Windows.Controls.Primitives.Popup.Child%2A> contenu de <xref:System.Windows.Controls.Primitives.Popup>. La largeur et la hauteur de la nouvelle fenêtre ne peuvent pas dépasser 75 % de la largeur et de la hauteur de l’écran.  
  
 Le <xref:System.Windows.Controls.Primitives.Popup> contrôle conserve une référence à son <xref:System.Windows.Controls.Primitives.Popup.Child%2A> contenu comme un enfant logique. Lorsque la nouvelle fenêtre est créée, le contenu de <xref:System.Windows.Controls.Primitives.Popup> devient un enfant visuel de la fenêtre et reste l’enfant logique de <xref:System.Windows.Controls.Primitives.Popup>. À l’inverse, <xref:System.Windows.Controls.Primitives.Popup> reste le parent logique de son <xref:System.Windows.Controls.Primitives.Popup.Child%2A> contenu.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Primitives.Popup>
- <xref:System.Windows.Controls.Primitives.PopupPrimaryAxis>
- <xref:System.Windows.Controls.Primitives.PlacementMode>
- <xref:System.Windows.Controls.Primitives.CustomPopupPlacement>
- <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback>
- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [Rubriques de guide pratique](popup-how-to-topics.md)
- [Rubriques de guide pratique](tooltip-how-to-topics.md)
