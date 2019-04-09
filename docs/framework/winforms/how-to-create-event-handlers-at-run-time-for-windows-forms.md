---
title: 'Procédure : créer des gestionnaires d’événements au moment de l’exécution pour Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, event handling
- event handlers [Windows Forms], creating
- run time [Windows Forms], creating event handlers at
- examples [Windows Forms], event handling
- Button control [Windows Forms], event handlers
ms.assetid: 2e7c9e1a-61fe-444d-8113-3c5bacf1c8cb
ms.openlocfilehash: 3c1dca420b9e63fe8a2cb93b2e7918d9dc35e84d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59158546"
---
# <a name="how-to-create-event-handlers-at-run-time-for-windows-forms"></a>Procédure : créer des gestionnaires d’événements au moment de l’exécution pour Windows Forms
Outre la création d’événements à l’aide du Concepteur Windows Forms, vous pouvez créer un gestionnaire d’événements au moment de l’exécution. Cette action vous permet de connecter des gestionnaires d’événements en fonction de conditions spécifiées dans le code lors de l’exécution au lieu de les connecter au premier démarrage du programme.  
  
### <a name="to-create-an-event-handler-at-run-time"></a>Pour créer un gestionnaire d’événements au moment de l’exécution  
  
1.  Ouvrez le formulaire auquel vous souhaitez ajouter un gestionnaire d’événements dans l’éditeur de code.  
  
2.  Ajoutez une méthode à votre formulaire avec la signature de méthode pour l’événement que vous souhaitez gérer.  
  
     Par exemple, si vous gérez le <xref:System.Windows.Forms.Control.Click> événement d’un <xref:System.Windows.Forms.Button> contrôle, vous pouvez créer une méthode telle que la suivante :  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As Object, ByVal e As EventArgs)  
       ' Add event handler code here.  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)   
    {  
    // Add event handler code here.  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,   
          System::EventArgs ^ e)  
       {  
          // Add event handler code here.  
       }  
    ```  
  
3.  Ajoutez le code au gestionnaire d’événements en fonction de votre application.  
  
4.  Déterminez le formulaire ou le contrôle pour lequel vous souhaitez créer un gestionnaire d’événements.  
  
5.  Dans une méthode de classe de votre formulaire, ajoutez le code qui spécifie au gestionnaire d’événements de gérer l’événement. Par exemple, le code suivant spécifie le Gestionnaire d’événements `button1_Click` gère la <xref:System.Windows.Forms.Control.Click> événement d’un <xref:System.Windows.Forms.Button> contrôle :  
  
    ```vb  
    AddHandler Button1.Click, AddressOf Button1_Click  
    ```  
  
    ```csharp  
    button1.Click += new EventHandler(button1_Click);  
    ```  
  
    ```cpp  
    button1->Click += gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
     Le <xref:System.ComponentModel.EventHandlerList.AddHandler%2A> méthode présentée dans le code Visual Basic ci-dessus établit un gestionnaire d’événements click du bouton.  
  
## <a name="see-also"></a>Voir aussi

- [Création de gestionnaires d'événements dans les Windows Forms](creating-event-handlers-in-windows-forms.md)
- [Vue d’ensemble des gestionnaires d’événements](event-handlers-overview-windows-forms.md)
- [Dépannage des gestionnaires d'événements hérités dans Visual Basic](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)
