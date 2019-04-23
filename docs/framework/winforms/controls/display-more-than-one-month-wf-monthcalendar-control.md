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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209552"
---
# <a name="how-to-display-more-than-one-month-in-the-windows-forms-monthcalendar-control"></a><span data-ttu-id="b5513-102">Procédure : afficher plusieurs mois dans le contrôle MonthCalendar Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b5513-102">How to: Display More than One Month in the Windows Forms MonthCalendar Control</span></span>
<span data-ttu-id="b5513-103">Les formulaires Windows <xref:System.Windows.Forms.MonthCalendar> contrôle peut afficher jusqu'à 12 mois à la fois.</span><span class="sxs-lookup"><span data-stu-id="b5513-103">The Windows Forms <xref:System.Windows.Forms.MonthCalendar> control can display up to 12 months at a time.</span></span> <span data-ttu-id="b5513-104">Par défaut, le contrôle affiche uniquement un mois, mais vous pouvez spécifier le nombre de mois est affiché et comment ils sont organisés dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b5513-104">By default, the control displays only one month, but you can specify how many months are displayed and how they are arranged within the control.</span></span> <span data-ttu-id="b5513-105">Lorsque vous modifiez la taille du calendrier, le contrôle est redimensionné, veillez donc à que l’espace est suffisant sur le formulaire pour les nouvelles dimensions.</span><span class="sxs-lookup"><span data-stu-id="b5513-105">When you change the calendar dimensions, the control is resized, so be sure there is enough room on the form for the new dimensions.</span></span>  
  
### <a name="to-display-multiple-months"></a><span data-ttu-id="b5513-106">Pour afficher plusieurs mois</span><span class="sxs-lookup"><span data-stu-id="b5513-106">To display multiple months</span></span>  
  
-   <span data-ttu-id="b5513-107">Définir le <xref:System.Windows.Forms.MonthCalendar.CalendarDimensions%2A> propriété au nombre de mois à afficher horizontalement et verticalement.</span><span class="sxs-lookup"><span data-stu-id="b5513-107">Set the <xref:System.Windows.Forms.MonthCalendar.CalendarDimensions%2A> property to the number of months to display horizontally and vertically.</span></span>  
  
    ```vb  
    MonthCalendar1.CalendarDimensions = New System.Drawing.Size (3,2)  
    ```  
  
    ```csharp  
    monthCalendar1.CalendarDimensions = new System.Drawing.Size (3,2);  
    ```  
  
    ```cpp  
    monthCalendar1->CalendarDimensions = System::Drawing::Size (3,2);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b5513-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5513-108">See also</span></span>

- [<span data-ttu-id="b5513-109">MonthCalendar, contrôle</span><span class="sxs-lookup"><span data-stu-id="b5513-109">MonthCalendar Control</span></span>](monthcalendar-control-windows-forms.md)
- [<span data-ttu-id="b5513-110">Guide pratique pour Sélectionnez une plage de Dates dans le contrôle MonthCalendar Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b5513-110">How to: Select a Range of Dates in the Windows Forms MonthCalendar Control</span></span>](how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control.md)
- [<span data-ttu-id="b5513-111">Guide pratique pour Modifier l’apparence du contrôle de MonthCalendar de formulaires Windows</span><span class="sxs-lookup"><span data-stu-id="b5513-111">How to: Change the Windows Forms MonthCalendar Control's Appearance</span></span>](how-to-change-monthcalendar-control-appearance.md)
