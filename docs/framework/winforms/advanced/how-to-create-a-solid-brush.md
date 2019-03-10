---
title: 'Procédure : Créer un pinceau uni'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- solid color brushes
- brushes [Windows Forms], examples
- brushes [Windows Forms], creating solid
ms.assetid: 85c3fe7d-fb1d-4591-8a9f-d75b556b90af
ms.openlocfilehash: d7fb7c11a69cae69210dd2eece3336bc40c505c7
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711978"
---
# <a name="how-to-create-a-solid-brush"></a><span data-ttu-id="1db51-102">Procédure : Créer un pinceau uni</span><span class="sxs-lookup"><span data-stu-id="1db51-102">How to: Create a Solid Brush</span></span>
<span data-ttu-id="1db51-103">Cet exemple crée un <xref:System.Drawing.SolidBrush> objet qui peut être utilisé par un <xref:System.Drawing.Graphics> objet pour remplir des formes.</span><span class="sxs-lookup"><span data-stu-id="1db51-103">This example creates a <xref:System.Drawing.SolidBrush> object that can be used by a <xref:System.Drawing.Graphics> object for filling shapes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1db51-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1db51-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#1)]
 [!code-csharp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#1)]
 [!code-vb[System.Drawing.ConceptualHowTos#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#1)]  
  
## <a name="robust-programming"></a><span data-ttu-id="1db51-105">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="1db51-105">Robust Programming</span></span>  
 <span data-ttu-id="1db51-106">Une fois que vous avez terminé, vous devez appeler <xref:System.IDisposable.Dispose%2A> sur les objets qui consomment des ressources système, tels que les objets de pinceau.</span><span class="sxs-lookup"><span data-stu-id="1db51-106">After you have finished using them, you should call <xref:System.IDisposable.Dispose%2A> on objects that consume system resources, such as brush objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1db51-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1db51-107">See also</span></span>
- <xref:System.Drawing.SolidBrush>
- <xref:System.Drawing.Brush>
- [<span data-ttu-id="1db51-108">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="1db51-108">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="1db51-109">Pinceaux et remplissage de formes dans GDI+</span><span class="sxs-lookup"><span data-stu-id="1db51-109">Brushes and Filled Shapes in GDI+</span></span>](brushes-and-filled-shapes-in-gdi.md)
- [<span data-ttu-id="1db51-110">Utilisation d'un pinceau pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="1db51-110">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
