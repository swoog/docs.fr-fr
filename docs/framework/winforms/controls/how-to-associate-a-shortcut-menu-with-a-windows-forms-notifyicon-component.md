---
title: 'Procédure : associer un menu contextuel à un composant NotifyIcon Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- context menus [Windows Forms], for background processes
- NotifyIcon component [Windows Forms], associating shortcut menus
- shortcut menus [Windows Forms], for background processes
ms.assetid: d68f3926-08d3-4f7d-949f-1981b29cf188
ms.openlocfilehash: f2a086cc25eb6996b2643742a887bccf481916d6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62010941"
---
# <a name="how-to-associate-a-shortcut-menu-with-a-windows-forms-notifyicon-component"></a>Procédure : associer un menu contextuel à un composant NotifyIcon Windows Forms
> [!NOTE]
>  Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.  
  
 Le <xref:System.Windows.Forms.NotifyIcon> composant affiche une icône dans la zone de notification d’état de la barre des tâches. En général, les applications permettent d’avec le bouton droit de cette icône afin d’envoyer des commandes à l’application qu’elle représente. En associant un <xref:System.Windows.Forms.ContextMenu> composant portant le <xref:System.Windows.Forms.NotifyIcon> composant, vous pouvez ajouter cette fonctionnalité à vos applications.  
  
> [!NOTE]
>  Si vous souhaitez que votre application soit réduite au démarrage lors de l’affichage d’une instance de la <xref:System.Windows.Forms.NotifyIcon> jeu de composants dans la barre des tâches, le formulaire principal <xref:System.Windows.Forms.Form.WindowState%2A> propriété <xref:System.Windows.Forms.FormWindowState.Minimized> et vérifiez que le <xref:System.Windows.Forms.NotifyIcon> du composant <xref:System.Windows.Forms.NotifyIcon.Visible%2A> propriété a la valeur `true`.  
  
### <a name="to-associate-a-shortcut-menu-with-the-notifyicon-component-at-design-time"></a>Pour associer un menu contextuel avec le composant NotifyIcon au moment du design  
  
1. Ajouter un <xref:System.Windows.Forms.NotifyIcon> à votre formulaire et définissez les propriétés importantes, telles que la <xref:System.Windows.Forms.NotifyIcon.Icon%2A> et <xref:System.Windows.Forms.NotifyIcon.Visible%2A> propriétés.  
  
     Pour plus d'informations, voir [Procédure : Ajouter des icônes d’Application à la barre des tâches avec les Windows Forms du composant NotifyIcon](app-icons-to-the-taskbar-with-wf-notifyicon.md).  
  
2. Ajouter un <xref:System.Windows.Forms.ContextMenu> à votre formulaire Windows.  
  
     Ajouter des éléments de menu au menu contextuel qui représente les commandes que vous souhaitez rendre disponible au moment de l’exécution. C’est également un bon moment pour ajouter des améliorations à ces éléments de menu, tels que les clés d’accès.  
  
3. Définir le <xref:System.Windows.Forms.NotifyIcon.ContextMenu%2A> propriété de la <xref:System.Windows.Forms.NotifyIcon> composant au menu contextuel que vous avez ajouté.  
  
     Avec cette propriété est définie, le menu contextuel s’affichera lorsque l’utilisateur clique sur l’icône dans la barre des tâches.  
  
### <a name="to-associate-a-shortcut-menu-with-the-notifyicon-component-programmatically"></a>Pour associer un menu contextuel au composant NotifyIcon par programme  
  
1. Créez une instance de la <xref:System.Windows.Forms.NotifyIcon> classe et un <xref:System.Windows.Forms.ContextMenu> (classe), avec les paramètres de propriété sont nécessaires pour l’application (<xref:System.Windows.Forms.NotifyIcon.Icon%2A> et <xref:System.Windows.Forms.NotifyIcon.Visible%2A> propriétés pour le <xref:System.Windows.Forms.NotifyIcon> composant, les éléments de menu pour le <xref:System.Windows.Forms.ContextMenu> composant).  
  
2. Définir le <xref:System.Windows.Forms.NotifyIcon.ContextMenu%2A> propriété de la <xref:System.Windows.Forms.NotifyIcon> composant au menu contextuel que vous avez ajouté.  
  
     Avec cette propriété est définie, le menu contextuel s’affichera lorsque l’utilisateur clique sur l’icône dans la barre des tâches.  
  
    > [!NOTE]
    >  L’exemple de code suivant crée une structure de menu de base. Vous devrez personnaliser les options de menu à ceux qui correspondent à l’application que vous développez. En outre, vous devez écrire du code pour gérer le <xref:System.Windows.Forms.MenuItem.Click> événements pour ces éléments de menu.  
  
    ```vb  
    Public ContextMenu1 As New ContextMenu  
    Public NotifyIcon1 As New NotifyIcon  
  
    Public Sub CreateIconMenuStructure()  
       ' Add menu items to shortcut menu.  
       ContextMenu1.MenuItems.Add("&Open Application")  
       ContextMenu1.MenuItems.Add("S&uspend Application")  
       ContextMenu1.MenuItems.Add("E&xit")  
  
       ' Set properties of NotifyIcon component.  
       NotifyIcon1.Icon = New System.Drawing.Icon _   
          (System.Environment.GetFolderPath _   
          (System.Environment.SpecialFolder.Personal)  _   
          & "\Icon.ico")  
       NotifyIcon1.Text = "Right-click me!"  
       NotifyIcon1.Visible = True  
       NotifyIcon1.ContextMenu = ContextMenu1  
    End Sub  
    ```  
  
```csharp  
public NotifyIcon notifyIcon1 = new NotifyIcon();  
public ContextMenu contextMenu1 = new ContextMenu();  
  
public void createIconMenuStructure()  
{  
   // Add menu items to shortcut menu.  
   contextMenu1.MenuItems.Add("&Open Application");  
   contextMenu1.MenuItems.Add("S&uspend Application");  
   contextMenu1.MenuItems.Add("E&xit");  
  
   // Set properties of NotifyIcon component.  
   notifyIcon1.Icon = new System.Drawing.Icon  
      (System.Environment.GetFolderPath  
      (System.Environment.SpecialFolder.Personal)  
      + @"\Icon.ico");  
   notifyIcon1.Visible = true;  
   notifyIcon1.Text = "Right-click me!";  
   notifyIcon1.Visible = true;  
   notifyIcon1.ContextMenu = contextMenu1;  
}  
```  
  
```cpp  
public:  
   System::Windows::Forms::NotifyIcon ^ notifyIcon1;  
   System::Windows::Forms::ContextMenu ^ contextMenu1;  
  
   void createIconMenuStructure()  
   {  
      // Add menu items to shortcut menu.  
      contextMenu1->MenuItems->Add("&Open Application");  
      contextMenu1->MenuItems->Add("S&uspend Application");  
      contextMenu1->MenuItems->Add("E&xit");  
  
      // Set properties of NotifyIcon component.  
      notifyIcon1->Icon = gcnew System::Drawing::Icon  
          (String::Concat(System::Environment::GetFolderPath  
          (System::Environment::SpecialFolder::Personal),  
          "\\Icon.ico"));  
      notifyIcon1->Text = "Right-click me!";  
      notifyIcon1->Visible = true;  
      notifyIcon1->ContextMenu = contextMenu1;  
   }  
```  
  
> [!NOTE]
>  Vous devez initialiser `notifyIcon1` et `contextMenu1,` ce que vous pouvez faire en incluant les instructions suivantes dans le constructeur de votre formulaire :  
  
```cpp  
notifyIcon1 = gcnew System::Windows::Forms::NotifyIcon();  
contextMenu1 = gcnew System::Windows::Forms::ContextMenu();  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.NotifyIcon>
- <xref:System.Windows.Forms.NotifyIcon.Icon%2A>
- [Guide pratique pour Ajouter des icônes d’Application à la barre des tâches avec le composant NotifyIcon Windows Forms](app-icons-to-the-taskbar-with-wf-notifyicon.md)
- [NotifyIcon, composant](notifyicon-component-windows-forms.md)
- [Vue d’ensemble du composant NotifyIcon](notifyicon-component-overview-windows-forms.md)
