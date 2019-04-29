---
title: 'Procédure : Appliquer des transformations à du texte'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], rotated text
- typography [WPF], scaled text
- skewed text [WPF]
- typography [WPF], translated text
- typography [WPF], shadowed text
- rotated text [WPF]
- translated text [WPF]
- shadowed text [WPF]
- transforms in text [WPF]
- typography [WPF], transforms
- scaled text [WPF]
- typography [WPF], skewed text
ms.assetid: 0d61678a-4185-4f2a-85c6-c1d020f96fa0
ms.openlocfilehash: 46a57364e0c18cc4c9fe7884642cd0b718c20f31
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776960"
---
# <a name="how-to-apply-transforms-to-text"></a><span data-ttu-id="d10b0-102">Procédure : Appliquer des transformations à du texte</span><span class="sxs-lookup"><span data-stu-id="d10b0-102">How to: Apply Transforms to Text</span></span>
<span data-ttu-id="d10b0-103">Les transformations peuvent modifier l’affichage de texte dans votre application.</span><span class="sxs-lookup"><span data-stu-id="d10b0-103">Transforms can alter the display of text in your application.</span></span> <span data-ttu-id="d10b0-104">Les exemples suivants utilisent différents types de transformations du rendu pour changer l’affichage du texte dans un <xref:System.Windows.Controls.TextBlock> contrôle.</span><span class="sxs-lookup"><span data-stu-id="d10b0-104">The following examples use different types of rendering transforms to affect the display of text in a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d10b0-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="d10b0-105">Example</span></span>  
 <span data-ttu-id="d10b0-106">L’exemple suivant présente un texte pivoté par rapport à un point spécifié dans le plan x-y à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="d10b0-106">The following example shows text rotated about a specified point in the two-dimensional x-y plane.</span></span>  
  
 ![Texte pivoté à l'aide de RotateTransform](./media/how-to-apply-transforms-to-text/text-rotated-ninety-degrees.jpg)  
  
 <span data-ttu-id="d10b0-108">Le code suivant exemple utilise un <xref:System.Windows.Media.RotateTransform> pour faire pivoter le texte.</span><span class="sxs-lookup"><span data-stu-id="d10b0-108">The following code example uses a <xref:System.Windows.Media.RotateTransform> to rotate text.</span></span> <span data-ttu-id="d10b0-109">Un <xref:System.Windows.Media.RotateTransform.Angle%2A> valeur de 90 fait pivoter l’élément à 90 degrés dans le sens horaire.</span><span class="sxs-lookup"><span data-stu-id="d10b0-109">An <xref:System.Windows.Media.RotateTransform.Angle%2A> value of 90 rotates the element 90 degrees clockwise.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample1)]  
  
 <span data-ttu-id="d10b0-110">Dans l’exemple suivant, la deuxième ligne du texte est mise à l’échelle par 150 % le long de l’axe x et la troisième ligne du texte est mise à l’échelle par 150 % le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="d10b0-110">The following example shows the second line of text scaled by 150% along the x-axis, and the third line of text scaled by 150% along the y-axis.</span></span>  
  
 ![Texte mis à l'échelle à l'aide de ScaleTransform](./media/how-to-apply-transforms-to-text/scaled-text-scaletransform.jpg) 
  
 <span data-ttu-id="d10b0-112">Le code suivant exemple utilise un <xref:System.Windows.Media.ScaleTransform> à l’échelle un texte à partir de sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="d10b0-112">The following code example uses a <xref:System.Windows.Media.ScaleTransform> to scale text from its original size.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample2)]  
  
> [!NOTE]
>  <span data-ttu-id="d10b0-113">La mise à l’échelle du texte est différente de l’augmentation de la taille de police du texte.</span><span class="sxs-lookup"><span data-stu-id="d10b0-113">Scaling text is not the same as increasing the font size of text.</span></span> <span data-ttu-id="d10b0-114">Les tailles de police sont calculées indépendamment les unes des autres pour fournir la meilleure résolution à des tailles différentes.</span><span class="sxs-lookup"><span data-stu-id="d10b0-114">Font sizes are calculated independently of each other in order to provide the best resolution at different sizes.</span></span> <span data-ttu-id="d10b0-115">Le texte mis à l’échelle, en revanche, conserve les proportions du texte à la taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="d10b0-115">Scaled text, on the other hand, preserves the proportions of the original-sized text.</span></span>  
  
 <span data-ttu-id="d10b0-116">L’exemple suivant présente le texte incliné le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="d10b0-116">The following example shows text skewed along the x-axis.</span></span>  
  
 ![Texte incliné à l'aide de SkewTransform](./media/how-to-apply-transforms-to-text/skewed-transformed-text.jpg)
   
 <span data-ttu-id="d10b0-118">Le code suivant exemple utilise un <xref:System.Windows.Media.SkewTransform> pour incliner du texte.</span><span class="sxs-lookup"><span data-stu-id="d10b0-118">The following code example uses a <xref:System.Windows.Media.SkewTransform> to skew text.</span></span> <span data-ttu-id="d10b0-119">Une inclinaison est une transformation qui étire l’espace de coordonnées de façon non uniforme.</span><span class="sxs-lookup"><span data-stu-id="d10b0-119">A skew, also known as a shear, is a transformation that stretches the coordinate space in a non-uniform manner.</span></span> <span data-ttu-id="d10b0-120">Dans cet exemple, les deux chaînes de texte sont inclinées de -30° et 30° le long de la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="d10b0-120">In this example, the two text strings are skewed -30° and 30° along the x-coordinate.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample3)]  
  
 <span data-ttu-id="d10b0-121">L’exemple suivant présente le texte traduit ou déplacé, le long des axes x et y.</span><span class="sxs-lookup"><span data-stu-id="d10b0-121">The following example shows text translated, or moved, along the x- and y-axis.</span></span>  
  
 ![Décalage de texte utilisant TranslateTransform](./media/how-to-apply-transforms-to-text/transformed-text-x-y-axis.jpg)
  
 <span data-ttu-id="d10b0-123">Le code suivant exemple utilise un <xref:System.Windows.Media.TranslateTransform> pour décaler le texte.</span><span class="sxs-lookup"><span data-stu-id="d10b0-123">The following code example uses a <xref:System.Windows.Media.TranslateTransform> to offset text.</span></span> <span data-ttu-id="d10b0-124">Dans cet exemple, une copie légèrement décalée de texte en dessous du texte principal crée un effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="d10b0-124">In this example, a slightly offset copy of text below the primary text creates a shadow effect.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample4](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample4)]  
  
> [!NOTE]
>  <span data-ttu-id="d10b0-125">Le <xref:System.Windows.Media.Effects.DropShadowBitmapEffect> fournit un ensemble rich de fonctionnalités pour fournir des effets d’ombre.</span><span class="sxs-lookup"><span data-stu-id="d10b0-125">The <xref:System.Windows.Media.Effects.DropShadowBitmapEffect> provides a rich set of features for providing shadow effects.</span></span> <span data-ttu-id="d10b0-126">Pour plus d’informations, consultez [créer du texte avec une ombre](how-to-create-text-with-a-shadow.md).</span><span class="sxs-lookup"><span data-stu-id="d10b0-126">For more information, see [Create Text with a Shadow](how-to-create-text-with-a-shadow.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d10b0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d10b0-127">See also</span></span>

- [<span data-ttu-id="d10b0-128">Guide pratique pour appliquer des animations à du texte</span><span class="sxs-lookup"><span data-stu-id="d10b0-128">Apply Animations to Text</span></span>](how-to-apply-animations-to-text.md)
