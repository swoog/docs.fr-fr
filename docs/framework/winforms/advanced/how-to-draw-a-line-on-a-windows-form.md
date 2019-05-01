---
title: 'Procédure : dessiner une ligne dans un formulaire Windows'
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
ms.openlocfilehash: aab04b9236175cedd154b817db5a6f6450503105
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62004157"
---
# <a name="how-to-draw-a-line-on-a-windows-form"></a><span data-ttu-id="a2f1c-102">Procédure : dessiner une ligne dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="a2f1c-102">How to: Draw a Line on a Windows Form</span></span>
<span data-ttu-id="a2f1c-103">Cet exemple dessine une ligne dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-103">This example draws a line on a form.</span></span> <span data-ttu-id="a2f1c-104">En général, lorsque vous dessinez dans un formulaire, vous gérez le formulaire <xref:System.Windows.Forms.Control.Paint> événements et effectuer le dessin à l’aide du <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> propriété de la <xref:System.Windows.Forms.PaintEventArgs>, comme illustré dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="a2f1c-104">Typically, when you draw on a form, you handle the form’s  <xref:System.Windows.Forms.Control.Paint> event and perform the drawing using the <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> property of the <xref:System.Windows.Forms.PaintEventArgs>, as shown in this example</span></span>  
  
## <a name="example"></a><span data-ttu-id="a2f1c-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2f1c-105">Example</span></span>  
 [!code-csharp[System.Drawing.UsingAPen#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingAPen#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a2f1c-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="a2f1c-106">Compiling the Code</span></span>  
 <span data-ttu-id="a2f1c-107">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-107">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="a2f1c-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="a2f1c-108">Robust Programming</span></span>  
 <span data-ttu-id="a2f1c-109">Vous devez toujours appeler <xref:System.IDisposable.Dispose%2A> sur tous les objets qui consomment des ressources système, telles que <xref:System.Drawing.Pen> objets.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-109">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Pen> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2f1c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f1c-110">See also</span></span>

- <xref:System.Drawing.Graphics.DrawLine%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [<span data-ttu-id="a2f1c-111">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="a2f1c-111">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="a2f1c-112">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="a2f1c-112">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="a2f1c-113">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a2f1c-113">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
