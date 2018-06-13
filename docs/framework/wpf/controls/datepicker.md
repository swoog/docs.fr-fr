---
title: Sélecteur de dates
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], DatePicker
- DatePicker control [WPF]
ms.assetid: 619765c8-8d25-4315-aec2-79aea08fed9f
ms.openlocfilehash: 910ce09bfad6a46e3d96784b980ee4175c3d26a3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33550063"
---
# <a name="datepicker"></a>Sélecteur de dates
Le <xref:System.Windows.Controls.DatePicker> contrôle permet à l’utilisateur de sélectionner une date en la tapant dans un champ de texte ou à l’aide d’une liste déroulante <xref:System.Windows.Controls.Calendar> contrôle.  
  
 L’illustration suivante montre un <xref:System.Windows.Controls.DatePicker>.  
  
 ![Contrôle DatePicker](../../../../docs/framework/wpf/controls/media/ndp-datepicker.png "NDP_DatePicker")  
Contrôle DatePicker  
  
 Un grand nombre d’un <xref:System.Windows.Controls.DatePicker> sont des propriétés de contrôle pour la gestion de son intégré <xref:System.Windows.Controls.Calendar>et la fonction identique à la propriété équivalente dans <xref:System.Windows.Controls.Calendar>. En particulier, la <xref:System.Windows.Controls.DatePicker.IsTodayHighlighted%2A?displayProperty=nameWithType>, <xref:System.Windows.Controls.DatePicker.FirstDayOfWeek%2A?displayProperty=nameWithType>, <xref:System.Windows.Controls.DatePicker.BlackoutDates%2A?displayProperty=nameWithType>, <xref:System.Windows.Controls.DatePicker.DisplayDateStart%2A?displayProperty=nameWithType>, <xref:System.Windows.Controls.DatePicker.DisplayDateEnd%2A?displayProperty=nameWithType>, <xref:System.Windows.Controls.DatePicker.DisplayDate%2A?displayProperty=nameWithType>, et <xref:System.Windows.Controls.DatePicker.SelectedDate%2A?displayProperty=nameWithType> propriétés fonctionnent de manière identique à leurs <xref:System.Windows.Controls.Calendar> équivalents. Pour plus d'informations, consultez <xref:System.Windows.Controls.Calendar>.  
  
 Les utilisateurs peuvent taper une date directement dans un champ de texte, qui définit le <xref:System.Windows.Controls.DatePicker.Text%2A> propriété. Si le <xref:System.Windows.Controls.DatePicker> Impossible de convertir la chaîne d’entrée à une date valide, la <xref:System.Windows.Controls.DatePicker.DateValidationError> événement sera déclenché. Par défaut, cela provoque une exception, mais un gestionnaire d’événements <xref:System.Windows.Controls.DatePicker.DateValidationError> peut définir le <xref:System.Windows.Controls.DatePickerDateValidationErrorEventArgs.ThrowException%2A> propriété `false` et empêcher la levée d’une exception.  
  
## <a name="see-also"></a>Voir aussi  
 [Contrôles](../../../../docs/framework/wpf/controls/index.md)  
 [Application d’un style et création de modèles](../../../../docs/framework/wpf/controls/styling-and-templating.md)
