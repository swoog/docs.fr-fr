---
title: 'Procédure : afficher plusieurs mois dans le contrôle MonthCalendar Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- calendars [Windows Forms], formatting display
- examples [Windows Forms], calendar controls
- calendars [Windows Forms], multiple months
- MonthCalendar control [Windows Forms], formatting display
ms.assetid: d197caa2-38a5-4cb4-acc3-562130c2ace3
ms.openlocfilehash: 79100b52d8e0a5b651edb9d6555a4497287ed858
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59209552"
---
# <a name="how-to-display-more-than-one-month-in-the-windows-forms-monthcalendar-control"></a>Procédure : afficher plusieurs mois dans le contrôle MonthCalendar Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.MonthCalendar> contrôle peut afficher jusqu'à 12 mois à la fois. Par défaut, le contrôle affiche uniquement un mois, mais vous pouvez spécifier le nombre de mois est affiché et comment ils sont organisés dans le contrôle. Lorsque vous modifiez la taille du calendrier, le contrôle est redimensionné, veillez donc à que l’espace est suffisant sur le formulaire pour les nouvelles dimensions.  
  
### <a name="to-display-multiple-months"></a>Pour afficher plusieurs mois  
  
-   Définir le <xref:System.Windows.Forms.MonthCalendar.CalendarDimensions%2A> propriété au nombre de mois à afficher horizontalement et verticalement.  
  
    ```vb  
    MonthCalendar1.CalendarDimensions = New System.Drawing.Size (3,2)  
    ```  
  
    ```csharp  
    monthCalendar1.CalendarDimensions = new System.Drawing.Size (3,2);  
    ```  
  
    ```cpp  
    monthCalendar1->CalendarDimensions = System::Drawing::Size (3,2);  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [MonthCalendar, contrôle](monthcalendar-control-windows-forms.md)
- [Procédure : sélectionner une plage de dates dans le contrôle MonthCalendar Windows Forms](how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control.md)
- [Procédure : modifier l’aspect du contrôle MonthCalendar Windows Forms](how-to-change-monthcalendar-control-appearance.md)
