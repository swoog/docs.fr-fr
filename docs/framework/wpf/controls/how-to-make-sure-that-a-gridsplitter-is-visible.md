---
title: 'Procédure : Vérifier qu’un GridSplitter est visible'
ms.date: 03/30/2017
helpviewer_keywords:
- GridSplitter control [WPF], ensuring visibility of
ms.assetid: 0a62a964-89c8-48f0-9023-5df721a8cf47
ms.openlocfilehash: b7543d14ba39d854b5a2c3f4d0d19b9a457ea89b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770849"
---
# <a name="how-to-make-sure-that-a-gridsplitter-is-visible"></a><span data-ttu-id="2ef19-102">Procédure : Vérifier qu’un GridSplitter est visible</span><span class="sxs-lookup"><span data-stu-id="2ef19-102">How to: Make Sure That a GridSplitter Is Visible</span></span>
<span data-ttu-id="2ef19-103">Cet exemple montre comment vérifier une <xref:System.Windows.Controls.GridSplitter> contrôle n’est pas masqué par les autres contrôles dans un <xref:System.Windows.Controls.Grid>.</span><span class="sxs-lookup"><span data-stu-id="2ef19-103">This example shows how to make sure a <xref:System.Windows.Controls.GridSplitter> control is not hidden by the other controls in a <xref:System.Windows.Controls.Grid>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ef19-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2ef19-104">Example</span></span>  
 <span data-ttu-id="2ef19-105">Le <xref:System.Windows.Controls.Panel.Children%2A> d’un <xref:System.Windows.Controls.Grid> contrôle sont rendus dans l’ordre qu’ils sont définis dans le balisage ou de code.</span><span class="sxs-lookup"><span data-stu-id="2ef19-105">The <xref:System.Windows.Controls.Panel.Children%2A> of a <xref:System.Windows.Controls.Grid> control are rendered in the order that they are defined in markup or code.</span></span> <span data-ttu-id="2ef19-106"><xref:System.Windows.Controls.GridSplitter> les contrôles peuvent être masqués par d’autres contrôles si vous ne définissez pas comme les derniers éléments dans le <xref:System.Windows.Controls.Panel.Children%2A> collection, ou si vous donnez des autres contrôles un degré plus élevé <xref:System.Windows.Controls.Panel.ZIndexProperty>.</span><span class="sxs-lookup"><span data-stu-id="2ef19-106"><xref:System.Windows.Controls.GridSplitter> controls can be hidden by other controls if you do not define them as the last elements in the <xref:System.Windows.Controls.Panel.Children%2A> collection or if you give other controls a higher <xref:System.Windows.Controls.Panel.ZIndexProperty>.</span></span>  
  
 <span data-ttu-id="2ef19-107">Pour empêcher masqué <xref:System.Windows.Controls.GridSplitter> contrôles, effectuez l’une des opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ef19-107">To prevent hidden <xref:System.Windows.Controls.GridSplitter> controls, do one of the following.</span></span>  
  
- <span data-ttu-id="2ef19-108">Assurez-vous que l’option <xref:System.Windows.Controls.GridSplitter> contrôles sont les dernières <xref:System.Windows.Controls.Panel.Children%2A> ajouté à la <xref:System.Windows.Controls.Grid>.</span><span class="sxs-lookup"><span data-stu-id="2ef19-108">Make sure that <xref:System.Windows.Controls.GridSplitter> controls are the last <xref:System.Windows.Controls.Panel.Children%2A> added to the <xref:System.Windows.Controls.Grid>.</span></span> <span data-ttu-id="2ef19-109">L’exemple suivant montre le <xref:System.Windows.Controls.GridSplitter> en tant que le dernier élément dans le <xref:System.Windows.Controls.Panel.Children%2A> collection de la <xref:System.Windows.Controls.Grid>.</span><span class="sxs-lookup"><span data-stu-id="2ef19-109">The following example shows the <xref:System.Windows.Controls.GridSplitter> as the last element in the <xref:System.Windows.Controls.Panel.Children%2A> collection of the <xref:System.Windows.Controls.Grid>.</span></span>  
  
 [!code-xaml[GridSplitterSnips#GridSplitterLastChild](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterlastchild)]  
  
- <span data-ttu-id="2ef19-110">Définir le <xref:System.Windows.Controls.Panel.ZIndexProperty> sur la <xref:System.Windows.Controls.GridSplitter> supérieure à un contrôle qui masquez-le dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2ef19-110">Set the <xref:System.Windows.Controls.Panel.ZIndexProperty> on the <xref:System.Windows.Controls.GridSplitter> to be higher than a control that would otherwise hide it.</span></span> <span data-ttu-id="2ef19-111">L’exemple suivant donne le <xref:System.Windows.Controls.GridSplitter> contrôler un degré plus élevé <xref:System.Windows.Controls.Panel.ZIndexProperty> que le <xref:System.Windows.Controls.Button> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2ef19-111">The following example gives the <xref:System.Windows.Controls.GridSplitter> control a higher <xref:System.Windows.Controls.Panel.ZIndexProperty> than the <xref:System.Windows.Controls.Button> control.</span></span>  
  
 [!code-xaml[GridSplitterSnips#GridSplitterZIndex](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterzindex)]  
  
- <span data-ttu-id="2ef19-112">Définissez des marges sur le contrôle qui, sinon, masquerait le <xref:System.Windows.Controls.GridSplitter> afin que le <xref:System.Windows.Controls.GridSplitter> est exposé.</span><span class="sxs-lookup"><span data-stu-id="2ef19-112">Set margins on the control that would otherwise hide the <xref:System.Windows.Controls.GridSplitter> so that the <xref:System.Windows.Controls.GridSplitter> is exposed.</span></span> <span data-ttu-id="2ef19-113">L’exemple suivant définit les marges sur un contrôle qui, sinon, chevaucherait et masquer le <xref:System.Windows.Controls.GridSplitter>.</span><span class="sxs-lookup"><span data-stu-id="2ef19-113">The following example sets margins on a control that would otherwise overlay and hide the <xref:System.Windows.Controls.GridSplitter>.</span></span>  
  
 [!code-xaml[GridSplitterSnips#GridSplitterMargin](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplittermargin)]  
  
## <a name="see-also"></a><span data-ttu-id="2ef19-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ef19-114">See also</span></span>

- <xref:System.Windows.Controls.GridSplitter>
- [<span data-ttu-id="2ef19-115">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="2ef19-115">How-to Topics</span></span>](gridsplitter-how-to-topics.md)
