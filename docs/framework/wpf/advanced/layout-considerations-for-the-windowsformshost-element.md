---
title: Considérations sur la disposition de l'élément WindowsFormsHost
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms [WPF], interoperability with
- Windows Forms [WPF], WPF interoperation
- interoperability [WPF], Windows Forms
- WindowsFormsHost element layout considerations [WPF]
- dynamic layout [WPF interoperability]
- device-independent pixels
ms.assetid: 3c574597-bbde-440f-95cc-01371f1a5d9d
ms.openlocfilehash: ff52d3bbf7bf5d9d85f7a6fd5f73d9730dde8fad
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59168985"
---
# <a name="layout-considerations-for-the-windowsformshost-element"></a>Considérations sur la disposition de l'élément WindowsFormsHost
Cette rubrique décrit comment la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément interagit avec le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] système de disposition.  
  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] prennent en charge des logiques différentes mais similaire, pour dimensionner et positionner des éléments sur un formulaire ou la page. Lorsque vous créez une interface utilisateur de hybride (IU) qui héberge [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] des contrôles dans des [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément intègre les deux méthodes de disposition.  
  
## <a name="differences-in-layout-between-wpf-and-windows-forms"></a>Différences de disposition entre WPF et Windows Forms  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] utilise une disposition indépendante de la résolution. Tous les [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] dimensions de mise en page sont spécifiées à l’aide de *pixels indépendants du périphérique*. Un pixel indépendant du périphérique étant un sixième quatre-vingt-dix d’un pouce et indépendant de toute résolution, vous obtenez des résultats similaires indépendamment de si vous effectuez un rendu à un moniteur de 72 ppp ou une imprimante 19 200 ppp.  
  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] est également basé sur *disposition dynamique*. Cela signifie qu’un élément d’interface utilisateur se positionne sur un formulaire ou une page en fonction de son contenu, de son conteneur de disposition du parent et de la taille d’écran disponible. Disposition dynamique facilite la localisation en ajustant automatiquement la taille et la position des éléments d’interface utilisateur lorsque les chaînes qu’ils contiennent changent de longueur.  
  
 Mise en page dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] est dépendante de l’appareil et le plus susceptible d’être statique. En règle générale, [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles sont positionnés de façon absolue sur un formulaire à l’aide de dimensions spécifiées en pixels de matériel. Toutefois, [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] prend en charge certaines fonctionnalités de disposition dynamique, comme décrit dans le tableau suivant.  
  
|Fonctionnalité de mise en page|Description|  
|--------------------|-----------------|  
|Redimensionner automatiquement|Certains [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] redimensionnement des contrôles eux-mêmes pour leur contenu s’affiche correctement. Pour plus d’informations, consultez [vue d’ensemble de la propriété AutoSize](../../winforms/controls/autosize-property-overview.md).|  
|Ancrer|[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles prennent en charge le positionnement et le dimensionnement basé sur le conteneur parent. Pour plus d’informations, consultez <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType> et <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>.|  
|Mise à l’échelle|Contrôles conteneurs redimensionnent elles-mêmes et leurs enfants selon la résolution de l’appareil de sortie ou la taille, en pixels, de la police du conteneur par défaut. Pour plus d’informations, consultez [mise à l’échelle automatique dans les Windows Forms](../../winforms/automatic-scaling-in-windows-forms.md).|  
|Conteneurs de disposition|Le <xref:System.Windows.Forms.FlowLayoutPanel> et <xref:System.Windows.Forms.TableLayoutPanel> contrôles organiser leurs contrôles enfants et se dimensionnent en fonction de leur contenu.|  
  
## <a name="layout-limitations"></a>Limitations de disposition  
 En règle générale, [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles ne peut pas être mis à l’échelle et transformées dans la mesure du possible dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]. La liste suivante décrit les limitations connues lors de la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément tente d’intégrer ses hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] un contrôle dans le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] système de disposition.  
  
-   Dans certains cas, les contrôles [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] ne peuvent pas être redimensionnés, ou peuvent l’être uniquement à des dimensions particulières. Par exemple, un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.ComboBox> contrôle prend en charge la seule hauteur définie par la taille de police du contrôle. Dans un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] disposition dynamique où éléments peuvent être étirés verticalement, hébergé <xref:System.Windows.Forms.ComboBox> contrôle s’étirera pas comme prévu.  
  
-   [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles ne peut pas faire pivoter ou décalées. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> l’élément qui déclenche le <xref:System.Windows.Forms.Integration.WindowsFormsHost.LayoutError> événement si vous appliquez une transformation d’inclinaison ou une rotation. Si vous ne gérez pas la <xref:System.Windows.Forms.Integration.WindowsFormsHost.LayoutError> événement, un <xref:System.InvalidOperationException> est déclenché.  
  
-   Dans la plupart des cas, les contrôles [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] ne prennent pas en charge la mise à l’échelle proportionnelle. Les dimensions globales du contrôle sont mises à l’échelle, mais les contrôles enfants et les composants du contrôle risquent de ne pas être redimensionnés comme prévu. Cette limitation dépend de la prise en charge de la mise à l’échelle de chaque contrôle [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]. En outre, vous ne pouvez pas mettre à l’échelle [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles à une taille de 0 pixels.  
  
-   [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles prennent en charge la mise à l’échelle, dans lequel le formulaire va se redimensionner automatiquement lui-même et ses contrôles selon la taille de police. Dans une interface utilisateur [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], le changement de la taille de police ne redimensionne pas la disposition entière, mais peut entraîner le redimensionnement dynamique des éléments de façon individuelle.  
  
### <a name="z-order"></a>Ordre de plan  
 Dans une interface utilisateur [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], vous pouvez changer l’ordre de plan des éléments pour en contrôler la superposition. Un contrôle [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] hébergé est dessiné dans un HWND séparé. Ainsi, il s’affiche toujours par-dessus les éléments [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].  
  
 Hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] est également dessiné sur toute <xref:System.Windows.Documents.Adorner> éléments.  
  
## <a name="layout-behavior"></a>Comportement de disposition  
 Les sections suivantes décrivent les aspects spécifiques du comportement de disposition lors de l’hébergement [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].  
  
### <a name="scaling-unit-conversion-and-device-independence"></a>Mise à l’échelle, la Conversion d’unité et indépendance de l’appareil  
 Chaque fois que le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément effectue des opérations implique [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] dimensions, les deux systèmes de coordonnées sont impliquées : pixels indépendants du périphérique pour [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et pixels matériels pour [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]. Par conséquent, vous devez appliquer unité appropriée et les conversions de mise à l’échelle pour obtenir une disposition cohérente.  
  
 Conversion entre les systèmes de coordonnées dépend de la résolution actuelle de l’appareil et toute disposition ou rendu les transformations appliquées à la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément ou de ses ancêtres.  
  
 Si le périphérique de sortie est de 96 PPP et aucune mise à l’échelle n’a été appliquée à la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément, un pixel indépendant du périphérique est égal à un pixel de matériel.  
  
 Tous les autres cas nécessitent la mise à l’échelle du système de coordonnées. Le contrôle hébergé n’est pas redimensionné. Au lieu de cela, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément tente de mettre à l’échelle le contrôle hébergé et tous ses contrôles enfants. Étant donné que [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] ne prend pas entièrement en charge mise à l’échelle, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément met à l’échelle pour le degré de prise en charge par les contrôles particuliers.  
  
 Remplacer le <xref:System.Windows.Forms.Integration.WindowsFormsHost.ScaleChild%2A> méthode pour fournir un comportement de mise à l’échelle personnalisé pour le contrôle Windows Forms hébergé.  
  
 En plus de la mise à l’échelle, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément gère des cas d’arrondi et de dépassement de capacité comme décrit dans le tableau suivant.  
  
|Problème de conversion|Description|  
|----------------------|-----------------|  
|Arrondi|[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] dimensions de pixel indépendant du périphérique sont spécifiées en tant que `double`, et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] dimensions en pixels matériels sont spécifiées en tant que `int`. Dans le cas où `double`-en fonction des dimensions sont converties en `int`-en fonction des dimensions, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément utilise l’arrondi standard, afin que les valeurs fractionnaires inférieures à 0,5 sont arrondies à 0.|  
|Dépassement|Lorsque le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément convertit de `double` valeurs `int` valeurs, le dépassement de capacité est possible. Les valeurs supérieures à <xref:System.Int32.MaxValue> sont définies sur <xref:System.Int32.MaxValue>.|  
  
### <a name="layout-related-properties"></a>Propriétés relatives à la disposition  
 Propriétés qui contrôlent le comportement de disposition dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles et [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] éléments sont mappés de manière appropriée par le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément. Pour plus d’informations, consultez [Mappage de propriétés Windows Forms et WPF](windows-forms-and-wpf-property-mapping.md).  
  
### <a name="layout-changes-in-the-hosted-control"></a>Changements de disposition dans le contrôle hébergé  
 Les changements de disposition dans hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle sont propagées à [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pour déclencher des mises à jour de disposition. Le <xref:System.Windows.UIElement.InvalidateMeasure%2A> méthode sur <xref:System.Windows.Forms.Integration.WindowsFormsHost> garantit que les modifications de disposition dans le contrôle hébergé provoquent la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] moteur de disposition à exécuter.  
  
### <a name="continuously-sized-windows-forms-controls"></a>Taille en permanence les contrôles Windows Forms  
 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] les contrôles qui prennent en charge l’évolution continue entièrement interagissent avec le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] système de disposition. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément utilise le <xref:System.Windows.FrameworkElement.MeasureOverride%2A> et <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> méthodes comme d’habitude pour dimensionner et organiser hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.  
  
### <a name="sizing-algorithm"></a>Algorithme de redimensionnement  
 Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément utilise la procédure suivante pour dimensionner le contrôle hébergé :  
  
1.  Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément remplace la <xref:System.Windows.FrameworkElement.MeasureOverride%2A> et <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> méthodes.  
  
2.  Pour déterminer la taille du contrôle hébergé, le <xref:System.Windows.FrameworkElement.MeasureOverride%2A> méthode appelle le contrôle hébergé <xref:System.Windows.Forms.Control.GetPreferredSize%2A> méthode avec une contrainte traduite de la contrainte passée à la <xref:System.Windows.FrameworkElement.MeasureOverride%2A> (méthode).  
  
3.  Le <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> méthode tente de définir le contrôle hébergé à la contrainte de taille donnée.  
  
4.  Si le contrôle hébergé <xref:System.Windows.Forms.Control.Size%2A> propriété correspond à la contrainte spécifiée, le contrôle hébergé est dimensionné à la contrainte.  
  
 Si le <xref:System.Windows.Forms.Control.Size%2A> propriété ne correspond pas à la contrainte spécifiée, le contrôle hébergé ne prend pas en charge le dimensionnement continu. Par exemple, le <xref:System.Windows.Forms.MonthCalendar> contrôle autorise uniquement des tailles discrètes. Les tailles autorisées pour ce contrôle sont des entiers (représentant le nombre de mois) pour la hauteur et la largeur. Dans le cas de ce type, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément se comporte comme suit :  
  
-   Si le <xref:System.Windows.Forms.Control.Size%2A> propriété retourne une taille supérieure à la contrainte spécifiée, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément découpe le contrôle hébergé. Hauteur et la largeur sont gérées séparément, le contrôle hébergé peut être tronqué dans les deux sens.  
  
-   Si le <xref:System.Windows.Forms.Control.Size%2A> propriété retourne une taille inférieure à la contrainte spécifiée, <xref:System.Windows.Forms.Integration.WindowsFormsHost> accepte cette valeur et retourne la valeur à la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] système de disposition.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Procédure pas à pas : organisation des contrôles Windows Forms dans WPF](walkthrough-arranging-windows-forms-controls-in-wpf.md)
- [Organisation des Windows Forms contrôles dans WPF, exemple](https://go.microsoft.com/fwlink/?LinkID=159971)
- [Mappage de propriétés Windows Forms et WPF](windows-forms-and-wpf-property-mapping.md)
- [Migration et interopérabilité](migration-and-interoperability.md)
