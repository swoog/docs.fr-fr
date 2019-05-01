---
title: 'Procédure : Lier les propriétés de deux contrôles'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], binding properties of two controls
- binding properties of two controls [WPF]
- controls [WPF], binding properties of
ms.assetid: 06318fac-6afd-4c7d-a277-6d7ef50f47bc
ms.openlocfilehash: 332e8e0dfa30ff7aff27c95652f07446baf6511a
ms.sourcegitcommit: 89fcad7e816c12eb1299128481183f01c73f2c07
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "63809524"
---
# <a name="how-to-bind-the-properties-of-two-controls"></a>Procédure : Lier les propriétés de deux contrôles
Cet exemple montre comment lier la propriété d’un contrôle instancié à celle d’un autre en utilisant le <xref:System.Windows.Data.Binding.ElementName%2A> propriété.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment lier le <xref:System.Windows.Controls.Panel.Background%2A> propriété d’un <xref:System.Windows.Controls.Canvas> à la <xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>.<xref:System.Windows.Controls.ContentControl.Content%2A> propriété d’un <xref:System.Windows.Controls.ComboBox>:  
  
 [!code-xaml[BindDptoDp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/BindDPtoDP/CS/Window1.xaml#1)]  
  
 Lors de l’affichage, on obtient un résultat similaire à ce qui suit :  
  
![Capture d’écran montrant une liste déroulante case avec la valeur verte et un carré vert.](./media/how-to-bind-the-properties-of-two-controls/data-binding-bind-background-canvas.png)

> [!NOTE]
> La propriété de cible de liaison (dans cet exemple, le <xref:System.Windows.Controls.Panel.Background%2A> propriété) doit être une propriété de dépendance. Pour plus d’informations, consultez [Vue d’ensemble de la liaison de données](data-binding-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- [Spécifier la source de liaison](how-to-specify-the-binding-source.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
