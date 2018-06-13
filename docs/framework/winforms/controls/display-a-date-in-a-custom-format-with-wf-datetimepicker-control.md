---
title: "Comment : afficher une date dans un format personnalisé à l'aide du contrôle DateTimePicker Windows Forms"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DateTimePicker control [Windows Forms], display styles
- examples [Windows Forms], DateTimePicker control
- dates [Windows Forms], displaying in DateTimePicker control
ms.assetid: 39767691-2d2b-46b6-a663-b7901e581a6e
ms.openlocfilehash: 2f563b5de9b80dab2af00290e8a6b3b309410a9e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33526007"
---
# <a name="how-to-display-a-date-in-a-custom-format-with-the-windows-forms-datetimepicker-control"></a><span data-ttu-id="ca682-102">Comment : afficher une date dans un format personnalisé à l'aide du contrôle DateTimePicker Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca682-102">How to: Display a Date in a Custom Format with the Windows Forms DateTimePicker Control</span></span>
<span data-ttu-id="ca682-103">Windows Forms <xref:System.Windows.Forms.DateTimePicker> contrôle offre une grande souplesse dans la mise en forme l’affichage des dates et heures dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ca682-103">The Windows Forms <xref:System.Windows.Forms.DateTimePicker> control gives you flexibility in formatting the display of dates and times in the control.</span></span> <span data-ttu-id="ca682-104">Le <xref:System.Windows.Forms.DateTimePicker.Format%2A> propriété vous permet de sélectionner à partir des formats prédéfinis répertoriés dans le <xref:System.Windows.Forms.DateTimePickerFormat>.</span><span class="sxs-lookup"><span data-stu-id="ca682-104">The <xref:System.Windows.Forms.DateTimePicker.Format%2A> property allows you to select from predefined formats, listed in the <xref:System.Windows.Forms.DateTimePickerFormat>.</span></span> <span data-ttu-id="ca682-105">Si aucun de ces éléments est adaptée à vos besoins, vous pouvez créer votre propre style de format à l’aide de caractères de format répertoriés dans <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A>.</span><span class="sxs-lookup"><span data-stu-id="ca682-105">If none of these is adequate for your purposes, you can create your own format style using format characters listed in <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A>.</span></span>  
  
### <a name="to-display-a-custom-format"></a><span data-ttu-id="ca682-106">Pour afficher un format personnalisé</span><span class="sxs-lookup"><span data-stu-id="ca682-106">To display a custom format</span></span>  
  
1.  <span data-ttu-id="ca682-107">Affectez à la propriété <xref:System.Windows.Forms.DateTimePicker.Format%2A> la valeur `DateTimePickerFormat.Custom`.</span><span class="sxs-lookup"><span data-stu-id="ca682-107">Set the <xref:System.Windows.Forms.DateTimePicker.Format%2A> property to `DateTimePickerFormat.Custom`.</span></span>  
  
2.  <span data-ttu-id="ca682-108">Définir le <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> propriété à une chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="ca682-108">Set the <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> property to a format string.</span></span>  
  
    ```vb  
    DateTimePicker1.Format = DateTimePickerFormat.Custom  
    ' Display the date as "Mon 27 Feb 2012".  
    DateTimePicker1.CustomFormat = "ddd dd MMM yyyy"  
    ```  
  
    ```csharp  
    dateTimePicker1.Format = DateTimePickerFormat.Custom;  
    // Display the date as "Mon 27 Feb 2012".  
    dateTimePicker1.CustomFormat = "ddd dd MMM yyyy";  
    ```  
  
    ```cpp  
    dateTimePicker1->Format = DateTimePickerFormat::Custom;  
    // Display the date as "Mon 27 Feb 2012".  
    dateTimePicker1->CustomFormat = "ddd dd MMM yyyy";  
    ```  
  
### <a name="to-add-text-to-the-formatted-value"></a><span data-ttu-id="ca682-109">Pour ajouter du texte à la valeur mise en forme</span><span class="sxs-lookup"><span data-stu-id="ca682-109">To add text to the formatted value</span></span>  
  
1.  <span data-ttu-id="ca682-110">Utilisez des guillemets simples pour encadrer tout caractère qui n’est pas un caractère de format comme « M » ou un délimiteur comme « : ».</span><span class="sxs-lookup"><span data-stu-id="ca682-110">Use single quotation marks to enclose any character that is not a format character like "M" or a delimiter like ":".</span></span> <span data-ttu-id="ca682-111">Par exemple, la chaîne de format ci-dessous affiche la date actuelle au format « aujourd'hui est : 05:30:31 vendredi 02 mars 2012 » dans l’anglais (États-Unis) de culture.</span><span class="sxs-lookup"><span data-stu-id="ca682-111">For example, the format string below displays the current date with the format "Today is: 05:30:31 Friday March 02, 2012" in the English (United States) culture.</span></span>  
  
    ```vb  
    DateTimePicker1.CustomFormat = "'Today is:' hh:mm:ss dddd MMMM dd, yyyy"  
    ```  
  
    ```csharp  
    dateTimePicker1.CustomFormat = "'Today is:' hh:mm:ss dddd MMMM dd, yyyy";  
    ```  
  
    ```cpp  
    dateTimePicker1->CustomFormat =  
       "'Today is:' hh:mm:ss dddd MMMM dd, yyyy";  
    ```  
  
     <span data-ttu-id="ca682-112">Selon le paramètre de culture, les caractères ne pas entourés de guillemets simples peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="ca682-112">Depending on the culture setting, any characters not enclosed in single quotation marks may be changed.</span></span> <span data-ttu-id="ca682-113">Par exemple, la chaîne de format ci-dessus affiche la date actuelle au format « aujourd'hui est : 05:30:31 vendredi 02 mars 2012 » dans l’anglais (États-Unis) de culture.</span><span class="sxs-lookup"><span data-stu-id="ca682-113">For example, the format string above displays the current date with the format "Today is: 05:30:31 Friday March 02, 2012" in the English (United States) culture.</span></span> <span data-ttu-id="ca682-114">Notez que le premier signe deux-points est placée entre guillemets simples, car elle n’est pas destinée à être un caractère de délimitation comme dans « hh : mm : ».</span><span class="sxs-lookup"><span data-stu-id="ca682-114">Note that the first colon is enclosed in single quotation marks, because it is not intended to be a delimiting character as it is in "hh:mm:ss".</span></span> <span data-ttu-id="ca682-115">Dans une autre culture, le format peut apparaître en tant que « aujourd'hui est : 05.30.31 vendredi 02 mars 2012 ».</span><span class="sxs-lookup"><span data-stu-id="ca682-115">In another culture, the format might appear as "Today is: 05.30.31 Friday March 02, 2012".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca682-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca682-116">See Also</span></span>  
 [<span data-ttu-id="ca682-117">DateTimePicker, contrôle</span><span class="sxs-lookup"><span data-stu-id="ca682-117">DateTimePicker Control</span></span>](../../../../docs/framework/winforms/controls/datetimepicker-control-windows-forms.md)  
 [<span data-ttu-id="ca682-118">Guide pratique pour définir et retourner des dates à l'aide du contrôle DateTimePicker Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca682-118">How to: Set and Return Dates with the Windows Forms DateTimePicker Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)
