---
title: 'Procédure : implémenter l’interface INotifyPropertyChanged'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- INotifyPropertyChanged interface [Windows Forms], implementing
ms.assetid: eac428af-b43b-46ac-80d9-1a5f88658725
ms.openlocfilehash: cfdfb22fd854a8f630243e0f612761c71cb778d8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59225597"
---
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a>Procédure : implémenter l’interface INotifyPropertyChanged
L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.INotifyPropertyChanged> interface. Implémentez cette interface sur les objets métier qui sont utilisés dans la liaison de données Windows Forms. En cas d’implémentation, l’interface communique à un contrôle dépendant les modifications des propriétés sur un objet métier.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : appliquer le modèle PropertyNameChanged](how-to-apply-the-propertynamechanged-pattern.md)
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
- [Procédure : générer des notifications de modification à l’aide de BindingSource et de l’interface INotifyPropertyChanged](./controls/raise-change-notifications--bindingsource.md)
- [Notification de modifications dans la liaison de données Windows Forms](change-notification-in-windows-forms-data-binding.md)
