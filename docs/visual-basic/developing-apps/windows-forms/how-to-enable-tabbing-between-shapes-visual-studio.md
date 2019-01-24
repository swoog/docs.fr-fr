---
title: 'Procédure : Activer la tabulation entre les formes (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Line control [Visual Basic], implementing tabbing
- Shape control [Visual Basic], implementing tabbing
ms.assetid: 09731b34-3900-4fcb-a9df-ce5280328433
ms.openlocfilehash: c47d94317008af57907b747e53bd13ae7ca229f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498279"
---
# <a name="how-to-enable-tabbing-between-shapes-visual-studio"></a><span data-ttu-id="157c2-102">Procédure : Activer la tabulation entre les formes (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="157c2-102">How to: Enable Tabbing Between Shapes (Visual Studio)</span></span>
<span data-ttu-id="157c2-103">Contrôles Line et shape n’ont pas `TabStop` ou `TabIndex` propriétés, mais vous pouvez toujours activer la tabulation entre eux.</span><span class="sxs-lookup"><span data-stu-id="157c2-103">Line and shape controls do not have `TabStop` or `TabIndex` properties, but you can still enable tabbing among them.</span></span> <span data-ttu-id="157c2-104">Dans l’exemple suivant, en appuyant sur la touche CTRL et les touches TAB sera onglet entre les formes. uniquement la touche TAB sera onglet entre les boutons.</span><span class="sxs-lookup"><span data-stu-id="157c2-104">In the following example, pressing both the CTRL and the TAB keys will tab between shapes; pressing only the TAB key will tab between the buttons.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="157c2-105">Il est possible que pour certains des éléments de l’interface utilisateur de Visual Studio, votre ordinateur affiche des noms ou des emplacements différents de ceux indiqués dans les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="157c2-105">Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions.</span></span> <span data-ttu-id="157c2-106">L’édition de Visual Studio dont vous disposez et les paramètres que vous utilisez déterminent ces éléments.</span><span class="sxs-lookup"><span data-stu-id="157c2-106">The Visual Studio edition that you have and the settings that you use determine these elements.</span></span> <span data-ttu-id="157c2-107">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="157c2-107">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="to-enable-tabbing-among-shapes"></a><span data-ttu-id="157c2-108">Pour activer la tabulation entre les formes</span><span class="sxs-lookup"><span data-stu-id="157c2-108">To enable tabbing among shapes</span></span>  
  
1.  <span data-ttu-id="157c2-109">Faites glisser trois <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> contrôles et deux <xref:System.Windows.Forms.Button> des contrôles de la **boîte à outils** à un formulaire.</span><span class="sxs-lookup"><span data-stu-id="157c2-109">Drag three <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> controls and two <xref:System.Windows.Forms.Button> controls from the **Toolbox** to a form.</span></span>  
  
2.  <span data-ttu-id="157c2-110">Dans le **éditeur de Code**, ajoutez un `Imports` ou `using` instruction en haut du module :</span><span class="sxs-lookup"><span data-stu-id="157c2-110">In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:</span></span>  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  

3.  <span data-ttu-id="157c2-111">Dans une procédure événementielle, ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="157c2-111">Add the following code in an event procedure:</span></span>  
  
[!code-csharp[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_1.cs)]
[!code-vb[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_1.vb)]  
  
4.  <span data-ttu-id="157c2-112">Ajoutez le code suivant dans le `Button1_PreviewKeyDown` procédure événementielle :</span><span class="sxs-lookup"><span data-stu-id="157c2-112">Add the following code in the `Button1_PreviewKeyDown` event procedure:</span></span>  
  
[!code-csharp[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_2.cs)]
[!code-vb[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="157c2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="157c2-113">See also</span></span>
- [<span data-ttu-id="157c2-114">Guide pratique pour Dessiner des formes avec les contrôles OvalShape et RectangleShape</span><span class="sxs-lookup"><span data-stu-id="157c2-114">How to: Draw Shapes with the OvalShape and RectangleShape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
- [<span data-ttu-id="157c2-115">Guide pratique pour Dessiner des lignes avec le contrôle LineShape</span><span class="sxs-lookup"><span data-stu-id="157c2-115">How to: Draw Lines with the LineShape Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
- [<span data-ttu-id="157c2-116">Introduction aux contrôles Line et Shape</span><span class="sxs-lookup"><span data-stu-id="157c2-116">Introduction to the Line and Shape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
