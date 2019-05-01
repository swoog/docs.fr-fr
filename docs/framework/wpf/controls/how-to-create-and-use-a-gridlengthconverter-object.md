---
title: 'Procédure : Créer et utiliser un objet GridLengthConverter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], creating [WPF], GridLengthConverter objects
ms.assetid: 5ab75911-e36a-4825-80e4-081c57e8e182
ms.openlocfilehash: 498d2b9c531f391f4cbeb1478469a99d381deec7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62050985"
---
# <a name="how-to-create-and-use-a-gridlengthconverter-object"></a>Procédure : Créer et utiliser un objet GridLengthConverter
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer et utiliser une instance de <xref:System.Windows.GridLengthConverter>. L’exemple définit une méthode personnalisée nommée `changeCol`, qui passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.GridLengthConverter> qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Windows.GridLength>. La valeur convertie est ensuite passée comme valeur de la <xref:System.Windows.Controls.ColumnDefinition.Width%2A> propriété de la <xref:System.Windows.Controls.ColumnDefinition> élément.  
  
 L’exemple définit également une deuxième méthode personnalisée, appelée `changeColVal`. Cette méthode personnalisée convertit le <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> d’un <xref:System.Windows.Controls.Slider> à un <xref:System.String> puis passe cette valeur à la <xref:System.Windows.Controls.ColumnDefinition> en tant que le <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de l’élément.  
  
 Notez que distinct [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier définit le contenu d’un <xref:System.Windows.Controls.ListBoxItem>.  
  
 [!code-csharp[gridlengthConverterGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/gridlengthConverterGrid/CSharp/Window1.xaml.cs#1)]
 [!code-vb[gridlengthConverterGrid#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridlengthConverterGrid/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.GridLengthConverter>
- <xref:System.Windows.GridLength>
