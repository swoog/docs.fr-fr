---
title: Notification de modifications dans la liaison de données Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, data binding
- Windows Forms, adding change notification for data binding
ms.assetid: b5b10f90-0585-41d9-a377-409835262a92
ms.openlocfilehash: b4a70f96ad256b22ce0d933a633475161160e5a4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665860"
---
# <a name="change-notification-in-windows-forms-data-binding"></a>Notification de modifications dans la liaison de données Windows Forms
Un des concepts plus importants de la liaison de données Windows Forms est *notification de modification*. Pour vous assurer que votre source de données et les contrôles liés ont toujours des données les plus récentes, vous devez ajouter la notification de modification pour la liaison de données. Plus précisément, vous souhaitez vous assurer que les contrôles dépendants sont avertis des modifications qui ont été apportées à leur source de données, et la source de données est avertie des modifications qui ont été apportées aux propriétés d’un contrôle liées.  
  
 Il existe différents types de notification de modifications, en fonction du type de liaison de données :  
  
- Liaison simple dans lequel une seule propriété de contrôle est liée à une seule instance d’un objet.  
  
- Liaison de liste, qui peut inclure une propriété de contrôle unique liée à la propriété d’un élément dans une liste ou une propriété du contrôle lié à une liste d’objets.  
  
 En outre, si vous créez des contrôles Windows Forms que vous souhaitez utiliser pour la liaison de données, vous devez appliquer le *PropertyName*modifié le modèle pour les contrôles, afin que les modifications apportées à la propriété liée d’un contrôle sont propagées à la source de données.  
  
## <a name="change-notification-for-simple-binding"></a>Notification de modification pour la liaison Simple  
 Pour la liaison simple, les objets métier doivent fournir des notification de modification lorsque la valeur d’une propriété liée change. Vous pouvez le faire en exposant un *PropertyName*événement Changed pour chaque propriété de votre objet métier et la liaison de l’objet métier aux contrôles avec le <xref:System.Windows.Forms.BindingSource> ou la méthode par défaut dans lequel votre objet métier implémente le <xref:System.ComponentModel.INotifyPropertyChanged> interface et déclenche une <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> événement lorsque la valeur d’une propriété change. Pour plus d'informations, voir [Procédure : Implémenter l’Interface INotifyPropertyChanged](how-to-implement-the-inotifypropertychanged-interface.md). Lorsque vous utilisez des objets qui implémentent le <xref:System.ComponentModel.INotifyPropertyChanged> interface, il est inutile d’utiliser le <xref:System.Windows.Forms.BindingSource> pour lier l’objet à un contrôle, mais l’utilisation du <xref:System.Windows.Forms.BindingSource> est recommandé.  
  
## <a name="change-notification-for-list-based-binding"></a>Notification de modification pour la liaison de liste  
 Windows Forms dépend d’une liste liée pour fournir la modification de propriété (une valeur de propriété d’élément liste change) et à une liste (un élément est supprimé ou ajouté à la liste) informations aux contrôles dépendants. Par conséquent, les listes utilisées pour la liaison de données doivent implémenter le <xref:System.ComponentModel.IBindingList>, qui fournit les deux types de notification de modification. Le <xref:System.ComponentModel.BindingList%601> est une implémentation générique de <xref:System.ComponentModel.IBindingList> et est conçu pour une utilisation avec la liaison de données Windows Forms. Vous pouvez créer un <xref:System.ComponentModel.BindingList%601> qui contient un type d’objet métier qui implémente <xref:System.ComponentModel.INotifyPropertyChanged> et convertit automatiquement la liste le <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> événements <xref:System.ComponentModel.IBindingList.ListChanged> événements. Si la liste liée n’est pas un <xref:System.ComponentModel.IBindingList>, vous devez lier la liste d’objets aux contrôles Windows Forms à l’aide de la <xref:System.Windows.Forms.BindingSource> composant. Le <xref:System.Windows.Forms.BindingSource> composant fournit une conversion de propriété à la liste similaire à celle de la <xref:System.ComponentModel.BindingList%601>. Pour plus d'informations, voir [Procédure : Générer des Notifications de modification à l’aide d’un BindingSource et l’Interface INotifyPropertyChanged](./controls/raise-change-notifications--bindingsource.md).  
  
## <a name="change-notification-for-custom-controls"></a>Notification de modification pour les contrôles personnalisés  
 Enfin, du côté du contrôle, vous devez exposer un *PropertyName*événement Changed pour chaque propriété conçue pour être lié aux données. Les modifications apportées à la propriété du contrôle sont ensuite propagées à la source de données. Pour plus d'informations, voir [Procédure : Appliquer le modèle PropertyNameChanged](how-to-apply-the-propertynamechanged-pattern.md)  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.BindingSource>
- <xref:System.ComponentModel.INotifyPropertyChanged>
- <xref:System.ComponentModel.BindingList%601>
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
- [Sources de données prises en charge par les Windows Forms](data-sources-supported-by-windows-forms.md)
- [Liaison de données et Windows Forms](data-binding-and-windows-forms.md)
