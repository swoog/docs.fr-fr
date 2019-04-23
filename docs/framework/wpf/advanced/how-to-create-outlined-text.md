---
title: 'Procédure : Créer du texte avec contour'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], linear gradient brush
- outlined text [WPF]
- gradient brush [WPF]
- linear gradient brush [WPF]
- typography [WPF], outline effects
ms.assetid: 4aa3cf6e-1953-4f26-8230-7c1409e5f28d
ms.openlocfilehash: 237bdc097cd2a3fbfff6dd79bce401c2d091e211
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162226"
---
# <a name="how-to-create-outlined-text"></a><span data-ttu-id="5bb0f-102">Procédure : Créer du texte avec contour</span><span class="sxs-lookup"><span data-stu-id="5bb0f-102">How to: Create Outlined Text</span></span>
<span data-ttu-id="5bb0f-103">Dans la plupart des cas, lorsque vous ajoutez ornementation élaborée pour les chaînes de texte dans votre [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] application, à l’aide de texte en termes d’une collection de caractères discrets, ou glyphes.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-103">In most cases, when you are adding ornamentation to text strings in your [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] application, you are using text in terms of a collection of discrete characters, or glyphs.</span></span> <span data-ttu-id="5bb0f-104">Par exemple, Impossible de créer un pinceau dégradé linéaire et de l’appliquer à la <xref:System.Windows.Controls.Control.Foreground%2A> propriété d’un <xref:System.Windows.Controls.TextBox> objet.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-104">For example, you could create a linear gradient brush and apply it to the <xref:System.Windows.Controls.Control.Foreground%2A> property of a <xref:System.Windows.Controls.TextBox> object.</span></span> <span data-ttu-id="5bb0f-105">Lorsque vous affichez ou modifiez la zone de texte, le pinceau de dégradé linéaire est automatiquement appliqué à l’ensemble actuel de caractères dans la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-105">When you display or edit the text box, the linear gradient brush is automatically applied to the current set of characters in the text string.</span></span>  
  
 ![Texte affiché avec un pinceau de dégradé linéaire](./media/how-to-create-outlined-text/text-linear-gradient.jpg)    
  
 <span data-ttu-id="5bb0f-107">Toutefois, vous pouvez également convertir le texte en <xref:System.Windows.Media.Geometry> objets, ce qui vous permet de créer d’autres types de texte visuellement enrichi.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-107">However, you can also convert text into <xref:System.Windows.Media.Geometry> objects, allowing you to create other types of visually rich text.</span></span> <span data-ttu-id="5bb0f-108">Par exemple, vous pouvez créer un <xref:System.Windows.Media.Geometry> objet basé sur le contour d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-108">For example, you could create a <xref:System.Windows.Media.Geometry> object based on the outline of a text string.</span></span>  
  
 ![Contour du texte utilisant un pinceau de dégradé linéaire](./media/how-to-create-outlined-text/text-outline-linear-gradient.jpg)  
  
 <span data-ttu-id="5bb0f-110">Lorsque le texte est converti en un <xref:System.Windows.Media.Geometry> de l’objet, il n’est plus une collection de caractères, vous ne pouvez pas modifier les caractères dans la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-110">When text is converted to a <xref:System.Windows.Media.Geometry> object, it is no longer a collection of characters—you cannot modify the characters in the text string.</span></span> <span data-ttu-id="5bb0f-111">Vous pouvez néanmoins modifier l’apparence du texte converti en changeant ses propriétés de trait et de remplissage.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-111">However, you can affect the appearance of the converted text by modifying its stroke and fill properties.</span></span> <span data-ttu-id="5bb0f-112">Le trait fait référence au contour du texte converti et le remplissage à la zone située à l’intérieur du contour du texte converti.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-112">The stroke refers to the outline of the converted text; the fill refers to the area inside the outline of the converted text.</span></span>  
  
 <span data-ttu-id="5bb0f-113">Les exemples suivants illustrent plusieurs façons de créer des effets visuels en modifiant le trait et le remplissage de texte converti.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-113">The following examples illustrate several ways of creating visual effects by modifying the stroke and fill of converted text.</span></span>  
  
 ![Texte avec différentes couleurs de trait et de remplissage](./media/how-to-create-outlined-text/fill-stroke-text-effect.jpg)  
  
 ![Texte avec pinceau image appliqué au trait](./media/how-to-create-outlined-text/image-brush-application.jpg)
  
 <span data-ttu-id="5bb0f-116">Il est également possible de modifier le rectangle de cadre englobant ou mise en surbrillance, du texte converti.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-116">It is also possible to modify the bounding box rectangle, or highlight, of the converted text.</span></span> <span data-ttu-id="5bb0f-117">L’exemple suivant illustre un moyen de créer des effets visuels en modifiant le trait et surbrillance du texte converti.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-117">The following example illustrates a way to creating visual effects by modifying the stroke and highlight of converted text.</span></span>  
  
 ![Texte avec pinceau image appliqué pour tracer et mettre en surbrillance](./media/how-to-create-outlined-text/image-brush-text-application.jpg)

## <a name="example"></a><span data-ttu-id="5bb0f-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="5bb0f-119">Example</span></span>  
 <span data-ttu-id="5bb0f-120">La clé pour la conversion de texte à un <xref:System.Windows.Media.Geometry> objet consiste à utiliser le <xref:System.Windows.Media.FormattedText> objet.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-120">The key to converting text to a <xref:System.Windows.Media.Geometry> object is to use the <xref:System.Windows.Media.FormattedText> object.</span></span> <span data-ttu-id="5bb0f-121">Une fois que vous avez créé cet objet, vous pouvez utiliser la <xref:System.Windows.Media.FormattedText.BuildGeometry%2A> et <xref:System.Windows.Media.FormattedText.BuildHighlightGeometry%2A> méthodes pour convertir le texte à <xref:System.Windows.Media.Geometry> objets.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-121">Once you have created this object, you can use the <xref:System.Windows.Media.FormattedText.BuildGeometry%2A> and <xref:System.Windows.Media.FormattedText.BuildHighlightGeometry%2A> methods to convert the text to <xref:System.Windows.Media.Geometry> objects.</span></span> <span data-ttu-id="5bb0f-122">La première méthode retourne la géométrie du texte mis en forme ; la deuxième méthode retourne que la géométrie de la mise en forme du texte de la zone de délimitation.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-122">The first method returns the geometry of the formatted text; the second method returns the geometry of the formatted text's bounding box.</span></span> <span data-ttu-id="5bb0f-123">L’exemple de code suivant montre comment créer un <xref:System.Windows.Media.FormattedText> objet et récupérer les géométries du texte mis en forme et son cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-123">The following code example shows how to create a <xref:System.Windows.Media.FormattedText> object and to retrieve the geometries of the formatted text and its bounding box.</span></span>  
  
 [!code-csharp[OutlineTextControlViewer#CreateText](~/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs#createtext)]
 [!code-vb[OutlineTextControlViewer#CreateText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb#createtext)]  
  
 <span data-ttu-id="5bb0f-124">Pour afficher les données récupérées les <xref:System.Windows.Media.Geometry> objets, vous devez accéder à la <xref:System.Windows.Media.DrawingContext> de l’objet qui affiche le texte converti.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-124">In order to display the retrieved the <xref:System.Windows.Media.Geometry> objects, you need to access the <xref:System.Windows.Media.DrawingContext> of the object that is displaying the converted text.</span></span> <span data-ttu-id="5bb0f-125">Dans ces exemples de code, cela en créant un objet de contrôle personnalisé qui est dérivé d’une classe qui prend en charge le rendu défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-125">In these code examples, this is done by creating a custom control object that is derived from a class that supports user-defined rendering.</span></span>  
  
 <span data-ttu-id="5bb0f-126">Pour afficher <xref:System.Windows.Media.Geometry> objets dans le contrôle personnalisé, fournissez une substitution pour la <xref:System.Windows.UIElement.OnRender%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="5bb0f-126">To display <xref:System.Windows.Media.Geometry> objects in the custom control, provide an override for the <xref:System.Windows.UIElement.OnRender%2A> method.</span></span> <span data-ttu-id="5bb0f-127">Votre méthode de substitution doit utiliser le <xref:System.Windows.Media.DrawingContext.DrawGeometry%2A> méthode pour dessiner le <xref:System.Windows.Media.Geometry> objets.</span><span class="sxs-lookup"><span data-stu-id="5bb0f-127">Your overridden method should use the <xref:System.Windows.Media.DrawingContext.DrawGeometry%2A> method to draw the <xref:System.Windows.Media.Geometry> objects.</span></span>  
  
 [!code-csharp[OutlineTextControlViewer#OnRender](~/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs#onrender)]
 [!code-vb[OutlineTextControlViewer#OnRender](~/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb#onrender)]  
  
  <span data-ttu-id="5bb0f-128">Pour la source de l’exemple d’objet d’un contrôle utilisateur personnalisé, consultez [OutlineTextControl.cs pour C# ](https://github.com/dotnet/samples/blob/master/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs) et [OutlineTextControl.vb pour Visual Basic](https://github.com/dotnet/samples/blob/master/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb).</span><span class="sxs-lookup"><span data-stu-id="5bb0f-128">For the source of the example custom user control object, see [OutlineTextControl.cs for C#](https://github.com/dotnet/samples/blob/master/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs) and [OutlineTextControl.vb for Visual Basic](https://github.com/dotnet/samples/blob/master/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bb0f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bb0f-129">See also</span></span>

- [<span data-ttu-id="5bb0f-130">Dessin du texte mis en forme</span><span class="sxs-lookup"><span data-stu-id="5bb0f-130">Drawing Formatted Text</span></span>](drawing-formatted-text.md)
