---
title: 'Procédure : capturer des entrées utilisateur à partir d’un PrintDialog au moment de l’exécution'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print options [Windows Forms], changing at run time
- printing [Windows Forms], options
- print options
- run time [Windows Forms], changing print options
ms.assetid: 438501d8-9a70-4fb3-aae6-e46579aba0c6
ms.openlocfilehash: 2aaf988f362baf9cd80eb16e4a08f7f65a5077bb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311420"
---
# <a name="how-to-capture-user-input-from-a-printdialog-at-run-time"></a>Procédure : capturer des entrées utilisateur à partir d’un PrintDialog au moment de l’exécution
Pendant que vous pouvez définir les options relatives à l’impression au moment du design, il est parfois utile de modifier ces options en cours d’exécution, probablement en raison des choix effectués par l’utilisateur. Vous pouvez capturer des entrées d’utilisateur pour l’impression d’un document à l’aide de la <xref:System.Windows.Forms.PrintDialog> et <xref:System.Drawing.Printing.PrintDocument> composants.  
  
### <a name="to-change-print-options-programmatically"></a>Pour modifier les options d’impression par programmation  
  
1. Ajouter un <xref:System.Windows.Forms.PrintDialog> et une <xref:System.Drawing.Printing.PrintDocument> à votre formulaire.  
  
2. Définir le <xref:System.Windows.Forms.PrintDialog.Document%2A> propriété de la <xref:System.Windows.Forms.PrintDialog> à la <xref:System.Drawing.Printing.PrintDocument> ajouté au formulaire.  
  
    ```vb  
    PrintDialog1.Document = PrintDocument1  
    ```  
  
    ```csharp  
    printDialog1.Document = PrintDocument1;  
    ```  
  
    ```cpp  
    printDialog1->Document = PrintDocument1;  
    ```  
  
3. Afficher le <xref:System.Windows.Forms.PrintDialog> composant à l’aide de la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).  
  
    ```vb  
    PrintDialog1.ShowDialog()  
    ```  
  
    ```csharp  
    printDialog1.ShowDialog();  
    ```  
  
    ```cpp  
    printDialog1->ShowDialog();  
    ```  
  
4. Choix de l’impression de l’utilisateur à partir de la boîte de dialogue seront copiés vers le <xref:System.Drawing.Printing.PrinterSettings> propriété de la <xref:System.Drawing.Printing.PrintDocument> composant.  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Imprimer un fichier texte de plusieurs pages dans les Windows Forms](how-to-print-a-multi-page-text-file-in-windows-forms.md)
- [Prise en charge de l’impression dans les Windows Forms](windows-forms-print-support.md)
