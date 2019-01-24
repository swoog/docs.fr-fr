---
title: 'Procédure : Dessiner une ligne dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- Graphics.DrawLine
helpviewer_keywords:
- examples [Windows Forms], drawing lines on forms
- drawing [Windows Forms], lines
- lines [Windows Forms], drawing
- drawing lines
ms.assetid: 55c1dbeb-75d0-430c-9814-a24b8971ad8c
ms.openlocfilehash: 4274072b55c79cfe88e906d1401d275b414ebe97
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54586746"
---
# <a name="how-to-draw-a-line-on-a-windows-form"></a><span data-ttu-id="75709-102">Procédure : Dessiner une ligne dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="75709-102">How to: Draw a Line on a Windows Form</span></span>
<span data-ttu-id="75709-103">Cet exemple dessine une ligne dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="75709-103">This example draws a line on a form.</span></span> <span data-ttu-id="75709-104">En général, lorsque vous dessinez dans un formulaire, vous gérez le formulaire <xref:System.Windows.Forms.Control.Paint> événements et effectuer le dessin à l’aide du <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> propriété de la <xref:System.Windows.Forms.PaintEventArgs>, comme illustré dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="75709-104">Typically, when you draw on a form, you handle the form’s  <xref:System.Windows.Forms.Control.Paint> event and perform the drawing using the <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> property of the <xref:System.Windows.Forms.PaintEventArgs>, as shown in this example</span></span>  
  
## <a name="example"></a><span data-ttu-id="75709-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="75709-105">Example</span></span>  
 [!code-csharp[System.Drawing.UsingAPen#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingAPen#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="75709-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="75709-106">Compiling the Code</span></span>  
 <span data-ttu-id="75709-107">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="75709-107">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="75709-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="75709-108">Robust Programming</span></span>  
 <span data-ttu-id="75709-109">Vous devez toujours appeler <xref:System.IDisposable.Dispose%2A> sur tous les objets qui consomment des ressources système, telles que <xref:System.Drawing.Pen> objets.</span><span class="sxs-lookup"><span data-stu-id="75709-109">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Pen> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75709-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75709-110">See also</span></span>
- <xref:System.Drawing.Graphics.DrawLine%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [<span data-ttu-id="75709-111">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="75709-111">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [<span data-ttu-id="75709-112">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="75709-112">Using a Pen to Draw Lines and Shapes</span></span>](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="75709-113">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="75709-113">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
