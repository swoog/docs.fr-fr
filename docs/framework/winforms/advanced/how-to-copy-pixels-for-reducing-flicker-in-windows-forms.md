---
title: 'Procédure : Copier des Pixels pour réduire le scintillement dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitblt
- graphics [Windows Forms], copying
- flicker [Windows Forms], reducing in Windows Forms
- graphics [Windows Forms], reducing flicker
- pixels [Windows Forms], copying
- flicker
- bit-block transfer
ms.assetid: 33b76910-13a3-4521-be98-5c097341ae3b
ms.openlocfilehash: d03a9b79dc2c0ec61bbafe2ff09b5aba7fffc57b
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57719245"
---
# <a name="how-to-copy-pixels-for-reducing-flicker-in-windows-forms"></a><span data-ttu-id="c4d48-102">Procédure : Copier des Pixels pour réduire le scintillement dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c4d48-102">How to: Copy Pixels for Reducing Flicker in Windows Forms</span></span>
<span data-ttu-id="c4d48-103">Lorsque vous animez un graphique simple, les utilisateurs peuvent rencontrer parfois le scintillement ou autres effets visuels indésirables.</span><span class="sxs-lookup"><span data-stu-id="c4d48-103">When you animate a simple graphic, users can sometimes encounter flicker or other undesirable visual effects.</span></span> <span data-ttu-id="c4d48-104">Une pour limiter ce problème consiste à utiliser un processus « bitblt » sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="c4d48-104">One way to limit this problem is to use a "bitblt" process on the graphic.</span></span> <span data-ttu-id="c4d48-105">BitBlt est le « transfert de bloc bits » des données de couleur à partir d’un rectangle d’origine de pixels à un rectangle de destination de pixels.</span><span class="sxs-lookup"><span data-stu-id="c4d48-105">Bitblt is the "bit-block transfer" of the color data from an origin rectangle of pixels to a destination rectangle of pixels.</span></span>  
  
 <span data-ttu-id="c4d48-106">Avec Windows Forms, le processus bitblt s’effectue à l’aide de la <xref:System.Drawing.Graphics.CopyFromScreen%2A> méthode de la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="c4d48-106">With Windows Forms, bitblt is accomplished using the <xref:System.Drawing.Graphics.CopyFromScreen%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="c4d48-107">Dans les paramètres de la méthode, vous spécifiez la source et destination (en tant que points), la taille de la zone doit être copié et l’objet graphics utilisé pour dessiner la nouvelle forme.</span><span class="sxs-lookup"><span data-stu-id="c4d48-107">In the parameters of the method, you specify the source and destination (as points), the size of the area to be copied, and the graphics object used to draw the new shape.</span></span>  
  
 <span data-ttu-id="c4d48-108">Dans l’exemple ci-dessous, une forme est dessinée sur le formulaire dans son <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="c4d48-108">In the example below, a shape is drawn on the form in its <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="c4d48-109">Ensuite, le <xref:System.Drawing.Graphics.CopyFromScreen%2A> méthode est utilisée pour dupliquer la forme.</span><span class="sxs-lookup"><span data-stu-id="c4d48-109">Then, the <xref:System.Drawing.Graphics.CopyFromScreen%2A> method is used to duplicate the shape.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c4d48-110">Définition du formulaire <xref:System.Windows.Forms.Control.DoubleBuffered%2A> propriété `true` rendra le code de graphiques dans le <xref:System.Windows.Forms.Control.Paint> événement être mis en mémoire tampon double.</span><span class="sxs-lookup"><span data-stu-id="c4d48-110">Setting the form's <xref:System.Windows.Forms.Control.DoubleBuffered%2A> property to `true` will make graphics-based code in the <xref:System.Windows.Forms.Control.Paint> event be double-buffered.</span></span> <span data-ttu-id="c4d48-111">Bien que cela n’aura pas les gains de performances apparent lorsque vous utilisez le code ci-dessous, il est quelque chose à prendre en compte lorsque vous travaillez avec le code de manipulation de graphiques plus complexe.</span><span class="sxs-lookup"><span data-stu-id="c4d48-111">While this will not have any discernible performance gains when using the code below, it is something to keep in mind when working with more complex graphics-manipulation code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c4d48-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4d48-112">Example</span></span>  
  
```vb  
Private Sub Form1_Paint(ByVal sender As Object, ByVal e As _  
    System.Windows.Forms.PaintEventArgs) Handles MyBase.Paint  
    ' Draw a circle with a bar on top.  
        e.Graphics.FillEllipse(Brushes.DarkBlue, New Rectangle _  
             (10, 10, 60, 60))  
        e.Graphics.FillRectangle(Brushes.Khaki, New Rectangle _  
             (20, 30, 60, 10))  
    ' Copy the graphic to a new location.  
        e.Graphics.CopyFromScreen(New Point(10, 10), New Point _  
             (100, 100), New Size(70, 70))  
End Sub  
```  
  
```csharp  
private void Form1_Paint(System.Object sender,  
    System.Windows.Forms.PaintEventArgs e)  
        {  
        e.Graphics.FillEllipse(Brushes.DarkBlue, new  
            Rectangle(10,10,60,60));  
        e.Graphics.FillRectangle(Brushes.Khaki, new  
            Rectangle(20,30,60,10));  
        e.Graphics.CopyFromScreen(new Point(10, 10), new Point(100, 100),   
            new Size(70, 70));  
}  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c4d48-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="c4d48-113">Compiling the Code</span></span>  
 <span data-ttu-id="c4d48-114">Le code ci-dessus est exécuté dans le formulaire <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements afin que les graphiques persistent si le formulaire est redessiné.</span><span class="sxs-lookup"><span data-stu-id="c4d48-114">The code above is run in the form's <xref:System.Windows.Forms.Control.Paint> event handler so that the graphics persist when the form is redrawn.</span></span> <span data-ttu-id="c4d48-115">Par conséquent, n’appelez pas de méthodes graphiques dans le <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements, étant donné que le contenu dessiné ne sera pas redessiné si le formulaire est redimensionné ou masqué par un autre formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4d48-115">As such, do not call graphics-related methods in the <xref:System.Windows.Forms.Form.Load> event handler, because the drawn content will not be redrawn if the form is resized or obscured by another form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4d48-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4d48-116">See also</span></span>
- <xref:System.Drawing.CopyPixelOperation>
- <xref:System.Drawing.Graphics.FillRectangle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.OnPaint%2A?displayProperty=nameWithType>
- [<span data-ttu-id="c4d48-117">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c4d48-117">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="c4d48-118">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="c4d48-118">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
