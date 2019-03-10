---
title: 'Procédure : Étirer un ToolStripTextBox pour remplir la largeur restante d’un ToolStrip (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text boxes [Windows Forms], stretching in ToolStrip control [Windows Forms]
- ToolStrip control [Windows Forms], stretching a text box
ms.assetid: 0e610fbf-85fe-414c-900c-9704a5dd5cc6
ms.openlocfilehash: 7a557a3d278c2b6d8d083b2ebf8c8129bc498afa
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702761"
---
# <a name="how-to-stretch-a-toolstriptextbox-to-fill-the-remaining-width-of-a-toolstrip-windows-forms"></a><span data-ttu-id="bda55-102">Procédure : Étirer un ToolStripTextBox pour remplir la largeur restante d’un ToolStrip (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="bda55-102">How to: Stretch a ToolStripTextBox to Fill the Remaining Width of a ToolStrip (Windows Forms)</span></span>
<span data-ttu-id="bda55-103">Lorsque vous définissez la <xref:System.Windows.Forms.ToolStrip.Stretch%2A> propriété d’un <xref:System.Windows.Forms.ToolStrip> le contrôle à `true`, le contrôle remplit son conteneur de bout en bout et se redimensionne quand son conteneur est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="bda55-103">When you set the <xref:System.Windows.Forms.ToolStrip.Stretch%2A> property of a <xref:System.Windows.Forms.ToolStrip> control to `true`, the control fills its container from end to end, and resizes when its container resizes.</span></span> <span data-ttu-id="bda55-104">Dans cette configuration, il peut s’avérer utile d’étirer un élément dans le contrôle, comme un <xref:System.Windows.Forms.ToolStripTextBox>, pour remplir l’espace disponible et redimensionner lorsque le contrôle est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="bda55-104">In this configuration, you may find it useful to stretch an item in the control, such as a <xref:System.Windows.Forms.ToolStripTextBox>, to fill the available space and to resize when the control resizes.</span></span> <span data-ttu-id="bda55-105">Cet étirement est utile, par exemple, si vous souhaitez obtenir une apparence et un comportement similaire à la barre d’adresses dans Microsoft® Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bda55-105">This stretching is useful, for example, if you want to achieve appearance and behavior similar to the address bar in Microsoft® Internet Explorer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bda55-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="bda55-106">Example</span></span>  
 <span data-ttu-id="bda55-107">L’exemple de code suivant fournit une classe dérivée de <xref:System.Windows.Forms.ToolStripTextBox> appelée `ToolStripSpringTextBox`.</span><span class="sxs-lookup"><span data-stu-id="bda55-107">The following code example provides a class derived from <xref:System.Windows.Forms.ToolStripTextBox> called `ToolStripSpringTextBox`.</span></span> <span data-ttu-id="bda55-108">Cette classe substitue la <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> méthode pour calculer la largeur disponible du parent <xref:System.Windows.Forms.ToolStrip> contrôler une fois que la largeur combinée de tous les autres éléments a été soustrait.</span><span class="sxs-lookup"><span data-stu-id="bda55-108">This class overrides the <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> method to calculate the available width of the parent <xref:System.Windows.Forms.ToolStrip> control after the combined width of all other items has been subtracted.</span></span> <span data-ttu-id="bda55-109">Cet exemple de code fournit également un <xref:System.Windows.Forms.Form> classe et un `Program` pour illustrer le nouveau comportement.</span><span class="sxs-lookup"><span data-stu-id="bda55-109">This code example also provides a <xref:System.Windows.Forms.Form> class and a `Program` class to demonstrate the new behavior.</span></span>  
  
 [!code-csharp[ToolStripSpringTextBox#00](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripSpringTextBox/cs/ToolStripSpringTextBox.cs#00)]
 [!code-vb[ToolStripSpringTextBox#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripSpringTextBox/vb/ToolStripSpringTextBox.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="bda55-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="bda55-110">Compiling the Code</span></span>  
 <span data-ttu-id="bda55-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="bda55-111">This example requires:</span></span>  
  
-   <span data-ttu-id="bda55-112">Références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="bda55-112">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bda55-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bda55-113">See also</span></span>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.Stretch%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripTextBox>
- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A?displayProperty=nameWithType>
- [<span data-ttu-id="bda55-114">Architecture du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="bda55-114">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="bda55-115">Guide pratique pour Utiliser la propriété Spring dans un StatusStrip de manière interactive</span><span class="sxs-lookup"><span data-stu-id="bda55-115">How to: Use the Spring Property Interactively in a StatusStrip</span></span>](how-to-use-the-spring-property-interactively-in-a-statusstrip.md)
