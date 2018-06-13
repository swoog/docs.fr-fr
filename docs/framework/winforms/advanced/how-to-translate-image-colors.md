---
title: "Comment : traduire les couleurs d'une image"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], changing colors
- images [Windows Forms], changing colors
- image colors [Windows Forms]
ms.assetid: 2106fb9a-4d60-4dcf-9220-9f189a6c4d19
ms.openlocfilehash: 48f506f76ff6e9ca648822d073b6f6a852b9ca8e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33522534"
---
# <a name="how-to-translate-image-colors"></a><span data-ttu-id="058c8-102">Comment : traduire les couleurs d'une image</span><span class="sxs-lookup"><span data-stu-id="058c8-102">How to: Translate Image Colors</span></span>
<span data-ttu-id="058c8-103">Une traduction ajoute une valeur à une ou plusieurs des quatre composantes de couleur.</span><span class="sxs-lookup"><span data-stu-id="058c8-103">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="058c8-104">Les entrées de matrice de couleurs représentant les traductions sont présentées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="058c8-104">The color matrix entries that represent translations are given in the following table.</span></span>  
  
|<span data-ttu-id="058c8-105">Composant à traduire</span><span class="sxs-lookup"><span data-stu-id="058c8-105">Component to be translated</span></span>|<span data-ttu-id="058c8-106">Entrée de la matrice</span><span class="sxs-lookup"><span data-stu-id="058c8-106">Matrix entry</span></span>|  
|--------------------------------|------------------|  
|<span data-ttu-id="058c8-107">Rouge</span><span class="sxs-lookup"><span data-stu-id="058c8-107">Red</span></span>|<span data-ttu-id="058c8-108">[4][0]</span><span class="sxs-lookup"><span data-stu-id="058c8-108">[4][0]</span></span>|  
|<span data-ttu-id="058c8-109">Vert</span><span class="sxs-lookup"><span data-stu-id="058c8-109">Green</span></span>|<span data-ttu-id="058c8-110">[4][1]</span><span class="sxs-lookup"><span data-stu-id="058c8-110">[4][1]</span></span>|  
|<span data-ttu-id="058c8-111">Bleu</span><span class="sxs-lookup"><span data-stu-id="058c8-111">Blue</span></span>|<span data-ttu-id="058c8-112">[4][2]</span><span class="sxs-lookup"><span data-stu-id="058c8-112">[4][2]</span></span>|  
|<span data-ttu-id="058c8-113">Alpha</span><span class="sxs-lookup"><span data-stu-id="058c8-113">Alpha</span></span>|<span data-ttu-id="058c8-114">[4][3]</span><span class="sxs-lookup"><span data-stu-id="058c8-114">[4][3]</span></span>|  
  
## <a name="example"></a><span data-ttu-id="058c8-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="058c8-115">Example</span></span>  
 <span data-ttu-id="058c8-116">L’exemple suivant construit une <xref:System.Drawing.Image> objet à partir du fichier ColorBars.bmp.</span><span class="sxs-lookup"><span data-stu-id="058c8-116">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars.bmp.</span></span> <span data-ttu-id="058c8-117">Puis le code ajoute 0,75 au composant rouge de chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="058c8-117">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="058c8-118">L’image d’origine est dessinée en même temps que l’image transformée.</span><span class="sxs-lookup"><span data-stu-id="058c8-118">The original image is drawn alongside the transformed image.</span></span>  
  
 <span data-ttu-id="058c8-119">L’illustration suivante montre l’image d’origine sur la gauche et l’image transformée sur la droite.</span><span class="sxs-lookup"><span data-stu-id="058c8-119">The following illustration shows the original image on the left and the transformed image on the right.</span></span>  
  
 <span data-ttu-id="058c8-120">![Traduction des couleurs](../../../../docs/framework/winforms/advanced/media/colortrans2.png "colortrans2")</span><span class="sxs-lookup"><span data-stu-id="058c8-120">![Translate Colors](../../../../docs/framework/winforms/advanced/media/colortrans2.png "colortrans2")</span></span>  
  
 <span data-ttu-id="058c8-121">Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la traduction rouge.</span><span class="sxs-lookup"><span data-stu-id="058c8-121">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="058c8-122">Notez que la valeur maximale pour un composant de couleur est 1, le composant rouge dans la deuxième ligne ne change pas.</span><span class="sxs-lookup"><span data-stu-id="058c8-122">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="058c8-123">(De même, la valeur minimale d’un composant de couleur est 0.)</span><span class="sxs-lookup"><span data-stu-id="058c8-123">(Similarly, the minimum value for a color component is 0.)</span></span>  
  
|<span data-ttu-id="058c8-124">D'origine</span><span class="sxs-lookup"><span data-stu-id="058c8-124">Original</span></span>|<span data-ttu-id="058c8-125">Langue cible</span><span class="sxs-lookup"><span data-stu-id="058c8-125">Translated</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="058c8-126">Noir (0, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-126">Black (0, 0, 0, 1)</span></span>|<span data-ttu-id="058c8-127">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-127">(0.75, 0, 0, 1)</span></span>|  
|<span data-ttu-id="058c8-128">Rouge (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-128">Red (1, 0, 0, 1)</span></span>|<span data-ttu-id="058c8-129">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-129">(1, 0, 0, 1)</span></span>|  
|<span data-ttu-id="058c8-130">Vert (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-130">Green (0, 1, 0, 1)</span></span>|<span data-ttu-id="058c8-131">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-131">(0.75, 1, 0, 1)</span></span>|  
|<span data-ttu-id="058c8-132">Bleu (0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-132">Blue (0, 0, 1, 1)</span></span>|<span data-ttu-id="058c8-133">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="058c8-133">(0.75, 0, 1, 1)</span></span>|  
  
 [!code-csharp[System.Drawing.RecoloringImages#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.RecoloringImages#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="058c8-134">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="058c8-134">Compiling the Code</span></span>  
 <span data-ttu-id="058c8-135">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="058c8-135">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="058c8-136">Remplacez `ColorBars.bmp` avec un nom de fichier image et le chemin d’accès valides sur votre système.</span><span class="sxs-lookup"><span data-stu-id="058c8-136">Replace `ColorBars.bmp` with an image file name and path that are valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="058c8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="058c8-137">See Also</span></span>  
 <xref:System.Drawing.Imaging.ColorMatrix>  
 <xref:System.Drawing.Imaging.ImageAttributes>  
 [<span data-ttu-id="058c8-138">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="058c8-138">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)  
 [<span data-ttu-id="058c8-139">Recoloriage des images</span><span class="sxs-lookup"><span data-stu-id="058c8-139">Recoloring Images</span></span>](../../../../docs/framework/winforms/advanced/recoloring-images.md)
