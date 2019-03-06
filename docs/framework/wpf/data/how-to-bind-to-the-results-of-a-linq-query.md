---
title: "Procédure : Effectuer une liaison avec les résultats d'une requête LINQ"
ms.date: 03/30/2017
helpviewer_keywords:
- running a LINQ query [WPF], bind to results
- binding to LINQ query results [WPF]
ms.assetid: ff2844d9-17ed-4ea6-aab1-5111af0bc684
ms.openlocfilehash: 9be0f95824c97456b50996f9cd6f010442b523f2
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57355946"
---
# <a name="how-to-bind-to-the-results-of-a-linq-query"></a>Procédure : Effectuer une liaison avec les résultats d'une requête LINQ
Cet exemple montre comment exécuter une requête LINQ, puis lier aux résultats.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée deux zones de liste. La première zone de liste contient trois éléments de liste.  
  
 [!code-xaml[LinqExample#UI](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml#ui)]  
  
 Sélectionner un élément dans la zone de liste appelle le Gestionnaire d’événements. Dans cet exemple, `Tasks` est une collection de `Task` objets. Le `Task` classe a une propriété nommée `Priority`. Ce gestionnaire d’événements s’exécute une requête LINQ qui retourne la collection de `Task` les objets qui ont la valeur de priorité sélectionnée, puis la définit comme le <xref:System.Windows.FrameworkElement.DataContext%2A>:  
  
 [!code-csharp[LinqExample#Using](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#using)]  
[!code-csharp[LinqExample#Tasks](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#tasks)]  
[!code-csharp[LinqExample#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#handler)]  
  
 La deuxième zone de liste est lié à cette collection, car son <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> a la valeur `{Binding}`. Par conséquent, il affiche la collection retournée (selon le `myTaskTemplate` <xref:System.Windows.DataTemplate>).  
  
## <a name="see-also"></a>Voir aussi
- [Rendre des données disponibles pour la liaison en XAML](how-to-make-data-available-for-binding-in-xaml.md)
- [Effectuer une liaison à une collection et afficher des informations basées sur la sélection](how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [Nouveautés de WPF version 4.5](../getting-started/whats-new.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
