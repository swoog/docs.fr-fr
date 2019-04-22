---
title: Calendrier
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Calendar
- Calendar control [WPF]
ms.assetid: ee844e4a-eefe-48e2-bd0d-1d82cc5e960b
ms.openlocfilehash: 9a64c6cd6fc1cc53383f2617f7a7a78959e87c4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59124785"
---
# <a name="calendar"></a>Calendrier
Un calendrier permet à un utilisateur de sélectionner une date en affichant un calendrier visuel.  
  
 Un <xref:System.Windows.Controls.Calendar> contrôle peut être utilisé seul, ou dans le cadre de la liste déroulante d’un <xref:System.Windows.Controls.DatePicker> contrôle. Pour plus d'informations, consultez <xref:System.Windows.Controls.DatePicker>.  
  
 L’illustration suivante montre deux <xref:System.Windows.Controls.Calendar> des contrôles, un avec des sélections et des dates d’arrêt complet et l’autre sans.  
  
 ![Les contrôles de calendrier](./media/ndp-calendarcontrols.png "NDP_CalendarControls")  
Contrôles Calendar  
  
 Le tableau suivant fournit des informations sur les tâches qui sont généralement associés à la <xref:System.Windows.Controls.Calendar>.  
  
|Tâche|Implémentation|  
|----------|--------------------|  
|Spécifier des dates qui ne peuvent pas être sélectionnés.|Utilisez la propriété <xref:System.Windows.Controls.Calendar.BlackoutDates%2A>.|  
|Avoir le <xref:System.Windows.Controls.Calendar> afficher un mois, une année entière ou une décennie.|Définir le <xref:System.Windows.Controls.Calendar.DisplayMode%2A> mois, année ou décennie à la propriété.|  
|Spécifiez si l’utilisateur peut sélectionner une date, une plage de dates ou plusieurs plages de dates.|Utilisez le <xref:System.Windows.Controls.Calendar.SelectionMode%2A>.|  
|Spécifiez la plage de dates qui le <xref:System.Windows.Controls.Calendar> affiche.|Utilisez le <xref:System.Windows.Controls.Calendar.DisplayDateStart%2A> et <xref:System.Windows.Controls.Calendar.DisplayDateEnd%2A> propriétés.|  
|Spécifiez si la date actuelle est mise en surbrillance.|Utilisez la propriété <xref:System.Windows.Controls.Calendar.IsTodayHighlighted%2A>. Par défaut, <xref:System.Windows.Controls.Calendar.IsTodayHighlighted%2A> est `true`.|  
|Modifier la taille de la <xref:System.Windows.Controls.Calendar>.|Utilisez un <xref:System.Windows.Controls.Viewbox> ou définir le <xref:System.Windows.FrameworkElement.LayoutTransform%2A> propriété à un <xref:System.Windows.Media.ScaleTransform>. Notez que si vous définissez la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés d’un <xref:System.Windows.Controls.Calendar>, le calendrier réel ne change pas sa taille.|  
  
 Le <xref:System.Windows.Controls.Calendar> contrôle fournit une navigation de base à l’aide de la souris ou le clavier. Le tableau suivant résume la navigation au clavier.  
  
|Combinaison de touches|<xref:System.Windows.Controls.Calendar.DisplayMode%2A>|Action|  
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|  
|FLÈCHE|<xref:System.Windows.Controls.CalendarMode.Month>|Modifications du <xref:System.Windows.Controls.Calendar.SelectedDate%2A> propriété si le <xref:System.Windows.Controls.Calendar.SelectionMode%2A> propriété n’est pas définie sur <xref:System.Windows.Controls.CalendarSelectionMode.None>.|  
|FLÈCHE|<xref:System.Windows.Controls.CalendarMode.Year>|Modifie le mois de la <xref:System.Windows.Controls.Calendar.DisplayDate%2A> propriété. Notez que le <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ne change pas.|  
|FLÈCHE|<xref:System.Windows.Controls.CalendarMode.Decade>|Modifier l’année de la <xref:System.Windows.Controls.Calendar.DisplayDate%2A>. Notez que le <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ne change pas.|  
|MAJ + TOUCHE DE DIRECTION|<xref:System.Windows.Controls.CalendarMode.Month>|Si <xref:System.Windows.Controls.Calendar.SelectionMode%2A> n’a pas la valeur <xref:System.Windows.Controls.CalendarSelectionMode.SingleDate> ou <xref:System.Windows.Controls.CalendarSelectionMode.None>, étend la plage de dates sélectionnées.|  
|ORIGINE|<xref:System.Windows.Controls.CalendarMode.Month>|Modifications du <xref:System.Windows.Controls.Calendar.SelectedDate%2A> au premier jour du mois en cours.|  
|ORIGINE|<xref:System.Windows.Controls.CalendarMode.Year>|Modifie le mois de la <xref:System.Windows.Controls.Calendar.DisplayDate%2A> au premier mois de l’année. Le <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ne change pas.|  
|ORIGINE|<xref:System.Windows.Controls.CalendarMode.Decade>|Modifier l’année de la <xref:System.Windows.Controls.Calendar.DisplayDate%2A> pour la première année de la décennie. Le <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ne change pas.|  
|FIN|<xref:System.Windows.Controls.CalendarMode.Month>|Modifications du <xref:System.Windows.Controls.Calendar.SelectedDate%2A> au dernier jour du mois en cours.|  
|FIN|<xref:System.Windows.Controls.CalendarMode.Year>|Modifie le mois de la <xref:System.Windows.Controls.Calendar.DisplayDate%2A> au mois de l’année dernière. Le <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ne change pas.|  
|FIN|<xref:System.Windows.Controls.CalendarMode.Decade>|Modifier l’année de la <xref:System.Windows.Controls.Calendar.DisplayDate%2A> à la dernière année de la décennie. Le <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ne change pas.|  
|CTRL+HAUT|Any|Bascule vers la prochaine plus grande <xref:System.Windows.Controls.Calendar.DisplayMode%2A>. Si <xref:System.Windows.Controls.Calendar.DisplayMode%2A> est déjà <xref:System.Windows.Controls.CalendarMode.Decade>, aucune action.|  
|CTRL+BAS|Any|Bascule vers la prochaine plus petits <xref:System.Windows.Controls.Calendar.DisplayMode%2A>. Si <xref:System.Windows.Controls.Calendar.DisplayMode%2A> est déjà <xref:System.Windows.Controls.CalendarMode.Month>, aucune action.|  
|ESPACE ou entrée|<xref:System.Windows.Controls.CalendarMode.Year> ou <xref:System.Windows.Controls.CalendarMode.Decade>|Commutateurs <xref:System.Windows.Controls.Calendar.DisplayMode%2A> à la <xref:System.Windows.Controls.CalendarMode.Month> ou <xref:System.Windows.Controls.CalendarMode.Year> représenté par l’élément ayant le focus.|  
  
## <a name="see-also"></a>Voir aussi

- [Contrôles](index.md)
- [Application d’un style et création de modèles](styling-and-templating.md)
