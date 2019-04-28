---
title: 'Procédure : répondre aux clics de bouton Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], responding to Click events
- events [Windows Forms], Click events
- Click event [Windows Forms], Button control
- MouseDown event
- Button control [Windows Forms], click response
- double-clicks
- examples [Windows Forms], controls
- Click event [Windows Forms], responding to
ms.assetid: 7a4951bd-369c-4662-b246-28ad83eda484
ms.openlocfilehash: a10eaa3ea62df9301a53f5609b503bfabcb50a46
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913079"
---
# <a name="how-to-respond-to-windows-forms-button-clicks"></a>Procédure : répondre aux clics de bouton Windows Forms
L’utilisation la plus élémentaire d’un formulaire Windows <xref:System.Windows.Forms.Button> contrôle consiste à exécuter du code lorsque le bouton est activé.  
  
 En cliquant sur un <xref:System.Windows.Forms.Button> contrôle génère également un nombre d’événements, tels que le <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseDown>, et <xref:System.Windows.Forms.Control.MouseUp> événements. Si vous avez l’intention d’attacher des gestionnaires d’événements pour ces événements connexes, veillez à ce que leurs actions ne sont pas en conflit. Par exemple, si vous cliquez sur le bouton efface les informations que l’utilisateur a tapé dans une zone de texte, suspendant le pointeur de la souris sur le bouton ne doit pas afficher une info-bulle contenant ces informations inexistante pour l’instant.  
  
 Si l’utilisateur tente de double-cliquer sur le <xref:System.Windows.Forms.Button> contrôle, chaque clic sera traité séparément ; autrement dit, le contrôle ne prend pas en charge l’événement de double-clic.  
  
### <a name="to-respond-to-a-button-click"></a>Pour répondre à un clic de bouton  
  
- Dans le bouton `Click` <xref:System.EventHandler> écrire le code à exécuter. `Button1_Click` doit être lié au contrôle. Pour plus d'informations, voir [Procédure : Créer des gestionnaires d’événements en cours d’exécution pour les Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       MessageBox.Show("Button1 was clicked")  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       MessageBox.Show("button1 was clicked");  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          MessageBox::Show("button1 was clicked");  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble du contrôle Button](button-control-overview-windows-forms.md)
- [Méthodes de sélection du contrôle Button Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Button, contrôle](button-control-windows-forms.md)
