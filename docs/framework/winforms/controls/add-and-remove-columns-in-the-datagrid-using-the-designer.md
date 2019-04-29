---
title: 'Procédure : ajouter et supprimer des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
f1_keywords:
- vs.DataGridViewAddColumnDialog
helpviewer_keywords:
- DataGridView control [Windows Forms], adding columns
- DataGridView control [Windows Forms], removing columns
ms.assetid: 9e709f35-0a8c-4e7e-b4c4-bacb7a834077
ms.openlocfilehash: 80ede9b7bc5bf667e03dc0a745fbc0b5f6c2663a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61640479"
---
# <a name="how-to-add-and-remove-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="703e1-102">Procédure : ajouter et supprimer des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="703e1-102">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="703e1-103">Les formulaires Windows <xref:System.Windows.Forms.DataGridView> contrôle doit contenir des colonnes pour afficher des données.</span><span class="sxs-lookup"><span data-stu-id="703e1-103">The Windows Forms <xref:System.Windows.Forms.DataGridView> control must contain columns in order to display data.</span></span> <span data-ttu-id="703e1-104">Si vous envisagez de remplir le contrôle manuellement, vous devez ajouter les colonnes vous-même.</span><span class="sxs-lookup"><span data-stu-id="703e1-104">If you plan to populate the control manually, you must add the columns yourself.</span></span> <span data-ttu-id="703e1-105">Alternativement, vous pouvez lier le contrôle à une source de données, ce qui génère et remplit automatiquement les colonnes.</span><span class="sxs-lookup"><span data-stu-id="703e1-105">Alternately, you can bind the control to a data source, which generates and populates the columns automatically.</span></span> <span data-ttu-id="703e1-106">Si la source de données contient plus de colonnes que vous souhaitez afficher, vous pouvez supprimer les colonnes indésirables.</span><span class="sxs-lookup"><span data-stu-id="703e1-106">If the data source contains more columns than you want to display, you can remove the unwanted columns.</span></span>  
  
 <span data-ttu-id="703e1-107">Les procédures suivantes nécessitent un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="703e1-107">The following procedures require a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="703e1-108">Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="703e1-108">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="703e1-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="703e1-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="703e1-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="703e1-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="703e1-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="703e1-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-add-a-column-using-the-designer"></a><span data-ttu-id="703e1-112">Pour ajouter une colonne à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="703e1-112">To add a column using the designer</span></span>  
  
1. <span data-ttu-id="703e1-113">Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **ajouter une colonne**.</span><span class="sxs-lookup"><span data-stu-id="703e1-113">Click the smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Add Column**.</span></span>  
  
2. <span data-ttu-id="703e1-114">Dans le **ajouter une colonne** boîte de dialogue, sélectionnez le **colonne liée aux données** option et sélectionnez une colonne dans la source de données ou choisissez le **colonne indépendante** option et définissez la colonne à l’aide des champs fournis.</span><span class="sxs-lookup"><span data-stu-id="703e1-114">In the **Add Column** dialog box, choose the **Databound Column** option and select a column from the data source, or choose the **Unbound Column** option and define the column using the fields provided.</span></span>  
  
3. <span data-ttu-id="703e1-115">Cliquez sur le **ajouter** pour ajouter la colonne, qui n’apparaissent dans le concepteur, si les colonnes existantes ne remplissent pas déjà de la zone d’affichage de contrôle.</span><span class="sxs-lookup"><span data-stu-id="703e1-115">Click the **Add** button to add the column, causing it to appear in the designer if the existing columns do not already fill the control display area.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="703e1-116">Vous pouvez modifier les propriétés des colonnes dans le **modifier les colonnes** boîte de dialogue, vous pouvez accéder à partir de la balise active du contrôle.</span><span class="sxs-lookup"><span data-stu-id="703e1-116">You can modify column properties in the **Edit Columns** dialog box, which you can access from the control's smart tag.</span></span>  
  
### <a name="to-remove-a-column-using-the-designer"></a><span data-ttu-id="703e1-117">Pour supprimer une colonne à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="703e1-117">To remove a column using the designer</span></span>  
  
1. <span data-ttu-id="703e1-118">Choisissez **modifier les colonnes** à partir de la balise active du contrôle.</span><span class="sxs-lookup"><span data-stu-id="703e1-118">Choose **Edit Columns** from the control's smart tag.</span></span>  
  
2. <span data-ttu-id="703e1-119">Sélectionnez une colonne dans la **colonnes sélectionnées** liste.</span><span class="sxs-lookup"><span data-stu-id="703e1-119">Select a column from the **Selected Columns** list.</span></span>  
  
3. <span data-ttu-id="703e1-120">Cliquez sur le **supprimer** bouton pour supprimer la colonne, qui n’apparaît plus dans le concepteur.</span><span class="sxs-lookup"><span data-stu-id="703e1-120">Click the **Remove** button to delete the column, causing it to disappear from the designer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="703e1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="703e1-121">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- [<span data-ttu-id="703e1-122">Guide pratique pour Créer un projet Application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="703e1-122">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="703e1-123">Guide pratique pour Ajouter des contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="703e1-123">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
