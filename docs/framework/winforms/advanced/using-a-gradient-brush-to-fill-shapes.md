---
title: Utilisation d'un pinceau à dégradé pour remplir des formes
ms.date: 03/30/2017
helpviewer_keywords:
- brushes [Windows Forms], gradient brushes
- gradient brushes
- examples [Windows Forms], gradient brushes
ms.assetid: 2c6037b9-05bd-44c0-a22a-19584b722524
ms.openlocfilehash: 5771aaabd283d71f5fa6934f86a1c24a57f38dca
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61954470"
---
# <a name="using-a-gradient-brush-to-fill-shapes"></a><span data-ttu-id="76fcb-102">Utilisation d'un pinceau à dégradé pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="76fcb-102">Using a Gradient Brush to Fill Shapes</span></span>
<span data-ttu-id="76fcb-103">Vous pouvez utiliser un pinceau de dégradé pour remplir une forme avec une couleur.</span><span class="sxs-lookup"><span data-stu-id="76fcb-103">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="76fcb-104">Par exemple, vous pouvez utiliser un dégradé horizontal pour remplir une forme avec une couleur qui change graduellement à mesure que vous déplacez le bord gauche de la forme vers le bord droit.</span><span class="sxs-lookup"><span data-stu-id="76fcb-104">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="76fcb-105">Imaginez un rectangle avec un bord gauche qui est noir (représenté par les composants rouges, vert et bleus 0, 0, 0) et un bord droit de rouge (représenté par 255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="76fcb-105">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="76fcb-106">Si le rectangle est 256 pixels de large, le composant rouge d’un pixel donné sera égale à celle de la composante rouge de pixel à sa gauche.</span><span class="sxs-lookup"><span data-stu-id="76fcb-106">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="76fcb-107">Le pixel de gauche dans une ligne a des composants de couleur (0, 0, 0), le deuxième pixel a (1, 0, 0), le troisième pixel (2, 0, 0) et ainsi de suite, jusqu'à ce que vous arriviez au pixel plus à droite, ce qui a des composants de couleur (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="76fcb-107">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="76fcb-108">Ces valeurs de couleur interpolée composent le dégradé de couleur.</span><span class="sxs-lookup"><span data-stu-id="76fcb-108">These interpolated color values make up the color gradient.</span></span>  
  
 <span data-ttu-id="76fcb-109">Un dégradé linéaire change de couleur quand vous déplacez horizontalement, verticalement ou parallèlement à une ligne inclinée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="76fcb-109">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="76fcb-110">Un dégradé de tracé change de couleur quand vous déplacez sur l’intérieur et de la limite d’un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="76fcb-110">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="76fcb-111">Vous pouvez personnaliser les dégradés de chemin d’accès pour obtenir une grande variété d’effets.</span><span class="sxs-lookup"><span data-stu-id="76fcb-111">You can customize path gradients to achieve a wide variety of effects.</span></span>  
  
 <span data-ttu-id="76fcb-112">L’illustration suivante montre un rectangle rempli avec un pinceau dégradé linéaire et une ellipse remplie avec un pinceau de dégradé de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="76fcb-112">The following illustration shows a rectangle filled with a linear gradient brush and an ellipse filled with a path gradient brush.</span></span>  
  
 <span data-ttu-id="76fcb-113">![Gradient](./media/gradient2.png "gradient2")</span><span class="sxs-lookup"><span data-stu-id="76fcb-113">![Gradient](./media/gradient2.png "gradient2")</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="76fcb-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="76fcb-114">In This Section</span></span>  
 [<span data-ttu-id="76fcb-115">Guide pratique pour Créer un dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="76fcb-115">How to: Create a Linear Gradient</span></span>](how-to-create-a-linear-gradient.md)  
 <span data-ttu-id="76fcb-116">Montre comment créer un dégradé linéaire en utilisant la <xref:System.Drawing.Drawing2D.LinearGradientBrush> classe.</span><span class="sxs-lookup"><span data-stu-id="76fcb-116">Shows how to create a linear gradient using the <xref:System.Drawing.Drawing2D.LinearGradientBrush> class.</span></span>  
  
 [<span data-ttu-id="76fcb-117">Guide pratique pour Créer un dégradé de tracé</span><span class="sxs-lookup"><span data-stu-id="76fcb-117">How to: Create a Path Gradient</span></span>](how-to-create-a-path-gradient.md)  
 <span data-ttu-id="76fcb-118">Décrit comment créer un dégradé de chemin d’accès à l’aide la <xref:System.Drawing.Drawing2D.PathGradientBrush> classe.</span><span class="sxs-lookup"><span data-stu-id="76fcb-118">Describes how to create a path gradient using the <xref:System.Drawing.Drawing2D.PathGradientBrush> class.</span></span>  
  
 [<span data-ttu-id="76fcb-119">Guide pratique pour Appliquer une Correction Gamma à un dégradé</span><span class="sxs-lookup"><span data-stu-id="76fcb-119">How to: Apply Gamma Correction to a Gradient</span></span>](how-to-apply-gamma-correction-to-a-gradient.md)  
 <span data-ttu-id="76fcb-120">Explique comment utiliser la correction gamma avec un pinceau de dégradé.</span><span class="sxs-lookup"><span data-stu-id="76fcb-120">Explains how to use gamma correction with a gradient brush.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="76fcb-121">Référence</span><span class="sxs-lookup"><span data-stu-id="76fcb-121">Reference</span></span>  
 <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>  
 <span data-ttu-id="76fcb-122">Contient une description de cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="76fcb-122">Contains a description of this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Drawing2D.PathGradientBrush?displayProperty=nameWithType>  
 <span data-ttu-id="76fcb-123">Contient une description de cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="76fcb-123">Contains a description of this class and has links to all of its members.</span></span>
