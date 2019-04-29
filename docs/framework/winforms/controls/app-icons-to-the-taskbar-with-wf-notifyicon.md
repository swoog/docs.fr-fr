---
title: 'Procédure : ajouter des icônes d’application à la barre des tâches avec le composant NotifyIcon Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TrayIcon
helpviewer_keywords:
- status area icons
- icons [Windows Forms], adding to taskbar
- NotifyIcon component
- taskbar [Windows Forms], adding icons
ms.assetid: d28c0fe6-aaf2-4df7-ad74-928d861a8510
ms.openlocfilehash: 52c18b959361079aac6b95dc5d4584bf464a306a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61640319"
---
# <a name="how-to-add-application-icons-to-the-taskbar-with-the-windows-forms-notifyicon-component"></a>Procédure : ajouter des icônes d’application à la barre des tâches avec le composant NotifyIcon Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.NotifyIcon> composant affiche une icône dans la zone de notification d’état de la barre des tâches. Pour afficher plusieurs icônes dans la zone d’état, vous devez disposer de plusieurs <xref:System.Windows.Forms.NotifyIcon> composants sur votre formulaire. Pour définir l’icône affichée pour un contrôle, utilisez le <xref:System.Windows.Forms.NotifyIcon.Icon%2A> propriété. Vous pouvez également écrire du code le <xref:System.Windows.Forms.NotifyIcon.DoubleClick> Gestionnaire d’événements afin que quelque chose se produit lorsque l’utilisateur double-clique sur l’icône. Par exemple, vous pouvez créer une boîte de dialogue s’affichent pour l’utilisateur de configurer le processus d’arrière-plan représenté par l’icône.  
  
> [!NOTE]
>  Le <xref:System.Windows.Forms.NotifyIcon> composant est utilisé pour la notification uniquement, pour informer les utilisateurs qu’une action ou un événement s’est produite ou il y a eu un changement d’état quelconque. Vous devez utiliser les menus, barres d’outils et autres éléments d’interface utilisateur pour l’interaction avec les applications standard.  
  
### <a name="to-set-the-icon"></a>Pour définir l’icône  
  
1. Affecter une valeur à la <xref:System.Windows.Forms.NotifyIcon.Icon%2A> propriété. La valeur doit être de type `System.Drawing.Icon` et peut être chargée à partir d’un fichier .ico. Vous pouvez spécifier le fichier d’icône dans le code ou en cliquant sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.NotifyIcon.Icon%2A> propriété dans le  **Propriétés** fenêtre, puis en sélectionnant le fichier dans le **Open** boîte de dialogue qui s’affiche.  
  
2. Affectez à la propriété <xref:System.Windows.Forms.NotifyIcon.Visible%2A> la valeur `true`.  
  
3. Définir le <xref:System.Windows.Forms.NotifyIcon.Text%2A> propriété à une chaîne d’info-bulle appropriée.  
  
     Dans l’exemple de code suivant, le chemin d’accès défini pour l’emplacement de l’icône est la **Mes Documents** dossier. Cet emplacement est utilisé, car vous pouvez supposer que la plupart des ordinateurs exécutant le système d’exploitation Windows incluent ce dossier. Choix de cet emplacement permet également aux utilisateurs avec des niveaux d’accès système minimal en toute sécurité exécuter l’application. L’exemple suivant nécessite un formulaire avec un <xref:System.Windows.Forms.NotifyIcon> contrôle déjà ajouté. Il requiert également un fichier icône nommé `Icon.ico`.  
  
    ```vb  
    ' You should replace the bold icon in the sample below  
    ' with an icon of your own choosing.  
    NotifyIcon1.Icon = New _   
       System.Drawing.Icon(System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\Icon.ico")  
    NotifyIcon1.Visible = True  
    NotifyIcon1.Text = "Antivirus program"  
    ```  
  
    ```csharp  
    // You should replace the bold icon in the sample below  
    // with an icon of your own choosing.  
    // Note the escape character used (@) when specifying the path.  
    notifyIcon1.Icon =   
       new System.Drawing.Icon (System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.Personal)  
       + @"\Icon.ico");  
    notifyIcon1.Visible = true;  
    notifyIcon1.Text = "Antivirus program";  
    ```  
  
    ```cpp  
    // You should replace the bold icon in the sample below  
    // with an icon of your own choosing.  
    notifyIcon1->Icon = gcnew   
       System::Drawing::Icon(String::Concat  
       (System::Environment::GetFolderPath  
       (System::Environment::SpecialFolder::Personal),  
       "\\Icon.ico"));  
    notifyIcon1->Visible = true;  
    notifyIcon1->Text = "Antivirus program";  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.NotifyIcon>
- <xref:System.Windows.Forms.NotifyIcon.Icon%2A>
- [Guide pratique pour Associer un Menu contextuel à du composant NotifyIcon Windows Forms](how-to-associate-a-shortcut-menu-with-a-windows-forms-notifyicon-component.md)
- [NotifyIcon, composant](notifyicon-component-windows-forms.md)
- [Vue d’ensemble du composant NotifyIcon](notifyicon-component-overview-windows-forms.md)
