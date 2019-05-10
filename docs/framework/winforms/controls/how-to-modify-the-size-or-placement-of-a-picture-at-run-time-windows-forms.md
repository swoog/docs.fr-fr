---
title: 'Procédure : Modifier la taille ou l’emplacement d’une image au moment de l’exécution (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- images [Windows Forms], controlling placement in PictureBox control [Windows Forms]
- examples [Windows Forms], PictureBox control
- PictureBox control [Windows Forms], picture size and alignment
- pictures [Windows Forms], controlling placement in PictureBox control [Windows Forms]
ms.assetid: d0b332a3-fae2-4891-957c-dc3e17743326
ms.openlocfilehash: 695abf51870ef9164e4543a91b3183e801eee55f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64649251"
---
# <a name="how-to-modify-the-size-or-placement-of-a-picture-at-run-time-windows-forms"></a><span data-ttu-id="84b2c-102">Procédure : Modifier la taille ou l’emplacement d’une image au moment de l’exécution (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="84b2c-102">How to: Modify the Size or Placement of a Picture at Run Time (Windows Forms)</span></span>
<span data-ttu-id="84b2c-103">Si vous utilisez les formulaires Windows <xref:System.Windows.Forms.PictureBox> contrôle sur un formulaire, vous pouvez définir le <xref:System.Windows.Forms.PictureBox.SizeMode%2A> propriété dessus pour :</span><span class="sxs-lookup"><span data-stu-id="84b2c-103">If you use the Windows Forms <xref:System.Windows.Forms.PictureBox> control on a form, you can set the <xref:System.Windows.Forms.PictureBox.SizeMode%2A> property on it to:</span></span>  
  
- <span data-ttu-id="84b2c-104">Aligner le coin supérieur gauche de l’image sur l’angle supérieur gauche du contrôle</span><span class="sxs-lookup"><span data-stu-id="84b2c-104">Align the picture's upper left corner with the control's upper left corner</span></span>  
  
- <span data-ttu-id="84b2c-105">Centrer l’image dans le contrôle</span><span class="sxs-lookup"><span data-stu-id="84b2c-105">Center the picture within the control</span></span>  
  
- <span data-ttu-id="84b2c-106">Ajuster la taille du contrôle en fonction de l’image que s’affiche</span><span class="sxs-lookup"><span data-stu-id="84b2c-106">Adjust the size of the control to fit the picture it displays</span></span>  
  
- <span data-ttu-id="84b2c-107">Étirer une image, il s’affiche pour ajuster le contrôle</span><span class="sxs-lookup"><span data-stu-id="84b2c-107">Stretch any picture it displays to fit the control</span></span>  
  
 <span data-ttu-id="84b2c-108">Étirement d’une image (en particulier un au format bitmap) peut entraîner une dégradation de qualité d’image.</span><span class="sxs-lookup"><span data-stu-id="84b2c-108">Stretching a picture (especially one in bitmap format) can produce a loss in image quality.</span></span> <span data-ttu-id="84b2c-109">Métafichiers, qui sont des listes d’instructions graphiques pour le dessin d’images au moment de l’exécution, sont mieux adaptées aux étirement que les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="84b2c-109">Metafiles, which are lists of graphics instructions for drawing images at run time, are better suited for stretching than bitmaps are.</span></span>  
  
### <a name="to-set-the-sizemode-property-at-run-time"></a><span data-ttu-id="84b2c-110">Pour définir la propriété SizeMode au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="84b2c-110">To set the SizeMode property at run time</span></span>  
  
1. <span data-ttu-id="84b2c-111">Définissez <xref:System.Windows.Forms.PictureBox.SizeMode%2A> à <xref:System.Windows.Forms.PictureBoxSizeMode.Normal> (la valeur par défaut), <xref:System.Windows.Forms.PictureBoxSizeMode.AutoSize>, <xref:System.Windows.Forms.PictureBoxSizeMode.CenterImage>, ou <xref:System.Windows.Forms.PictureBoxSizeMode.StretchImage>.</span><span class="sxs-lookup"><span data-stu-id="84b2c-111">Set <xref:System.Windows.Forms.PictureBox.SizeMode%2A> to <xref:System.Windows.Forms.PictureBoxSizeMode.Normal> (the default), <xref:System.Windows.Forms.PictureBoxSizeMode.AutoSize>, <xref:System.Windows.Forms.PictureBoxSizeMode.CenterImage>, or <xref:System.Windows.Forms.PictureBoxSizeMode.StretchImage>.</span></span> <span data-ttu-id="84b2c-112"><xref:System.Windows.Forms.PictureBoxSizeMode.Normal> signifie que l’image est placée dans le coin supérieur gauche du contrôle ; Si l’image est plus grande que le contrôle, ses bords inférieurs et droit sont découpés.</span><span class="sxs-lookup"><span data-stu-id="84b2c-112"><xref:System.Windows.Forms.PictureBoxSizeMode.Normal> means that the image is placed in the control's upper-left corner; if the image is larger than the control, its lower and right edges are clipped.</span></span> <span data-ttu-id="84b2c-113"><xref:System.Windows.Forms.PictureBoxSizeMode.CenterImage> signifie que l’image est centrée dans le contrôle ; Si l’image est plus grande que le contrôle, les bords extérieurs sont découpés.</span><span class="sxs-lookup"><span data-stu-id="84b2c-113"><xref:System.Windows.Forms.PictureBoxSizeMode.CenterImage> means that the image is centered within the control; if the image is larger than the control, the picture's outside edges are clipped.</span></span> <span data-ttu-id="84b2c-114"><xref:System.Windows.Forms.PictureBoxSizeMode.AutoSize> signifie que la taille du contrôle est ajustée à la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="84b2c-114"><xref:System.Windows.Forms.PictureBoxSizeMode.AutoSize> means that the size of the control is adjusted to the size of the image.</span></span> <span data-ttu-id="84b2c-115"><xref:System.Windows.Forms.PictureBoxSizeMode.StretchImage> est l’inverse et signifie que la taille de l’image est ajustée à la taille du contrôle.</span><span class="sxs-lookup"><span data-stu-id="84b2c-115"><xref:System.Windows.Forms.PictureBoxSizeMode.StretchImage> is the reverse, and means that the size of the image is adjusted to the size of the control.</span></span>  
  
     <span data-ttu-id="84b2c-116">Dans l’exemple ci-dessous, le chemin d’accès défini pour l’emplacement de l’image est le dossier Mes Documents.</span><span class="sxs-lookup"><span data-stu-id="84b2c-116">In the example below, the path set for the location of the image is the My Documents folder.</span></span> <span data-ttu-id="84b2c-117">Pour cela, étant donné que vous pouvez supposer que la plupart des ordinateurs exécutant le système d’exploitation Windows incluent ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="84b2c-117">This is done, because you can assume that most computers running the Windows operating system will include this directory.</span></span> <span data-ttu-id="84b2c-118">Cela permet également aux utilisateurs avec des niveaux d’accès minimum au système d’exécuter l’application en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="84b2c-118">This also allows users with minimal system access levels to safely run the application.</span></span> <span data-ttu-id="84b2c-119">L’exemple suivant suppose un formulaire avec un <xref:System.Windows.Forms.PictureBox> contrôle déjà ajouté.</span><span class="sxs-lookup"><span data-stu-id="84b2c-119">The example below assumes a form with a <xref:System.Windows.Forms.PictureBox> control already added.</span></span>  
  
    ```vb  
    Private Sub StretchPic()  
       ' Stretch the picture to fit the control.  
       PictureBox1.SizeMode = PictureBoxSizeMode.StretchImage  
       ' Load the picture into the control.  
       ' You should replace the bold image   
       ' in the sample below with an icon of your own choosing.  
       PictureBox1.Image = Image.FromFile _  
       (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\Image.gif")  
    End Sub  
    ```  
  
    ```csharp  
    private void StretchPic(){  
       // Stretch the picture to fit the control.  
       PictureBox1.SizeMode = PictureBoxSizeMode.StretchImage;  
       // Load the picture into the control.  
       // You should replace the bold image   
       // in the sample below with an icon of your own choosing.  
       // Note the escape character used (@) when specifying the path.  
       PictureBox1.Image = Image.FromFile _  
       (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       + @"\Image.gif")  
    }  
    ```  
  
    ```cpp  
    private:  
       void StretchPic()  
       {  
          // Stretch the picture to fit the control.  
          pictureBox1->SizeMode = PictureBoxSizeMode::StretchImage;  
          // Load the picture into the control.  
          // You should replace the bold image   
          // in the sample below with an icon of your own choosing.  
          pictureBox1->Image = Image::FromFile(String::Concat(  
             System::Environment::GetFolderPath(  
             System::Environment::SpecialFolder::Personal),  
             "\\Image.gif"));  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="84b2c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84b2c-120">See also</span></span>

- <xref:System.Windows.Forms.PictureBox>
- [<span data-ttu-id="84b2c-121">Guide pratique pour Charger une image à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="84b2c-121">How to: Load a Picture Using the Designer</span></span>](how-to-load-a-picture-using-the-designer-windows-forms.md)
- [<span data-ttu-id="84b2c-122">Vue d’ensemble du contrôle PictureBox</span><span class="sxs-lookup"><span data-stu-id="84b2c-122">PictureBox Control Overview</span></span>](picturebox-control-overview-windows-forms.md)
- [<span data-ttu-id="84b2c-123">Guide pratique pour Définir des images au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="84b2c-123">How to: Set Pictures at Run Time</span></span>](how-to-set-pictures-at-run-time-windows-forms.md)
- [<span data-ttu-id="84b2c-124">PictureBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="84b2c-124">PictureBox Control</span></span>](picturebox-control-windows-forms.md)
