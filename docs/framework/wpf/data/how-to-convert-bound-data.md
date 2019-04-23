---
title: 'Procédure : Convertir des données liées'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- converting [WPF], bound data
- data binding [WPF], converting bound data
- binding data [WPF], converting bound data
ms.assetid: b00aaa19-c6df-4c3b-a9fd-88a0b488df2b
ms.openlocfilehash: 40699bec1c6cd775f7f8495b7a49eda15fb2ed83
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59093798"
---
# <a name="how-to-convert-bound-data"></a>Procédure : Convertir des données liées
Cet exemple montre comment appliquer la conversion de données qui sont utilisées dans les liaisons.  
  
 Pour convertir des données pendant la liaison, vous devez créer une classe qui implémente le <xref:System.Windows.Data.IValueConverter> interface, ce qui inclut le <xref:System.Windows.Data.IValueConverter.Convert%2A> et <xref:System.Windows.Data.IValueConverter.ConvertBack%2A> méthodes.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre l’implémentation d’un convertisseur de date qui convertit la valeur de date passée pour qu’il affiche uniquement l’année, mois et jour. Lorsque vous implémentez le <xref:System.Windows.Data.IValueConverter> interface, il est conseillé pour décorer l’implémentation avec un <xref:System.Windows.Data.ValueConversionAttribute> attribut pour indiquer au développement des outils les types de données impliqués dans la conversion, comme dans l’exemple suivant :  
  
 [!code-csharp[DataBindingLab#18](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DateConverter.cs#18)]
 [!code-vb[DataBindingLab#18](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/DateConverter.vb#18)]  
  
 Une fois que vous avez créé un convertisseur, vous pouvez l’ajouter en tant que ressource dans votre [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier. Dans l’exemple suivant, *src* est mappé à l’espace de noms dans lequel *convertisseur de date* est défini.  
  
 [!code-xaml[DataBindingLab#15](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#15)]  
  
 Enfin, vous pouvez utiliser le convertisseur dans votre liaison à l’aide de la syntaxe suivante. Dans l’exemple suivant, le contenu textuel de la <xref:System.Windows.Controls.TextBlock> est lié à *StartDate*, qui est une propriété de source de données externe.  
  
 [!code-xaml[DataBindingLab#17](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#17)]  
  
 Les ressources de style référencées dans l’exemple ci-dessus sont définies dans une section de ressources ne pas présentée dans cette rubrique.  
  
## <a name="see-also"></a>Voir aussi

- [Implémenter la validation de la liaison](how-to-implement-binding-validation.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
