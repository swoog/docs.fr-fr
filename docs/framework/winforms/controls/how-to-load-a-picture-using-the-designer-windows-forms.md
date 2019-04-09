---
title: 'Procédure : Charger une image à l’aide du concepteur (Windows Forms)'
ms.date: 03/30/2017
helpviewer_keywords:
- picture formats
- images [Windows Forms], displaying on Windows Forms
- pictures [Windows Forms], displaying
- forms [Windows Forms], displaying images
- PictureBox control [Windows Forms], adding pictures
ms.assetid: 4dc7b973-afb1-4276-8322-20825af96655
ms.openlocfilehash: 5aa8ff1efa045d52382cc5c24a0cae1f0f1bb510
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59127138"
---
# <a name="how-to-load-a-picture-using-the-designer-windows-forms"></a><span data-ttu-id="94329-102">Procédure : Charger une image à l’aide du concepteur (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="94329-102">How to: Load a Picture Using the Designer (Windows Forms)</span></span>
<span data-ttu-id="94329-103">Avec les formulaires Windows <xref:System.Windows.Forms.PictureBox> contrôle, vous pouvez charger et afficher une image sur un formulaire au moment du design en définissant le <xref:System.Windows.Forms.PictureBox.Image%2A> propriété à une image valide.</span><span class="sxs-lookup"><span data-stu-id="94329-103">With the Windows Forms <xref:System.Windows.Forms.PictureBox> control, you can load and display a picture on a form at design time by setting the <xref:System.Windows.Forms.PictureBox.Image%2A> property to a valid picture.</span></span> <span data-ttu-id="94329-104">Le tableau suivant présente les types de fichier acceptables.</span><span class="sxs-lookup"><span data-stu-id="94329-104">The following table shows the acceptable file types.</span></span>  
  
|<span data-ttu-id="94329-105">Type</span><span class="sxs-lookup"><span data-stu-id="94329-105">Type</span></span>|<span data-ttu-id="94329-106">Extension de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="94329-106">File name extension</span></span>|  
|----------|-------------------------|  
|<span data-ttu-id="94329-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="94329-107">Bitmap</span></span>|<span data-ttu-id="94329-108">.bmp</span><span class="sxs-lookup"><span data-stu-id="94329-108">.bmp</span></span>|  
|<span data-ttu-id="94329-109">Icône</span><span class="sxs-lookup"><span data-stu-id="94329-109">Icon</span></span>|<span data-ttu-id="94329-110">.ico</span><span class="sxs-lookup"><span data-stu-id="94329-110">.ico</span></span>|  
|<span data-ttu-id="94329-111">GIF</span><span class="sxs-lookup"><span data-stu-id="94329-111">GIF</span></span>|<span data-ttu-id="94329-112">.gif</span><span class="sxs-lookup"><span data-stu-id="94329-112">.gif</span></span>|  
|<span data-ttu-id="94329-113">Métafichier</span><span class="sxs-lookup"><span data-stu-id="94329-113">Metafile</span></span>|<span data-ttu-id="94329-114">.wmf</span><span class="sxs-lookup"><span data-stu-id="94329-114">.wmf</span></span>|  
|<span data-ttu-id="94329-115">JPEG</span><span class="sxs-lookup"><span data-stu-id="94329-115">JPEG</span></span>|<span data-ttu-id="94329-116">.jpg</span><span class="sxs-lookup"><span data-stu-id="94329-116">.jpg</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="94329-117">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="94329-117">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="94329-118">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="94329-118">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="94329-119">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="94329-119">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-display-a-picture-at-design-time"></a><span data-ttu-id="94329-120">Pour afficher une image au moment du design</span><span class="sxs-lookup"><span data-stu-id="94329-120">To display a picture at design time</span></span>  
  
1.  <span data-ttu-id="94329-121">Dessiner un <xref:System.Windows.Forms.PictureBox> contrôle sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="94329-121">Draw a <xref:System.Windows.Forms.PictureBox> control on a form.</span></span>  
  
2.  <span data-ttu-id="94329-122">Dans la fenêtre Propriétés, sélectionnez le <xref:System.Windows.Forms.PictureBox.Image%2A> propriété, puis cliquez sur le bouton de sélection pour afficher la **Open** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="94329-122">On the Properties window, select the <xref:System.Windows.Forms.PictureBox.Image%2A> property, then click the ellipsis button to display the **Open** dialog box.</span></span>  
  
3.  <span data-ttu-id="94329-123">Si vous recherchez un type de fichier spécifique (par exemple, des fichiers .gif), sélectionnez-le dans la **fichiers de type** boîte.</span><span class="sxs-lookup"><span data-stu-id="94329-123">If you are looking for a specific file type (for example, .gif files), select it in the **Files of type** box.</span></span>  
  
4.  <span data-ttu-id="94329-124">Sélectionnez le fichier que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="94329-124">Select the file you want to display.</span></span>  
  
### <a name="to-clear-the-picture-at-design-time"></a><span data-ttu-id="94329-125">Pour effacer l’image au moment du design</span><span class="sxs-lookup"><span data-stu-id="94329-125">To clear the picture at design time</span></span>  
  
1.  <span data-ttu-id="94329-126">Sur le **propriétés** fenêtre, sélectionnez le <xref:System.Windows.Forms.PictureBox.Image%2A> propriété et clic droit de l’image miniature qui s’affiche à gauche du nom de l’objet image.</span><span class="sxs-lookup"><span data-stu-id="94329-126">On the **Properties** window, select the <xref:System.Windows.Forms.PictureBox.Image%2A> property and right-click the small thumbnail image that appears to the left of the name of the image object.</span></span> <span data-ttu-id="94329-127">Choisissez **réinitialiser**.</span><span class="sxs-lookup"><span data-stu-id="94329-127">Choose **Reset**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94329-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94329-128">See also</span></span>

- <xref:System.Windows.Forms.PictureBox>
- [<span data-ttu-id="94329-129">Vue d’ensemble du contrôle PictureBox</span><span class="sxs-lookup"><span data-stu-id="94329-129">PictureBox Control Overview</span></span>](picturebox-control-overview-windows-forms.md)
- [<span data-ttu-id="94329-130">Procédure : modifier la taille ou l’emplacement d’une image au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="94329-130">How to: Modify the Size or Placement of a Picture at Run Time</span></span>](how-to-modify-the-size-or-placement-of-a-picture-at-run-time-windows-forms.md)
- [<span data-ttu-id="94329-131">Procédure : définir des images au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="94329-131">How to: Set Pictures at Run Time</span></span>](how-to-set-pictures-at-run-time-windows-forms.md)
- [<span data-ttu-id="94329-132">PictureBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="94329-132">PictureBox Control</span></span>](picturebox-control-windows-forms.md)
