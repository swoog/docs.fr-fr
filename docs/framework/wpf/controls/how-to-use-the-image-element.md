---
title: "Procédure : Utiliser l'élément Image"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Image
- Image control [WPF]
- rendering images [WPF]
ms.assetid: 5b92e74b-1b56-4756-ac64-d5e9e08d9854
ms.openlocfilehash: d7aa2e0e9bd33dfcd68bd19b5084fa1666232a5c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54530799"
---
# <a name="how-to-use-the-image-element"></a><span data-ttu-id="f263f-102">Procédure : Utiliser l'élément Image</span><span class="sxs-lookup"><span data-stu-id="f263f-102">How to: Use the Image Element</span></span>
<span data-ttu-id="f263f-103">Cet exemple montre comment inclure des images dans une application à l’aide de la <xref:System.Windows.Controls.Image> élément.</span><span class="sxs-lookup"><span data-stu-id="f263f-103">This example shows how to include images in an application by using the <xref:System.Windows.Controls.Image> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f263f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f263f-104">Example</span></span>  
 <span data-ttu-id="f263f-105">L’exemple suivant montre comment afficher une image de 200 pixels de large.</span><span class="sxs-lookup"><span data-stu-id="f263f-105">The following example shows how to render an image 200 pixels wide.</span></span> <span data-ttu-id="f263f-106">Dans cet exemple en [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], la syntaxe d’attribut et la syntaxe de balise de propriété sont utilisées pour définir l’image.</span><span class="sxs-lookup"><span data-stu-id="f263f-106">In this [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] example, both attribute syntax and property tag syntax are used to define the image.</span></span> <span data-ttu-id="f263f-107">Pour plus d’informations sur les syntaxes d’attribut et de propriété, consultez [Vue d’ensemble des propriétés de dépendance](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f263f-107">For more information on attribute syntax and property syntax, see [Dependency Properties Overview](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md).</span></span> <span data-ttu-id="f263f-108">Un <xref:System.Windows.Media.Imaging.BitmapImage> est utilisé pour définir les données de l’image source et est définie explicitement pour l’exemple de syntaxe de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="f263f-108">A <xref:System.Windows.Media.Imaging.BitmapImage> is used to define the image's source data and is explicitly defined for the property tag syntax example.</span></span> <span data-ttu-id="f263f-109">En outre, le <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> de la <xref:System.Windows.Media.Imaging.BitmapImage> est défini sur la même largeur que le <xref:System.Windows.FrameworkElement.Width%2A> de la <xref:System.Windows.Controls.Image>.</span><span class="sxs-lookup"><span data-stu-id="f263f-109">In addition, the <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> of the <xref:System.Windows.Media.Imaging.BitmapImage> is set to the same width as the <xref:System.Windows.FrameworkElement.Width%2A> of the <xref:System.Windows.Controls.Image>.</span></span> <span data-ttu-id="f263f-110">Cela garantit que la quantité minimale de mémoire est utilisée pour le rendu de l’image.</span><span class="sxs-lookup"><span data-stu-id="f263f-110">This is done to ensure that the minimum amount of memory is used rendering the image.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f263f-111">En règle générale, si vous souhaitez spécifier la taille d’un rendu d’image, spécifiez uniquement le <xref:System.Windows.FrameworkElement.Width%2A> ou <xref:System.Windows.FrameworkElement.Height%2A> mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="f263f-111">In general, if you want to specify the size of a rendered image, specify only the <xref:System.Windows.FrameworkElement.Width%2A> or the <xref:System.Windows.FrameworkElement.Height%2A> but not both.</span></span> <span data-ttu-id="f263f-112">Si vous ne spécifiez qu’un seul de ces paramètres, les proportions de l’image sont conservées.</span><span class="sxs-lookup"><span data-stu-id="f263f-112">If you only specify one, the image's aspect ratio is preserved.</span></span> <span data-ttu-id="f263f-113">Dans le cas contraire, l’image peut apparaître étirée ou déformée.</span><span class="sxs-lookup"><span data-stu-id="f263f-113">Otherwise, the image may unexpectedly appear stretched or warped.</span></span> <span data-ttu-id="f263f-114">Pour contrôler l’image d’étirement de comportement, utilisez le <xref:System.Windows.Controls.Image.Stretch%2A> et <xref:System.Windows.Controls.Image.StretchDirection%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="f263f-114">To control the image's stretching behavior, use the <xref:System.Windows.Controls.Image.Stretch%2A> and <xref:System.Windows.Controls.Image.StretchDirection%2A> properties.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f263f-115">Lorsque vous spécifiez la taille d’une image avec soit <xref:System.Windows.FrameworkElement.Width%2A> ou <xref:System.Windows.FrameworkElement.Height%2A>, vous devez également définir soit <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> ou <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelHeight%2A> à la même taille.</span><span class="sxs-lookup"><span data-stu-id="f263f-115">When you specify the size of an image with either <xref:System.Windows.FrameworkElement.Width%2A> or <xref:System.Windows.FrameworkElement.Height%2A>, you should also set either <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> or <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelHeight%2A> to the same respective size.</span></span>  
  
 <span data-ttu-id="f263f-116">Le <xref:System.Windows.Controls.Image.Stretch%2A> propriété détermine la manière dont la source de l’image est étirée pour remplir l’élément image.</span><span class="sxs-lookup"><span data-stu-id="f263f-116">The <xref:System.Windows.Controls.Image.Stretch%2A> property determines how the image source is stretched to fill the image element.</span></span> <span data-ttu-id="f263f-117">Pour plus d’informations, consultez l’énumération <xref:System.Windows.Media.Stretch>.</span><span class="sxs-lookup"><span data-stu-id="f263f-117">For more information, see the <xref:System.Windows.Media.Stretch> enumeration.</span></span>  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a><span data-ttu-id="f263f-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="f263f-118">Example</span></span>  
 <span data-ttu-id="f263f-119">L’exemple suivant montre comment afficher une image de 200 pixels de large à l’aide de code.</span><span class="sxs-lookup"><span data-stu-id="f263f-119">The following example shows how to render an image 200 pixels wide using code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f263f-120">Paramètre <xref:System.Windows.Media.Imaging.BitmapImage> propriétés doivent être effectuées au sein d’un <xref:System.Windows.Media.Imaging.BitmapImage.BeginInit%2A> et <xref:System.Windows.Media.Imaging.BitmapImage.EndInit%2A> bloc.</span><span class="sxs-lookup"><span data-stu-id="f263f-120">Setting <xref:System.Windows.Media.Imaging.BitmapImage> properties must be done within a <xref:System.Windows.Media.Imaging.BitmapImage.BeginInit%2A> and <xref:System.Windows.Media.Imaging.BitmapImage.EndInit%2A> block.</span></span>  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a><span data-ttu-id="f263f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f263f-121">See also</span></span>
- [<span data-ttu-id="f263f-122">Vue d’ensemble de la création d’images</span><span class="sxs-lookup"><span data-stu-id="f263f-122">Imaging Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
