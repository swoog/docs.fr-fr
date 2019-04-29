---
title: 'Procédure : Créer une liaison dans du code'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- binding data [WPF], creating
- data binding [WPF], creating
ms.assetid: 1a606db9-cf5f-42ed-a1c5-9e4722ec77a0
ms.openlocfilehash: 57ec845c5c9a5bddb801428b9ecde035a97cf447
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931623"
---
# <a name="how-to-create-a-binding-in-code"></a>Procédure : Créer une liaison dans du code
Cet exemple montre comment créer et définir un <xref:System.Windows.Data.Binding> dans le code.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.FrameworkElement> classe et le <xref:System.Windows.FrameworkContentElement> exposent toutes deux un `SetBinding` (méthode). Si vous liez un élément qui hérite de ces classes, vous pouvez appeler la <xref:System.Windows.FrameworkElement.SetBinding%2A> directement la méthode.  
  
 L’exemple suivant crée une classe nommée, `MyData`, qui contient une propriété nommée `MyDataProperty`.  
  
 [!code-csharp[CodeOnlyBinding#DataObject](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/MyData.cs#dataobject)]
 [!code-vb[CodeOnlyBinding#DataObject](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/MyData.vb#dataobject)]  
  
 L’exemple suivant montre comment créer un objet de liaison pour définir la source de la liaison.  L’exemple utilise <xref:System.Windows.FrameworkElement.SetBinding%2A> pour lier le <xref:System.Windows.Controls.TextBlock.Text%2A> propriété du `myText`, qui est un <xref:System.Windows.Controls.TextBlock> contrôler, à `MyDataProperty`.  
  
 [!code-csharp[CodeOnlyBinding#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#1)]
 [!code-vb[CodeOnlyBinding#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#1)]  
  
 Pour l’exemple de code complet, consultez [uniquement par le Code de liaison, exemple](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms771500(v=vs.90)).  
  
 Au lieu d’appeler <xref:System.Windows.FrameworkElement.SetBinding%2A>, vous pouvez utiliser la <xref:System.Windows.Data.BindingOperations.SetBinding%2A> méthode statique de la <xref:System.Windows.Data.BindingOperations> classe. L’exemple suivant, les appels <xref:System.Windows.Data.BindingOperations.SetBinding%2A?displayProperty=nameWithType> au lieu de <xref:System.Windows.FrameworkElement.SetBinding%2A?displayProperty=nameWithType> pour lier `myText` à `myDataProperty`.  
  
 [!code-csharp[CodeOnlyBinding#BOSetBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#bosetbinding)]
 [!code-vb[CodeOnlyBinding#BOSetBinding](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#bosetbinding)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
