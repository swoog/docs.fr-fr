---
title: 'Optimisation des performances : Liaison de données'
ms.date: 03/30/2017
helpviewer_keywords:
- binding data [WPF], performance
- data binding [WPF], performance
ms.assetid: 1506a35d-c009-43db-9f1e-4e230ad5be73
ms.openlocfilehash: ac7ca815bedf180c8a680840f585d08f7018d6ab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59087831"
---
# <a name="optimizing-performance-data-binding"></a>Optimisation des performances : Liaison de données
La liaison de données [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] offre un moyen simple et cohérent pour les applications de présenter les données et d’interagir avec elles. Les éléments peuvent être liés à des données émanant de diverses sources de données sous la forme d’objets [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] et de [!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)].  
  
 Cette rubrique fournit des recommandations sur les performances de la liaison de données.  

<a name="HowDataBindingReferencesAreResolved"></a>   
## <a name="how-data-binding-references-are-resolved"></a>Comment les références de liaison de données sont résolues  
 Avant d’aborder les problèmes de performances de la liaison de données, il est utile d’explorer la façon dont le moteur de liaison de données [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] résout les références d’objet pour la liaison.  
  
 La source d’une liaison de données [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] peut être n’importe quel objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)]. Vous pouvez créer une liaison avec les propriétés, sous-propriétés ou indexeurs d’un objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)]. Les références de liaison sont résolues en utilisant soit la réflexion de Microsoft .NET Framework ou un <xref:System.ComponentModel.ICustomTypeDescriptor>. Voici trois méthodes permettant de résoudre les références d’objet pour la liaison.  
  
 La première méthode repose sur l’utilisation de la réflexion. Dans ce cas, le <xref:System.Reflection.PropertyInfo> objet est utilisé pour découvrir les attributs de la propriété et fournit l’accès aux métadonnées de propriété. Lorsque vous utilisez le <xref:System.ComponentModel.ICustomTypeDescriptor> interface, le moteur de liaison de données utilise cette interface pour accéder aux valeurs de propriété. Le <xref:System.ComponentModel.ICustomTypeDescriptor> interface est particulièrement utile dans les cas où l’objet n’a pas un ensemble statique de propriétés.  
  
 Notifications de modification de propriété peuvent être fournies en implémentant la <xref:System.ComponentModel.INotifyPropertyChanged> interface ou en utilisant les notifications de modification associées à la <xref:System.ComponentModel.TypeDescriptor>. Toutefois, la stratégie privilégiée pour implémenter les notifications de modification de propriété consiste à utiliser <xref:System.ComponentModel.INotifyPropertyChanged>.  
  
 Si l’objet source est un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] objet et la propriété source est un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] propriété, le [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] moteur de liaison de données doit tout d’abord utiliser la réflexion sur l’objet source pour obtenir le <xref:System.ComponentModel.TypeDescriptor>, puis interrogez un <xref:System.ComponentModel.PropertyDescriptor>. Cette séquence d’opérations de réflexion peut s’avérer très fastidieuse du point de vue des performances.  
  
 La deuxième méthode pour résoudre les références d’objet implique un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] objet source qui implémente le <xref:System.ComponentModel.INotifyPropertyChanged> interface et une propriété source qui est un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] propriété. Dans ce cas, le moteur de liaison de données applique la réflexion directement au type de source et obtient la propriété nécessaire. Ce n’est toujours pas la méthode optimale, mais elle est moins exigeante que la première méthode en termes de spécifications de la plage de travail.  
  
 La troisième méthode pour résoudre les références d’objet implique un objet source qui est un <xref:System.Windows.DependencyObject> et une propriété source qui est un <xref:System.Windows.DependencyProperty>. Dans ce cas, le moteur de liaison de données n’a pas besoin d’utiliser la réflexion. Au lieu de cela, le moteur de propriété et le moteur de liaison de données résolvent ensemble la référence de propriété de manière indépendante. Il s’agit de la méthode optimale pour résoudre les références d’objet utilisées pour la liaison de données.  
  
 Le tableau ci-dessous compare la vitesse de liaison de données la <xref:System.Windows.Controls.TextBlock.Text%2A> propriété d’un millier <xref:System.Windows.Controls.TextBlock> éléments à l’aide de ces trois méthodes.  
  
|**Liaison de la propriété Text d’un TextBlox**|**Temps de liaison (ms)**|**Temps de rendu -- liaison incluse (ms)**|  
|--------------------------------------------------|-----------------------------|--------------------------------------------------|  
|À une propriété d’un objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)]|115|314|  
|Pour une propriété d’un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] objet qui implémente <xref:System.ComponentModel.INotifyPropertyChanged>|115|305|  
|Pour un <xref:System.Windows.DependencyProperty> d’un <xref:System.Windows.DependencyObject>.|90|263|  
  
<a name="Binding_to_Large_CLR_Objects"></a>   
## <a name="binding-to-large-clr-objects"></a>Liaison à des objets CLR volumineux  
 Le fait de lier des données à un même objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] possédant plusieurs milliers de propriétés a un impact important sur les performances. Vous pouvez limiter cet impact en divisant l’objet en plusieurs objets [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] englobant moins de propriétés. Le tableau indique les temps de liaison et de rendu dans les cas d’une liaison de données à un même objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] volumineux et à plusieurs objets plus petits.  
  
|**Liaison de données de 1 000 objets TextBlock**|**Temps de liaison (ms)**|**Temps de rendu -- liaison incluse (ms)**|  
|---------------------------------------------|-----------------------------|--------------------------------------------------|  
|À un objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] doté de 1 000 propriétés|950|1200|  
|À 1 000 objets [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] dotés d’une propriété|115|314|  
  
<a name="Binding_to_an_ItemsSource"></a>   
## <a name="binding-to-an-itemssource"></a>Liaison à un ItemsSource  
 Imaginez un scénario dans lequel vous avez un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] <xref:System.Collections.Generic.List%601> objet qui contient une liste d’employés que vous souhaitez afficher dans un <xref:System.Windows.Controls.ListBox>. Pour créer une correspondance entre ces deux objets, vous devez lier votre liste d’employés à la <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox>. Or, il se trouve qu’un nouvel employé rejoint le groupe. Vous pouvez penser que pour insérer cette nouvelle personne dans votre limite <xref:System.Windows.Controls.ListBox> valeurs, vous simplement ajouter cette personne à votre liste d’employés et attendre que cette modification soit reconnue automatiquement par le moteur de liaison de données. Cette hypothèse est fausse ; en réalité, la modification est répercutée dans le <xref:System.Windows.Controls.ListBox> automatiquement. Il s’agit, car le [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] <xref:System.Collections.Generic.List%601> objet ne déclenche pas automatiquement une collection d’événement modifié. Afin d’obtenir le <xref:System.Windows.Controls.ListBox> pour récupérer les modifications, vous seriez obligé de recréer votre liste d’employés et la joindre à nouveau à la <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox>. Bien que cette solution fonctionne, elle a un fort impact sur les performances. Chaque fois vous réaffectez le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> de <xref:System.Windows.Controls.ListBox> vers un nouvel objet, le <xref:System.Windows.Controls.ListBox> tout d’abord lève immédiatement ses éléments précédents et regénère sa liste entière. L’impact sur les performances est amplifié si votre <xref:System.Windows.Controls.ListBox> est mappé à un type complexe <xref:System.Windows.DataTemplate>.  
  
 Une solution très efficace à ce problème consiste à rendre votre liste d’employés une <xref:System.Collections.ObjectModel.ObservableCollection%601>. Un <xref:System.Collections.ObjectModel.ObservableCollection%601> objet déclenche une notification de modification que le moteur de liaison de données peut recevoir. L’événement ajoute ou supprime un élément d’un <xref:System.Windows.Controls.ItemsControl> sans avoir à regénérer la liste entière.  
  
 Le tableau ci-dessous montre le temps nécessaire pour mettre à jour le <xref:System.Windows.Controls.ListBox> (avec la virtualisation de l’interface utilisateur désactivée) lorsqu’un élément est ajouté. Le nombre figurant dans la première ligne représente le temps écoulé lors de la [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] <xref:System.Collections.Generic.List%601> objet est lié à <xref:System.Windows.Controls.ListBox> l’élément <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>. Le nombre figurant dans la deuxième ligne représente le temps écoulé quand un <xref:System.Collections.ObjectModel.ObservableCollection%601> est lié à la <xref:System.Windows.Controls.ListBox> l’élément <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>. Notez que les économies de beaucoup de temps à l’aide du <xref:System.Collections.ObjectModel.ObservableCollection%601> stratégie de liaison de données.  
  
|**Liaison de données de la propriété ItemsSource**|**Temps de mise à jour pour 1 élément (ms)**|  
|--------------------------------------|---------------------------------------|  
|Pour un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] <xref:System.Collections.Generic.List%601> objet|1 656|  
|Pour un <xref:System.Collections.ObjectModel.ObservableCollection%601>|20|  
  
<a name="Binding_IList_to_ItemsControl_not_IEnumerable"></a>   
## <a name="bind-ilist-to-itemscontrol-not-ienumerable"></a>Lier un objet IList à un objet ItemsControl non IEnumerable  
 Si vous avez le choix entre lier un <xref:System.Collections.Generic.IList%601> ou un <xref:System.Collections.IEnumerable> à un <xref:System.Windows.Controls.ItemsControl> d’objet, choisissez la <xref:System.Collections.Generic.IList%601> objet. Liaison <xref:System.Collections.IEnumerable> à un <xref:System.Windows.Controls.ItemsControl> force [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pour créer un wrapper <xref:System.Collections.Generic.IList%601> objet, ce qui signifie que vos performances sont affectées par une surcharge inutile d’un deuxième objet.  
  
<a name="Do_not_Convert_CLR_objects_to_Xml_Just_For_Data_Binding"></a>   
## <a name="do-not-convert-clr-objects-to-xml-just-for-data-binding"></a>Ne convertissez pas des objets CLR en XML seulement à des fins de liaison de données.  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] vous autorise à lier des données à du contenu [!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)] ; or, lier des données à du contenu [!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)] s’avère plus lent que de lier des données à des objets [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)]. Ne convertissez pas des données d’objet [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] en XML si l’unique but est la liaison de données.  
  
## <a name="see-also"></a>Voir aussi

- [Optimisation des performances des applications WPF](optimizing-wpf-application-performance.md)
- [Planification des performances des applications](planning-for-application-performance.md)
- [Tirer parti du matériel](optimizing-performance-taking-advantage-of-hardware.md)
- [Disposition et conception](optimizing-performance-layout-and-design.md)
- [Graphiques 2D et acquisition d'images](optimizing-performance-2d-graphics-and-imaging.md)
- [Comportement de l’objet](optimizing-performance-object-behavior.md)
- [Ressources d'application](optimizing-performance-application-resources.md)
- [Text](optimizing-performance-text.md)
- [Autres recommandations relatives aux performances](optimizing-performance-other-recommendations.md)
- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Procédure pas à pas : La mise en cache des données d’Application dans une Application WPF](walkthrough-caching-application-data-in-a-wpf-application.md)
