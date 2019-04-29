---
title: 'Procédure : Implémenter la notification des modifications de propriétés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- notifications of change [WPF]
- data binding [WPF], property change notifications
- change notifications [WPF]
- properties [WPF], change notifications
ms.assetid: 30b59d9e-8c3a-4349-aa82-4be837e841cf
ms.openlocfilehash: d37d468acc94470be8c2afdc495b40168932ec83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931441"
---
# <a name="how-to-implement-property-change-notification"></a>Procédure : Implémenter la notification des modifications de propriétés
Pour prendre en charge <xref:System.Windows.Data.BindingMode.OneWay> ou <xref:System.Windows.Data.BindingMode.TwoWay> de liaison pour activer les propriétés de votre cible de liaison afin de refléter automatiquement les modifications dynamiques de la source de liaison (par exemple, pour que le volet de visualisation mis à jour automatiquement lorsque l’utilisateur modifie un formulaire), votre classe doit fournir les notifications de modification de propriété appropriées. Cet exemple montre comment créer une classe qui implémente <xref:System.ComponentModel.INotifyPropertyChanged>.  
  
## <a name="example"></a>Exemple  
 Pour implémenter <xref:System.ComponentModel.INotifyPropertyChanged> vous devez déclarer le <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> événement et créer le `OnPropertyChanged` (méthode). Pour chaque propriété pour laquelle vous souhaitez modifier les notifications, vous devez ensuite appeler `OnPropertyChanged` chaque fois que la propriété est mise à jour.  
  
 [!code-csharp[SimpleBinding#PersonClass](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Person.cs#personclass)]
 [!code-vb[SimpleBinding#PersonClass](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleBinding/VisualBasic/Person.vb#personclass)]  
  
 Pour voir un exemple montrant comment les `Person` classe peut être utilisée pour prendre en charge <xref:System.Windows.Data.BindingMode.TwoWay> liaison, consultez [contrôler quand le texte TextBox met à jour la Source](how-to-control-when-the-textbox-text-updates-the-source.md).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble des sources de liaison](binding-sources-overview.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
