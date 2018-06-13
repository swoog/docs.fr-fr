---
title: "Comment : afficher l'heure avec le contrôle DateTimePicker"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time [Windows Forms], displaying in DateTimePicker control
- examples [Windows Forms], DateTimePicker control
- DateTimePicker control [Windows Forms], displaying time
ms.assetid: 0c1c8b40-1b50-4301-a90c-39516775ccb1
ms.openlocfilehash: 16e09225c9447f9ec8be3b658ac0ed1aa3b2edab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33531828"
---
# <a name="how-to-display-time-with-the-datetimepicker-control"></a>Comment : afficher l'heure avec le contrôle DateTimePicker
Si vous souhaitez que votre application permette aux utilisateurs de sélectionner une date et une heure et qu'elle affiche la date et l'heure au format spécifié, utilisez le contrôle <xref:System.Windows.Forms.DateTimePicker>. La procédure suivante montre comment utiliser le contrôle <xref:System.Windows.Forms.DateTimePicker> pour afficher l'heure.  
  
### <a name="to-display-the-time-with-the-datetimepicker-control"></a>Pour afficher l'heure avec le contrôle DateTimePicker  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.DateTimePicker.Format%2A> la valeur <xref:System.Windows.Forms.DateTimePickerFormat.Time>  
  
     [!code-csharp[System.Windows.Forms.DateTimePickerTimeOnly#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.DateTimePickerTimeOnly#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/VB/Form1.vb#2)]  
  
2.  Affectez à la propriété <xref:System.Windows.Forms.DateTimePicker.ShowUpDown%2A> de <xref:System.Windows.Forms.DateTimePicker> la valeur `true`.  
  
     [!code-csharp[System.Windows.Forms.DateTimePickerTimeOnly#3](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.DateTimePickerTimeOnly#3](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/VB/Form1.vb#3)]  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment créer un <xref:System.Windows.Forms.DateTimePicker> qui permet aux utilisateurs de choisir uniquement une heure.  
  
 [!code-csharp[System.Windows.Forms.DateTimePickerTimeOnly#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.DateTimePickerTimeOnly#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également la page [Comment : compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi  
 [DateTimePicker, contrôle](../../../../docs/framework/winforms/controls/datetimepicker-control-windows-forms.md)
