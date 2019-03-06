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
ms.openlocfilehash: fd86293c539bf58ac93894e0b879dddb984825e1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378944"
---
# <a name="how-to-apply-transforms-to-text"></a><span data-ttu-id="73ee3-102">Procédure : Appliquer des transformations à du texte</span><span class="sxs-lookup"><span data-stu-id="73ee3-102">How to: Apply Transforms to Text</span></span>
<span data-ttu-id="73ee3-103">Les transformations peuvent modifier l’affichage de texte dans votre application.</span><span class="sxs-lookup"><span data-stu-id="73ee3-103">Transforms can alter the display of text in your application.</span></span> <span data-ttu-id="73ee3-104">Les exemples suivants utilisent différents types de transformations du rendu pour changer l’affichage du texte dans un <xref:System.Windows.Controls.TextBlock> contrôle.</span><span class="sxs-lookup"><span data-stu-id="73ee3-104">The following examples use different types of rendering transforms to affect the display of text in a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73ee3-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="73ee3-105">Example</span></span>  
 <span data-ttu-id="73ee3-106">L’exemple suivant présente un texte pivoté par rapport à un point spécifié dans le plan x-y à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="73ee3-106">The following example shows text rotated about a specified point in the two-dimensional x-y plane.</span></span>  
  
 <span data-ttu-id="73ee3-107">![Texte pivoté à l’aide de RotateTransform](./media/transformedtext01.jpg "TransformedText01")</span><span class="sxs-lookup"><span data-stu-id="73ee3-107">![Text rotated using a RotateTransform](./media/transformedtext01.jpg "TransformedText01")</span></span>  
<span data-ttu-id="73ee3-108">Exemple de texte pivoté à 90 degrés</span><span class="sxs-lookup"><span data-stu-id="73ee3-108">Example of text rotated 90 degrees</span></span>  
  
 <span data-ttu-id="73ee3-109">Le code suivant exemple utilise un <xref:System.Windows.Media.RotateTransform> pour faire pivoter le texte.</span><span class="sxs-lookup"><span data-stu-id="73ee3-109">The following code example uses a <xref:System.Windows.Media.RotateTransform> to rotate text.</span></span> <span data-ttu-id="73ee3-110">Un <xref:System.Windows.Media.RotateTransform.Angle%2A> valeur de 90 fait pivoter l’élément à 90 degrés dans le sens horaire.</span><span class="sxs-lookup"><span data-stu-id="73ee3-110">An <xref:System.Windows.Media.RotateTransform.Angle%2A> value of 90 rotates the element 90 degrees clockwise.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample1)]  
  
 <span data-ttu-id="73ee3-111">Dans l’exemple suivant, la deuxième ligne du texte est mise à l’échelle par 150 % le long de l’axe x et la troisième ligne du texte est mise à l’échelle par 150 % le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="73ee3-111">The following example shows the second line of text scaled by 150% along the x-axis, and the third line of text scaled by 150% along the y-axis.</span></span>  
  
 <span data-ttu-id="73ee3-112">![Texte mis à l’échelle avec ScaleTransform](./media/transformedtext02.jpg "TransformedText02")</span><span class="sxs-lookup"><span data-stu-id="73ee3-112">![Text scaled using a ScaleTransform](./media/transformedtext02.jpg "TransformedText02")</span></span>  
<span data-ttu-id="73ee3-113">Exemple de texte mis à l’échelle</span><span class="sxs-lookup"><span data-stu-id="73ee3-113">Example of scaled text</span></span>  
  
 <span data-ttu-id="73ee3-114">Le code suivant exemple utilise un <xref:System.Windows.Media.ScaleTransform> à l’échelle un texte à partir de sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="73ee3-114">The following code example uses a <xref:System.Windows.Media.ScaleTransform> to scale text from its original size.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample2)]  
  
> [!NOTE]
>  <span data-ttu-id="73ee3-115">La mise à l’échelle du texte est différente de l’augmentation de la taille de police du texte.</span><span class="sxs-lookup"><span data-stu-id="73ee3-115">Scaling text is not the same as increasing the font size of text.</span></span> <span data-ttu-id="73ee3-116">Les tailles de police sont calculées indépendamment les unes des autres pour fournir la meilleure résolution à des tailles différentes.</span><span class="sxs-lookup"><span data-stu-id="73ee3-116">Font sizes are calculated independently of each other in order to provide the best resolution at different sizes.</span></span> <span data-ttu-id="73ee3-117">Le texte mis à l’échelle, en revanche, conserve les proportions du texte à la taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="73ee3-117">Scaled text, on the other hand, preserves the proportions of the original-sized text.</span></span>  
  
 <span data-ttu-id="73ee3-118">L’exemple suivant présente le texte incliné le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="73ee3-118">The following example shows text skewed along the x-axis.</span></span>  
  
 <span data-ttu-id="73ee3-119">![Texte incliné à l’aide de SkewTransform](./media/transformedtext03.jpg "TransformedText03")</span><span class="sxs-lookup"><span data-stu-id="73ee3-119">![Text skewed using a SkewTransform](./media/transformedtext03.jpg "TransformedText03")</span></span>  
<span data-ttu-id="73ee3-120">Exemple de texte incliné</span><span class="sxs-lookup"><span data-stu-id="73ee3-120">Example of skewed text</span></span>  
  
 <span data-ttu-id="73ee3-121">Le code suivant exemple utilise un <xref:System.Windows.Media.SkewTransform> pour incliner du texte.</span><span class="sxs-lookup"><span data-stu-id="73ee3-121">The following code example uses a <xref:System.Windows.Media.SkewTransform> to skew text.</span></span> <span data-ttu-id="73ee3-122">Une inclinaison est une transformation qui étire l’espace de coordonnées de façon non uniforme.</span><span class="sxs-lookup"><span data-stu-id="73ee3-122">A skew, also known as a shear, is a transformation that stretches the coordinate space in a non-uniform manner.</span></span> <span data-ttu-id="73ee3-123">Dans cet exemple, les deux chaînes de texte sont inclinées de -30° et 30° le long de la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="73ee3-123">In this example, the two text strings are skewed -30° and 30° along the x-coordinate.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample3)]  
  
 <span data-ttu-id="73ee3-124">L’exemple suivant présente le texte traduit ou déplacé, le long des axes x et y.</span><span class="sxs-lookup"><span data-stu-id="73ee3-124">The following example shows text translated, or moved, along the x- and y-axis.</span></span>  
  
 <span data-ttu-id="73ee3-125">![Décalage de texte utilisant TranslateTransform](./media/transformedtext04.jpg "TransformedText04")</span><span class="sxs-lookup"><span data-stu-id="73ee3-125">![Text offset using a TranslateTransform](./media/transformedtext04.jpg "TransformedText04")</span></span>  
<span data-ttu-id="73ee3-126">Exemple de texte traduit</span><span class="sxs-lookup"><span data-stu-id="73ee3-126">Example of translated text</span></span>  
  
 <span data-ttu-id="73ee3-127">Le code suivant exemple utilise un <xref:System.Windows.Media.TranslateTransform> pour décaler le texte.</span><span class="sxs-lookup"><span data-stu-id="73ee3-127">The following code example uses a <xref:System.Windows.Media.TranslateTransform> to offset text.</span></span> <span data-ttu-id="73ee3-128">Dans cet exemple, une copie légèrement décalée de texte en dessous du texte principal crée un effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="73ee3-128">In this example, a slightly offset copy of text below the primary text creates a shadow effect.</span></span>  
  
 [!code-xaml[TextTransformSample#TextTransformSample4](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTransformSample/CS/Window1.xaml#texttransformsample4)]  
  
> [!NOTE]
>  <span data-ttu-id="73ee3-129">Le <xref:System.Windows.Media.Effects.DropShadowBitmapEffect> fournit un ensemble rich de fonctionnalités pour fournir des effets d’ombre.</span><span class="sxs-lookup"><span data-stu-id="73ee3-129">The <xref:System.Windows.Media.Effects.DropShadowBitmapEffect> provides a rich set of features for providing shadow effects.</span></span> <span data-ttu-id="73ee3-130">Pour plus d’informations, consultez [créer du texte avec une ombre](how-to-create-text-with-a-shadow.md).</span><span class="sxs-lookup"><span data-stu-id="73ee3-130">For more information, see [Create Text with a Shadow](how-to-create-text-with-a-shadow.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73ee3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73ee3-131">See also</span></span>
- [<span data-ttu-id="73ee3-132">Guide pratique pour appliquer des animations à du texte</span><span class="sxs-lookup"><span data-stu-id="73ee3-132">Apply Animations to Text</span></span>](how-to-apply-animations-to-text.md)
