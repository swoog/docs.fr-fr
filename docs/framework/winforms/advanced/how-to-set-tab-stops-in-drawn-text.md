---
title: 'Procédure : définir des taquets de tabulation dans du texte dessiné'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing with tab stops
- tabs [Windows Forms], drawn text
ms.assetid: 64878f98-39ba-4303-b63f-0859ab682eeb
ms.openlocfilehash: 68dbebfc4fab773fe749f9443d0c61883099d2ab
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967067"
---
# <a name="how-to-set-tab-stops-in-drawn-text"></a><span data-ttu-id="2517a-102">Procédure : définir des taquets de tabulation dans du texte dessiné</span><span class="sxs-lookup"><span data-stu-id="2517a-102">How to: Set Tab Stops in Drawn Text</span></span>
<span data-ttu-id="2517a-103">Vous pouvez définir des taquets de tabulation pour le texte en appelant le <xref:System.Drawing.StringFormat.SetTabStops%2A> méthode d’un <xref:System.Drawing.StringFormat> et transmettre qui <xref:System.Drawing.StringFormat> objet le <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="2517a-103">You can set tab stops for text by calling the <xref:System.Drawing.StringFormat.SetTabStops%2A> method of a <xref:System.Drawing.StringFormat> object and then passing that <xref:System.Drawing.StringFormat> object to the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2517a-104">Le <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType> prend pas en charge l’ajout de taquets de tabulation au texte dessiné, bien que vous pouvez développer onglet existant s’arrête à l’aide de la <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> indicateur.</span><span class="sxs-lookup"><span data-stu-id="2517a-104">The <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType> does not support adding tab stops to drawn text, although you can expand existing tab stops using the <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> flag.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2517a-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="2517a-105">Example</span></span>  
 <span data-ttu-id="2517a-106">L’exemple suivant définit des taquets de tabulation à 150, 250 et 350.</span><span class="sxs-lookup"><span data-stu-id="2517a-106">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="2517a-107">Ensuite, le code affiche une liste avec onglets des noms et scores de test.</span><span class="sxs-lookup"><span data-stu-id="2517a-107">Then, the code displays a tabbed list of names and test scores.</span></span>  
  
 <span data-ttu-id="2517a-108">L’illustration suivante montre le texte à onglets :</span><span class="sxs-lookup"><span data-stu-id="2517a-108">The following illustration shows the tabbed text:</span></span>  
  
 ![Capture d’écran qui affiche la liste de noms et de scores à onglets.](./media/how-to-set-tab-stops-in-drawn-text/tab-list-names-test-scores.png)  
  
 <span data-ttu-id="2517a-110">Le code suivant passe deux arguments à la <xref:System.Drawing.StringFormat.SetTabStops%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="2517a-110">The following code passes two arguments to the <xref:System.Drawing.StringFormat.SetTabStops%2A> method.</span></span> <span data-ttu-id="2517a-111">Le deuxième argument est un tableau qui contient les décalages de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2517a-111">The second argument is an array that contains tab offsets.</span></span> <span data-ttu-id="2517a-112">Le premier argument passé à <xref:System.Drawing.StringFormat.SetTabStops%2A> est 0, ce qui indique que le premier offset dans le tableau est mesuré à partir de la position 0, le bord gauche du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="2517a-112">The first argument passed to <xref:System.Drawing.StringFormat.SetTabStops%2A> is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.FontsAndText#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2517a-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="2517a-113">Compiling the Code</span></span>  
  
- <span data-ttu-id="2517a-114">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="2517a-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2517a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2517a-115">See also</span></span>

- [<span data-ttu-id="2517a-116">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="2517a-116">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="2517a-117">Guide pratique pour Dessiner du texte avec GDI</span><span class="sxs-lookup"><span data-stu-id="2517a-117">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
