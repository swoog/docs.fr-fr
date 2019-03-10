---
title: 'Procédure : Définir une icône pour un bouton de barre d’outils'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- toolbars [Windows Forms], adding icons to buttons
- buttons [Windows Forms], icons
- examples [Windows Forms], toolbars
- images [Windows Forms], toolbar buttons
- icons [Windows Forms], toolbar buttons
- ToolBar control [Windows Forms], adding icons to buttons
ms.assetid: 84db98b4-8566-49ce-b2c8-1fd66a5eb3a0
ms.openlocfilehash: fb4a492b081cd9f9e3ccc1d47a4120c705058dd0
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57712745"
---
# <a name="how-to-define-an-icon-for-a-toolbar-button"></a><span data-ttu-id="fc518-102">Procédure : Définir une icône pour un bouton de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="fc518-102">How to: Define an Icon for a ToolBar Button</span></span>
> [!NOTE]
>  <span data-ttu-id="fc518-103">Le contrôle <xref:System.Windows.Forms.ToolStrip> remplace le contrôle <xref:System.Windows.Forms.ToolBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.ToolBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="fc518-103">The <xref:System.Windows.Forms.ToolStrip> control replaces and adds functionality to the <xref:System.Windows.Forms.ToolBar> control; however, the <xref:System.Windows.Forms.ToolBar> control is retained for both backward compatibility and future use, if you choose.</span></span>  
  
 <span data-ttu-id="fc518-104"><xref:System.Windows.Forms.ToolBar> boutons sont en mesure d’afficher des icônes pour faciliter l’identification par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fc518-104"><xref:System.Windows.Forms.ToolBar> buttons are able to display icons within them for easy identification by users.</span></span> <span data-ttu-id="fc518-105">Pour cela ajouter des images à la [composant ImageList](imagelist-component-windows-forms.md) composant et en l’associant le <xref:System.Windows.Forms.ImageList> composant portant le <xref:System.Windows.Forms.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="fc518-105">This is achieved through adding images to the [ImageList Component](imagelist-component-windows-forms.md) component and then associating the <xref:System.Windows.Forms.ImageList> component with the <xref:System.Windows.Forms.ToolBar> control.</span></span>  
  
### <a name="to-set-an-icon-for-a-toolbar-button-programmatically"></a><span data-ttu-id="fc518-106">Pour définir une icône pour un bouton de barre d’outils par programmation</span><span class="sxs-lookup"><span data-stu-id="fc518-106">To set an icon for a toolbar button programmatically</span></span>  
  
1.  <span data-ttu-id="fc518-107">Dans une procédure, instanciez un <xref:System.Windows.Forms.ImageList> composant et un <xref:System.Windows.Forms.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="fc518-107">In a procedure, instantiate an <xref:System.Windows.Forms.ImageList> component and a <xref:System.Windows.Forms.ToolBar> control.</span></span>  
  
2.  <span data-ttu-id="fc518-108">Dans la même procédure, assignez une image à la <xref:System.Windows.Forms.ImageList> composant.</span><span class="sxs-lookup"><span data-stu-id="fc518-108">In the same procedure, assign an image to the <xref:System.Windows.Forms.ImageList> component.</span></span>  
  
3.  <span data-ttu-id="fc518-109">Dans la même procédure, assignez le <xref:System.Windows.Forms.ImageList> le contrôle à la <xref:System.Windows.Forms.ToolBar> contrôler et d’affecter le <xref:System.Windows.Forms.ToolBarButton.ImageIndex%2A> propriété des boutons de barre d’outils individuels.</span><span class="sxs-lookup"><span data-stu-id="fc518-109">In the same procedure, assign the <xref:System.Windows.Forms.ImageList> control to the <xref:System.Windows.Forms.ToolBar> control and assign the <xref:System.Windows.Forms.ToolBarButton.ImageIndex%2A> property of the individual toolbar buttons.</span></span>  
  
     <span data-ttu-id="fc518-110">Dans l’exemple de code suivant, le chemin d’accès défini pour l’emplacement de l’image est la **Mes Documents** dossier.</span><span class="sxs-lookup"><span data-stu-id="fc518-110">In the following code example, the path set for the location of the image is the **My Documents** folder.</span></span> <span data-ttu-id="fc518-111">Pour cela, étant donné que vous pouvez supposer que la plupart des ordinateurs exécutant le système d’exploitation Windows incluent ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="fc518-111">This is done, because you can assume that most computers running the Windows operating system will include this directory.</span></span> <span data-ttu-id="fc518-112">Cela permet également aux utilisateurs avec des niveaux d’accès minimum au système d’exécuter l’application en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="fc518-112">This also allows users with minimal system access levels to safely run the application.</span></span> <span data-ttu-id="fc518-113">L’exemple suivant suppose un formulaire avec un <xref:System.Windows.Forms.PictureBox> contrôle déjà ajouté.</span><span class="sxs-lookup"><span data-stu-id="fc518-113">The example below assumes a form with a <xref:System.Windows.Forms.PictureBox> control already added.</span></span>  
  
     <span data-ttu-id="fc518-114">En suivant les étapes ci-dessus, doit avoir écrit un code semblable à celui affiché ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fc518-114">Following the steps above, you should have written code similar to that displayed below.</span></span>  
  
    ```vb  
    Public Sub InitializeMyToolBar()  
    ' Instantiate an ImageList component and a ToolBar control.  
       Dim ToolBar1 as New ToolBar  
       Dim ImageList1 as New ImageList  
    ' Assign an image to the ImageList component.  
    ' You should replace the bold image  
    ' in the sample below with an icon of your own choosing.  
       Dim myImage As System.Drawing.Image = _   
          Image.FromFile Image.FromFile _  
          (System.Environment.GetFolderPath _  
          (System.Environment.SpecialFolder.Personal) _  
          & "\Image.gif")  
       ImageList1.Images.Add(myImage)  
    ' Create a ToolBarButton.  
       Dim ToolBarButton1 As New ToolBarButton()  
    ' Add the ToolBarButton to the ToolBar.  
       ToolBar1.Buttons.Add(toolBarButton1)  
    ' Assign an ImageList to the ToolBar.  
       ToolBar1.ImageList = ImageList1  
    ' Assign the ImageIndex property of the ToolBarButton.  
       ToolBarButton1.ImageIndex = 0  
    End Sub  
    ```  
  
    ```csharp  
    public void InitializeMyToolBar()  
    {  
       // Instantiate an ImageList component and a ToolBar control.  
       ToolBar toolBar1 = new  ToolBar();   
       ImageList imageList1 = new ImageList();  
       // Assign an image to the ImageList component.  
       // You should replace the bold image   
       // in the sample below with an icon of your own choosing.  
       // Note the escape character used (@) when specifying the path.  
       Image myImage = Image.FromFile  
       (System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.Personal)  
       + @"\Image.gif");  
       imageList1.Images.Add(myImage);  
       // Create a ToolBarButton.  
       ToolBarButton toolBarButton1 = new ToolBarButton();  
       // Add the ToolBarButton to the ToolBar.  
       toolBar1.Buttons.Add(toolBarButton1);  
       // Assign an ImageList to the ToolBar.  
       toolBar1.ImageList = imageList1;  
       // Assign ImageIndex property of the ToolBarButton.  
       toolBarButton1.ImageIndex = 0;  
    }  
    ```  
  
    ```cpp  
    public:  
       void InitializeMyToolBar()  
       {  
          // Instantiate an ImageList component and a ToolBar control.  
          ToolBar ^ toolBar1 = gcnew  ToolBar();   
          ImageList ^ imageList1 = gcnew ImageList();  
          // Assign an image to the ImageList component.  
          // You should replace the bold image   
          // in the sample below with an icon of your own choosing.  
          Image ^ myImage = Image::FromFile(String::Concat  
             (System::Environment::GetFolderPath  
             (System::Environment::SpecialFolder::Personal),  
             "\\Image.gif"));  
          imageList1->Images->Add(myImage);  
          // Create a ToolBarButton.  
          ToolBarButton ^ toolBarButton1 = gcnew ToolBarButton();  
          // Add the ToolBarButton to the ToolBar.  
          toolBar1->Buttons->Add(toolBarButton1);  
          // Assign an ImageList to the ToolBar.  
          toolBar1->ImageList = imageList1;  
          // Assign ImageIndex property of the ToolBarButton.  
          toolBarButton1->ImageIndex = 0;  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="fc518-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc518-115">See also</span></span>
- <xref:System.Windows.Forms.ToolBar>
- [<span data-ttu-id="fc518-116">Guide pratique pour Déclencher des événements de Menu pour les boutons de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="fc518-116">How to: Trigger Menu Events for Toolbar Buttons</span></span>](how-to-trigger-menu-events-for-toolbar-buttons.md)
- [<span data-ttu-id="fc518-117">ToolBar, contrôle</span><span class="sxs-lookup"><span data-stu-id="fc518-117">ToolBar Control</span></span>](toolbar-control-windows-forms.md)
- [<span data-ttu-id="fc518-118">ImageList, composant</span><span class="sxs-lookup"><span data-stu-id="fc518-118">ImageList Component</span></span>](imagelist-component-windows-forms.md)
