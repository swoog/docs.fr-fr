---
title: 'Procédure : Définir et référencer une ressource'
ms.date: 03/30/2017
helpviewer_keywords:
- resources [WPF], defining
- defining resources [WPF]
- resources [WPF], referencing
- referencing resources [WPF]
ms.assetid: b86b876b-0a10-489b-9a5d-581ea9b32406
ms.openlocfilehash: 39cde252ce98e55f155edfb7a4c2268219d6858e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692871"
---
# <a name="how-to-define-and-reference-a-resource"></a>Procédure : Définir et référencer une ressource
Cet exemple montre comment définir une ressource et de faire référence à l’aide d’un attribut dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit deux types de ressources : un <xref:System.Windows.Media.SolidColorBrush> de ressources et plusieurs <xref:System.Windows.Style> ressources. Le <xref:System.Windows.Media.SolidColorBrush> ressource `MyBrush` est utilisé pour fournir la valeur de plusieurs propriétés qui prennent chacune un <xref:System.Windows.Media.Brush> type valeur. Le <xref:System.Windows.Style> ressources `PageBackground`, `TitleText` et `Label` chacun cibler un type de contrôle particulier. Les styles de définissent diverses propriétés différentes sur les contrôles ciblés lorsque cette ressource de style est référencée par la clé de ressource et est utilisée pour définir le <xref:System.Windows.FrameworkElement.Style%2A> propriété de plusieurs éléments de contrôle spécifiques définis dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].  
  
 Notez que l’une des propriétés des accesseurs Set de la `Label` style fait également référence le `MyBrush` ressource définie précédemment. Il s’agit d’une technique courante, mais il est important de se rappeler que les ressources sont analysées et entrés dans un dictionnaire de ressources dans l’ordre où elles sont fournies. Ressources sont également demandées dans l’ordre qui se trouvent dans le dictionnaire si vous utilisez le [Extension de balisage StaticResource](../../../../docs/framework/wpf/advanced/staticresource-markup-extension.md) pour les référencer à partir d’une autre ressource. Assurez-vous que n’importe quelle ressource que vous référencez est défini précédemment dans la collection de ressources dans lequel cette ressource est demandée. Si nécessaire, vous pouvez contourner l’ordre strict de création des références de ressources à l’aide un [Extension de balisage DynamicResource](../../../../docs/framework/wpf/advanced/dynamicresource-markup-extension.md) pour référencer la ressource lors de l’exécution au lieu de cela, mais vous devez être conscient que cette DynamicResource technique a des conséquences sur les performances. Pour plus d’informations, consultez [XAML ressources](../../../../docs/framework/wpf/advanced/xaml-resources.md).  
  
 [!code-xaml[FEResource#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEResource/CS/default.xaml#xaml)]  
  
## <a name="see-also"></a>Voir aussi
- [Ressources XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md)
- [Application d’un style et création de modèles](../../../../docs/framework/wpf/controls/styling-and-templating.md)
