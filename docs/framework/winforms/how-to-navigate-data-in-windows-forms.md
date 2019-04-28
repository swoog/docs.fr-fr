---
title: 'Procédure : parcourir les données dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cursors [Windows Forms], data sources
- data sources [Windows Forms], Windows Forms
- Windows Forms, navigating
- CurrencyManager class [Windows Forms], navigating Windows Forms data
- data [Windows Forms], navigating
ms.assetid: 97360f7b-b181-4084-966a-4c62518f735b
ms.openlocfilehash: 2ba33f9ecb3a12a62c41af17d3f9ad6f6e3f8a5d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61801710"
---
# <a name="how-to-navigate-data-in-windows-forms"></a>Procédure : parcourir les données dans Windows Forms
Dans une application Windows, pour parcourir les enregistrements dans une source de données le plus simple consiste à lier un <xref:System.Windows.Forms.BindingSource> composant à la source de données, puis lier les contrôles à le <xref:System.Windows.Forms.BindingSource>. Vous pouvez ensuite utiliser la méthode de navigation intégrée sur le <xref:System.Windows.Forms.BindingSource> tel un <xref:System.Windows.Forms.BindingSource.MoveNext%2A>, <xref:System.Windows.Forms.BindingSource.MoveLast%2A>, <xref:System.Windows.Forms.BindingSource.MovePrevious%2A> et <xref:System.Windows.Forms.BindingSource.MoveFirst%2A>. À l’aide de ces méthodes ajustera la <xref:System.Windows.Forms.BindingSource.Position%2A> et <xref:System.Windows.Forms.BindingSource.Current%2A> propriétés de la <xref:System.Windows.Forms.BindingSource> en conséquence. Vous pouvez également rechercher un élément et définissez-le comme l’élément actuel en définissant le <xref:System.Windows.Forms.BindingSource.Position%2A> propriété.  
  
### <a name="to-increment-the-position-in-a-data-source"></a>Pour incrémenter la position dans une source de données  
  
1. Définir le <xref:System.Windows.Forms.BindingSource.Position%2A> propriété de la <xref:System.Windows.Forms.BindingSource> de vos données liées à la position de l’enregistrement à atteindre. L’exemple suivant illustre l’utilisation de la <xref:System.Windows.Forms.BindingSource.MoveNext%2A> méthode de la <xref:System.Windows.Forms.BindingSource> pour incrémenter le <xref:System.Windows.Forms.BindingSource.Position%2A> propriété lorsque la `nextButton` un clic sur. Le <xref:System.Windows.Forms.BindingSource> est associé le `Customers` table d’un dataset `Northwind`.  
  
    > [!NOTE]
    >  Définition de la <xref:System.Windows.Forms.BindingSource.Position%2A> propriété avec une valeur au-delà du premier ou dernier enregistrement n’entraîne pas une erreur, comme le [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] vous autorisera pas à définir la position sur une valeur en dehors des limites de la liste. S’il est important dans votre application pour savoir si vous avez dépassé le premier ou dernier enregistrement, inclure une logique pour déterminer si vous dépassez le nombre d’éléments de données.  
  
     [!code-csharp[System.Windows.Forms.NavigatingData#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.NavigatingData/CS/Form1.cs#4)]
     [!code-vb[System.Windows.Forms.NavigatingData#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.NavigatingData/VB/Form1.vb#4)]  
  
### <a name="to-check-whether-you-have-passed-the-end-or-beginning"></a>Pour vérifier si vous avez dépassé la fin ou au début  
  
1. Créez un gestionnaire d'événements pour l'événement <xref:System.Windows.Forms.BindingSource.PositionChanged>. Dans le gestionnaire, vous pouvez tester si la valeur de position proposée a dépassé le nombre d’éléments de données réelles.  
  
     L’exemple suivant illustre comment vous pouvez tester si vous avez atteint le dernier élément de données. Dans l’exemple, si vous êtes sur le dernier élément, le **suivant** bouton sur le formulaire est désactivé.  
  
    > [!NOTE]
    >  N’oubliez pas que, vous modifiez la liste que vous naviguez dans le code, vous devrez réactiver la **suivant** bouton, afin que les utilisateurs puissent parcourir toute la durée de la nouvelle liste. En outre, n’oubliez pas que la méthode ci-dessus <xref:System.Windows.Forms.BindingSource.PositionChanged> événement spécifique <xref:System.Windows.Forms.BindingSource> vous travaillez doit être associé à sa méthode de gestion des événements. Voici un exemple d’une méthode pour la gestion de la <xref:System.Windows.Forms.BindingSource.PositionChanged> événement :  
  
     [!code-csharp[System.Windows.Forms.NavigatingData#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.NavigatingData/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.NavigatingData#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.NavigatingData/VB/Form1.vb#3)]  
  
### <a name="to-find-an-item-and-set-it-as-the-current-item"></a>Pour rechercher un élément et le définir comme élément actuel  
  
1. Recherchez l’enregistrement que vous souhaitez définir comme élément actuel. Vous pouvez le faire à l’aide de la <xref:System.Windows.Forms.BindingSource.Find%2A> méthode de la <xref:System.Windows.Forms.BindingSource>, si votre source de données implémente <xref:System.ComponentModel.IBindingList>. Quelques exemples de données sources qui implémentent <xref:System.ComponentModel.IBindingList> sont <xref:System.ComponentModel.BindingList%601> et <xref:System.Data.DataView>.  
  
     [!code-csharp[System.Windows.Forms.NavigatingData#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.NavigatingData/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.NavigatingData#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.NavigatingData/VB/Form1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Sources de données prises en charge par les Windows Forms](data-sources-supported-by-windows-forms.md)
- [Notification de modifications dans la liaison de données Windows Forms](change-notification-in-windows-forms-data-binding.md)
- [Liaison de données et Windows Forms](data-binding-and-windows-forms.md)
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
