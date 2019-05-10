---
title: 'Procédure : créer une disposition Windows Forms qui répond bien à la localisation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: 74c6a51dd4ed74dbd149a3f54fad07bcd15f7d27
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64623654"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a><span data-ttu-id="7559b-102">Procédure : créer une disposition Windows Forms qui répond bien à la localisation</span><span class="sxs-lookup"><span data-stu-id="7559b-102">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>
<span data-ttu-id="7559b-103">La création de formulaires qui sont prêts à être localisés accélère considérablement le développement pour les marchés internationaux.</span><span class="sxs-lookup"><span data-stu-id="7559b-103">Creating forms that are ready to be localized greatly speeds development for international markets.</span></span> <span data-ttu-id="7559b-104">Vous pouvez utiliser le contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour implémenter des dispositions qui répondent correctement au redimensionnement des contrôles suite aux modifications de leurs valeurs de propriétés <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="7559b-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to implement layouts that respond gracefully as controls resize due to changes in their <xref:System.Windows.Forms.Control.Text%2A> property values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7559b-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="7559b-105">Example</span></span>  
 <span data-ttu-id="7559b-106">Ce formulaire montre comment créer une disposition qui s'ajuste proportionnellement quand vous traduisez les valeurs de chaînes affichées dans d'autres langues.</span><span class="sxs-lookup"><span data-stu-id="7559b-106">This form demonstrates how to create a layout that proportionally adjusts when you translate displayed string values into other languages.</span></span> <span data-ttu-id="7559b-107">Ce processus de traduction est appelé *localisation*.</span><span class="sxs-lookup"><span data-stu-id="7559b-107">This process of translation is called *localization*.</span></span> <span data-ttu-id="7559b-108">Pour plus d’informations, consultez [Localisation](../../../standard/globalization-localization/localization.md).</span><span class="sxs-lookup"><span data-stu-id="7559b-108">For more information, see [Localization](../../../standard/globalization-localization/localization.md).</span></span>  
  
 <span data-ttu-id="7559b-109">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7559b-109">There is extensive support for this task in Visual Studio.</span></span>  <span data-ttu-id="7559b-110">Voir aussi [procédure pas à pas : Création d’une présentation qui ajuste la Proportion pour la localisation](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/7k9fa71y(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="7559b-110">See also [Walkthrough: Creating a Layout That Adjusts Proportion for Localization](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/7k9fa71y(v=vs.100)).</span></span>  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
## <a name="additional-resources"></a><span data-ttu-id="7559b-111">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7559b-111">Additional resources</span></span>
1. [<span data-ttu-id="7559b-112">Guide pratique pour Aligner et étirer un contrôle dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="7559b-112">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2. [<span data-ttu-id="7559b-113">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="7559b-113">Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)  

3. [<span data-ttu-id="7559b-114">Guide pratique pour Étendre des lignes et colonnes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="7559b-114">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4. [<span data-ttu-id="7559b-115">Guide pratique pour Modifier des colonnes et lignes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="7559b-115">How to: Edit Columns and Rows in a TableLayoutPanel Control</span></span>](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5. [<span data-ttu-id="7559b-116">Procédure pas à pas : Effectuer des tâches courantes à l’aide d’intelligent des balises sur Windows Forms contrôles</span><span class="sxs-lookup"><span data-stu-id="7559b-116">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>](performing-common-tasks-using-smart-tags-on-wf-controls.md)  
  
6. [<span data-ttu-id="7559b-117">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="7559b-117">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  

7. [<span data-ttu-id="7559b-118">Procédure pas à pas : Disposition des Windows Forms contrôles avec la propriété AutoSize, des marges et remplissage</span><span class="sxs-lookup"><span data-stu-id="7559b-118">Walkthrough: Laying Out Windows Forms Controls with Padding, Margins, and the AutoSize Property</span></span>](windows-forms-controls-padding-autosize.md)  
  
8. <span data-ttu-id="7559b-119">[Guide pratique pour Prend en charge de la localisation sur les formulaires Windows à l’aide du redimensionnement automatique et le contrôle TableLayoutPanel](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7559b-119">[How to: Support Localization on Windows Forms Using AutoSize and the TableLayoutPanel Control](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100))</span></span>  
  
9. <span data-ttu-id="7559b-120">[Procédure pas à pas : Création d’un formulaire Windows redimensionnable pour l’entrée de données](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7559b-120">[Walkthrough: Creating a Resizable Windows Form for Data Entry](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100))</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7559b-121">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="7559b-121">Compiling the Code</span></span>  
 <span data-ttu-id="7559b-122">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="7559b-122">This example requires:</span></span>  
  
- <span data-ttu-id="7559b-123">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="7559b-123">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="7559b-124">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="7559b-124">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="7559b-125">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="7559b-125">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7559b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7559b-126">See also</span></span>

- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [<span data-ttu-id="7559b-127">Localisation</span><span class="sxs-lookup"><span data-stu-id="7559b-127">Localization</span></span>](../../../standard/globalization-localization/localization.md)
