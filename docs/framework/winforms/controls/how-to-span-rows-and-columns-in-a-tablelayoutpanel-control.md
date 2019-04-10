---
title: 'Procédure : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.SpanRowsColumns
helpviewer_keywords:
- columns [Windows Forms], spanning
- merging cells
- TableLayoutPanel control [Windows Forms], spanning rows and columns
- rows [Windows Forms], spanning
- cells [Windows Forms], merging
ms.assetid: a8a2fdd3-a848-48b0-a4cd-4e85ebded87e
ms.openlocfilehash: 02db78b07930676235e55e535fb24f6ff618d823
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59339019"
---
# <a name="how-to-span-rows-and-columns-in-a-tablelayoutpanel-control"></a><span data-ttu-id="3f6b0-102">Procédure : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="3f6b0-102">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>
<span data-ttu-id="3f6b0-103">Contrôles dans un <xref:System.Windows.Forms.TableLayoutPanel> contrôle peut s’étendre sur les lignes et colonnes adjacentes.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-103">Controls in a <xref:System.Windows.Forms.TableLayoutPanel> control can span adjacent rows and columns.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f6b0-104">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="3f6b0-105">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="3f6b0-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="3f6b0-106">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="3f6b0-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-span-columns-and-rows"></a><span data-ttu-id="3f6b0-107">Pour couvrir des colonnes et lignes</span><span class="sxs-lookup"><span data-stu-id="3f6b0-107">To span columns and rows</span></span>  
  
1. <span data-ttu-id="3f6b0-108">Faites glisser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> de la **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-108">Drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>  
  
2. <span data-ttu-id="3f6b0-109">Faites glisser un <xref:System.Windows.Forms.Button> contrôler à partir de la **boîte à outils** dans la cellule supérieure gauche de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-109">Drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** into the upper-left cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>  
  
3. <span data-ttu-id="3f6b0-110">Définir le <xref:System.Windows.Forms.Button> du contrôle **ColumnSpan** propriété **2**.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-110">Set the <xref:System.Windows.Forms.Button> control's **ColumnSpan** property to **2**.</span></span> <span data-ttu-id="3f6b0-111">Notez que le <xref:System.Windows.Forms.Button> contrôle s’étend sur les première et deuxième colonnes.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-111">Note that the <xref:System.Windows.Forms.Button> control spans the first and second columns.</span></span>  
  
4. <span data-ttu-id="3f6b0-112">Définir le <xref:System.Windows.Forms.Button> du contrôle **RowSpan** propriété **2**.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-112">Set the <xref:System.Windows.Forms.Button> control's **RowSpan** property to **2**.</span></span> <span data-ttu-id="3f6b0-113">Notez que le <xref:System.Windows.Forms.Button> contrôle s’étend sur les première et deuxième lignes.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-113">Note that the <xref:System.Windows.Forms.Button> control spans the first and second rows.</span></span>  
  
5. <span data-ttu-id="3f6b0-114">Définir le <xref:System.Windows.Forms.Button> du contrôle **ColumnSpan** propriété **1**.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-114">Set the <xref:System.Windows.Forms.Button> control's **ColumnSpan** property to **1**.</span></span> <span data-ttu-id="3f6b0-115">Notez que le <xref:System.Windows.Forms.Button> contrôle se déplace dans la première colonne et couvre les première et deuxième lignes.</span><span class="sxs-lookup"><span data-stu-id="3f6b0-115">Note that the <xref:System.Windows.Forms.Button> control moves into the first column and spans the first and second rows.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f6b0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f6b0-116">See also</span></span>

- [<span data-ttu-id="3f6b0-117">TableLayoutPanel, contrôle</span><span class="sxs-lookup"><span data-stu-id="3f6b0-117">TableLayoutPanel Control</span></span>](tablelayoutpanel-control-windows-forms.md)
