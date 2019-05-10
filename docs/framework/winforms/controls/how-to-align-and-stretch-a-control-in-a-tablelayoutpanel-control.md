---
title: 'Procédure : aligner et étirer un contrôle dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AlignStretchCtrl
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms], stretching controls
- controls [Windows Forms], stretching
- controls [Windows Forms], aligning
ms.assetid: 7dc1a157-6fee-4995-8ebc-b65bdc0909a8
ms.openlocfilehash: fd32593bcad9e3f3ef93edee8aa2659d423f9feb
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65210362"
---
# <a name="how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control"></a><span data-ttu-id="006c3-102">Procédure : aligner et étirer un contrôle dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="006c3-102">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>

<span data-ttu-id="006c3-103">Vous pouvez aligner et étirer des contrôles dans un <xref:System.Windows.Forms.TableLayoutPanel> avec la <xref:System.Windows.Forms.Control.Anchor%2A> et <xref:System.Windows.Forms.Control.Dock%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="006c3-103">You can align and stretch controls in a <xref:System.Windows.Forms.TableLayoutPanel> with the <xref:System.Windows.Forms.Control.Anchor%2A> and <xref:System.Windows.Forms.Control.Dock%2A> properties.</span></span>

## <a name="align-and-stretch-a-control"></a><span data-ttu-id="006c3-104">Aligner et étirer un contrôle</span><span class="sxs-lookup"><span data-stu-id="006c3-104">Align and stretch a control</span></span>

1. <span data-ttu-id="006c3-105">Dans Visual Studio, faites glisser un <xref:System.Windows.Forms.TableLayoutPanel> contrôle depuis la **boîte à outils** vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="006c3-105">In Visual Studio, drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>

2. <span data-ttu-id="006c3-106">Faites glisser un <xref:System.Windows.Forms.Button> contrôler à partir de la **boîte à outils** dans la cellule supérieure gauche de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="006c3-106">Drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** into the upper-left cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span> <span data-ttu-id="006c3-107">Le <xref:System.Windows.Forms.Button> contrôle est centré dans la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-107">The <xref:System.Windows.Forms.Button> control is centered in the cell.</span></span>

3. <span data-ttu-id="006c3-108">Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Left,Right`.</span><span class="sxs-lookup"><span data-stu-id="006c3-108">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to `Left,Right`.</span></span> <span data-ttu-id="006c3-109">Le <xref:System.Windows.Forms.Button> contrôler s’étire pour correspondre à la largeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-109">The <xref:System.Windows.Forms.Button> control stretches to match the width of the cell.</span></span>

4. <span data-ttu-id="006c3-110">Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Top,Bottom`.</span><span class="sxs-lookup"><span data-stu-id="006c3-110">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to `Top,Bottom`.</span></span> <span data-ttu-id="006c3-111">Le <xref:System.Windows.Forms.Button> contrôler s’étire pour correspondre à la hauteur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-111">The <xref:System.Windows.Forms.Button> control stretches to match the height of the cell.</span></span>

5. <span data-ttu-id="006c3-112">Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="006c3-112">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span> <span data-ttu-id="006c3-113">Le <xref:System.Windows.Forms.Button> contrôle se développe pour remplir la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-113">The <xref:System.Windows.Forms.Button> control expands to fill the cell.</span></span>

6. <span data-ttu-id="006c3-114">Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.None>.</span><span class="sxs-lookup"><span data-stu-id="006c3-114">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.None>.</span></span> <span data-ttu-id="006c3-115">Le <xref:System.Windows.Forms.Button> contrôle retourne à sa taille d’origine et se déplace vers l’angle supérieur gauche de la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-115">The <xref:System.Windows.Forms.Button> control returns to its original size and moves to the upper-left corner of the cell.</span></span> <span data-ttu-id="006c3-116">Le **Windows Forms Designer** a défini le <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Top, Left`.</span><span class="sxs-lookup"><span data-stu-id="006c3-116">The **Windows Forms Designer** has set the <xref:System.Windows.Forms.Control.Anchor%2A> property to `Top, Left`.</span></span>

7. <span data-ttu-id="006c3-117">Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Bottom,Right`.</span><span class="sxs-lookup"><span data-stu-id="006c3-117">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to `Bottom,Right`.</span></span> <span data-ttu-id="006c3-118">Le <xref:System.Windows.Forms.Button> contrôle se déplace vers l’angle inférieur droit de la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-118">The <xref:System.Windows.Forms.Button> control moves to the lower-right corner of the cell.</span></span>

8. <span data-ttu-id="006c3-119">Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété <xref:System.Windows.Forms.AnchorStyles.None>.</span><span class="sxs-lookup"><span data-stu-id="006c3-119">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to <xref:System.Windows.Forms.AnchorStyles.None>.</span></span> <span data-ttu-id="006c3-120">Le <xref:System.Windows.Forms.Button> contrôle se déplace vers le centre de la cellule.</span><span class="sxs-lookup"><span data-stu-id="006c3-120">The <xref:System.Windows.Forms.Button> control moves to the center of the cell.</span></span>

## <a name="see-also"></a><span data-ttu-id="006c3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="006c3-121">See also</span></span>

- [<span data-ttu-id="006c3-122">TableLayoutPanel, contrôle</span><span class="sxs-lookup"><span data-stu-id="006c3-122">TableLayoutPanel Control</span></span>](tablelayoutpanel-control-windows-forms.md)
