---
title: 'Procédure : créer un pinceau dégradé linéaire'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- linear gradients [Windows Forms], creating
- gradients [Windows Forms], creating linear
- colors [Windows Forms], creating linear gradients
- gradients
ms.assetid: 6c88e1cc-1217-4399-ac12-cb37592b9f01
ms.openlocfilehash: 953a1944073a8cb5b19ef072e2a523baec3a5605
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64650009"
---
# <a name="how-to-create-a-linear-gradient"></a><span data-ttu-id="e9d53-102">Procédure : créer un pinceau dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="e9d53-102">How to: Create a Linear Gradient</span></span>
<span data-ttu-id="e9d53-103">GDI + fournit des dégradés linéaires horizontales, verticales et diagonales.</span><span class="sxs-lookup"><span data-stu-id="e9d53-103">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="e9d53-104">Par défaut, la couleur d’un dégradé linéaire Modifie uniformément.</span><span class="sxs-lookup"><span data-stu-id="e9d53-104">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="e9d53-105">Toutefois, vous pouvez personnaliser un dégradé linéaire de sorte que la couleur change de façon non uniforme.</span><span class="sxs-lookup"><span data-stu-id="e9d53-105">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>  

> [!NOTE]
> <span data-ttu-id="e9d53-106">Les exemples de cet article sont des méthodes qui sont appelées à partir d’un contrôle <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="e9d53-106">The examples in this article are methods that are called from a control's <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  

<span data-ttu-id="e9d53-107">L’exemple suivant remplit une ligne, une ellipse et un rectangle avec un pinceau de dégradé linéaire horizontal.</span><span class="sxs-lookup"><span data-stu-id="e9d53-107">The following example fills a line, an ellipse, and a rectangle with a horizontal linear gradient brush.</span></span>  
  
<span data-ttu-id="e9d53-108">Le <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructeur reçoit quatre arguments : deux points et deux couleurs.</span><span class="sxs-lookup"><span data-stu-id="e9d53-108">The <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="e9d53-109">Le premier point (0, 10) est associé à la première couleur (rouge), et le deuxième point (200, 10) est associé à la deuxième couleur (bleu).</span><span class="sxs-lookup"><span data-stu-id="e9d53-109">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="e9d53-110">Comme vous pouvez l’imaginer, la ligne dessinée de (0, 10) à (200, 10) passe progressivement du rouge au bleu.</span><span class="sxs-lookup"><span data-stu-id="e9d53-110">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>  
  
 <span data-ttu-id="e9d53-111">Les 10 s dans les points (0, 10) et (200, 10) ne sont pas importants.</span><span class="sxs-lookup"><span data-stu-id="e9d53-111">The 10s in the points (0, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="e9d53-112">L’important est que les deux points ont la même coordonnée deuxième, la ligne qui relie les est horizontale.</span><span class="sxs-lookup"><span data-stu-id="e9d53-112">What is important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="e9d53-113">L’ellipse et rectangle également changer progressivement du rouge au bleu puisque la coordonnée horizontale va de 0 à 200.</span><span class="sxs-lookup"><span data-stu-id="e9d53-113">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>  
  
 <span data-ttu-id="e9d53-114">L’illustration suivante montre la ligne, l’ellipse et le rectangle.</span><span class="sxs-lookup"><span data-stu-id="e9d53-114">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="e9d53-115">Notez que le dégradé de couleur se répète à mesure que la coordonnée horizontale augmente au-delà de 200.</span><span class="sxs-lookup"><span data-stu-id="e9d53-115">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>  
  
 <span data-ttu-id="e9d53-116">![Dégradé linéaire](./media/cslineargradient1.png "cslineargradient1")</span><span class="sxs-lookup"><span data-stu-id="e9d53-116">![Linear Gradient](./media/cslineargradient1.png "cslineargradient1")</span></span>  
  
### <a name="to-use-horizontal-linear-gradients"></a><span data-ttu-id="e9d53-117">Pour utiliser des dégradés linéaires horizontales</span><span class="sxs-lookup"><span data-stu-id="e9d53-117">To use horizontal linear gradients</span></span>  
  
- <span data-ttu-id="e9d53-118">Transmettre l’opaque rouge et le bleu opaque en tant que l’argument troisième et quatrième, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e9d53-118">Pass in the opaque red and opaque blue as the third and fourth argument, respectively.</span></span>  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#21)]
     [!code-vb[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#21)]  
  
 <span data-ttu-id="e9d53-119">Dans l’exemple précédent, les composants de couleur changent linéairement lorsque vous passez de la coordonnée horizontale de 0 à une coordonnée horizontale de 200.</span><span class="sxs-lookup"><span data-stu-id="e9d53-119">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="e9d53-120">Par exemple, un point dont la première coordonnée se trouve à mi-chemin entre 0 et 200 aura un composant bleu qui se trouve à mi-chemin entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="e9d53-120">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>  
  
 <span data-ttu-id="e9d53-121">GDI + vous permet d’ajuster la façon dont une couleur varie d’un bord d’un dégradé à l’autre.</span><span class="sxs-lookup"><span data-stu-id="e9d53-121">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="e9d53-122">Supposons que vous souhaitez créer un pinceau de dégradé qui passe du noir au rouge conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9d53-122">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>  
  
|<span data-ttu-id="e9d53-123">Coordonnée horizontale</span><span class="sxs-lookup"><span data-stu-id="e9d53-123">Horizontal coordinate</span></span>|<span data-ttu-id="e9d53-124">Composants RVB</span><span class="sxs-lookup"><span data-stu-id="e9d53-124">RGB components</span></span>|  
|---------------------------|--------------------|  
|<span data-ttu-id="e9d53-125">0</span><span class="sxs-lookup"><span data-stu-id="e9d53-125">0</span></span>|<span data-ttu-id="e9d53-126">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="e9d53-126">(0, 0, 0)</span></span>|  
|<span data-ttu-id="e9d53-127">40</span><span class="sxs-lookup"><span data-stu-id="e9d53-127">40</span></span>|<span data-ttu-id="e9d53-128">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="e9d53-128">(128, 0, 0)</span></span>|  
|<span data-ttu-id="e9d53-129">200</span><span class="sxs-lookup"><span data-stu-id="e9d53-129">200</span></span>|<span data-ttu-id="e9d53-130">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="e9d53-130">(255, 0, 0)</span></span>|  
  
 <span data-ttu-id="e9d53-131">Notez que le composant rouge est à moitié intensité lorsque la coordonnée horizontale est seulement 20 pour cent de la façon de 0 à 200.</span><span class="sxs-lookup"><span data-stu-id="e9d53-131">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>  
  
 <span data-ttu-id="e9d53-132">L’exemple suivant définit le <xref:System.Drawing.Drawing2D.LinearGradientBrush.Blend%2A?displayProperty=nameWithType> propriété à associer trois intensité relative à trois positions relatives.</span><span class="sxs-lookup"><span data-stu-id="e9d53-132">The following example sets the <xref:System.Drawing.Drawing2D.LinearGradientBrush.Blend%2A?displayProperty=nameWithType> property to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="e9d53-133">Comme dans le tableau précédent, une intensité relative de 0,5 est associée à une position relative de 0,2.</span><span class="sxs-lookup"><span data-stu-id="e9d53-133">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="e9d53-134">Le code remplit une ellipse et un rectangle avec le pinceau de dégradé.</span><span class="sxs-lookup"><span data-stu-id="e9d53-134">The code fills an ellipse and a rectangle with the gradient brush.</span></span>  
  
 <span data-ttu-id="e9d53-135">L’illustration suivante montre l’ellipse qui en résulte et un rectangle.</span><span class="sxs-lookup"><span data-stu-id="e9d53-135">The following illustration shows the resulting ellipse and rectangle.</span></span>  
  
 <span data-ttu-id="e9d53-136">![Dégradé linéaire](./media/cslineargradient2.png "cslineargradient2")</span><span class="sxs-lookup"><span data-stu-id="e9d53-136">![Linear Gradient](./media/cslineargradient2.png "cslineargradient2")</span></span>  

### <a name="to-customize-linear-gradients"></a><span data-ttu-id="e9d53-137">Pour personnaliser des dégradés linéaires</span><span class="sxs-lookup"><span data-stu-id="e9d53-137">To customize linear gradients</span></span>  
  
- <span data-ttu-id="e9d53-138">Transmettre la rouge à noir et opaque opaque en tant que l’argument troisième et quatrième, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e9d53-138">Pass in the opaque black and opaque red as the third and fourth argument, respectively.</span></span>  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#22)]
     [!code-vb[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#22)]  
  
 <span data-ttu-id="e9d53-139">Les dégradés dans les exemples précédents ont été horizontales ; Autrement dit, la couleur passe progressivement à mesure que vous déplacez le long de n’importe quelle ligne horizontale.</span><span class="sxs-lookup"><span data-stu-id="e9d53-139">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="e9d53-140">Vous pouvez également définir des dégradés verticaux et en diagonale.</span><span class="sxs-lookup"><span data-stu-id="e9d53-140">You can also define vertical gradients and diagonal gradients.</span></span>  
  
 <span data-ttu-id="e9d53-141">L’exemple suivant passe les points (0, 0) et (200, 100) à un <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="e9d53-141">The following example passes the points (0, 0) and (200, 100) to a <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructor.</span></span> <span data-ttu-id="e9d53-142">Associé à la couleur bleue (0, 0), et est associée à la couleur verte (200, 100).</span><span class="sxs-lookup"><span data-stu-id="e9d53-142">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="e9d53-143">Le pinceau de dégradé linéaire remplit une ligne (largeur du stylet 10) et une ellipse.</span><span class="sxs-lookup"><span data-stu-id="e9d53-143">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>  
  
 <span data-ttu-id="e9d53-144">L’illustration suivante montre la ligne et l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="e9d53-144">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="e9d53-145">Notez que la couleur de l’ellipse change progressivement à mesure que vous déplacez le long d’une ligne qui est parallèle à la ligne passant par (0, 0) et (200, 100).</span><span class="sxs-lookup"><span data-stu-id="e9d53-145">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>  
  
 <span data-ttu-id="e9d53-146">![Dégradé linéaire](./media/cslineargradient3.png "cslineargradient3")</span><span class="sxs-lookup"><span data-stu-id="e9d53-146">![Linear Gradient](./media/cslineargradient3.png "cslineargradient3")</span></span>  
  
### <a name="to-create-diagonal-linear-gradients"></a><span data-ttu-id="e9d53-147">Pour créer des dégradés linéaires en diagonale</span><span class="sxs-lookup"><span data-stu-id="e9d53-147">To create diagonal linear gradients</span></span>  
  
- <span data-ttu-id="e9d53-148">Transmettre l’opaque bleu et le vert opaque en tant que l’argument troisième et quatrième, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e9d53-148">Pass in the opaque blue and opaque green as the third and fourth argument, respectively.</span></span>  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#23)]
     [!code-vb[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#23)]  
  
## <a name="see-also"></a><span data-ttu-id="e9d53-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9d53-149">See also</span></span>

- [<span data-ttu-id="e9d53-150">Utilisation d'un pinceau à dégradé pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="e9d53-150">Using a Gradient Brush to Fill Shapes</span></span>](using-a-gradient-brush-to-fill-shapes.md)
- [<span data-ttu-id="e9d53-151">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e9d53-151">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
