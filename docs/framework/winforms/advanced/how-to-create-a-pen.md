---
title: 'Comment : créer un objet Pen'
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
ms.openlocfilehash: aff1771af12a9f59127a9f21f4b692d6214c457d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33520976"
---
# <a name="how-to-create-a-pen"></a><span data-ttu-id="0eb51-102">Comment : créer un objet Pen</span><span class="sxs-lookup"><span data-stu-id="0eb51-102">How to: Create a Pen</span></span>
<span data-ttu-id="0eb51-103">Cet exemple crée un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="0eb51-103">This example creates a <xref:System.Drawing.Pen> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0eb51-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0eb51-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#3](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#3)]
 [!code-csharp[System.Drawing.ConceptualHowTos#3](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#3)]
 [!code-vb[System.Drawing.ConceptualHowTos#3](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#3)]  
  
## <a name="robust-programming"></a><span data-ttu-id="0eb51-105">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="0eb51-105">Robust Programming</span></span>  
 <span data-ttu-id="0eb51-106">Une fois que vous avez fini d’utiliser des objets qui consomment des ressources système, telles que <xref:System.Drawing.Pen> des objets, vous devez appeler <xref:System.Drawing.Pen.Dispose%2A> sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="0eb51-106">After you have finished using objects that consume system resources, such as <xref:System.Drawing.Pen> objects, you should call <xref:System.Drawing.Pen.Dispose%2A> on them.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0eb51-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eb51-107">See Also</span></span>  
 <xref:System.Drawing.Pen>  
 [<span data-ttu-id="0eb51-108">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="0eb51-108">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)  
 [<span data-ttu-id="0eb51-109">Stylets, lignes et rectangles dans GDI+</span><span class="sxs-lookup"><span data-stu-id="0eb51-109">Pens, Lines, and Rectangles in GDI+</span></span>](../../../../docs/framework/winforms/advanced/pens-lines-and-rectangles-in-gdi.md)
