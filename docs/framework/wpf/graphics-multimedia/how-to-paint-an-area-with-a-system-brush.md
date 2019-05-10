---
title: 'Procédure : Peindre une zone avec un pinceau système'
ms.date: 03/30/2017
helpviewer_keywords:
- system brushes [WPF], painting with
- painting [WPF], with system brushes
- brushes [WPF], painting with system brushes [WPF]
ms.assetid: 5141a763-9235-42cb-a6bb-afc75513eac7
ms.openlocfilehash: 26511c577bf06b016dfc69cedc7fce2bafb35f32
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645377"
---
# <a name="how-to-paint-an-area-with-a-system-brush"></a><span data-ttu-id="2c519-102">Procédure : Peindre une zone avec un pinceau système</span><span class="sxs-lookup"><span data-stu-id="2c519-102">How to: Paint an Area with a System Brush</span></span>
<span data-ttu-id="2c519-103">Le <xref:System.Windows.SystemColors> classe fournit l’accès aux pinceaux système et les couleurs, tel que <xref:System.Windows.SystemColors.ControlBrush%2A>, <xref:System.Windows.SystemColors.ControlBrushKey%2A>, et <xref:System.Windows.SystemColors.DesktopBrush%2A>.</span><span class="sxs-lookup"><span data-stu-id="2c519-103">The <xref:System.Windows.SystemColors> class provides access to system brushes and colors, such as <xref:System.Windows.SystemColors.ControlBrush%2A>, <xref:System.Windows.SystemColors.ControlBrushKey%2A>, and <xref:System.Windows.SystemColors.DesktopBrush%2A>.</span></span> <span data-ttu-id="2c519-104">Un pinceau système est un <xref:System.Windows.Media.SolidColorBrush> objet qui peint une zone avec la couleur système spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c519-104">A system brush is a <xref:System.Windows.Media.SolidColorBrush> object that paints an area with the specified system color.</span></span> <span data-ttu-id="2c519-105">Un pinceau système produit toujours un remplissage uni ; vous ne pouvez pas l’utiliser pour créer un dégradé.</span><span class="sxs-lookup"><span data-stu-id="2c519-105">A system brush always produces a solid fill; it can't be used to create a gradient.</span></span>  
  
 <span data-ttu-id="2c519-106">Vous pouvez utiliser des pinceaux système comme ressource dynamique ou statique.</span><span class="sxs-lookup"><span data-stu-id="2c519-106">You can use system brushes as either a static or a dynamic resource.</span></span> <span data-ttu-id="2c519-107">Utilisez une ressource dynamique si vous souhaitez que le pinceau soit automatiquement mis à jour si l’utilisateur modifie le pinceau système alors que l’application est en cours d’exécution ; sinon, utilisez une ressource statique.</span><span class="sxs-lookup"><span data-stu-id="2c519-107">Use a dynamic resource if you want the brush to update automatically if the user changes the system brush as the application is running; otherwise, use a static resource.</span></span> <span data-ttu-id="2c519-108">La classe SystemColors contient diverses propriétés statiques qui suivent une convention d’affectation de noms stricte :</span><span class="sxs-lookup"><span data-stu-id="2c519-108">The SystemColors class contains a variety of static properties that follow a strict naming convention:</span></span>  
  
- <span data-ttu-id="2c519-109">*\<SystemColor>* Brush</span><span class="sxs-lookup"><span data-stu-id="2c519-109">*\<SystemColor>* Brush</span></span>  
  
     <span data-ttu-id="2c519-110">Obtient une référence statique à un <xref:System.Windows.Media.SolidColorBrush> de la couleur système spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c519-110">Gets a static reference to a <xref:System.Windows.Media.SolidColorBrush> of the specified system color.</span></span>  
  
- <span data-ttu-id="2c519-111">*\<SystemColor>* BrushKey</span><span class="sxs-lookup"><span data-stu-id="2c519-111">*\<SystemColor>* BrushKey</span></span>  
  
     <span data-ttu-id="2c519-112">Obtient une référence dynamique à un <xref:System.Windows.Media.SolidColorBrush> de la couleur système spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c519-112">Gets a dynamic reference to a <xref:System.Windows.Media.SolidColorBrush> of the specified system color.</span></span>  
  
- <span data-ttu-id="2c519-113">*\<SystemColor>* Color</span><span class="sxs-lookup"><span data-stu-id="2c519-113">*\<SystemColor>* Color</span></span>  
  
     <span data-ttu-id="2c519-114">Obtient une référence statique à un <xref:System.Windows.Media.Color> structure de la couleur système spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c519-114">Gets a static reference to a <xref:System.Windows.Media.Color> structure of the specified system color.</span></span>  
  
- <span data-ttu-id="2c519-115">*\<SystemColor>* ColorKey</span><span class="sxs-lookup"><span data-stu-id="2c519-115">*\<SystemColor>* ColorKey</span></span>  
  
     <span data-ttu-id="2c519-116">Obtient une référence dynamique à la <xref:System.Windows.Media.Color> structure de la couleur système spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c519-116">Gets a dynamic reference to the <xref:System.Windows.Media.Color> structure of the specified system color.</span></span>  
  
 <span data-ttu-id="2c519-117">Une couleur système est un <xref:System.Windows.Media.Color> structure qui peut être utilisé pour configurer un pinceau.</span><span class="sxs-lookup"><span data-stu-id="2c519-117">A system color is a <xref:System.Windows.Media.Color> structure that can be used to configure a brush.</span></span> <span data-ttu-id="2c519-118">Par exemple, vous pouvez créer un dégradé à l’aide de couleurs système en définissant le <xref:System.Windows.Media.GradientStop.Color%2A> propriétés d’un <xref:System.Windows.Media.LinearGradientBrush> de dégradé de l’objet avec les couleurs système.</span><span class="sxs-lookup"><span data-stu-id="2c519-118">For example, you can create a gradient using system colors by setting the <xref:System.Windows.Media.GradientStop.Color%2A> properties of a <xref:System.Windows.Media.LinearGradientBrush> object's gradient stops with system colors.</span></span> <span data-ttu-id="2c519-119">Pour obtenir un exemple, consultez [utiliser des couleurs système dans un dégradé](how-to-use-system-colors-in-a-gradient.md).</span><span class="sxs-lookup"><span data-stu-id="2c519-119">For an example, see [Use System Colors in a Gradient](how-to-use-system-colors-in-a-gradient.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c519-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c519-120">Example</span></span>  
 <span data-ttu-id="2c519-121">L’exemple suivant utilise une référence de pinceau système dynamique pour définir l’arrière-plan d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="2c519-121">The following example uses a dynamic system brush reference to set the Background of a button.</span></span>  
  
 [!code-xaml[brushsamples_snip#GraphicsMMDynamicSystemColorDesktopBrushKeyExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/DynamicSystemBrushExample.xaml#graphicsmmdynamicsystemcolordesktopbrushkeyexamplewholepage)]  
  
 <span data-ttu-id="2c519-122">L’exemple suivant utilise une référence de pinceau système statique pour définir l’arrière-plan d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="2c519-122">The next example uses a static system brush reference to set the Background of a button.</span></span>  
  
 [!code-xaml[brushsamples_snip#GraphicsMMStaticSystemColorDesktopBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/StaticSystemBrushExample.xaml#graphicsmmstaticsystemcolordesktopbrushexamplewholepage)]  
  
 <span data-ttu-id="2c519-123">Pour obtenir un exemple montrant comment utiliser une couleur système dans un dégradé, consultez [utiliser les couleurs système dans un dégradé](how-to-use-system-colors-in-a-gradient.md).</span><span class="sxs-lookup"><span data-stu-id="2c519-123">For an example showing how to use a system color in a gradient, see [Use System Colors in a Gradient](how-to-use-system-colors-in-a-gradient.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c519-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c519-124">See also</span></span>

- [<span data-ttu-id="2c519-125">Utiliser des couleurs système dans un dégradé</span><span class="sxs-lookup"><span data-stu-id="2c519-125">Use System Colors in a Gradient</span></span>](how-to-use-system-colors-in-a-gradient.md)
- [<span data-ttu-id="2c519-126">Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés</span><span class="sxs-lookup"><span data-stu-id="2c519-126">Painting with Solid Colors and Gradients Overview</span></span>](painting-with-solid-colors-and-gradients-overview.md)
