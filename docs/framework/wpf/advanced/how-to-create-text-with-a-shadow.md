---
title: 'Comment : créer du texte avec une ombre'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], shadow effects
- shadow effects in text [WPF]
- text [WPF], shadowed
ms.assetid: 6ab9c754-6001-4708-b479-5367f2fd1a35
ms.openlocfilehash: 1b7740284afcda6eab41fb68be3b4a2f032cc77d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544756"
---
# <a name="how-to-create-text-with-a-shadow"></a><span data-ttu-id="256d2-102">Comment : créer du texte avec une ombre</span><span class="sxs-lookup"><span data-stu-id="256d2-102">How to: Create Text with a Shadow</span></span>
<span data-ttu-id="256d2-103">Les exemples de cette section indiquent comment créer un effet d’ombre pour du texte affiché.</span><span class="sxs-lookup"><span data-stu-id="256d2-103">The examples in this section show how to create a shadow effect for displayed text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="256d2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="256d2-104">Example</span></span>  
 <span data-ttu-id="256d2-105">Le <xref:System.Windows.Media.Effects.DropShadowEffect> objet vous permet de créer plusieurs types de suppression pour les effets d’ombre [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] objets.</span><span class="sxs-lookup"><span data-stu-id="256d2-105">The <xref:System.Windows.Media.Effects.DropShadowEffect> object allows you to create a variety of drop shadow effects for [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] objects.</span></span> <span data-ttu-id="256d2-106">L’exemple suivant présente un effet d’ombre portée appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-106">The following example shows a drop shadow effect applied to text.</span></span> <span data-ttu-id="256d2-107">Dans ce cas, l’ombre est une ombre légère, ce qui signifie que sa couleur devient floue.</span><span class="sxs-lookup"><span data-stu-id="256d2-107">In this case, the shadow is a soft shadow, which means the shadow color blurs.</span></span>  
  
 <span data-ttu-id="256d2-108">![Ombre du texte avec adoucissement &#61; 0,25](../../../../docs/framework/wpf/advanced/media/shadowtext01.jpg "ShadowText01")</span><span class="sxs-lookup"><span data-stu-id="256d2-108">![Text shadow with Softness &#61; 0.25](../../../../docs/framework/wpf/advanced/media/shadowtext01.jpg "ShadowText01")</span></span>  
<span data-ttu-id="256d2-109">Exemple de texte avec une ombre légère</span><span class="sxs-lookup"><span data-stu-id="256d2-109">Example of text with a soft shadow</span></span>  
  
 <span data-ttu-id="256d2-110">Vous pouvez contrôler la largeur de l’ombre en définissant le <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="256d2-110">You can control the width of a shadow by setting the <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> property.</span></span> <span data-ttu-id="256d2-111">La valeur `4.0` indique une largeur de l’ombre de 4 pixels.</span><span class="sxs-lookup"><span data-stu-id="256d2-111">A value of `4.0` indicates a shadow width of 4 pixels.</span></span> <span data-ttu-id="256d2-112">Vous pouvez contrôler la douceur, ou flou d’une ombre en modifiant la <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="256d2-112">You can control the softness, or blur, of a shadow by modifying the <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> property.</span></span> <span data-ttu-id="256d2-113">La valeur `0.0` indique aucun flou.</span><span class="sxs-lookup"><span data-stu-id="256d2-113">A value of `0.0` indicates no blurring.</span></span> <span data-ttu-id="256d2-114">L’exemple de code suivant montre comment créer une ombre légère.</span><span class="sxs-lookup"><span data-stu-id="256d2-114">The following code example shows how to create a soft shadow.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet1)]  
  
> [!NOTE]
>  <span data-ttu-id="256d2-115">Ces effets d’ombre ne traversent pas la [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] pipeline de rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-115">These shadow effects do not go through the [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] text rendering pipeline.</span></span> <span data-ttu-id="256d2-116">En conséquence, ClearType est désactivé lors de l’utilisation de ces effets.</span><span class="sxs-lookup"><span data-stu-id="256d2-116">As a result, ClearType is disabled when using these effects.</span></span>  
  
 <span data-ttu-id="256d2-117">L’exemple suivant présente un effet d’ombre portée marquée appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-117">The following example shows a hard drop shadow effect applied to text.</span></span> <span data-ttu-id="256d2-118">Dans ce cas, l’ombre n’est pas floue.</span><span class="sxs-lookup"><span data-stu-id="256d2-118">In this case, the shadow is not blurred.</span></span>  
  
 <span data-ttu-id="256d2-119">![Ombre du texte avec adoucissement &#61; 0](../../../../docs/framework/wpf/advanced/media/shadowtext02.jpg "ShadowText02")</span><span class="sxs-lookup"><span data-stu-id="256d2-119">![Text shadow with Softness &#61; 0](../../../../docs/framework/wpf/advanced/media/shadowtext02.jpg "ShadowText02")</span></span>  
<span data-ttu-id="256d2-120">Exemple de texte avec une ombre marquée</span><span class="sxs-lookup"><span data-stu-id="256d2-120">Example of text with a hard shadow</span></span>  
  
 <span data-ttu-id="256d2-121">Vous pouvez créer une ombre foncée en définissant le <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> propriété `0.0`, ce qui indique qu’aucun flou est utilisé.</span><span class="sxs-lookup"><span data-stu-id="256d2-121">You can create a hard shadow by setting the <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> property to `0.0`, which indicates that no blurring is used.</span></span> <span data-ttu-id="256d2-122">Vous pouvez contrôler la direction de l’ombre en modifiant la <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="256d2-122">You can control the direction of the shadow by modifying the <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> property.</span></span> <span data-ttu-id="256d2-123">Définissez la valeur directionnelle de cette propriété à un degré entre `0` et `360`.</span><span class="sxs-lookup"><span data-stu-id="256d2-123">Set the directional value of this property to a degree between `0` and `360`.</span></span> <span data-ttu-id="256d2-124">L’illustration suivante montre les valeurs de direction du <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> paramètre de propriété.</span><span class="sxs-lookup"><span data-stu-id="256d2-124">The following illustration shows the directional values of the <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> property setting.</span></span>  
  
 <span data-ttu-id="256d2-125">![Degré DropShadow de l’ombre](../../../../docs/framework/wpf/advanced/media/shadowtext08.png "ShadowText08")</span><span class="sxs-lookup"><span data-stu-id="256d2-125">![DropShadow degree setting of shadow](../../../../docs/framework/wpf/advanced/media/shadowtext08.png "ShadowText08")</span></span>  
<span data-ttu-id="256d2-126">Diagramme de direction DropShadow</span><span class="sxs-lookup"><span data-stu-id="256d2-126">DropShadow Direction diagram</span></span>  
  
 <span data-ttu-id="256d2-127">L’exemple de code suivant montre comment créer une ombre marquée.</span><span class="sxs-lookup"><span data-stu-id="256d2-127">The following code example shows how to create a hard shadow.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet2)]  
  
## <a name="using-a-blur-effect"></a><span data-ttu-id="256d2-128">Utilisation d’un effet de flou</span><span class="sxs-lookup"><span data-stu-id="256d2-128">Using a Blur Effect</span></span>  
 <span data-ttu-id="256d2-129">Un <xref:System.Windows.Media.Effects.BlurBitmapEffect> peut être utilisé pour créer un effet de clichés instantanés qui peut être placé derrière un objet texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-129">A <xref:System.Windows.Media.Effects.BlurBitmapEffect> can be used to create a shadow-like effect that can be placed behind a text object.</span></span> <span data-ttu-id="256d2-130">Un effet bitmap flou appliqué au texte rend le texte flou uniformément dans toutes les directions.</span><span class="sxs-lookup"><span data-stu-id="256d2-130">A blur bitmap effect applied to text blurs the text evenly in all directions.</span></span>  
  
 <span data-ttu-id="256d2-131">L’exemple suivant présente un effet de flou appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-131">The following example shows a blur effect applied to text.</span></span>  
  
 <span data-ttu-id="256d2-132">![Ombre du texte utilisant BlurBitmapEffect](../../../../docs/framework/wpf/advanced/media/shadowtext06.jpg "ShadowText06")</span><span class="sxs-lookup"><span data-stu-id="256d2-132">![Text shadow using a BlurBitmapEffect](../../../../docs/framework/wpf/advanced/media/shadowtext06.jpg "ShadowText06")</span></span>  
<span data-ttu-id="256d2-133">Exemple de texte avec un effet de flou</span><span class="sxs-lookup"><span data-stu-id="256d2-133">Example of text with a blur effect</span></span>  
  
 <span data-ttu-id="256d2-134">L’exemple de code suivant montre comment créer un effet de flou.</span><span class="sxs-lookup"><span data-stu-id="256d2-134">The following code example shows how to create a blur effect.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/BlurShadows.xaml#textshadowsnippet6)]  
  
## <a name="using-a-translate-transform"></a><span data-ttu-id="256d2-135">Utilisation d’une transformation de traduction</span><span class="sxs-lookup"><span data-stu-id="256d2-135">Using a Translate Transform</span></span>  
 <span data-ttu-id="256d2-136">Un <xref:System.Windows.Media.TranslateTransform> peut être utilisé pour créer un effet de clichés instantanés qui peut être placé derrière un objet texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-136">A <xref:System.Windows.Media.TranslateTransform> can be used to create a shadow-like effect that can be placed behind a text object.</span></span>  
  
 <span data-ttu-id="256d2-137">Le code suivant exemple utilise un <xref:System.Windows.Media.TranslateTransform> pour décaler le texte.</span><span class="sxs-lookup"><span data-stu-id="256d2-137">The following code example uses a <xref:System.Windows.Media.TranslateTransform> to offset text.</span></span> <span data-ttu-id="256d2-138">Dans cet exemple, une copie légèrement décalée de texte en dessous du texte principal crée un effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="256d2-138">In this example, a slightly offset copy of text below the primary text creates a shadow effect.</span></span>  
  
 <span data-ttu-id="256d2-139">![Ombre du texte utilisant TranslateTransform](../../../../docs/framework/wpf/advanced/media/shadowtext07.jpg "ShadowText07")</span><span class="sxs-lookup"><span data-stu-id="256d2-139">![Text shadow using a TranslateTransform](../../../../docs/framework/wpf/advanced/media/shadowtext07.jpg "ShadowText07")</span></span>  
<span data-ttu-id="256d2-140">Exemple de texte utilisant une transformation pour un effet d’ombre</span><span class="sxs-lookup"><span data-stu-id="256d2-140">Example of text using a transform for a shadow effect</span></span>  
  
 <span data-ttu-id="256d2-141">L’exemple de code suivant indique comment créer une transformation pour un effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="256d2-141">The following code example shows how to create a transform for a shadow effect.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/TransformShadows.xaml#textshadowsnippet7)]
