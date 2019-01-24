---
title: 'Procédure : Dessiner une ligne en pointillés personnalisée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], custom
- lines [Windows Forms], drawing
- lines [Windows Forms], dashed
ms.assetid: cd0ed96a-cce4-47b9-b58a-3bae2e3d1bee
ms.openlocfilehash: 77b4b959523c6d35dece2d759eeb71be04b53d93
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538620"
---
# <a name="how-to-draw-a-custom-dashed-line"></a><span data-ttu-id="37e60-102">Procédure : Dessiner une ligne en pointillés personnalisée</span><span class="sxs-lookup"><span data-stu-id="37e60-102">How to: Draw a Custom Dashed Line</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="37e60-103">fournit plusieurs styles de ligne sont répertoriées dans le <xref:System.Drawing.Drawing2D.DashStyle> énumération.</span><span class="sxs-lookup"><span data-stu-id="37e60-103">provides several dash styles that are listed in the <xref:System.Drawing.Drawing2D.DashStyle> enumeration.</span></span> <span data-ttu-id="37e60-104">Si ces styles de tiret standard ne répondent pas à vos besoins, vous pouvez créer un modèle de tirets personnalisés.</span><span class="sxs-lookup"><span data-stu-id="37e60-104">If those standard dash styles do not suit your needs, you can create a custom dash pattern.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37e60-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="37e60-105">Example</span></span>  
 <span data-ttu-id="37e60-106">Pour dessiner une ligne en pointillés personnalisée, placez les longueurs des tirets et des espaces dans un tableau et assignez le tableau comme valeur de la <xref:System.Drawing.Pen.DashPattern%2A> propriété d’un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="37e60-106">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and assign the array as the value of the <xref:System.Drawing.Pen.DashPattern%2A> property of a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="37e60-107">L’exemple suivant dessine une ligne en pointillés personnalisée en fonction du tableau `{5, 2, 15, 4}`.</span><span class="sxs-lookup"><span data-stu-id="37e60-107">The following example draws a custom dashed line based on the array `{5, 2, 15, 4}`.</span></span> <span data-ttu-id="37e60-108">Si vous multipliez les éléments du tableau par la largeur du stylet 5, vous obtenez `{25, 10, 75, 20}`.</span><span class="sxs-lookup"><span data-stu-id="37e60-108">If you multiply the elements of the array by the pen width of 5, you get `{25, 10, 75, 20}`.</span></span> <span data-ttu-id="37e60-109">Les tirets affichées longueur alternent entre 25 et 75, et les espaces longueur alternent entre 10 et 20.</span><span class="sxs-lookup"><span data-stu-id="37e60-109">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>  
  
 <span data-ttu-id="37e60-110">L’illustration suivante montre la ligne en pointillés qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="37e60-110">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="37e60-111">Notez que le tiret final doit être inférieure à 25 unités afin que la ligne peut se terminer à (405, 5).</span><span class="sxs-lookup"><span data-stu-id="37e60-111">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>  
  
 <span data-ttu-id="37e60-112">![Stylets](../../../../docs/framework/winforms/advanced/media/pens6.gif "pens6")</span><span class="sxs-lookup"><span data-stu-id="37e60-112">![Pens](../../../../docs/framework/winforms/advanced/media/pens6.gif "pens6")</span></span>  
  
 [!code-csharp[System.Drawing.UsingAPen#51](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#51)]
 [!code-vb[System.Drawing.UsingAPen#51](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#51)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="37e60-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="37e60-113">Compiling the Code</span></span>  
 <span data-ttu-id="37e60-114">Créer un formulaire Windows et de gérer le formulaire <xref:System.Windows.Forms.Control.Paint> événement.</span><span class="sxs-lookup"><span data-stu-id="37e60-114">Create a Windows Form and handle the form's <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="37e60-115">Collez le code précédent dans le <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="37e60-115">Paste the preceding code into the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37e60-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37e60-116">See also</span></span>
- [<span data-ttu-id="37e60-117">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="37e60-117">Using a Pen to Draw Lines and Shapes</span></span>](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
