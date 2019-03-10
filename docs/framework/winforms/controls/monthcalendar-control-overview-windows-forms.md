---
title: Vue d'ensemble du contrôle MonthCalendar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- MonthCalendar
helpviewer_keywords:
- calendars [Windows Forms], Windows Forms controls
- calendar controls [Windows Forms], Windows Forms
- MonthCalendar control [Windows Forms], setting the first day of the week
ms.assetid: 788c5325-b721-44ec-95bf-9b680ba0f6a2
ms.openlocfilehash: a081c4e6d8210a6bb65fa14b31d12d4295931d53
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718881"
---
# <a name="monthcalendar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle MonthCalendar (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.MonthCalendar> contrôle présente une interface graphique intuitive permettant aux utilisateurs d’afficher et définir les informations de date. Le contrôle affiche un calendrier : une grille contenant les jours du mois, répartis dans des colonnes sous les jours de la semaine, avec la plage de dates en surbrillance sélectionnée numérotés. Vous pouvez sélectionner un autre mois en cliquant sur les boutons de direction de chaque côté de la légende du mois. Contrairement à la similaire <xref:System.Windows.Forms.DateTimePicker> contrôle, vous pouvez sélectionner plusieurs dates avec ce contrôle. Pour plus d’informations sur la <xref:System.Windows.Forms.DateTimePicker> du contrôle, consultez [contrôle DateTimePicker](datetimepicker-control-windows-forms.md).  
  
## <a name="configuring-the-monthcalendar-control"></a>Configuration du contrôle MonthCalendar  
 Le <xref:System.Windows.Forms.MonthCalendar> apparence du contrôle est hautement configurable. Par défaut, la date du jour s’affiche, comme indiqué par un cercle et est également indiquée au bas de la grille. Vous pouvez modifier cette fonctionnalité en définissant le <xref:System.Windows.Forms.MonthCalendar.ShowToday%2A> et <xref:System.Windows.Forms.MonthCalendar.ShowTodayCircle%2A> propriétés à `false`. Vous pouvez également ajouter des numéros de semaine au calendrier en définissant le <xref:System.Windows.Forms.MonthCalendar.ShowWeekNumbers%2A> propriété `true`. En définissant le <xref:System.Windows.Forms.MonthCalendar.CalendarDimensions%2A> propriété, vous pouvez afficher plusieurs mois horizontalement et verticalement. Par défaut, dimanche est le premier jour de la semaine, mais n’importe quel jour peut être désigné à l’aide de la <xref:System.Windows.Forms.MonthCalendar.FirstDayOfWeek%2A> propriété.  
  
 Vous pouvez également définir certaines dates à afficher en gras de manière ponctuelle, annuelle ou mensuelle, en ajoutant <xref:System.DateTime> des objets sur le <xref:System.Windows.Forms.MonthCalendar.BoldedDates%2A>, <xref:System.Windows.Forms.MonthCalendar.AnnuallyBoldedDates%2A>, et <xref:System.Windows.Forms.MonthCalendar.MonthlyBoldedDates%2A> propriétés. Pour plus d'informations, voir [Procédure : Afficher en gras certains jours avec les Windows Forms du contrôle MonthCalendar](display-specific-days-in-bold-with-wf-monthcalendar-control.md).  
  
 La propriété de clé de la <xref:System.Windows.Forms.MonthCalendar> contrôle est <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A>, la plage de dates sélectionnées dans le contrôle. Le <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A> valeur ne peut pas dépasser le nombre maximal de jours pouvant être sélectionnés, défini le <xref:System.Windows.Forms.MonthCalendar.MaxSelectionCount%2A> propriété. Les dates de premier et derniers que l’utilisateur peut sélectionner sont déterminées par la <xref:System.Windows.Forms.MonthCalendar.MaxDate%2A> et <xref:System.Windows.Forms.MonthCalendar.MinDate%2A> propriétés.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.MonthCalendar>
- [MonthCalendar, contrôle](monthcalendar-control-windows-forms.md)
