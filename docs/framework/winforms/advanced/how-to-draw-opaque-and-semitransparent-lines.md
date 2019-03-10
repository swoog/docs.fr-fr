---
title: 'Procédure : Dessiner des lignes opaques et translucides'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- transparency [Windows Forms], lines
- lines [Windows Forms], drawing alpha blended
- alpha blending [Windows Forms], drawing lines
ms.assetid: 8f2508af-f495-4223-b5cc-646cbbb520eb
ms.openlocfilehash: 44047b5a35c2ca87f3136d082331d2f31a1abbec
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57721149"
---
# <a name="how-to-draw-opaque-and-semitransparent-lines"></a><span data-ttu-id="f15fa-102">Procédure : Dessiner des lignes opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="f15fa-102">How to: Draw Opaque and Semitransparent Lines</span></span>
<span data-ttu-id="f15fa-103">Quand vous dessinez une ligne, vous devez passer un objet <xref:System.Drawing.Pen> à la méthode <xref:System.Drawing.Graphics.DrawLine%2A> de la classe <xref:System.Drawing.Graphics>.</span><span class="sxs-lookup"><span data-stu-id="f15fa-103">When you draw a line, you must pass a <xref:System.Drawing.Pen> object to the <xref:System.Drawing.Graphics.DrawLine%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="f15fa-104">L'un des paramètres du constructeur <xref:System.Drawing.Pen.%23ctor%2A> est un objet <xref:System.Drawing.Color>.</span><span class="sxs-lookup"><span data-stu-id="f15fa-104">One of the parameters of the <xref:System.Drawing.Pen.%23ctor%2A> constructor is a <xref:System.Drawing.Color> object.</span></span> <span data-ttu-id="f15fa-105">Pour dessiner une ligne opaque, affectez au composant alpha de la couleur la valeur 255.</span><span class="sxs-lookup"><span data-stu-id="f15fa-105">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="f15fa-106">Pour dessiner une ligne translucide, affectez au composant alpha n'importe quelle valeur comprise entre 1 et 254.</span><span class="sxs-lookup"><span data-stu-id="f15fa-106">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>  
  
 <span data-ttu-id="f15fa-107">Quand vous dessinez une ligne translucide sur un arrière-plan, la couleur de la ligne est fusionnée avec les couleurs de l'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f15fa-107">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="f15fa-108">Le composant alpha spécifie comment les couleurs de ligne et de l'arrière-plan sont mélangées ; les valeurs alpha proches de 0 favorisent les couleurs d'arrière-plan, tandis que les valeurs alpha proches de 255 favorisent la couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="f15fa-108">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weight on the line color.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f15fa-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="f15fa-109">Example</span></span>  
 <span data-ttu-id="f15fa-110">L'exemple suivant dessine une bitmap, puis dessine trois lignes qui utilisent la bitmap comme arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f15fa-110">The following example draws a bitmap and then draws three lines that use the bitmap as a background.</span></span> <span data-ttu-id="f15fa-111">La première ligne utilise un composant alpha de 255. Elle est donc opaque.</span><span class="sxs-lookup"><span data-stu-id="f15fa-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="f15fa-112">Les deuxième et troisième lignes utilisent un composant alpha de 128 et sont donc translucides. Vous pouvez voir l'image d'arrière-plan sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="f15fa-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="f15fa-113">L'instruction qui définit la propriété <xref:System.Drawing.Graphics.CompositingQuality%2A> fait en sorte que la fusion pour la troisième ligne s'effectue parallèlement à une correction gamma.</span><span class="sxs-lookup"><span data-stu-id="f15fa-113">The statement that sets the <xref:System.Drawing.Graphics.CompositingQuality%2A> property causes the blending for the third line to be done in conjunction with gamma correction.</span></span>  
  
 <span data-ttu-id="f15fa-114">L'illustration suivante montre la sortie du code suivant.</span><span class="sxs-lookup"><span data-stu-id="f15fa-114">The following illustration shows the output of the following code.</span></span>  
  
 <span data-ttu-id="f15fa-115">![Opaques et translucides](./media/compqualline.png "compqualline")</span><span class="sxs-lookup"><span data-stu-id="f15fa-115">![Opaque and Semitransparent](./media/compqualline.png "compqualline")</span></span>  
  
 [!code-csharp[System.Drawing.AlphaBlending#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.AlphaBlending#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f15fa-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f15fa-116">Compiling the Code</span></span>  
 <span data-ttu-id="f15fa-117">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="f15fa-117">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f15fa-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f15fa-118">See also</span></span>
- [<span data-ttu-id="f15fa-119">Fusion alpha de lignes et de remplissages</span><span class="sxs-lookup"><span data-stu-id="f15fa-119">Alpha Blending Lines and Fills</span></span>](alpha-blending-lines-and-fills.md)
- [<span data-ttu-id="f15fa-120">Guide pratique pour Affecter un arrière-plan Transparent à votre contrôle</span><span class="sxs-lookup"><span data-stu-id="f15fa-120">How to: Give Your Control a Transparent Background</span></span>](../controls/how-to-give-your-control-a-transparent-background.md)
- [<span data-ttu-id="f15fa-121">Guide pratique pour Dessiner avec des pinceaux opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="f15fa-121">How to: Draw with Opaque and Semitransparent Brushes</span></span>](how-to-draw-with-opaque-and-semitransparent-brushes.md)
