---
title: 'Procédure : activer la réorganisation des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], column order
- Windows Forms, columns
- columns [Windows Forms], reordering
- data [Windows Forms], displaying
ms.assetid: d82bd69c-6799-4439-a32c-91139c5901d1
ms.openlocfilehash: 966ffe131d10b97fe9632bb1ff23273b1dabd061
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59194966"
---
# <a name="how-to-enable-column-reordering-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="1a701-102">Procédure : activer la réorganisation des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="1a701-102">How to: Enable Column Reordering in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="1a701-103">Lorsque vous affichez les données affichées dans un formulaire Windows <xref:System.Windows.Forms.DataGridView> contrôle, les utilisateurs souhaitent parfois comparer les valeurs dans des colonnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1a701-103">When viewing data displayed in a Windows Forms <xref:System.Windows.Forms.DataGridView> control, users sometimes want to compare the values in specific columns.</span></span> <span data-ttu-id="1a701-104">Cela peut être gênant si les colonnes sont séparées largement dans le contrôle, en particulier si les utilisateurs doivent faire défiler horizontalement pour voir toutes les colonnes qui que les intéressent.</span><span class="sxs-lookup"><span data-stu-id="1a701-104">This can be inconvenient if the columns are widely separated in the control, especially if users must scroll back and forth horizontally in order to see all the columns they are interested in.</span></span> <span data-ttu-id="1a701-105">Vous pouvez rendre la tâche de la comparaison des valeurs de colonne en activant vos utilisateurs de réorganiser les colonnes.</span><span class="sxs-lookup"><span data-stu-id="1a701-105">You can make the task of comparing column values easier by enabling your users to reorder the columns.</span></span> <span data-ttu-id="1a701-106">Lorsque vous activez la réorganisation des colonnes, les utilisateurs peuvent déplacer une colonne vers une nouvelle position en faisant glisser l’en-tête de colonne avec la souris.</span><span class="sxs-lookup"><span data-stu-id="1a701-106">When you enable column reordering, users can move a column to a new position by dragging the column header with the mouse.</span></span>  
  
 <span data-ttu-id="1a701-107">La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1a701-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="1a701-108">Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="1a701-108">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1a701-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="1a701-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="1a701-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="1a701-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="1a701-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="1a701-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-enable-column-reordering"></a><span data-ttu-id="1a701-112">Pour activer la réorganisation des colonnes</span><span class="sxs-lookup"><span data-stu-id="1a701-112">To enable column reordering</span></span>  
  
-   <span data-ttu-id="1a701-113">Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **activer la réorganisation des colonnes**.</span><span class="sxs-lookup"><span data-stu-id="1a701-113">Click the smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Enable Column Reordering**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a701-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a701-114">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType>
- [<span data-ttu-id="1a701-115">Procédure : figer des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="1a701-115">How to: Freeze Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](freeze-columns-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="1a701-116">Procédure : Créer un projet d’application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1a701-116">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="1a701-117">Procédure : ajouter des contrôles à des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1a701-117">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
