---
title: Fonctionnalités de langage XAML 2009
ms.date: 03/30/2017
helpviewer_keywords:
- XAML 2009 [XAML Services]
- XAML [XAML Services], XAML 2009
ms.assetid: f6bb18d8-c86a-4549-8862-323e6b32a8dd
ms.openlocfilehash: 05f811cd0d95f7605963dae851430fb6bf0e9f7a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162278"
---
# <a name="xaml-2009-language-features"></a>Fonctionnalités de langage XAML 2009
XAML 2009 est l'abréviation désignant les nouvelles fonctionnalités du langage XAML qui étendent la spécification du langage XAML existante. XAML 2009 introduit plusieurs nouvelles directives et constructions. Ceux-ci incluent le [x : Arguments Directive](x-arguments-directive.md); le [x : FactoryMethod Directive](x-factorymethod-directive.md); le [x : Reference Markup Extension](x-reference-markup-extension.md); le [x : TypeArguments, Directive ](x-typearguments-directive.md); et les types intégrés pour les primitives de langage courantes (par exemple `x:Char`).  
  
<a name="xaml_2009_support_in_wpf_and_visual_studio"></a>   
## <a name="xaml-2009-support-in-wpf-and-visual-studio"></a>Prise en charge de XAML 2009 dans WPF et Visual Studio  
 Dans WPF, vous pouvez utiliser les fonctionnalités XAML 2009, mais uniquement pour le code XAML qui n'est pas compilé par balisage WPF. Le code XAML compilé par balisage et la forme BAML du code XAML ne prennent actuellement pas en charge les mots clés de langage et fonctionnalités XAML 2009.  
  
 Notez que les techniques existantes de chargement du code XAML libre dans WPF peuvent également avoir des restrictions de sécurité et d'accès aux types CLR et au système de type qui sont plus restrictives que pour le code XAML compilé par balisage. Pour plus d'informations, consultez [Sécurité (WPF)](../wpf/security-wpf.md) ou [Stratégie de sécurité de WPF - ingénierie de la plateforme](../wpf/wpf-security-strategy-platform-security.md).  
  
 XAML 2009 introduit également des fonctionnalités supplémentaires qui modifient les constructions XAML 2006 précédentes ou les formes de balisage de base.  
  
### <a name="xkey-as-an-object-element"></a>x:Key en tant qu'élément objet  
 XAML 2009 peut prendre en charge `x:Key` en tant qu'objet (élément de propriété qui a une valeur d'élément objet) ; toutefois, XAML 2006 prenait uniquement en charge `x:Key` en tant qu'attribut. Consultez la section « XAML 2009 » de la rubrique [x:Key Directive](x-key-directive.md).  
  
### <a name="xmlns-on-property-elements"></a>xmlns sur les éléments de propriété  
 XAML 2009 peut prendre en charge les définitions d'espace de noms (xmlns) XAML sur les éléments de propriété ; toutefois, XAML 2006 prend uniquement en charge les définitions xmlns sur les éléments objet.  
  
### <a name="event-attributes"></a>Attributs d'événement  
 Pour les attributs qui sont soutenus par des événements, XAML 2006 suppose que la compilation du balisage est impliquée et soumet les événements à la compilation du balisage. XAML 2009 prend en charge une forme de balisage ressemblant à une extension de balisage, ce qui diffère la connexion d'événements jusqu'au moment de l'analyse à l'exécution et du chargement du code XAML. Toutefois, les applications WPF et les scénarios XAML pour l'interface utilisateur WPF n'utilisent généralement pas cette fonction. WPF et son implémentation de XAML 2006 utilisent la combinaison de la connexion du gestionnaire d'événements pour les événements routés définis au niveau d' <xref:System.Windows.UIElement> et de l'étape de son compilateur de balisage pour une grande partie du traitement de ses attributs d'événement. Le compilateur de balisage prétraite également les attributs d'événement se trouvant dans le code XAML où les actions de génération déclarent que le compilateur de balisage est utilisé.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du langage XAML (WPF)](../wpf/advanced/xaml-overview-wpf.md)
