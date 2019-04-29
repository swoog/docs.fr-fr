---
title: 'Procédure : Créer du texte avec une ombre'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], shadow effects
- shadow effects in text [WPF]
- text [WPF], shadowed
ms.assetid: 6ab9c754-6001-4708-b479-5367f2fd1a35
ms.openlocfilehash: a2225e297dbc0b5f9d49799cb34eb5539746e62e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776820"
---
# <a name="how-to-create-text-with-a-shadow"></a><span data-ttu-id="e1ef3-102">Procédure : Créer du texte avec une ombre</span><span class="sxs-lookup"><span data-stu-id="e1ef3-102">How to: Create Text with a Shadow</span></span>
<span data-ttu-id="e1ef3-103">Les exemples de cette section indiquent comment créer un effet d’ombre pour du texte affiché.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-103">The examples in this section show how to create a shadow effect for displayed text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e1ef3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1ef3-104">Example</span></span>  
 <span data-ttu-id="e1ef3-105">Le <xref:System.Windows.Media.Effects.DropShadowEffect> objet permet de créer des effets d’ombre pour une variété de dépôt [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] objets.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-105">The <xref:System.Windows.Media.Effects.DropShadowEffect> object allows you to create a variety of drop shadow effects for [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] objects.</span></span> <span data-ttu-id="e1ef3-106">L’exemple suivant présente un effet d’ombre portée appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-106">The following example shows a drop shadow effect applied to text.</span></span> <span data-ttu-id="e1ef3-107">Dans ce cas, l’ombre est une ombre légère, ce qui signifie que sa couleur devient floue.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-107">In this case, the shadow is a soft shadow, which means the shadow color blurs.</span></span>  
  
 ![Ombre du texte avec adoucissement &#61; 0,25](./media/how-to-create-text-with-a-shadow/drop-shadow-text-effect.jpg) 
  
 <span data-ttu-id="e1ef3-109">Vous pouvez contrôler la largeur d’une ombre en définissant le <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-109">You can control the width of a shadow by setting the <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> property.</span></span> <span data-ttu-id="e1ef3-110">La valeur `4.0` indique une largeur d’ombre de 4 pixels.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-110">A value of `4.0` indicates a shadow width of 4 pixels.</span></span> <span data-ttu-id="e1ef3-111">Vous pouvez contrôler la douceur, ou flou d’une ombre en modifiant le <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-111">You can control the softness, or blur, of a shadow by modifying the <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> property.</span></span> <span data-ttu-id="e1ef3-112">La valeur `0.0` indique aucun flou.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-112">A value of `0.0` indicates no blurring.</span></span> <span data-ttu-id="e1ef3-113">L’exemple de code suivant montre comment créer une ombre légère.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-113">The following code example shows how to create a soft shadow.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet1)]  
  
> [!NOTE]
>  <span data-ttu-id="e1ef3-114">Ces effets d’ombre ne traversent pas le [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] pipeline de rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-114">These shadow effects do not go through the [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] text rendering pipeline.</span></span> <span data-ttu-id="e1ef3-115">En conséquence, ClearType est désactivé lors de l’utilisation de ces effets.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-115">As a result, ClearType is disabled when using these effects.</span></span>  
  
 <span data-ttu-id="e1ef3-116">L’exemple suivant présente un effet d’ombre portée marquée appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-116">The following example shows a hard drop shadow effect applied to text.</span></span> <span data-ttu-id="e1ef3-117">Dans ce cas, l’ombre n’est pas floue.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-117">In this case, the shadow is not blurred.</span></span>  
  
 ![Ombre du texte avec adoucissement &#61; 0](./media/how-to-create-text-with-a-shadow/text-shadow-softness.jpg) 
  
 <span data-ttu-id="e1ef3-119">Vous pouvez créer une ombre en définissant le <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> propriété `0.0`, qui indique qu’aucun flou n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-119">You can create a hard shadow by setting the <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> property to `0.0`, which indicates that no blurring is used.</span></span> <span data-ttu-id="e1ef3-120">Vous pouvez contrôler la direction de l’ombre en modifiant le <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-120">You can control the direction of the shadow by modifying the <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> property.</span></span> <span data-ttu-id="e1ef3-121">Définissez la valeur directionnelle de cette propriété à un degré entre `0` et `360`.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-121">Set the directional value of this property to a degree between `0` and `360`.</span></span> <span data-ttu-id="e1ef3-122">L’illustration suivante montre les valeurs directionnelles du <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> paramètre de propriété.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-122">The following illustration shows the directional values of the <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> property setting.</span></span>  
  
 ![Paramètre de degré DropShadow de l’ombre](./media/how-to-create-text-with-a-shadow/drop-shadow-degree-setting.png)
  
 <span data-ttu-id="e1ef3-124">L’exemple de code suivant montre comment créer une ombre marquée.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-124">The following code example shows how to create a hard shadow.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet2)]  
  
## <a name="using-a-blur-effect"></a><span data-ttu-id="e1ef3-125">Utilisation d’un effet de flou</span><span class="sxs-lookup"><span data-stu-id="e1ef3-125">Using a Blur Effect</span></span>  
 <span data-ttu-id="e1ef3-126">Un <xref:System.Windows.Media.Effects.BlurBitmapEffect> peut être utilisé pour créer un effet de clichés instantanés pouvant être placé derrière un objet texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-126">A <xref:System.Windows.Media.Effects.BlurBitmapEffect> can be used to create a shadow-like effect that can be placed behind a text object.</span></span> <span data-ttu-id="e1ef3-127">Un effet bitmap flou appliqué au texte rend le texte flou uniformément dans toutes les directions.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-127">A blur bitmap effect applied to text blurs the text evenly in all directions.</span></span>  
  
 <span data-ttu-id="e1ef3-128">L’exemple suivant présente un effet de flou appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-128">The following example shows a blur effect applied to text.</span></span>  
  
 ![Ombre du texte utilisant BlurBitmapEffect](./media/how-to-create-text-with-a-shadow/text-shadow-blur-effect.jpg)  
  
 <span data-ttu-id="e1ef3-130">L’exemple de code suivant montre comment créer un effet de flou.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-130">The following code example shows how to create a blur effect.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet6](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/BlurShadows.xaml#textshadowsnippet6)]  
  
## <a name="using-a-translate-transform"></a><span data-ttu-id="e1ef3-131">Utilisation d’une transformation de traduction</span><span class="sxs-lookup"><span data-stu-id="e1ef3-131">Using a Translate Transform</span></span>  
 <span data-ttu-id="e1ef3-132">Un <xref:System.Windows.Media.TranslateTransform> peut être utilisé pour créer un effet de clichés instantanés pouvant être placé derrière un objet texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-132">A <xref:System.Windows.Media.TranslateTransform> can be used to create a shadow-like effect that can be placed behind a text object.</span></span>  
  
 <span data-ttu-id="e1ef3-133">Le code suivant exemple utilise un <xref:System.Windows.Media.TranslateTransform> pour décaler le texte.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-133">The following code example uses a <xref:System.Windows.Media.TranslateTransform> to offset text.</span></span> <span data-ttu-id="e1ef3-134">Dans cet exemple, une copie légèrement décalée de texte en dessous du texte principal crée un effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-134">In this example, a slightly offset copy of text below the primary text creates a shadow effect.</span></span>  
  
 ![Ombre du texte utilisant TranslateTransform](./media/how-to-create-text-with-a-shadow/text-transform-shadow-effect.jpg)    
  
 <span data-ttu-id="e1ef3-136">L’exemple de code suivant indique comment créer une transformation pour un effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-136">The following code example shows how to create a transform for a shadow effect.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/TransformShadows.xaml#textshadowsnippet7)]
