---
title: Sécurité de propriété de dépendance
ms.date: 03/30/2017
helpviewer_keywords:
- wrappers [WPF], access
- wrappers [WPF], security
- dependency properties [WPF], security
- security [WPF], wrappers
- validation [WPF], dependency properties
- dependency properties [WPF], access
- security [WPF], dependency properties
ms.assetid: d10150ec-90c5-4571-8d35-84bafa2429a4
ms.openlocfilehash: 85806ee9fb01cd2ca07697230c46a8847fdf8c6a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59077470"
---
# <a name="dependency-property-security"></a>Sécurité de propriété de dépendance
Les propriétés de dépendance doivent généralement être considérées comme des propriétés publiques. La nature du système de propriétés [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] empêche de pouvoir garantir la sécurité d’une valeur de propriété de dépendance.  

<a name="AccessSecurity"></a>   
## <a name="access-and-security-of-wrappers-and-dependency-properties"></a>Accès et sécurité des wrappers et des propriétés de dépendance  
 En règle générale, les propriétés de dépendance sont implémentées avec des propriétés [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] « wrappers » qui simplifient l’obtention ou la définition de la propriété à partir d’une instance. Mais les wrappers sont des méthodes pratiques simplement qui implémentent sous-jacent <xref:System.Windows.DependencyObject.GetValue%2A> et <xref:System.Windows.DependencyObject.SetValue%2A> les appels statiques qui sont utilisés lors de l’interaction avec les propriétés de dépendance. Pris d’un autre point de vue, les propriétés sont exposées en tant que propriétés [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] stockées par une propriété de dépendance plutôt que par un champ privé. Les mécanismes de sécurité appliqués aux wrappers ne sont pas identiques au comportement du système de propriétés et au niveau d’accès de la propriété de dépendance sous-jacente. Placer une demande de sécurité sur le wrapper empêchera seulement l’utilisation de la méthode pratique mais n’empêchera pas les appels à <xref:System.Windows.DependencyObject.GetValue%2A> ou <xref:System.Windows.DependencyObject.SetValue%2A>. De même, placer un niveau d’accès privé ou protégé sur les wrappers ne procure pas une sécurité efficace.  
  
 Si vous écrivez vos propres propriétés de dépendance, vous devez déclarer les wrappers et le <xref:System.Windows.DependencyProperty> identificateur de champ en tant que membres publics, afin que les appelants ne pas obtenir des informations trompeuses sur le niveau d’accès réel de cette propriété (en raison de son magasin en cours implémenté comme une propriété de dépendance).  
  
 Pour une propriété de dépendance personnalisée, vous pouvez inscrire votre propriété comme propriété de dépendance en lecture seule, et cela constitue un moyen efficace d’empêcher une propriété qui est définie par une personne qui ne possède pas une référence à la <xref:System.Windows.DependencyPropertyKey> pour cette propriété. Pour plus d’informations, consultez [Propriétés de dépendance en lecture seule](read-only-dependency-properties.md).  
  
> [!NOTE]
>  Déclarer un <xref:System.Windows.DependencyProperty> identificateur champ privé n’est pas interdit et il peut parfaitement être utilisé pour aider à réduire l’espace de noms immédiatement exposé d’une classe personnalisée, mais une telle propriété ne doit pas être considérée « private » dans le même sens en tant que le [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] définitions linguistiques définissent ce niveau d’accès, pour les raisons décrites dans la section suivante.  
  
<a name="PropertySystemExposure"></a>   
## <a name="property-system-exposure-of-dependency-properties"></a>Exposition des propriétés de dépendance par le système de propriétés  
 Il est généralement pas utile, et il est potentiellement trompeur, de déclarer un <xref:System.Windows.DependencyProperty> niveau d’accès autre que public. Ce paramètre de niveau d’accès empêche seulement une personne d’obtenir une référence à l’instance à partir de la classe de déclaration. Mais il existe plusieurs aspects du système de propriétés qui retournera un <xref:System.Windows.DependencyProperty> comme moyen d’identifier une propriété particulière telle qu’elle existe sur une instance d’une classe ou une instance de la classe dérivée, et cet identificateur est toujours utilisable dans un <xref:System.Windows.DependencyObject.SetValue%2A> appeler même Si l’identificateur statique d’origine est déclaré comme non public. En outre, <xref:System.Windows.DependencyObject.OnPropertyChanged%2A> méthodes virtuelles recevoir des informations de toute propriété de dépendance existante qui a changé de valeur. En outre, le <xref:System.Windows.DependencyObject.GetLocalValueEnumerator%2A> méthode retourne des identificateurs pour toute propriété sur des instances avec définie localement valeur.  
  
### <a name="validation-and-security"></a>Validation et sécurité  
 Appliquer une demande à un <xref:System.Windows.DependencyProperty.ValidateValueCallback%2A> et attend l’échec de validation sur l’échec d’une demande pour empêcher une propriété d’être définie n’est pas un mécanisme de sécurité adéquat. Invalidation de la valeur définie appliquée via <xref:System.Windows.DependencyProperty.ValidateValueCallback%2A> pourrait également être supprimée par des appelants malveillants, si ces derniers opèrent dans le domaine d’application.  
  
## <a name="see-also"></a>Voir aussi

- [Propriétés de dépendance personnalisées](custom-dependency-properties.md)
