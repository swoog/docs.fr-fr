---
title: 'Procédure : Définir la couleur d’un stylet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- pens [Windows Forms], setting color
- colored pens
ms.assetid: a9df06f9-a6d5-4d9b-a2d1-583943540775
ms.openlocfilehash: d0402a7d6bb641ef6d97eb41bc25f3c59b3b4250
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569438"
---
# <a name="how-to-set-the-color-of-a-pen"></a><span data-ttu-id="b61b0-102">Procédure : Définir la couleur d’un stylet</span><span class="sxs-lookup"><span data-stu-id="b61b0-102">How to: Set the Color of a Pen</span></span>
<span data-ttu-id="b61b0-103">Cet exemple modifie la couleur d’un préexistants <xref:System.Drawing.Pen> objet</span><span class="sxs-lookup"><span data-stu-id="b61b0-103">This example changes the color of a pre-existing <xref:System.Drawing.Pen> object</span></span>  
  
## <a name="example"></a><span data-ttu-id="b61b0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b61b0-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#9](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#9)]
 [!code-csharp[System.Drawing.ConceptualHowTos#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#9)]
 [!code-vb[System.Drawing.ConceptualHowTos#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#9)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b61b0-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="b61b0-105">Compiling the Code</span></span>  
 <span data-ttu-id="b61b0-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="b61b0-106">This example requires:</span></span>  
  
-   <span data-ttu-id="b61b0-107">Un <xref:System.Drawing.Pen> objet nommé `myPen`.</span><span class="sxs-lookup"><span data-stu-id="b61b0-107">A <xref:System.Drawing.Pen> object named `myPen`.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="b61b0-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="b61b0-108">Robust Programming</span></span>  
 <span data-ttu-id="b61b0-109">Vous devez appeler <xref:System.Drawing.Pen.Dispose%2A> sur les objets qui consomment des ressources système (telles que <xref:System.Drawing.Pen> objets) une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="b61b0-109">You should call <xref:System.Drawing.Pen.Dispose%2A> on objects that consume system resources (such as <xref:System.Drawing.Pen> objects) after you are finished using them.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b61b0-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b61b0-110">See also</span></span>
- <xref:System.Drawing.Pen>
- [<span data-ttu-id="b61b0-111">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="b61b0-111">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [<span data-ttu-id="b61b0-112">Guide pratique pour Créer un stylet</span><span class="sxs-lookup"><span data-stu-id="b61b0-112">How to: Create a Pen</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-a-pen.md)
- [<span data-ttu-id="b61b0-113">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="b61b0-113">Using a Pen to Draw Lines and Shapes</span></span>](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="b61b0-114">Stylets, lignes et rectangles dans GDI+</span><span class="sxs-lookup"><span data-stu-id="b61b0-114">Pens, Lines, and Rectangles in GDI+</span></span>](../../../../docs/framework/winforms/advanced/pens-lines-and-rectangles-in-gdi.md)
