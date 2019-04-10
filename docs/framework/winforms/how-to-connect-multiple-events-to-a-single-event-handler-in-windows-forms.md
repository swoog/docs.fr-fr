---
title: 'Procédure : connecter plusieurs événements à un seul gestionnaire d’événements dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- vb
helpviewer_keywords:
- events [Windows Forms], connecting multiple to single event handler
- event handlers [Windows Forms], connecting events to
- menus [Windows Forms], event-handling methods for multiple menu items
- Windows Forms controls, events
- menu items [Windows Forms], multicasting event-handling methods
ms.assetid: 5a20749a-41b5-4acc-8eb1-9e5040b0a2c4
ms.openlocfilehash: eec6a754b885cd169e5542221caefb3233c4c8af
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59300721"
---
# <a name="how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms"></a>Procédure : connecter plusieurs événements à un seul gestionnaire d’événements dans Windows Forms
Conception de votre application, vous pouvez s’avérer nécessaire pour utiliser un seul gestionnaire d’événements pour plusieurs événements ou d’avoir plusieurs événements à effectuer la même procédure. Par exemple, il est souvent un temps précieux pour avoir une commande de menu à déclencher l’événement de même qu’un bouton sur votre formulaire peut si elles exposent les mêmes fonctionnalités. Vous pouvez faire à l’aide de l’affichage des événements de la fenêtre Propriétés dans C# ou à l’aide de la `Handles` mot clé et le **nom de la classe** et **nom de la méthode** listes déroulantes dans l’éditeur de Code Visual Basic.  
  
### <a name="to-connect-multiple-events-to-a-single-event-handler-in-visual-basic"></a>Pour connecter plusieurs événements à un seul gestionnaire d’événements en Visual Basic  
  
1. Avec le bouton droit de la forme et choisissez **afficher le Code**.  
  
2. À partir de la **nom de la classe** zone de liste déroulante, sélectionnez un des contrôles que vous souhaitez associer le Gestionnaire d’événements.  
  
3. À partir de la **nom de la méthode** zone de liste déroulante, sélectionnez un des événements que vous souhaitez que le Gestionnaire d’événements.  
  
4. L’éditeur de Code insère le Gestionnaire d’événements approprié et place le point d’insertion dans la méthode. Dans l’exemple ci-dessous, il est le <xref:System.Windows.Forms.Control.Click> événement pour le <xref:System.Windows.Forms.Button> contrôle.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
    ' Add event-handler code here.  
    End Sub  
    ```  
  
5. Ajoutez éventuellement les autres événements que vous souhaitez que gérées à le `Handles` clause.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click, Button2.Click  
    ' Add event-handler code here.  
    End Sub  
    ```  
  
6. Ajoutez le code approprié au gestionnaire d’événements.  
  
### <a name="to-connect-multiple-events-to-a-single-event-handler-in-c"></a>Pour connecter plusieurs événements à un seul gestionnaire d’événements en C\#
  
1. Sélectionnez le contrôle auquel vous souhaitez vous connecter à un gestionnaire d’événements.  
  
2. Dans la fenêtre Propriétés, cliquez sur le **événements** bouton (![bouton événements](./media/vxeventsbutton-propertieswindow.png "vxEventsButton_PropertiesWindow")).  
  
3. Cliquez sur le nom de l’événement que vous souhaitez gérer.  
  
4. Dans la section valeur en regard du nom de l’événement, cliquez sur le bouton de liste déroulante pour afficher une liste des gestionnaires d’événements qui correspondent à la signature de méthode de l’événement que vous souhaitez gérer.  
  
5. Sélectionnez le Gestionnaire d’événements appropriée dans la liste.  
  
     Code sera ajouté au formulaire pour lier l’événement au gestionnaire d’événements existant.  
  
## <a name="see-also"></a>Voir aussi

- [Création de gestionnaires d'événements dans les Windows Forms](creating-event-handlers-in-windows-forms.md)
- [Vue d’ensemble des gestionnaires d’événements](event-handlers-overview-windows-forms.md)
