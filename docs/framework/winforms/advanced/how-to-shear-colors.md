---
title: 'Procédure : incliner des couleurs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], transforming with color matrices
- colors [Windows Forms], shearing
ms.assetid: 0a424171-5b8b-45c4-afef-e9720a6c3e22
ms.openlocfilehash: bf645cf88c4905cd5cf47c2a6c7af088fa428c8a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076241"
---
# <a name="how-to-shear-colors"></a><span data-ttu-id="f1974-102">Procédure : incliner des couleurs</span><span class="sxs-lookup"><span data-stu-id="f1974-102">How to: Shear Colors</span></span>
<span data-ttu-id="f1974-103">L’inclinaison augmente ou diminue d’un composant de couleur d’un montant proportionnel à un autre composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="f1974-103">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="f1974-104">Par exemple, considérez la transformation où le composant rouge est augmenté par la moitié de la valeur du composant bleu.</span><span class="sxs-lookup"><span data-stu-id="f1974-104">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="f1974-105">Sous une transformation de ce type, la couleur (0,2, 0,5, 1) deviendrait (0,7, 0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="f1974-105">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="f1974-106">Le nouveau composant rouge est 0,2 + (1/2)(1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="f1974-106">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f1974-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f1974-107">Example</span></span>  
 <span data-ttu-id="f1974-108">L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir du fichier ColorBars4.bmp.</span><span class="sxs-lookup"><span data-stu-id="f1974-108">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="f1974-109">Le code applique ensuite la transformation d’inclinaison décrite dans le paragraphe précédent à chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="f1974-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>  
  
 <span data-ttu-id="f1974-110">L’illustration suivante montre l’image d’origine sur la gauche et l’image inclinée sur la droite :</span><span class="sxs-lookup"><span data-stu-id="f1974-110">The following illustration shows the original image on the left and the sheared image on the right:</span></span> 
  
 ![Deux des carrés avec rayures colorée côté à côte illustrant l’image d’origine et l’image inclinée.](./media/how-to-shear-colors/original-image-sheared-image.png)  
  
 <span data-ttu-id="f1974-112">Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la transformation d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="f1974-112">The following table lists the color vectors for the four bars before and after the shearing transformation.</span></span>  
  
|<span data-ttu-id="f1974-113">D'origine</span><span class="sxs-lookup"><span data-stu-id="f1974-113">Original</span></span>|<span data-ttu-id="f1974-114">Inclinée</span><span class="sxs-lookup"><span data-stu-id="f1974-114">Sheared</span></span>|  
|--------------|-------------|  
|<span data-ttu-id="f1974-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-115">(0, 0, 1, 1)</span></span>|<span data-ttu-id="f1974-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-116">(0.5, 0, 1, 1)</span></span>|  
|<span data-ttu-id="f1974-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-117">(0.5, 1, 0.5, 1)</span></span>|<span data-ttu-id="f1974-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-118">(0.75, 1, 0.5, 1)</span></span>|  
|<span data-ttu-id="f1974-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-119">(1, 1, 0, 1)</span></span>|<span data-ttu-id="f1974-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-120">(1, 1, 0, 1)</span></span>|  
|<span data-ttu-id="f1974-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-121">(0.4, 0.4, 0.4, 1)</span></span>|<span data-ttu-id="f1974-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f1974-122">(0.6, 0.4, 0.4, 1)</span></span>|  
  
 [!code-csharp[System.Drawing.Misc3#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Misc3/CS/Form1.cs#9)]
 [!code-vb[System.Drawing.Misc3#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Misc3/VB/Form1.vb#9)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f1974-123">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f1974-123">Compiling the Code</span></span>  
 <span data-ttu-id="f1974-124">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="f1974-124">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="f1974-125">Remplacez `ColorBars.bmp` avec un nom de l’image et le chemin d’accès valide sur votre système.</span><span class="sxs-lookup"><span data-stu-id="f1974-125">Replace `ColorBars.bmp` with an image name and path valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1974-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1974-126">See also</span></span>

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="f1974-127">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f1974-127">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="f1974-128">Recoloriage des images</span><span class="sxs-lookup"><span data-stu-id="f1974-128">Recoloring Images</span></span>](recoloring-images.md)
