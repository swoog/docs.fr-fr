---
title: 'Procédure : Créer des travaux d’impression Standard de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- printing [Windows Forms]
- printing [Windows Forms], creating print jobs
- printing [Visual Basic], in Windows applications
ms.assetid: 03342b90-9cfe-40b2-838b-b479a13c5dea
ms.openlocfilehash: b0568472dadceb46257a8d35211034a718aef74c
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57705219"
---
# <a name="how-to-create-standard-windows-forms-print-jobs"></a>Procédure : Créer des travaux d’impression Standard de Windows Forms
La base de l’impression dans Windows Forms est la <xref:System.Drawing.Printing.PrintDocument> composant, plus précisément, le <xref:System.Drawing.Printing.PrintDocument.PrintPage> événement. En écrivant du code pour gérer le <xref:System.Drawing.Printing.PrintDocument.PrintPage> événement, vous pouvez spécifier les éléments à imprimer et l’imprimer.  
  
### <a name="to-create-a-print-job"></a>Pour créer un travail d’impression  
  
1.  Ajouter un <xref:System.Drawing.Printing.PrintDocument> à votre formulaire.  
  
2.  Écrivez du code pour gérer l’événement <xref:System.Drawing.Printing.PrintDocument.PrintPage> .  
  
     Vous devrez coder votre propre logique d’impression. En outre, vous devez spécifier l’élément à imprimer.  
  
     Dans l’exemple de code suivant, un exemple de graphisme dans la forme d’un rectangle rouge est créé dans le <xref:System.Drawing.Printing.PrintDocument.PrintPage> Gestionnaire d’événements à l’élément à imprimer.  
  
    ```vb  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillRectangle(Brushes.Red, New Rectangle(500, 500, 500, 500))  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_PrintPage(object sender,   
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Red,   
         new Rectangle(500, 500, 500, 500));  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_PrintPage(System::Object ^ sender,  
          System::Drawing::Printing::PrintPageEventArgs ^ e)  
       {  
          e->Graphics->FillRectangle(Brushes::Red,  
             Rectangle(500, 500, 500, 500));  
       }  
    ```  
  
     (Visual c# et [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.printDocument1.PrintPage += new  
       System.Drawing.Printing.PrintPageEventHandler  
       (this.printDocument1_PrintPage);  
    ```  
  
    ```cpp  
    printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    ```  
  
     Vous souhaiterez également écrire du code pour le <xref:System.Drawing.Printing.PrintDocument.BeginPrint> et <xref:System.Drawing.Printing.PrintDocument.EndPrint> événements, en incluant éventuellement un entier représentant le nombre total de pages à imprimer qui est décrémenté comme imprime chaque page.  
  
    > [!NOTE]
    >  Vous pouvez ajouter un <xref:System.Windows.Forms.PrintDialog> à votre formulaire pour fournir une interface propre et efficace de l’utilisateur (IU) à vos utilisateurs. Définition de la <xref:System.Windows.Forms.PrintDialog.Document%2A> propriété de la <xref:System.Windows.Forms.PrintDialog> permet de composant vous permet de définir les propriétés relatives à l’impression de document vous travaillez sur votre formulaire. Pour plus d’informations sur la <xref:System.Windows.Forms.PrintDialog> composant, consultez [du composant PrintDialog](../controls/printdialog-component-windows-forms.md).  
  
     Pour plus d’informations sur les spécificités des Windows Forms les travaux d’impression, y compris la création d’un travail d’impression par programmation, consultez <xref:System.Drawing.Printing.PrintPageEventArgs>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Printing.PrintDocument>
- [Prise en charge de l’impression dans les Windows Forms](windows-forms-print-support.md)
