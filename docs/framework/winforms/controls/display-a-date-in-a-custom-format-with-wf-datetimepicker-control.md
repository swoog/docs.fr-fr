---
title: 'Procédure : Afficher une Date dans un Format personnalisé à l’aide du contrôle DateTimePicker Windows Forms'
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
ms.openlocfilehash: c201455acaa9bde521afd623424d0cfc403b1bff
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57705869"
---
# <a name="how-to-display-a-date-in-a-custom-format-with-the-windows-forms-datetimepicker-control"></a>Procédure : Afficher une Date dans un Format personnalisé à l’aide du contrôle DateTimePicker Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.DateTimePicker> contrôle vous donne la flexibilité dans la mise en forme l’affichage des dates et heures dans le contrôle. Le <xref:System.Windows.Forms.DateTimePicker.Format%2A> propriété vous permet de sélectionner à partir des formats prédéfinis répertoriés dans le <xref:System.Windows.Forms.DateTimePickerFormat>. Si aucune d'entre elles ne convient pas à vos besoins, vous pouvez créer votre propre style de format à l’aide de caractères de format répertoriés dans <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A>.  
  
### <a name="to-display-a-custom-format"></a>Pour afficher un format personnalisé  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.DateTimePicker.Format%2A> la valeur `DateTimePickerFormat.Custom`.  
  
2.  Définir le <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> propriété à une chaîne de format.  
  
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
  
### <a name="to-add-text-to-the-formatted-value"></a>Pour ajouter du texte à la valeur mise en forme  
  
1.  Utilisez des guillemets simples pour encadrer tout caractère qui n’est pas un caractère de format comme « M » ou un délimiteur comme « : ». Par exemple, la chaîne de format ci-dessous affiche la date actuelle au format « aujourd'hui est : 05:30:31 Friday March 02, 2012" dans la culture anglais (États-Unis).  
  
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
  
     Selon le paramètre de culture, les caractères ne pas entourés de guillemets simples peuvent être modifiés. Par exemple, la chaîne de format ci-dessus affiche la date actuelle au format « aujourd'hui est : 05:30:31 Friday March 02, 2012" dans la culture anglais (États-Unis). Notez que le premier signe deux-points est placé entre guillemets simples, car il n’est pas destiné à être un caractère de délimitation comme dans « hh ». Dans une autre culture, le format peut apparaître en tant que « aujourd'hui est : 05.30.31 Friday mars 02, 2012".  
  
## <a name="see-also"></a>Voir aussi
- [DateTimePicker, contrôle](datetimepicker-control-windows-forms.md)
- [Guide pratique pour Dates définies et de retour à l’aide du contrôle DateTimePicker Windows Forms](how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)
