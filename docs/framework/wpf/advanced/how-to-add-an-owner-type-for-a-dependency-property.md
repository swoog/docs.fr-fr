---
title: 'Procédure : Ajouter un type propriétaire d’une propriété de dépendance'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- classes [WPF], adding as owners of dependency properties
- dependency properties [WPF], adding classes as owners of
ms.assetid: edcce050-0576-4edb-a31a-3f909637b452
ms.openlocfilehash: 1b1f2b241868b02e430af82bac8e9f6a617e511b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777115"
---
# <a name="how-to-add-an-owner-type-for-a-dependency-property"></a>Procédure : Ajouter un type propriétaire d’une propriété de dépendance
Cet exemple montre comment ajouter une classe en tant que propriétaire d’une propriété de dépendance inscrite pour un type différent. En procédant ainsi, le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] lecteur et système de propriétés sont en mesure de reconnaître la classe en tant que propriétaire de la propriété supplémentaire. Ajout en tant que propriétaire éventuellement permet à la classe d’ajout fournir les métadonnées spécifiques au type.  
  
 Dans l’exemple suivant, `StateProperty` est une propriété inscrite par la `MyStateControl` classe. La classe `UnrelatedStateControl` ajoute lui-même en tant que propriétaire de la `StateProperty` à l’aide de la <xref:System.Windows.DependencyProperty.AddOwner%2A> méthode, en particulier à l’aide de la signature qui permet de nouvelles métadonnées pour la propriété de dépendance telle qu’elle existe sur le type d’ajout. Notez que vous devez fournir [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] accesseurs pour la propriété similaire à l’exemple présenté dans le [implémenter une propriété de dépendance](how-to-implement-a-dependency-property.md) exemple, ainsi que de nouveau exposer l’identificateur de propriété de dépendance sur la classe en cours d’ajout en tant que propriétaire.  
  
 Sans wrappers, la propriété de dépendance continuerait de fonctionner du point de vue de l’accès par programmation à l’aide <xref:System.Windows.DependencyObject.GetValue%2A> ou <xref:System.Windows.DependencyObject.SetValue%2A>. Mais vous souhaiterez généralement parallèlement ce comportement de système de propriétés avec le [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] wrappers de propriété. Les wrappers rendent plus facile de définir la propriété de dépendance par programme et permettent de définir les propriétés comme [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] attributs.  
  
 Pour savoir comment remplacer les métadonnées par défaut, consultez [substituer les métadonnées d’une propriété de dépendance](how-to-override-metadata-for-a-dependency-property.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[PropertySystemEsoterics#MyStateControl](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertySystemEsoterics/CSharp/SDKSampleLibrary/class1.cs#mystatecontrol)]
 [!code-vb[PropertySystemEsoterics#MyStateControl](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertySystemEsoterics/visualbasic/sdksamplelibrary/class1.vb#mystatecontrol)]  
[!code-csharp[PropertySystemEsoterics#UnrelatedStateControl](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertySystemEsoterics/CSharp/SDKSampleLibrary/class1.cs#unrelatedstatecontrol)]
[!code-vb[PropertySystemEsoterics#UnrelatedStateControl](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertySystemEsoterics/visualbasic/sdksamplelibrary/class1.vb#unrelatedstatecontrol)]  
  
## <a name="see-also"></a>Voir aussi

- [Propriétés de dépendance personnalisées](custom-dependency-properties.md)
- [Vue d’ensemble des propriétés de dépendance](dependency-properties-overview.md)
