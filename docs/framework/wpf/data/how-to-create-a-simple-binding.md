---
title: 'Procédure : Créer une liaison simple'
ms.date: 03/30/2017
helpviewer_keywords:
- simple binding [WPF], creating
- data binding [WPF], creating simple bindings
- binding data [WPF], creating
ms.assetid: 69b80f72-6259-44cb-8294-5bdcebca1e08
ms.openlocfilehash: d617c8b97aa679398ed2d061a652f5164f1e499b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931562"
---
# <a name="how-to-create-a-simple-binding"></a>Procédure : Créer une liaison simple
Cet exemple vous montre comment créer un simple <xref:System.Windows.Data.Binding>.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, vous avez un `Person` objet avec une propriété de chaîne nommée `PersonName`. Le `Person` objet est défini dans l’espace de noms appelé `SDKSample`.  
  
 La ligne en surbrillance qui contient le `<src>` élément dans l’exemple suivant instancie le `Person` de l’objet avec un `PersonName` valeur de propriété `Joe`. Cette opération est effectuée le `Resources` section et affecté un `x:Key`.  
  
 [!code-xaml[SimpleBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Page1.xaml?highlight=9,37)]  
  
 La ligne en surbrillance qui contient le `<TextBlock>` élément lie ensuite le <xref:System.Windows.Controls.TextBlock> le contrôle à la `PersonName` propriété. Par conséquent, le <xref:System.Windows.Controls.TextBlock> apparaît avec la valeur « Joe ».  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
