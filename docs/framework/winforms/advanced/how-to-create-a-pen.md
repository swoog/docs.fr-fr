---
title: 'Procédure : créer un stylet'
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
ms.openlocfilehash: 69fe6157c710ae63df9dbf391a5d355d1c3f9765
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59148107"
---
# <a name="how-to-create-a-pen"></a><span data-ttu-id="bd877-102">Procédure : créer un stylet</span><span class="sxs-lookup"><span data-stu-id="bd877-102">How to: Create a Pen</span></span>
<span data-ttu-id="bd877-103">Cet exemple crée un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="bd877-103">This example creates a <xref:System.Drawing.Pen> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd877-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd877-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#3](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#3)]
 [!code-csharp[System.Drawing.ConceptualHowTos#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#3)]
 [!code-vb[System.Drawing.ConceptualHowTos#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#3)]  
  
## <a name="robust-programming"></a><span data-ttu-id="bd877-105">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="bd877-105">Robust Programming</span></span>  
 <span data-ttu-id="bd877-106">Une fois que vous avez fini d’utiliser des objets qui consomment des ressources système, telles que <xref:System.Drawing.Pen> objets, vous devez appeler <xref:System.Drawing.Pen.Dispose%2A> sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="bd877-106">After you have finished using objects that consume system resources, such as <xref:System.Drawing.Pen> objects, you should call <xref:System.Drawing.Pen.Dispose%2A> on them.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd877-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd877-107">See also</span></span>

- <xref:System.Drawing.Pen>
- [<span data-ttu-id="bd877-108">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="bd877-108">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="bd877-109">Stylets, lignes et rectangles dans GDI+</span><span class="sxs-lookup"><span data-stu-id="bd877-109">Pens, Lines, and Rectangles in GDI+</span></span>](pens-lines-and-rectangles-in-gdi.md)
