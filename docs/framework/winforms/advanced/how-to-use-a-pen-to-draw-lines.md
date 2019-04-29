---
title: 'Procédure : utiliser un stylet pour dessiner des lignes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
ms.assetid: 0828c331-a438-4bdd-a4d6-3ef1e59e8795
ms.openlocfilehash: 8b4eb7684e15ffd5b0b528771490ba66f3b7bb45
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61954438"
---
# <a name="how-to-use-a-pen-to-draw-lines"></a><span data-ttu-id="3f969-102">Procédure : utiliser un stylet pour dessiner des lignes</span><span class="sxs-lookup"><span data-stu-id="3f969-102">How to: Use a Pen to Draw Lines</span></span>
<span data-ttu-id="3f969-103">Pour dessiner des lignes, vous devez un <xref:System.Drawing.Graphics> objet et un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="3f969-103">To draw lines, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="3f969-104">Le <xref:System.Drawing.Graphics> objet fournit les <xref:System.Drawing.Graphics.DrawLine%2A> (méthode) et le <xref:System.Drawing.Pen> objet stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="3f969-104">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawLine%2A> method, and the <xref:System.Drawing.Pen> object stores features of the line, such as color and width.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f969-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f969-105">Example</span></span>  
 <span data-ttu-id="3f969-106">L’exemple suivant dessine une ligne à partir de (20, 10) à (300, 100).</span><span class="sxs-lookup"><span data-stu-id="3f969-106">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="3f969-107">La première instruction utilise le <xref:System.Drawing.Pen.%23ctor%2A> constructeur de classe pour créer un stylet noir.</span><span class="sxs-lookup"><span data-stu-id="3f969-107">The first statement uses the <xref:System.Drawing.Pen.%23ctor%2A> class constructor to create a black pen.</span></span> <span data-ttu-id="3f969-108">L’argument passé à la <xref:System.Drawing.Pen.%23ctor%2A> constructeur est un <xref:System.Drawing.Color> objet créé avec le <xref:System.Drawing.Color.FromArgb%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3f969-108">The one argument passed to the <xref:System.Drawing.Pen.%23ctor%2A> constructor is a <xref:System.Drawing.Color> object created with the <xref:System.Drawing.Color.FromArgb%2A> method.</span></span> <span data-ttu-id="3f969-109">Les valeurs utilisées pour créer le <xref:System.Drawing.Color> objet — (255, 0, 0, 0), correspondent aux composants alphabétiques, rouges, vert et bleus de la couleur.</span><span class="sxs-lookup"><span data-stu-id="3f969-109">The values used to create the <xref:System.Drawing.Color> object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="3f969-110">Ces valeurs définissent un stylet noir opaque.</span><span class="sxs-lookup"><span data-stu-id="3f969-110">These values define an opaque black pen.</span></span>  
  
 [!code-csharp[System.Drawing.UsingAPen#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingAPen#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3f969-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="3f969-111">Compiling the Code</span></span>  
 <span data-ttu-id="3f969-112">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="3f969-112">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f969-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f969-113">See also</span></span>

- <xref:System.Drawing.Pen>
- [<span data-ttu-id="3f969-114">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="3f969-114">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="3f969-115">Stylets, lignes et rectangles dans GDI+</span><span class="sxs-lookup"><span data-stu-id="3f969-115">Pens, Lines, and Rectangles in GDI+</span></span>](pens-lines-and-rectangles-in-gdi.md)
