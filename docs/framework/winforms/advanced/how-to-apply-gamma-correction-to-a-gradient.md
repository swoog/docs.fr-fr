---
title: 'Procédure : Appliquer une Correction Gamma à un dégradé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- gradient brushes [Windows Forms], gamma correction
- gradients [Windows Forms], gamma correction
ms.assetid: da4690e7-5fac-4fd2-b3f0-5cb35c165b92
ms.openlocfilehash: b3b45c312542a3f8410bd93fcbe4e4cb70aa8516
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527157"
---
# <a name="how-to-apply-gamma-correction-to-a-gradient"></a><span data-ttu-id="47a21-102">Procédure : Appliquer une Correction Gamma à un dégradé</span><span class="sxs-lookup"><span data-stu-id="47a21-102">How to: Apply Gamma Correction to a Gradient</span></span>
<span data-ttu-id="47a21-103">Vous pouvez activer la correction gamma pour un pinceau dégradé linéaire en définissant le pinceau <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="47a21-103">You can enable gamma correction for a linear gradient brush by setting the brush's <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> property to `true`.</span></span> <span data-ttu-id="47a21-104">Vous pouvez désactiver la correction gamma en définissant le <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> propriété `false`.</span><span class="sxs-lookup"><span data-stu-id="47a21-104">You can disable gamma correction by setting the <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> property to `false`.</span></span> <span data-ttu-id="47a21-105">La correction du gamma est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a21-105">Gamma correction is disabled by default.</span></span>  
  
## <a name="example"></a><span data-ttu-id="47a21-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="47a21-106">Example</span></span>  
 <span data-ttu-id="47a21-107">L’exemple crée un pinceau dégradé linéaire et utilise ce pinceau pour remplir les deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="47a21-107">The example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="47a21-108">Le premier est rempli sans correction gamma, et le deuxième rectangle est rempli avec une correction gamma.</span><span class="sxs-lookup"><span data-stu-id="47a21-108">The first rectangle is filled without gamma correction, and the second rectangle is filled with gamma correction.</span></span>  
  
 <span data-ttu-id="47a21-109">L’illustration suivante montre les deux rectangles remplis.</span><span class="sxs-lookup"><span data-stu-id="47a21-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="47a21-110">Le rectangle supérieur, ce qui n’a pas de correction gamma, apparaît foncé au milieu.</span><span class="sxs-lookup"><span data-stu-id="47a21-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="47a21-111">Le rectangle en bas, ce qui a une correction gamma, semble intensité plus régulière.</span><span class="sxs-lookup"><span data-stu-id="47a21-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>  
  
 <span data-ttu-id="47a21-112">![Gradient](../../../../docs/framework/winforms/advanced/media/gammagradient1.png "gammagradient1")</span><span class="sxs-lookup"><span data-stu-id="47a21-112">![Gradient](../../../../docs/framework/winforms/advanced/media/gammagradient1.png "gammagradient1")</span></span>  
  
 [!code-csharp[System.Drawing.UsingaGradientBrush#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingaGradientBrush#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="47a21-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="47a21-113">Compiling the Code</span></span>  
 <span data-ttu-id="47a21-114">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="47a21-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47a21-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47a21-115">See also</span></span>
- <xref:System.Drawing.Drawing2D.LinearGradientBrush>
- [<span data-ttu-id="47a21-116">Utilisation d'un pinceau à dégradé pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="47a21-116">Using a Gradient Brush to Fill Shapes</span></span>](../../../../docs/framework/winforms/advanced/using-a-gradient-brush-to-fill-shapes.md)
