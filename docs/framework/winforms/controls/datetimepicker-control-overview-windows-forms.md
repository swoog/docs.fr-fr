---
title: Vue d'ensemble du contrôle DateTimePicker (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- DateTimePicker
helpviewer_keywords:
- DateTimePicker control [Windows Forms], about
- date and time picker controls
ms.assetid: 501af106-e9fc-4efc-b9b3-c9d8dcaf8c5c
ms.openlocfilehash: 451172b51427e4932470c53737c7bc276920271c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173591"
---
# <a name="datetimepicker-control-overview-windows-forms"></a>Vue d'ensemble du contrôle DateTimePicker (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.DateTimePicker> contrôle permet à l’utilisateur de sélectionner un élément unique dans une liste de dates ou heures. Lorsqu’il est utilisé pour représenter une date, il apparaît dans les deux parties : une liste déroulante, avec une date sous forme de texte et une grille qui s’affiche lorsque vous cliquez sur la flèche vers le bas en regard de la liste. La grille se présente comme la <xref:System.Windows.Forms.MonthCalendar> contrôle, qui peut être utilisé pour sélectionner plusieurs dates. Pour plus d’informations sur la <xref:System.Windows.Forms.MonthCalendar> du contrôle, consultez [vue d’ensemble du contrôle MonthCalendar](monthcalendar-control-overview-windows-forms.md).  
  
## <a name="key-properties"></a>Propriétés de clé  
 Si vous le souhaitez la <xref:System.Windows.Forms.DateTimePicker> apparaisse comme un contrôle permettant de choisir ou modifier des heures au lieu de dates, définissez la <xref:System.Windows.Forms.DateTimePicker.ShowUpDown%2A> propriété `true` et le <xref:System.Windows.Forms.DateTimePicker.Format%2A> propriété <xref:System.Windows.Forms.DateTimePickerFormat.Time>. Pour plus d'informations, consultez [Guide pratique pour Afficher l’heure avec le contrôle DateTimePicker](how-to-display-time-with-the-datetimepicker-control.md).  
  
 Lorsque le <xref:System.Windows.Forms.DateTimePicker.ShowCheckBox%2A> propriété est définie sur `true`, une case à cocher s’affiche en regard de la date sélectionnée dans le contrôle. Quand la case à cocher est activée, la valeur de date-heure sélectionnée peut être mis à jour. Lorsque la case à cocher est vide, la valeur apparaît comme indisponible.  
  
 Le contrôle <xref:System.Windows.Forms.DateTimePicker.MaxDate%2A> et <xref:System.Windows.Forms.DateTimePicker.MinDate%2A> propriétés déterminent la plage de dates et heures. Le <xref:System.Windows.Forms.DateTimePicker.Value%2A> propriété contient la date et heure actuelles du contrôle est défini sur. Pour plus d’informations, consultez [Guide pratique pour Définir et retourner des Dates avec les Windows Forms du contrôle DateTimePicker](how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md). Les valeurs peuvent être affichées dans les quatre formats qui sont définis par le <xref:System.Windows.Forms.DateTimePicker.Format%2A> propriété : <xref:System.Windows.Forms.DateTimePickerFormat.Long>, <xref:System.Windows.Forms.DateTimePickerFormat.Short>, <xref:System.Windows.Forms.DateTimePickerFormat.Time>, ou <xref:System.Windows.Forms.DateTimePickerFormat.Custom>. Si un format personnalisé est sélectionné, vous devez définir le <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> propriété à une chaîne appropriée. Pour plus d’informations, consultez [Guide pratique pour Afficher une Date dans un Format personnalisé à l’aide du contrôle DateTimePicker Windows Forms](display-a-date-in-a-custom-format-with-wf-datetimepicker-control.md).  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : afficher une date dans un format personnalisé avec le contrôle DateTimePicker Windows Forms](display-a-date-in-a-custom-format-with-wf-datetimepicker-control.md)
- [Procédure : définir et retourner des dates avec le contrôle DateTimePicker Windows Forms](how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)
