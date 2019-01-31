---
title: Comment afficher le composant PrintDialog
ms.date: 03/30/2017
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], displaying
- printing [Windows Forms], displaying print dialog box
ms.assetid: 745a8db7-0526-4b21-b09d-18e13ed32014
ms.openlocfilehash: 198ae75d407bd1837033a1cc186d84ff972fdc2f
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285153"
---
# <a name="how-to-display-the-printdialog-component"></a>Comment afficher le composant PrintDialog

Le <xref:System.Windows.Forms.PrintDialog> composant est la boîte de dialogue d’impression Windows standard qui la plupart de vos utilisateurs seront familiers. Étant donné que vos utilisateurs seront immédiatement à l’aise avec lui, il serait préférable que vous pouvez utiliser le <xref:System.Windows.Forms.PrintDialog> composant.

## <a name="to-display-the-printdialog-component"></a>Pour afficher le composant PrintDialog

- Appelez le <xref:System.Windows.Forms.Form.ShowDialog%2A> méthode à partir du code de votre application.

     Une fois le composant affiché, les utilisateurs interagissent avec lui et définissent les propriétés du travail d’impression. Celles-ci sont enregistrées dans le <xref:System.Drawing.Printing.PrinterSettings> classe (et le <xref:System.Drawing.Printing.PageSettings> classe, si l’utilisateur accède à la [du composant PageSetupDialog](pagesetupdialog-component-windows-forms.md) via la <xref:System.Windows.Forms.PrintDialog> composant) associé à ce travail d’impression. Vous pouvez ensuite faire des appels aux propriétés qu’elles définissent pour déterminer les caractéristiques du travail d’impression.

## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Créer des travaux d’impression Standard de Windows Forms](../advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [Guide pratique pour Capturer des entrées utilisateur à partir d’un composant PrintDialog au moment de l’exécution](../advanced/how-to-capture-user-input-from-a-printdialog-at-run-time.md)
- [PrintPreviewDialog, contrôle](printpreviewdialog-control-windows-forms.md)
- [PrintDialog, composant](printdialog-component-windows-forms.md)
- [Prise en charge de l’impression dans les Windows Forms](../advanced/windows-forms-print-support.md)
- [Contrôles Windows Forms](index.md)