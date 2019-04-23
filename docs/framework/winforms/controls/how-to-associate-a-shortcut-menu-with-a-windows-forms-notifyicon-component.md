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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337056"
---
# <a name="how-to-associate-a-shortcut-menu-with-a-windows-forms-notifyicon-component"></a><span data-ttu-id="3c0f4-102">Procédure : associer un menu contextuel à un composant NotifyIcon Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3c0f4-102">How to: Associate a Shortcut Menu with a Windows Forms NotifyIcon Component</span></span>
> [!NOTE]
>  <span data-ttu-id="3c0f4-103">Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-103">Although <xref:System.Windows.Forms.MenuStrip> and <xref:System.Windows.Forms.ContextMenuStrip> replace and add functionality to the <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> controls of previous versions, <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> are retained for both backward compatibility and future use if you choose.</span></span>  
  
 <span data-ttu-id="3c0f4-104">Le <xref:System.Windows.Forms.NotifyIcon> composant affiche une icône dans la zone de notification d’état de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-104">The <xref:System.Windows.Forms.NotifyIcon> component displays an icon in the status notification area of the taskbar.</span></span> <span data-ttu-id="3c0f4-105">En général, les applications permettent d’avec le bouton droit de cette icône afin d’envoyer des commandes à l’application qu’elle représente.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-105">Commonly, applications enable you to right-click this icon to send commands to the application it represents.</span></span> <span data-ttu-id="3c0f4-106">En associant un <xref:System.Windows.Forms.ContextMenu> composant portant le <xref:System.Windows.Forms.NotifyIcon> composant, vous pouvez ajouter cette fonctionnalité à vos applications.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-106">By associating a <xref:System.Windows.Forms.ContextMenu> component with the <xref:System.Windows.Forms.NotifyIcon> component, you can add this functionality to your applications.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3c0f4-107">Si vous souhaitez que votre application soit réduite au démarrage lors de l’affichage d’une instance de la <xref:System.Windows.Forms.NotifyIcon> jeu de composants dans la barre des tâches, le formulaire principal <xref:System.Windows.Forms.Form.WindowState%2A> propriété <xref:System.Windows.Forms.FormWindowState.Minimized> et vérifiez que le <xref:System.Windows.Forms.NotifyIcon> du composant <xref:System.Windows.Forms.NotifyIcon.Visible%2A> propriété a la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-107">If you want your application to be minimized at startup while displaying an instance of the <xref:System.Windows.Forms.NotifyIcon> component in the taskbar, set the main form's <xref:System.Windows.Forms.Form.WindowState%2A> property to <xref:System.Windows.Forms.FormWindowState.Minimized> and be sure the <xref:System.Windows.Forms.NotifyIcon> component's <xref:System.Windows.Forms.NotifyIcon.Visible%2A> property is set to `true`.</span></span>  
  
### <a name="to-associate-a-shortcut-menu-with-the-notifyicon-component-at-design-time"></a><span data-ttu-id="3c0f4-108">Pour associer un menu contextuel avec le composant NotifyIcon au moment du design</span><span class="sxs-lookup"><span data-stu-id="3c0f4-108">To associate a shortcut menu with the NotifyIcon component at design time</span></span>  
  
1. <span data-ttu-id="3c0f4-109">Ajouter un <xref:System.Windows.Forms.NotifyIcon> à votre formulaire et définissez les propriétés importantes, telles que la <xref:System.Windows.Forms.NotifyIcon.Icon%2A> et <xref:System.Windows.Forms.NotifyIcon.Visible%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-109">Add a <xref:System.Windows.Forms.NotifyIcon> component to your form, and set the important properties, such as the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> and <xref:System.Windows.Forms.NotifyIcon.Visible%2A> properties.</span></span>  
  
     <span data-ttu-id="3c0f4-110">Pour plus d'informations, voir [Procédure : Ajouter des icônes d’Application à la barre des tâches avec les Windows Forms du composant NotifyIcon](app-icons-to-the-taskbar-with-wf-notifyicon.md).</span><span class="sxs-lookup"><span data-stu-id="3c0f4-110">For more information, see [How to: Add Application Icons to the TaskBar with the Windows Forms NotifyIcon Component](app-icons-to-the-taskbar-with-wf-notifyicon.md).</span></span>  
  
2. <span data-ttu-id="3c0f4-111">Ajouter un <xref:System.Windows.Forms.ContextMenu> à votre formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-111">Add a <xref:System.Windows.Forms.ContextMenu> component to your Windows Form.</span></span>  
  
     <span data-ttu-id="3c0f4-112">Ajouter des éléments de menu au menu contextuel qui représente les commandes que vous souhaitez rendre disponible au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-112">Add menu items to the shortcut menu representing the commands you want to make available at run time.</span></span> <span data-ttu-id="3c0f4-113">C’est également un bon moment pour ajouter des améliorations à ces éléments de menu, tels que les clés d’accès.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-113">This is also a good time to add menu enhancements to these menu items, such as access keys.</span></span>  
  
3. <span data-ttu-id="3c0f4-114">Définir le <xref:System.Windows.Forms.NotifyIcon.ContextMenu%2A> propriété de la <xref:System.Windows.Forms.NotifyIcon> composant au menu contextuel que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-114">Set the <xref:System.Windows.Forms.NotifyIcon.ContextMenu%2A> property of the <xref:System.Windows.Forms.NotifyIcon> component to the shortcut menu that you added.</span></span>  
  
     <span data-ttu-id="3c0f4-115">Avec cette propriété est définie, le menu contextuel s’affichera lorsque l’utilisateur clique sur l’icône dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-115">With this property set, the shortcut menu will be displayed when the icon on the taskbar is clicked.</span></span>  
  
### <a name="to-associate-a-shortcut-menu-with-the-notifyicon-component-programmatically"></a><span data-ttu-id="3c0f4-116">Pour associer un menu contextuel au composant NotifyIcon par programme</span><span class="sxs-lookup"><span data-stu-id="3c0f4-116">To associate a shortcut menu with the NotifyIcon component programmatically</span></span>  
  
1. <span data-ttu-id="3c0f4-117">Créez une instance de la <xref:System.Windows.Forms.NotifyIcon> classe et un <xref:System.Windows.Forms.ContextMenu> (classe), avec les paramètres de propriété sont nécessaires pour l’application (<xref:System.Windows.Forms.NotifyIcon.Icon%2A> et <xref:System.Windows.Forms.NotifyIcon.Visible%2A> propriétés pour le <xref:System.Windows.Forms.NotifyIcon> composant, les éléments de menu pour le <xref:System.Windows.Forms.ContextMenu> composant).</span><span class="sxs-lookup"><span data-stu-id="3c0f4-117">Create an instance of the <xref:System.Windows.Forms.NotifyIcon> class and a <xref:System.Windows.Forms.ContextMenu> class, with whatever property settings are necessary for the application (<xref:System.Windows.Forms.NotifyIcon.Icon%2A> and <xref:System.Windows.Forms.NotifyIcon.Visible%2A> properties for the <xref:System.Windows.Forms.NotifyIcon> component, menu items for the <xref:System.Windows.Forms.ContextMenu> component).</span></span>  
  
2. <span data-ttu-id="3c0f4-118">Définir le <xref:System.Windows.Forms.NotifyIcon.ContextMenu%2A> propriété de la <xref:System.Windows.Forms.NotifyIcon> composant au menu contextuel que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-118">Set the <xref:System.Windows.Forms.NotifyIcon.ContextMenu%2A> property of the <xref:System.Windows.Forms.NotifyIcon> component to the shortcut menu that you added.</span></span>  
  
     <span data-ttu-id="3c0f4-119">Avec cette propriété est définie, le menu contextuel s’affichera lorsque l’utilisateur clique sur l’icône dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-119">With this property set, the shortcut menu will be displayed when the icon on the taskbar is clicked.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="3c0f4-120">L’exemple de code suivant crée une structure de menu de base.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-120">The following code example creates a basic menu structure.</span></span> <span data-ttu-id="3c0f4-121">Vous devrez personnaliser les options de menu à ceux qui correspondent à l’application que vous développez.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-121">You will need to customize the menu choices to those that fit the application you are developing.</span></span> <span data-ttu-id="3c0f4-122">En outre, vous devez écrire du code pour gérer le <xref:System.Windows.Forms.MenuItem.Click> événements pour ces éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-122">Additionally, you will want to write code to handle the <xref:System.Windows.Forms.MenuItem.Click> events for these menu items.</span></span>  
  
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
>  <span data-ttu-id="3c0f4-123">Vous devez initialiser `notifyIcon1` et `contextMenu1,` ce que vous pouvez faire en incluant les instructions suivantes dans le constructeur de votre formulaire :</span><span class="sxs-lookup"><span data-stu-id="3c0f4-123">You must initialize `notifyIcon1` and `contextMenu1,` which you can do by including the following statements in the constructor of your form:</span></span>  
  
```cpp  
notifyIcon1 = gcnew System::Windows::Forms::NotifyIcon();  
contextMenu1 = gcnew System::Windows::Forms::ContextMenu();  
```  
  
## <a name="see-also"></a><span data-ttu-id="3c0f4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c0f4-124">See also</span></span>

- <xref:System.Windows.Forms.NotifyIcon>
- <xref:System.Windows.Forms.NotifyIcon.Icon%2A>
- [<span data-ttu-id="3c0f4-125">Guide pratique pour Ajouter des icônes d’Application à la barre des tâches avec le composant NotifyIcon Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3c0f4-125">How to: Add Application Icons to the TaskBar with the Windows Forms NotifyIcon Component</span></span>](app-icons-to-the-taskbar-with-wf-notifyicon.md)
- [<span data-ttu-id="3c0f4-126">NotifyIcon, composant</span><span class="sxs-lookup"><span data-stu-id="3c0f4-126">NotifyIcon Component</span></span>](notifyicon-component-windows-forms.md)
- [<span data-ttu-id="3c0f4-127">Vue d’ensemble du composant NotifyIcon</span><span class="sxs-lookup"><span data-stu-id="3c0f4-127">NotifyIcon Component Overview</span></span>](notifyicon-component-overview-windows-forms.md)
