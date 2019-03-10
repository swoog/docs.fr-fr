---
title: 'Procédure : Créer un stylet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- graphics [Windows Forms], creating pens
- pens [Windows Forms], creating
- Pen object
ms.assetid: 7fbea8b7-7ac1-4413-9c17-733a850381e3
ms.openlocfilehash: 3d88824845bf357dd9ee5f1ee8fd02f095aee605
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716918"
---
# <a name="how-to-create-a-pen"></a><span data-ttu-id="ef647-102">Procédure : Créer un stylet</span><span class="sxs-lookup"><span data-stu-id="ef647-102">How to: Create a Pen</span></span>
<span data-ttu-id="ef647-103">Cet exemple crée un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="ef647-103">This example creates a <xref:System.Drawing.Pen> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ef647-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ef647-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#3](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#3)]
 [!code-csharp[System.Drawing.ConceptualHowTos#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#3)]
 [!code-vb[System.Drawing.ConceptualHowTos#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#3)]  
  
## <a name="robust-programming"></a><span data-ttu-id="ef647-105">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="ef647-105">Robust Programming</span></span>  
 <span data-ttu-id="ef647-106">Une fois que vous avez fini d’utiliser des objets qui consomment des ressources système, telles que <xref:System.Drawing.Pen> objets, vous devez appeler <xref:System.Drawing.Pen.Dispose%2A> sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="ef647-106">After you have finished using objects that consume system resources, such as <xref:System.Drawing.Pen> objects, you should call <xref:System.Drawing.Pen.Dispose%2A> on them.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef647-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef647-107">See also</span></span>
- <xref:System.Drawing.Pen>
- [<span data-ttu-id="ef647-108">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="ef647-108">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="ef647-109">Stylets, lignes et rectangles dans GDI+</span><span class="sxs-lookup"><span data-stu-id="ef647-109">Pens, Lines, and Rectangles in GDI+</span></span>](pens-lines-and-rectangles-in-gdi.md)
