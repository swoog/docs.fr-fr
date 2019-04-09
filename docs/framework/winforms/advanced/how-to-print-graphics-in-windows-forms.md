---
title: 'Procédure : imprimer des graphismes dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- graphics [Windows Forms], printing
- printing [Windows Forms], graphics
ms.assetid: 32b891e6-52ff-4fea-a9ff-2ce5db20a4c6
ms.openlocfilehash: ab2a230b7c6e303d712df058f450334b50c8a676
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59167204"
---
# <a name="how-to-print-graphics-in-windows-forms"></a>Procédure : imprimer des graphismes dans Windows Forms
Souvent, vous devez imprimer des graphiques dans votre application basée sur Windows. Le <xref:System.Drawing.Graphics> classe fournit des méthodes pour dessiner des objets sur un appareil, tel qu’un écran ou une imprimante.  
  
### <a name="to-print-graphics"></a>Pour imprimer des graphiques  
  
1.  Ajouter un <xref:System.Drawing.Printing.PrintDocument> à votre formulaire.  
  
2.  Dans le <xref:System.Drawing.Printing.PrintDocument.PrintPage> Gestionnaire d’événements, utilisez le <xref:System.Drawing.Printing.PrintPageEventArgs.Graphics%2A> propriété de la <xref:System.Drawing.Printing.PrintPageEventArgs> classe pour indiquer à l’imprimante sur les types de graphismes à imprimer.  
  
     L’exemple de code suivant montre un gestionnaire d’événements utilisé pour créer une ellipse bleue dans un rectangle englobant. Le rectangle a l’emplacement et les dimensions suivantes : début à 100, 150 avec une largeur de 250 et une hauteur de 250.  
  
    ```vb  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillEllipse(Brushes.Blue, New Rectangle(100, 150, 250, 250))  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_PrintPage(object sender,   
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Blue,   
         new Rectangle(100, 150, 250, 250));  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_PrintPage(System::Object ^ sender,  
          System::Drawing::Printing::PrintPageEventArgs ^ e)  
       {  
          e->Graphics->FillRectangle(Brushes::Blue,  
             Rectangle(100, 150, 250, 250));  
       }  
    ```  
  
     (Visual c# et [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.printDocument1.PrintPage += new  
       System.Drawing.Printing.PrintPageEventHandler  
       (this.printDocument1_PrintPage);  
    ```  
  
    ```cpp  
    this->printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Graphics>
- <xref:System.Drawing.Brush>
- [Prise en charge de l'impression dans les Windows Forms](windows-forms-print-support.md)
