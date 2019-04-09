---
title: 'Procédure : obtenir des métriques de polices'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], obtaining metrics
- font metrics [Windows Forms], obtaining
ms.assetid: ff7c0616-67f7-4fa2-84ee-b8d642f2b09b
ms.openlocfilehash: 24cada3962339cae0608bbe01e070a0b8e256e73
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59119052"
---
# <a name="how-to-obtain-font-metrics"></a><span data-ttu-id="e0493-102">Procédure : obtenir des métriques de polices</span><span class="sxs-lookup"><span data-stu-id="e0493-102">How to: Obtain Font Metrics</span></span>
<span data-ttu-id="e0493-103">Le <xref:System.Drawing.FontFamily> classe fournit les méthodes suivantes qui récupèrent diverses métriques pour une combinaison famille/style particulière :</span><span class="sxs-lookup"><span data-stu-id="e0493-103">The <xref:System.Drawing.FontFamily> class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>  
  
-   <xref:System.Drawing.FontFamily.GetEmHeight%2A><span data-ttu-id="e0493-104">(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="e0493-104">(FontStyle)</span></span>  
  
-   <xref:System.Drawing.FontFamily.GetCellAscent%2A><span data-ttu-id="e0493-105">(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="e0493-105">(FontStyle)</span></span>  
  
-   <xref:System.Drawing.FontFamily.GetCellDescent%2A><span data-ttu-id="e0493-106">(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="e0493-106">(FontStyle)</span></span>  
  
-   <xref:System.Drawing.FontFamily.GetLineSpacing%2A><span data-ttu-id="e0493-107">(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="e0493-107">(FontStyle)</span></span>  
  
 <span data-ttu-id="e0493-108">Les nombres retournés par ces méthodes sont en unités de design de police, afin qu’ils soient indépendants de la taille et les unités d’un particulier <xref:System.Drawing.Font> objet.</span><span class="sxs-lookup"><span data-stu-id="e0493-108">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular <xref:System.Drawing.Font> object.</span></span>  
  
 <span data-ttu-id="e0493-109">L’illustration suivante montre les différentes mesures.</span><span class="sxs-lookup"><span data-stu-id="e0493-109">The following illustration shows the various metrics.</span></span>  
  
 <span data-ttu-id="e0493-110">![Polices du texte](./media/fontstext7a.png "fontstext7A")</span><span class="sxs-lookup"><span data-stu-id="e0493-110">![Fonts Text](./media/fontstext7a.png "fontstext7A")</span></span>  
  
## <a name="example"></a><span data-ttu-id="e0493-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0493-111">Example</span></span>  
 <span data-ttu-id="e0493-112">L’exemple suivant affiche les métriques pour le style normal de la famille de polices Arial.</span><span class="sxs-lookup"><span data-stu-id="e0493-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="e0493-113">Le code crée également un <xref:System.Drawing.Font> objet (basé sur la famille Arial) avec la taille de 16 pixels et affiche la métrique (en pixels) pour ce particulier <xref:System.Drawing.Font> objet.</span><span class="sxs-lookup"><span data-stu-id="e0493-113">The code also creates a <xref:System.Drawing.Font> object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular <xref:System.Drawing.Font> object.</span></span>  
  
 <span data-ttu-id="e0493-114">L’illustration suivante montre la sortie de l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="e0493-114">The following illustration shows the output of the example code.</span></span>  
  
 <span data-ttu-id="e0493-115">![Fonts Text](./media/csfontstext8.png "csFontsText8")</span><span class="sxs-lookup"><span data-stu-id="e0493-115">![Fonts Text](./media/csfontstext8.png "csFontsText8")</span></span>  
  
 <span data-ttu-id="e0493-116">Notez les deux premières lignes de sortie dans l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="e0493-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="e0493-117">Le <xref:System.Drawing.Font> objet renvoie une taille de 16 et le <xref:System.Drawing.FontFamily> objet retourne une hauteur de 2 048.</span><span class="sxs-lookup"><span data-stu-id="e0493-117">The <xref:System.Drawing.Font> object returns a size of 16, and the <xref:System.Drawing.FontFamily> object returns an em height of 2,048.</span></span> <span data-ttu-id="e0493-118">Ces deux nombres (16 et 2 048) sont la clé à la conversion entre les unités de design de police et les unités (dans ce cas des pixels) de la <xref:System.Drawing.Font> objet.</span><span class="sxs-lookup"><span data-stu-id="e0493-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the <xref:System.Drawing.Font> object.</span></span>  
  
 <span data-ttu-id="e0493-119">Par exemple, vous pouvez convertir le jambage ascendant à partir d’unités de design pixels comme suit :</span><span class="sxs-lookup"><span data-stu-id="e0493-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>  
  
 <span data-ttu-id="e0493-120">![Polices du texte](./media/fontstext9.png "FontsText9")</span><span class="sxs-lookup"><span data-stu-id="e0493-120">![Fonts Text](./media/fontstext9.png "FontsText9")</span></span>  
  
 <span data-ttu-id="e0493-121">Le code suivant positionne le texte verticalement en définissant le <xref:System.Drawing.PointF.Y%2A> membre de données d’un <xref:System.Drawing.PointF> objet.</span><span class="sxs-lookup"><span data-stu-id="e0493-121">The following code positions text vertically by setting the <xref:System.Drawing.PointF.Y%2A> data member of a <xref:System.Drawing.PointF> object.</span></span> <span data-ttu-id="e0493-122">La coordonnée y est augmentée `font.Height` pour chaque nouvelle ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="e0493-122">The y-coordinate is increased by `font.Height` for each new line of text.</span></span> <span data-ttu-id="e0493-123">Le <xref:System.Drawing.Font.Height%2A> propriété d’un <xref:System.Drawing.Font> objet retourne l’interligne (en pixels) pour ce particulier <xref:System.Drawing.Font> objet.</span><span class="sxs-lookup"><span data-stu-id="e0493-123">The <xref:System.Drawing.Font.Height%2A> property of a <xref:System.Drawing.Font> object returns the line spacing (in pixels) for that particular <xref:System.Drawing.Font> object.</span></span> <span data-ttu-id="e0493-124">Dans cet exemple, le nombre retourné par <xref:System.Drawing.Font.Height%2A> est 19.</span><span class="sxs-lookup"><span data-stu-id="e0493-124">In this example, the number returned by <xref:System.Drawing.Font.Height%2A> is 19.</span></span> <span data-ttu-id="e0493-125">Notez que cela est le même que le nombre (arrondi à un entier) obtenu en convertissant la métrique d’interligne en pixels.</span><span class="sxs-lookup"><span data-stu-id="e0493-125">Note that this is the same as the number (rounded up to an integer) obtained by converting the line-spacing metric to pixels.</span></span>  
  
 <span data-ttu-id="e0493-126">Notez que la hauteur du carré cadratin (également appelée taille taille ou em) n’est pas la somme de la hauteur et de la profondeur.</span><span class="sxs-lookup"><span data-stu-id="e0493-126">Note that the em height (also called size or em size) is not the sum of the ascent and the descent.</span></span> <span data-ttu-id="e0493-127">La somme de la hauteur et de la profondeur est appelée la hauteur de cellule.</span><span class="sxs-lookup"><span data-stu-id="e0493-127">The sum of the ascent and the descent is called the cell height.</span></span> <span data-ttu-id="e0493-128">La hauteur de cellule moins l’espacement interne est égale à la hauteur du carré cadratin.</span><span class="sxs-lookup"><span data-stu-id="e0493-128">The cell height minus the internal leading is equal to the em height.</span></span> <span data-ttu-id="e0493-129">La hauteur de cellule plus l’espacement externe est égale à l’interligne.</span><span class="sxs-lookup"><span data-stu-id="e0493-129">The cell height plus the external leading is equal to the line spacing.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.FontsAndText#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e0493-130">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e0493-130">Compiling the Code</span></span>  
 <span data-ttu-id="e0493-131">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="e0493-131">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0493-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0493-132">See also</span></span>

- [<span data-ttu-id="e0493-133">Graphiques et dessins dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e0493-133">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="e0493-134">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="e0493-134">Using Fonts and Text</span></span>](using-fonts-and-text.md)
