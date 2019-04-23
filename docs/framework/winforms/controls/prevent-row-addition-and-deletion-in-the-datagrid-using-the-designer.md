---
title: 'Procédure : empêcher l’ajout et la suppression de lignes dans le contrôle DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], preventing row addition or deletion
ms.assetid: a17722bd-9400-41e6-8dcc-c9c151f0a749
ms.openlocfilehash: 9f78068597edb616017876c9c72b01d44111f6f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59220550"
---
# <a name="how-to-prevent-row-addition-and-deletion-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="bfbf2-102">Procédure : empêcher l’ajout et la suppression de lignes dans le contrôle DataGridView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="bfbf2-102">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="bfbf2-103">Vous pouvez vouloir empêcher les utilisateurs d'ajouter de nouvelles lignes de données à votre contrôle <xref:System.Windows.Forms.DataGridView> ou d'en supprimer des lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-103">Sometimes you will want to prevent users from entering new rows of data or deleting existing rows in your <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="bfbf2-104">Nouvelles lignes sont insérées dans la ligne spéciale pour les nouveaux enregistrements en bas du contrôle.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-104">New rows are entered in the special row for new records at the bottom of the control.</span></span> <span data-ttu-id="bfbf2-105">Lorsque vous désactivez Ajout de ligne, la ligne pour les nouveaux enregistrements n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-105">When you disable row addition, the row for new records is not displayed.</span></span> <span data-ttu-id="bfbf2-106">Vous pouvez ensuite rendre le contrôle entièrement en lecture seule en désactivant la suppression des lignes et la modification de cellule.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-106">You can then make the control entirely read-only by disabling row deletion and cell editing.</span></span>  
  
 <span data-ttu-id="bfbf2-107">La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="bfbf2-108">Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="bfbf2-108">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bfbf2-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="bfbf2-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="bfbf2-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="bfbf2-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="bfbf2-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-prevent-row-addition-and-deletion"></a><span data-ttu-id="bfbf2-112">Pour empêcher la suppression et ajout de ligne</span><span class="sxs-lookup"><span data-stu-id="bfbf2-112">To prevent row addition and deletion</span></span>  
  
-   <span data-ttu-id="bfbf2-113">Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler et désactivez le **activer l’ajout** et **activer la suppression** cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-113">Click the smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then clear the **Enable Adding** and **Enable Deleting** check boxes.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="bfbf2-114">Pour rendre le contrôle entièrement en lecture seule, désactivez le **activer la modification** aussi la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="bfbf2-114">To make the control entirely read-only, clear the **Enable Editing** check box as well.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfbf2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfbf2-115">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A?displayProperty=nameWithType>
- [<span data-ttu-id="bfbf2-116">Guide pratique pour Créer un projet Application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="bfbf2-116">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="bfbf2-117">Guide pratique pour Ajouter des contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="bfbf2-117">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
