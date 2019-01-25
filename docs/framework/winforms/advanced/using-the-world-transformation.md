---
title: Utilisation de la transformation universelle
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], world transformation
- world transformation [Windows Forms], examples
ms.assetid: 1e717711-1361-448e-aa49-0f3ec43110c9
ms.openlocfilehash: ec232c92d32b91a7b334b237c869db8eb428eccc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647606"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="c20b6-102">Utilisation de la transformation universelle</span><span class="sxs-lookup"><span data-stu-id="c20b6-102">Using the World Transformation</span></span>
<span data-ttu-id="c20b6-103">La transformation universelle est une propriété de la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="c20b6-103">The world transformation is a property of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="c20b6-104">Les nombres qui spécifient la transformation universelle sont stockés dans un <xref:System.Drawing.Drawing2D.Matrix> objet qui représente une matrice 3 x 3.</span><span class="sxs-lookup"><span data-stu-id="c20b6-104">The numbers that specify the world transformation are stored in a <xref:System.Drawing.Drawing2D.Matrix> object, which represents a 3×3 matrix.</span></span> <span data-ttu-id="c20b6-105">Le <xref:System.Drawing.Drawing2D.Matrix> et <xref:System.Drawing.Graphics> classes disposent de plusieurs méthodes pour définir les nombres dans la matrice de transformation de monde.</span><span class="sxs-lookup"><span data-stu-id="c20b6-105">The <xref:System.Drawing.Drawing2D.Matrix> and <xref:System.Drawing.Graphics> classes have several methods for setting the numbers in the world transformation matrix.</span></span>  
  
## <a name="different-types-of-transformations"></a><span data-ttu-id="c20b6-106">Différents Types de Transformations</span><span class="sxs-lookup"><span data-stu-id="c20b6-106">Different Types of Transformations</span></span>  
 <span data-ttu-id="c20b6-107">Dans l’exemple suivant, le code crée un rectangle de 50 x 50 tout d’abord et situe à l’origine (0, 0).</span><span class="sxs-lookup"><span data-stu-id="c20b6-107">In the following example, the code first creates a 50×50 rectangle and locates it at the origin (0, 0).</span></span> <span data-ttu-id="c20b6-108">L’origine est dans l’angle supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="c20b6-108">The origin is at the upper-left corner of the client area.</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#11)]  
  
 <span data-ttu-id="c20b6-109">Le code suivant applique une transformation de mise à l’échelle qui développe le rectangle par un facteur de 1,75 dans la direction x et réduit le rectangle par un facteur de 0,5 dans la direction y :</span><span class="sxs-lookup"><span data-stu-id="c20b6-109">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#12)]  
  
 <span data-ttu-id="c20b6-110">Le résultat est un rectangle qui est plus longue dans la direction x et plus court sur l’axe y que l’original.</span><span class="sxs-lookup"><span data-stu-id="c20b6-110">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>  
  
 <span data-ttu-id="c20b6-111">Pour faire pivoter le rectangle au lieu de la mise à l’échelle il, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c20b6-111">To rotate the rectangle instead of scaling it, use the following code:</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#13)]  
  
 <span data-ttu-id="c20b6-112">Pour traduire le rectangle, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c20b6-112">To translate the rectangle, use the following code:</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#14)]  
  
## <a name="see-also"></a><span data-ttu-id="c20b6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c20b6-113">See also</span></span>
- <xref:System.Drawing.Drawing2D.Matrix>
- [<span data-ttu-id="c20b6-114">Systèmes de coordonnées et transformations</span><span class="sxs-lookup"><span data-stu-id="c20b6-114">Coordinate Systems and Transformations</span></span>](../../../../docs/framework/winforms/advanced/coordinate-systems-and-transformations.md)
- [<span data-ttu-id="c20b6-115">Utilisation des transformations dans GDI+ managé</span><span class="sxs-lookup"><span data-stu-id="c20b6-115">Using Transformations in Managed GDI+</span></span>](../../../../docs/framework/winforms/advanced/using-transformations-in-managed-gdi.md)
