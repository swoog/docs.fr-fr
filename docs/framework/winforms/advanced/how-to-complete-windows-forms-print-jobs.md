---
title: 'Procédure : exécuter des travaux d’impression Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print jobs [Windows Forms], completing in Windows Forms
- printing [Windows Forms], print jobs
ms.assetid: 23ec74f7-34c5-4710-82a0-ee2914518548
ms.openlocfilehash: f8d0f1f067efbae6e2b667328e75996179b91737
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59159820"
---
# <a name="how-to-complete-windows-forms-print-jobs"></a>Procédure : exécuter des travaux d’impression Windows Forms
Fréquemment, les traitements de texte et d’autres applications qui impliquent l’impression fournit l’option pour afficher un message aux utilisateurs qu’un travail d’impression est terminé. Vous pouvez fournir cette fonctionnalité dans vos formulaires Windows en gérant la <xref:System.Drawing.Printing.PrintDocument.EndPrint> événements de la <xref:System.Drawing.Printing.PrintDocument> composant.  
  
 La procédure suivante nécessite que vous avez créé une application Windows avec un <xref:System.Drawing.Printing.PrintDocument> composant dessus, ce qui est le moyen standard de l’activation de l’impression à partir d’une application basée sur Windows. Pour plus d’informations sur l’impression à partir de Windows Forms à l’aide du <xref:System.Drawing.Printing.PrintDocument> composant, consultez [Comment : Créer des travaux d’impression Standard de Windows Forms](how-to-create-standard-windows-forms-print-jobs.md).  
  
### <a name="to-complete-a-print-job"></a>Pour effectuer un travail d’impression  
  
1.  Définir le <xref:System.Drawing.Printing.PrintDocument.DocumentName%2A> propriété de la <xref:System.Drawing.Printing.PrintDocument> composant.  
  
    ```vb  
    PrintDocument1.DocumentName = "MyTextFile"  
    ```  
  
    ```csharp  
    printDocument1.DocumentName = "MyTextFile";  
    ```  
  
    ```cpp  
    printDocument1->DocumentName = "MyTextFile";  
    ```  
  
2.  Écrivez du code pour gérer l’événement <xref:System.Drawing.Printing.PrintDocument.EndPrint> .  
  
     Dans l’exemple de code suivant, une boîte de message s’affiche, indiquant que la fin du document d’impression.  
  
    ```vb  
    Private Sub PrintDocument1_EndPrint(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintEventArgs) Handles PrintDocument1.EndPrint  
       MessageBox.Show(PrintDocument1.DocumentName + " has finished printing.")  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_EndPrint(object sender,   
    System.Drawing.Printing.PrintEventArgs e)  
    {  
       MessageBox.Show(printDocument1.DocumentName +   
          " has finished printing.");  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_EndPrint(System::Object ^ sender,  
          System::Drawing::Printing::PrintEventArgs ^ e)  
       {  
          MessageBox::Show(String::Concat(printDocument1->DocumentName,  
             " has finished printing."));  
       }  
    ```  
  
     (Visual c# et [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.printDocument1.EndPrint += new  
       System.Drawing.Printing.PrintEventHandler  
       (this.printDocument1_EndPrint);  
    ```  
  
    ```cpp  
    this->printDocument1->EndPrint += gcnew  
       System::Drawing::Printing::PrintEventHandler  
       (this, &Form1::printDocument1_EndPrint);  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Printing.PrintDocument>
- [Prise en charge de l'impression dans les Windows Forms](windows-forms-print-support.md)
