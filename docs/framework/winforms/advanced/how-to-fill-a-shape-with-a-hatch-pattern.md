---
title: 'Procédure : Remplir une forme avec un motif hachuré'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- patterns [Windows Forms], adding to shapes
- shapes [Windows Forms], filling with patterns
- brushes [Windows Forms], using hatch brushes
ms.assetid: 9c8300ff-187b-404f-af1f-ebd499f5b16f
ms.openlocfilehash: 885f0d22e83767bda3ef76c54f0857dd2a148344
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57719713"
---
# <a name="how-to-fill-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="6e969-102">Procédure : Remplir une forme avec un motif hachuré</span><span class="sxs-lookup"><span data-stu-id="6e969-102">How to: Fill a Shape with a Hatch Pattern</span></span>
<span data-ttu-id="6e969-103">Un motif hachuré est effectué à partir de deux couleurs : un pour l’arrière-plan et un pour les lignes qui forment le modèle sur l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="6e969-103">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="6e969-104">Pour remplir une forme fermée avec un motif hachuré, utilisez un <xref:System.Drawing.Drawing2D.HatchBrush> objet.</span><span class="sxs-lookup"><span data-stu-id="6e969-104">To fill a closed shape with a hatch pattern, use a <xref:System.Drawing.Drawing2D.HatchBrush> object.</span></span> <span data-ttu-id="6e969-105">L’exemple suivant montre comment remplir une ellipse avec un motif hachuré :</span><span class="sxs-lookup"><span data-stu-id="6e969-105">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>  
  
## <a name="example"></a><span data-ttu-id="6e969-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="6e969-106">Example</span></span>  
 <span data-ttu-id="6e969-107">Le <xref:System.Drawing.Drawing2D.HatchBrush.%23ctor%2A> constructeur accepte trois arguments : le style de hachurage, la couleur de la ligne de hachurage et la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="6e969-107">The <xref:System.Drawing.Drawing2D.HatchBrush.%23ctor%2A> constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="6e969-108">L’argument de style de hachurage peut être n’importe quelle valeur à partir de la <xref:System.Drawing.Drawing2D.HatchStyle> énumération.</span><span class="sxs-lookup"><span data-stu-id="6e969-108">The hatch style argument can be any value from the <xref:System.Drawing.Drawing2D.HatchStyle> enumeration.</span></span> <span data-ttu-id="6e969-109">Il y a plus de 50 éléments dans le <xref:System.Drawing.Drawing2D.HatchStyle> énumération ; quelques-uns de ces éléments sont affichés dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="6e969-109">There are more than fifty elements in the <xref:System.Drawing.Drawing2D.HatchStyle> enumeration; a few of those elements are shown in the following list:</span></span>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.Horizontal>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.Vertical>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.ForwardDiagonal>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.BackwardDiagonal>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.Cross>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.DiagonalCross>  
  
 <span data-ttu-id="6e969-110">L’illustration suivante montre l’ellipse remplie.</span><span class="sxs-lookup"><span data-stu-id="6e969-110">The following illustration shows the filled ellipse.</span></span>  
  
 <span data-ttu-id="6e969-111">![Le modèle de hachurage](./media/hatch1.png "hatch1")</span><span class="sxs-lookup"><span data-stu-id="6e969-111">![Hatch Pattern](./media/hatch1.png "hatch1")</span></span>  
  
 [!code-csharp[System.Drawing.UsingABrush#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.UsingABrush#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6e969-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="6e969-112">Compiling the Code</span></span>  
 <span data-ttu-id="6e969-113">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="6e969-113">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e969-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e969-114">See also</span></span>
- [<span data-ttu-id="6e969-115">Utilisation d'un pinceau pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="6e969-115">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
