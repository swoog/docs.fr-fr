---
title: 'Procédure : Gérer le dépassement de capacité de ToolStrip dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], managing overflow
- toolbars [Windows Forms], managing overflow
- examples [Windows Forms], toolbars
- CanOverflow property
ms.assetid: fa10e0ad-4cbf-4c0d-9082-359c2f855d4e
ms.openlocfilehash: 53f610a728925d454a8833a49e705818f027aec5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913755"
---
# <a name="how-to-manage-toolstrip-overflow-in-windows-forms"></a><span data-ttu-id="de0d4-102">Procédure : Gérer le dépassement de capacité de ToolStrip dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="de0d4-102">How to: Manage ToolStrip Overflow in Windows Forms</span></span>

<span data-ttu-id="de0d4-103">Lorsque tous les éléments sur un <xref:System.Windows.Forms.ToolStrip> contrôle ne tiennent pas dans l’espace alloué, vous pouvez activer la fonctionnalité de dépassement de capacité sur le <xref:System.Windows.Forms.ToolStrip> et déterminer le comportement de dépassement de capacité de spécifiques <xref:System.Windows.Forms.ToolStripItem>s.</span><span class="sxs-lookup"><span data-stu-id="de0d4-103">When all the items on a <xref:System.Windows.Forms.ToolStrip> control do not fit in the allotted space, you can enable overflow functionality on the <xref:System.Windows.Forms.ToolStrip> and determine the overflow behavior of specific <xref:System.Windows.Forms.ToolStripItem>s.</span></span>

<span data-ttu-id="de0d4-104">Lorsque vous ajoutez <xref:System.Windows.Forms.ToolStripItem>s qui nécessitent davantage d’espace est alloué à la <xref:System.Windows.Forms.ToolStrip> étant donné la taille du formulaire actuel, un <xref:System.Windows.Forms.ToolStripOverflowButton> apparaît automatiquement sur le <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="de0d4-104">When you add <xref:System.Windows.Forms.ToolStripItem>s that require more space than is allotted to the <xref:System.Windows.Forms.ToolStrip> given the form's current size, a <xref:System.Windows.Forms.ToolStripOverflowButton> automatically appears on the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="de0d4-105">Le <xref:System.Windows.Forms.ToolStripOverflowButton> s’affiche, et prenant en charge le dépassement de capacité des éléments sont déplacés dans le menu de dépassement de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="de0d4-105">The <xref:System.Windows.Forms.ToolStripOverflowButton> appears, and overflow-enabled items are moved into the drop-down overflow menu.</span></span> <span data-ttu-id="de0d4-106">Cela vous permet de personnaliser les hiérarchiser comment votre <xref:System.Windows.Forms.ToolStrip> éléments s’ajustent aux différentes tailles de formulaire.</span><span class="sxs-lookup"><span data-stu-id="de0d4-106">This allows you to customize and prioritize how your <xref:System.Windows.Forms.ToolStrip> items properly adjust to different form sizes.</span></span> <span data-ttu-id="de0d4-107">Vous pouvez également modifier l’apparence de vos éléments lorsqu’elles se trouvent dans le dépassement de capacité à l’aide de la <xref:System.Windows.Forms.ToolStripItem.Placement%2A> et <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> propriétés et le <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> événement.</span><span class="sxs-lookup"><span data-stu-id="de0d4-107">You can also change the appearance of your items when they fall into the overflow by using the <xref:System.Windows.Forms.ToolStripItem.Placement%2A> and <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> properties and the <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> event.</span></span> <span data-ttu-id="de0d4-108">Si vous agrandissez le formulaire au moment du design ou au moment de l’exécution, plus <xref:System.Windows.Forms.ToolStripItem>s peuvent être affichées sur les principaux <xref:System.Windows.Forms.ToolStrip> et <xref:System.Windows.Forms.ToolStripOverflowButton> peut même disparaître jusqu'à ce que vous diminuez la taille du formulaire.</span><span class="sxs-lookup"><span data-stu-id="de0d4-108">If you enlarge the form at either design time or run time, more <xref:System.Windows.Forms.ToolStripItem>s can be displayed on the main <xref:System.Windows.Forms.ToolStrip> and the <xref:System.Windows.Forms.ToolStripOverflowButton> might even disappear until you decrease the size of the form.</span></span>

## <a name="to-enable-overflow-on-a-toolstrip-control"></a><span data-ttu-id="de0d4-109">Pour activer le dépassement de capacité sur un contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="de0d4-109">To enable overflow on a ToolStrip control</span></span>

- <span data-ttu-id="de0d4-110">Vérifiez que le <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> propriété n’est pas définie sur `false` pour le <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="de0d4-110">Ensure that the <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> property is not set to `false` for the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="de0d4-111">La valeur par défaut est `True`.</span><span class="sxs-lookup"><span data-stu-id="de0d4-111">The default is `True`.</span></span>

     <span data-ttu-id="de0d4-112">Lorsque <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> est `True` (la valeur par défaut), un <xref:System.Windows.Forms.ToolStripItem> est envoyé au menu déroulant de dépassement de capacité lorsque le contenu de la <xref:System.Windows.Forms.ToolStripItem> dépasse la largeur d’un horizontal <xref:System.Windows.Forms.ToolStrip> ou la hauteur d’une verticale <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="de0d4-112">When <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> is `True` (the default), a <xref:System.Windows.Forms.ToolStripItem> is sent to the drop-down overflow menu when the content of the <xref:System.Windows.Forms.ToolStripItem> exceeds the width of a horizontal <xref:System.Windows.Forms.ToolStrip> or the height of a vertical <xref:System.Windows.Forms.ToolStrip>.</span></span>

## <a name="to-specify-overflow-behavior-of-a-specific-toolstripitem"></a><span data-ttu-id="de0d4-113">Pour spécifier le comportement de dépassement de capacité d’un ToolStripItem spécifique</span><span class="sxs-lookup"><span data-stu-id="de0d4-113">To specify overflow behavior of a specific ToolStripItem</span></span>

- <span data-ttu-id="de0d4-114">Définir le <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> propriété de la <xref:System.Windows.Forms.ToolStripItem> sur la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="de0d4-114">Set the <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> property of the <xref:System.Windows.Forms.ToolStripItem> to the desired value.</span></span> <span data-ttu-id="de0d4-115">Les possibilités sont `Always`, `Never`, et `AsNeeded`.</span><span class="sxs-lookup"><span data-stu-id="de0d4-115">The possibilities are `Always`, `Never`, and `AsNeeded`.</span></span> <span data-ttu-id="de0d4-116">La valeur par défaut est `AsNeeded`.</span><span class="sxs-lookup"><span data-stu-id="de0d4-116">The default is `AsNeeded`.</span></span>

    ```vb
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never
    ```

    ```csharp
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never;
    ```

## <a name="see-also"></a><span data-ttu-id="de0d4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de0d4-117">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripOverflowButton>
- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [<span data-ttu-id="de0d4-118">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="de0d4-118">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="de0d4-119">Architecture du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="de0d4-119">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="de0d4-120">Résumé de la technologie ToolStrip</span><span class="sxs-lookup"><span data-stu-id="de0d4-120">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
