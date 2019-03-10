---
title: 'Procédure : Charge et affichage métafichiers'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], metafiles
- metafiles [Windows Forms], displaying
ms.assetid: 60af1714-f148-4d85-a739-0557965ffa73
ms.openlocfilehash: 121f285a95d0169db79bdc302d80dba03b3b40c2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57720041"
---
# <a name="how-to-load-and-display-metafiles"></a><span data-ttu-id="a3f90-102">Procédure : Charge et affichage métafichiers</span><span class="sxs-lookup"><span data-stu-id="a3f90-102">How to: Load and Display Metafiles</span></span>
<span data-ttu-id="a3f90-103">Le <xref:System.Drawing.Imaging.Metafile> (classe), qui hérite de la <xref:System.Drawing.Image> class, fournit des méthodes pour l’enregistrement, d’affichage et examen d’images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="a3f90-103">The <xref:System.Drawing.Imaging.Metafile> class, which inherits from the <xref:System.Drawing.Image> class, provides methods for recording, displaying, and examining vector images.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3f90-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3f90-104">Example</span></span>  
 <span data-ttu-id="a3f90-105">Pour afficher une image vectorielle (métafichier) sur l’écran, vous devez un <xref:System.Drawing.Imaging.Metafile> objet et un <xref:System.Drawing.Graphics> objet.</span><span class="sxs-lookup"><span data-stu-id="a3f90-105">To display a vector image (metafile) on the screen, you need a <xref:System.Drawing.Imaging.Metafile> object and a <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="a3f90-106">Passez le nom d’un fichier (ou un flux de données) à un <xref:System.Drawing.Imaging.Metafile> constructeur.</span><span class="sxs-lookup"><span data-stu-id="a3f90-106">Pass the name of a file (or a stream) to a <xref:System.Drawing.Imaging.Metafile> constructor.</span></span> <span data-ttu-id="a3f90-107">Après avoir créé un <xref:System.Drawing.Imaging.Metafile> d’objet, qui passez <xref:System.Drawing.Imaging.Metafile> de l’objet à la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet.</span><span class="sxs-lookup"><span data-stu-id="a3f90-107">After you have created a <xref:System.Drawing.Imaging.Metafile> object, pass that <xref:System.Drawing.Imaging.Metafile> object to the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object.</span></span>  
  
 <span data-ttu-id="a3f90-108">L’exemple crée un <xref:System.Drawing.Imaging.Metafile> objet à partir d’un fichier EMF (métafichier amélioré), puis dessine l’image avec son coin supérieur gauche à (60, 10).</span><span class="sxs-lookup"><span data-stu-id="a3f90-108">The example creates a <xref:System.Drawing.Imaging.Metafile> object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10).</span></span>  
  
 <span data-ttu-id="a3f90-109">L’illustration suivante montre le métafichier dessiné à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3f90-109">The following illustration shows the metafile drawn at the specified location.</span></span>  
  
 <span data-ttu-id="a3f90-110">![Position de l’image](./media/imageposition2.png "imageposition2")</span><span class="sxs-lookup"><span data-stu-id="a3f90-110">![Image Position](./media/imageposition2.png "imageposition2")</span></span>  
  
 [!code-csharp[System.Drawing.WorkingWithImages#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.WorkingWithImages#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a3f90-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="a3f90-111">Compiling the Code</span></span>  
 <span data-ttu-id="a3f90-112">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="a3f90-112">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3f90-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f90-113">See also</span></span>
- [<span data-ttu-id="a3f90-114">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="a3f90-114">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
