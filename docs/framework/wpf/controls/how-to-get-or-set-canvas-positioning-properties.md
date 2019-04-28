---
title: 'Procédure : Obtenir ou définir des propriétés de positionnement du canevas'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Canvas control [WPF], setting positioning properties
ms.assetid: 1636b950-2b5a-4507-8a10-c5034cc58b1c
ms.openlocfilehash: 06508e1198736ccb1cbda41641dff4bc634ef82b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910479"
---
# <a name="how-to-get-or-set-canvas-positioning-properties"></a>Procédure : Obtenir ou définir des propriétés de positionnement du canevas
Cet exemple montre comment utiliser les méthodes de positionnement de la <xref:System.Windows.Controls.Canvas> élément pour positionner le contenu enfant. Cet exemple utilise le contenu d’un <xref:System.Windows.Controls.ListBoxItem> pour représenter les valeurs de positionnement et convertit les valeurs en instances de <xref:System.Double>, qui est un argument obligatoire de positionnement. Les valeurs sont converties en chaînes, puis affichées sous forme de texte dans un <xref:System.Windows.Controls.TextBlock> élément à l’aide de la <xref:System.Windows.Controls.Canvas.GetLeft%2A> (méthode).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un <xref:System.Windows.Controls.ListBox> élément qui possède onze sélectionnable <xref:System.Windows.Controls.ListBoxItem> éléments. Le <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> déclencheurs d’événements le `ChangeLeft` méthode personnalisée, qui définit le bloc de code suivant.  
  
 Chaque <xref:System.Windows.Controls.ListBoxItem> représente un <xref:System.Double> valeur, qui est un des arguments qui la <xref:System.Windows.Controls.Canvas.SetLeft%2A> méthode <xref:System.Windows.Controls.Canvas> accepte. Pour pouvoir utiliser un <xref:System.Windows.Controls.ListBoxItem> pour représenter une instance de <xref:System.Double>, vous devez d’abord convertir le <xref:System.Windows.Controls.ListBoxItem> au type de données correct.  
  
 [!code-xaml[CanvasPositioningProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml#1)]  
  
 Lorsqu’un utilisateur modifie le <xref:System.Windows.Controls.ListBox> sélection, elle appelle le `ChangeLeft` méthode personnalisée. Cette méthode passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.LengthConverter> objet, qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Double> (Notez que cette valeur a déjà été convertie en un <xref:System.String> à l’aide de la <xref:System.Windows.Controls.Control.ToString%2A> méthode). Cette valeur est ensuite transmise vers le <xref:System.Windows.Controls.Canvas.SetLeft%2A> et <xref:System.Windows.Controls.Canvas.GetLeft%2A> méthodes de <xref:System.Windows.Controls.Canvas> afin de modifier la position de la `text1` objet.  
  
 [!code-csharp[CanvasPositioningProperties#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml.cs#2)]
 [!code-vb[CanvasPositioningProperties#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasPositioningProperties/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.ListBoxItem>
- <xref:System.Windows.LengthConverter>
- [Vue d’ensemble de Panel](panels-overview.md)
