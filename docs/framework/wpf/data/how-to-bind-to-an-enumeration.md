---
title: 'Procédure : Effectuer une liaison à une énumération'
ms.date: 03/30/2017
helpviewer_keywords:
- binding data [WPF], enumeration
- data binding [WPF], enumeration
- enumeration [WPF]
ms.assetid: b9091eba-1119-424e-868b-d1a4168b3732
ms.openlocfilehash: df26d2bd08e4691837f739a4e71d3bb1a25bdd00
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57377792"
---
# <a name="how-to-bind-to-an-enumeration"></a>Procédure : Effectuer une liaison à une énumération
Cet exemple montre comment effectuer une liaison à une énumération en le liant à une méthode de GetValues de l’énumération.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, le <xref:System.Windows.Controls.ListBox> affiche la liste des <xref:System.Windows.HorizontalAlignment> des valeurs d’énumération via la liaison de données. Le <xref:System.Windows.Controls.ListBox> et le <xref:System.Windows.Controls.Button> sont liés de telle sorte que vous pouvez modifier le <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> valeur de propriété de la <xref:System.Windows.Controls.Button> en sélectionnant une valeur dans la <xref:System.Windows.Controls.ListBox>.  
  
 [!code-xaml[BindToEnum#BindToEnum](~/samples/snippets/csharp/VS_Snippets_Wpf/BindToEnum/CS/Window1.xaml#bindtoenum)]  
  
## <a name="see-also"></a>Voir aussi
- [Effectuer une liaison à une méthode](how-to-bind-to-a-method.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
