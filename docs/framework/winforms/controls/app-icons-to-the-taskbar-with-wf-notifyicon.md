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
ms.openlocfilehash: 18a78b7ecb5268463607508869e77fa163cbd06f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59146443"
---
# <a name="how-to-add-application-icons-to-the-taskbar-with-the-windows-forms-notifyicon-component"></a><span data-ttu-id="ca223-102">Procédure : ajouter des icônes d’application à la barre des tâches avec le composant NotifyIcon Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca223-102">How to: Add Application Icons to the TaskBar with the Windows Forms NotifyIcon Component</span></span>
<span data-ttu-id="ca223-103">Les formulaires Windows <xref:System.Windows.Forms.NotifyIcon> composant affiche une icône dans la zone de notification d’état de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="ca223-103">The Windows Forms <xref:System.Windows.Forms.NotifyIcon> component displays a single icon in the status notification area of the taskbar.</span></span> <span data-ttu-id="ca223-104">Pour afficher plusieurs icônes dans la zone d’état, vous devez disposer de plusieurs <xref:System.Windows.Forms.NotifyIcon> composants sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="ca223-104">To display multiple icons in the status area, you must have multiple <xref:System.Windows.Forms.NotifyIcon> components on your form.</span></span> <span data-ttu-id="ca223-105">Pour définir l’icône affichée pour un contrôle, utilisez le <xref:System.Windows.Forms.NotifyIcon.Icon%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ca223-105">To set the icon displayed for a control, use the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property.</span></span> <span data-ttu-id="ca223-106">Vous pouvez également écrire du code le <xref:System.Windows.Forms.NotifyIcon.DoubleClick> Gestionnaire d’événements afin que quelque chose se produit lorsque l’utilisateur double-clique sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="ca223-106">You can also write code in the <xref:System.Windows.Forms.NotifyIcon.DoubleClick> event handler so that something happens when the user double-clicks the icon.</span></span> <span data-ttu-id="ca223-107">Par exemple, vous pouvez créer une boîte de dialogue s’affichent pour l’utilisateur de configurer le processus d’arrière-plan représenté par l’icône.</span><span class="sxs-lookup"><span data-stu-id="ca223-107">For example, you could make a dialog box appear for the user to configure the background process represented by the icon.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ca223-108">Le <xref:System.Windows.Forms.NotifyIcon> composant est utilisé pour la notification uniquement, pour informer les utilisateurs qu’une action ou un événement s’est produite ou il y a eu un changement d’état quelconque.</span><span class="sxs-lookup"><span data-stu-id="ca223-108">The <xref:System.Windows.Forms.NotifyIcon> component is used for notification purposes only, to alert users that an action or event has occurred or there has been a change in status of some sort.</span></span> <span data-ttu-id="ca223-109">Vous devez utiliser les menus, barres d’outils et autres éléments d’interface utilisateur pour l’interaction avec les applications standard.</span><span class="sxs-lookup"><span data-stu-id="ca223-109">You should use menus, toolbars, and other user-interface elements for standard interaction with applications.</span></span>  
  
### <a name="to-set-the-icon"></a><span data-ttu-id="ca223-110">Pour définir l’icône</span><span class="sxs-lookup"><span data-stu-id="ca223-110">To set the icon</span></span>  
  
1.  <span data-ttu-id="ca223-111">Affecter une valeur à la <xref:System.Windows.Forms.NotifyIcon.Icon%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ca223-111">Assign a value to the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property.</span></span> <span data-ttu-id="ca223-112">La valeur doit être de type `System.Drawing.Icon` et peut être chargée à partir d’un fichier .ico.</span><span class="sxs-lookup"><span data-stu-id="ca223-112">The value must be of type `System.Drawing.Icon` and can be loaded from an .ico file.</span></span> <span data-ttu-id="ca223-113">Vous pouvez spécifier le fichier d’icône dans le code ou en cliquant sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.NotifyIcon.Icon%2A> propriété dans le  **Propriétés** fenêtre, puis en sélectionnant le fichier dans le **Open** boîte de dialogue qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ca223-113">You can specify the icon file in code or by clicking the ellipsis button (![VisualStudioEllipsesButton screenshot](../media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property in the **Properties** window, and then selecting the file in the **Open** dialog box that appears.</span></span>  
  
2.  <span data-ttu-id="ca223-114">Affectez à la propriété <xref:System.Windows.Forms.NotifyIcon.Visible%2A> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="ca223-114">Set the <xref:System.Windows.Forms.NotifyIcon.Visible%2A> property to `true`.</span></span>  
  
3.  <span data-ttu-id="ca223-115">Définir le <xref:System.Windows.Forms.NotifyIcon.Text%2A> propriété à une chaîne d’info-bulle appropriée.</span><span class="sxs-lookup"><span data-stu-id="ca223-115">Set the <xref:System.Windows.Forms.NotifyIcon.Text%2A> property to an appropriate ToolTip string.</span></span>  
  
     <span data-ttu-id="ca223-116">Dans l’exemple de code suivant, le chemin d’accès défini pour l’emplacement de l’icône est la **Mes Documents** dossier.</span><span class="sxs-lookup"><span data-stu-id="ca223-116">In the following code example, the path set for the location of the icon is the **My Documents** folder.</span></span> <span data-ttu-id="ca223-117">Cet emplacement est utilisé, car vous pouvez supposer que la plupart des ordinateurs exécutant le système d’exploitation Windows incluent ce dossier.</span><span class="sxs-lookup"><span data-stu-id="ca223-117">This location is used because you can assume that most computers running the Windows operating system will include this folder.</span></span> <span data-ttu-id="ca223-118">Choix de cet emplacement permet également aux utilisateurs avec des niveaux d’accès système minimal en toute sécurité exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="ca223-118">Choosing this location also enables users with minimal system access levels to safely run the application.</span></span> <span data-ttu-id="ca223-119">L’exemple suivant nécessite un formulaire avec un <xref:System.Windows.Forms.NotifyIcon> contrôle déjà ajouté.</span><span class="sxs-lookup"><span data-stu-id="ca223-119">The following example requires a form with a <xref:System.Windows.Forms.NotifyIcon> control already added.</span></span> <span data-ttu-id="ca223-120">Il requiert également un fichier icône nommé `Icon.ico`.</span><span class="sxs-lookup"><span data-stu-id="ca223-120">It also requires an icon file named `Icon.ico`.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="ca223-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca223-121">See also</span></span>

- <xref:System.Windows.Forms.NotifyIcon>
- <xref:System.Windows.Forms.NotifyIcon.Icon%2A>
- [<span data-ttu-id="ca223-122">Procédure : associer un menu contextuel à un composant NotifyIcon Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca223-122">How to: Associate a Shortcut Menu with a Windows Forms NotifyIcon Component</span></span>](how-to-associate-a-shortcut-menu-with-a-windows-forms-notifyicon-component.md)
- [<span data-ttu-id="ca223-123">NotifyIcon, composant</span><span class="sxs-lookup"><span data-stu-id="ca223-123">NotifyIcon Component</span></span>](notifyicon-component-windows-forms.md)
- [<span data-ttu-id="ca223-124">Vue d’ensemble du composant NotifyIcon</span><span class="sxs-lookup"><span data-stu-id="ca223-124">NotifyIcon Component Overview</span></span>](notifyicon-component-overview-windows-forms.md)
