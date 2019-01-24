---
title: 'Procédure : Effectuer une liaison à une méthode'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], binding to methods using ObjectDataProvider
- binding [WPF], to methods
- methods [WPF], binding to
ms.assetid: 5f55e71e-2182-42a0-88d1-700cc1427a7a
ms.openlocfilehash: afa7801709d733ed40389f240fa5d92a2557c7a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732074"
---
# <a name="how-to-bind-to-a-method"></a>Procédure : Effectuer une liaison à une méthode
L’exemple suivant montre comment lier une à l’aide de la méthode <xref:System.Windows.Data.ObjectDataProvider>.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, `TemperatureScale` est une classe qui possède une méthode `ConvertTemp`, qui prend deux paramètres (`TempType)`, un de type `double` et l’autre de type `enum`) et convertit la valeur donnée d’une échelle de température à une autre. Dans l’exemple suivant, un <xref:System.Windows.Data.ObjectDataProvider> est utilisé pour instancier le `TemperatureScale` objet. La méthode `ConvertTemp` est appelée avec deux paramètres spécifiés.  
  
 [!code-xaml[BindToMethod#WindowResources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindToMethod/CS/Window1.xaml#windowresources)]  
  
 Maintenant que la méthode est disponible en tant que ressource, vous pouvez effectuer la liaison à ses résultats. Dans l’exemple suivant, le <xref:System.Windows.Controls.TextBox.Text%2A> propriété de la <xref:System.Windows.Controls.TextBox> et <xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A> de la <xref:System.Windows.Controls.ComboBox> sont liés aux deux paramètres de la méthode. Cela permet aux utilisateurs de spécifier la température à convertir et l’échelle de température à partir de laquelle effectuer la conversion. Notez que <xref:System.Windows.Data.Binding.BindsDirectlyToSource%2A> a la valeur `true` , car nous effectuons une liaison à la <xref:System.Windows.Data.ObjectDataProvider.MethodParameters%2A> propriété de la <xref:System.Windows.Data.ObjectDataProvider> instance et non aux propriétés de l’objet encapsulé par le <xref:System.Windows.Data.ObjectDataProvider> (le `TemperatureScale` objet).  
  
 Le <xref:System.Windows.Controls.ContentControl.Content%2A> du dernier <xref:System.Windows.Controls.Label> met à jour lorsque l’utilisateur modifie le contenu de la <xref:System.Windows.Controls.TextBox> ou la sélection de la <xref:System.Windows.Controls.ComboBox>.  
  
 [!code-xaml[BindToMethod#UI](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindToMethod/CS/Window1.xaml#ui)]  
  
 Le convertisseur `DoubleToString` prend une valeur double et la convertit en une chaîne dans le <xref:System.Windows.Data.IValueConverter.Convert%2A> direction (à partir de la source de liaison à la cible de liaison, qui est la <xref:System.Windows.Controls.TextBox.Text%2A> propriété) et convertit un `string` à un `double` dans le <xref:System.Windows.Data.IValueConverter.ConvertBack%2A> direction.  
  
 Le `InvalidationCharacterRule` est un <xref:System.Windows.Controls.ValidationRule> qui vérifie les caractères non valides. Le modèle d’erreur par défaut, qui est une bordure rouge autour de la <xref:System.Windows.Controls.TextBox>, s’affiche pour signaler aux utilisateurs la valeur d’entrée n’est pas une valeur double.  
  
## <a name="see-also"></a>Voir aussi
- [Rubriques de guide pratique](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
- [Effectuer une liaison à une énumération](../../../../docs/framework/wpf/data/how-to-bind-to-an-enumeration.md)
