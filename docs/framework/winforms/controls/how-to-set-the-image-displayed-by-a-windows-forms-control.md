---
title: 'Procédure : Définir l’Image affichée par un Windows Forms de contrôle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Button control [Windows Forms], images
- Windows Forms controls, images
- controls [Windows Forms], images
- images [Windows Forms], Windows Forms controls
- examples [Windows Forms], controls
ms.assetid: 9445af8f-4f62-48b0-a3f6-068058964b9f
ms.openlocfilehash: 93bc7970ce7c287273f8bd7ff50b07c6658e2a08
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644922"
---
# <a name="how-to-set-the-image-displayed-by-a-windows-forms-control"></a><span data-ttu-id="04f26-102">Procédure : Définir l’Image affichée par un Windows Forms de contrôle</span><span class="sxs-lookup"><span data-stu-id="04f26-102">How to: Set the Image Displayed by a Windows Forms Control</span></span>
<span data-ttu-id="04f26-103">Plusieurs contrôles Windows Forms peuvent afficher des images.</span><span class="sxs-lookup"><span data-stu-id="04f26-103">Several Windows Forms controls can display images.</span></span> <span data-ttu-id="04f26-104">Ces images peuvent être des icônes qui clarifient l’objectif du contrôle, par exemple une icône de disquette sur un bouton qui dénote le **enregistrer** commande.</span><span class="sxs-lookup"><span data-stu-id="04f26-104">These images can be icons that clarify the purpose of the control, such as a diskette icon on a button denoting the **Save** command.</span></span> <span data-ttu-id="04f26-105">Les icônes peuvent être également des images d’arrière-plan pour donner le contrôle l’apparence et le comportement de que votre choix.</span><span class="sxs-lookup"><span data-stu-id="04f26-105">Alternatively, the icons can be background images to give the control the appearance and behavior you want.</span></span>  
  
### <a name="to-set-the-image-displayed-by-a-control"></a><span data-ttu-id="04f26-106">Pour définir l’image affichée par un contrôle</span><span class="sxs-lookup"><span data-stu-id="04f26-106">To set the image displayed by a control</span></span>  
  
1.  <span data-ttu-id="04f26-107">Définir le contrôle `Image` ou `BackgroundImage` propriété à un objet de type <xref:System.Drawing.Image>.</span><span class="sxs-lookup"><span data-stu-id="04f26-107">Set the control's `Image` or `BackgroundImage` property to an object of type <xref:System.Drawing.Image>.</span></span> <span data-ttu-id="04f26-108">En règle générale, vous chargez l’image à partir d’un fichier à l’aide de la <xref:System.Drawing.Image.FromFile%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="04f26-108">Generally, you will be loading the image from a file by using the <xref:System.Drawing.Image.FromFile%2A> method.</span></span>  
  
     <span data-ttu-id="04f26-109">Dans l’exemple de code suivant, le chemin d’accès défini pour l’emplacement de l’image est la **Mes images** dossier.</span><span class="sxs-lookup"><span data-stu-id="04f26-109">In the following code example, the path set for the location of the image is the **My Pictures** folder.</span></span> <span data-ttu-id="04f26-110">La plupart des ordinateurs exécutant le système d’exploitation Windows incluent ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="04f26-110">Most computers running the Windows operating system will include this directory.</span></span> <span data-ttu-id="04f26-111">Cela permet également aux utilisateurs avec des niveaux d’accès système minimal exécuter l’application en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="04f26-111">This also enables users with minimal system access levels to run the application safely.</span></span> <span data-ttu-id="04f26-112">L’exemple de code suivant requiert que vous disposez déjà d’un formulaire avec un <xref:System.Windows.Forms.PictureBox> contrôle ajouté.</span><span class="sxs-lookup"><span data-stu-id="04f26-112">The following code example requires that you already have a form with a <xref:System.Windows.Forms.PictureBox> control added.</span></span>  
  
    ```vb  
    ' Replace the image named below  
    ' with an icon of your own choosing.  
    PictureBox1.Image = Image.FromFile _  
       (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.MyPictures) _  
       & "\Image.gif")  
    ```  
  
    ```csharp  
    // Replace the image named below  
    // with an icon of your own choosing.  
    // Note the escape character used (@) when specifying the path.  
    pictureBox1.Image = Image.FromFile  
       (System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.MyPictures)  
       + @"\Image.gif");  
    ```  
  
    ```cpp  
    // Replace the image named below  
    // with an icon of your own choosing.  
    pictureBox1->Image = Image::FromFile(String::Concat  
       (System::Environment::GetFolderPath  
       (System::Environment::SpecialFolder::MyPictures),  
       "\\Image.gif"));  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="04f26-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04f26-113">See also</span></span>
- <xref:System.Drawing.Image.FromFile%2A>
- <xref:System.Drawing.Image>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
