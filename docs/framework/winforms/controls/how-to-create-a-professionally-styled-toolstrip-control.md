---
title: 'Procédure : créer un contrôle ToolStrip de style professionnel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStripRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c208b2f6-8105-474b-9075-d582e1792870
ms.openlocfilehash: 4e4e899d583eb87b3ced7161f1fd274c0bcc591c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65586553"
---
# <a name="how-to-create-a-professionally-styled-toolstrip-control"></a><span data-ttu-id="273ac-102">Procédure : créer un contrôle ToolStrip de style professionnel</span><span class="sxs-lookup"><span data-stu-id="273ac-102">How to: Create a Professionally Styled ToolStrip Control</span></span>
<span data-ttu-id="273ac-103">Vous pouvez donner aux contrôles <xref:System.Windows.Forms.ToolStrip> de votre application une apparence et un comportement professionnels en écrivant votre propre classe dérivée du type <xref:System.Windows.Forms.ToolStripProfessionalRenderer>.</span><span class="sxs-lookup"><span data-stu-id="273ac-103">You can give your application’s <xref:System.Windows.Forms.ToolStrip> controls a professional appearance and behavior (look and feel) by writing your own class derived from the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> type.</span></span>  
  
 <span data-ttu-id="273ac-104">Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="273ac-104">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="273ac-105">Consultez [Procédure pas à pas : Création d’un contrôle ToolStrip de style professionnel](walkthrough-creating-a-professionally-styled-toolstrip-control.md).</span><span class="sxs-lookup"><span data-stu-id="273ac-105">See [Walkthrough: Creating a Professionally Styled ToolStrip Control](walkthrough-creating-a-professionally-styled-toolstrip-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="273ac-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="273ac-106">Example</span></span>  
 <span data-ttu-id="273ac-107">L’exemple de code suivant montre comment utiliser <xref:System.Windows.Forms.ToolStrip> contrôles pour créer un contrôle composite qui reproduit le **volet de Navigation** fourni par Microsoft® Outlook®.</span><span class="sxs-lookup"><span data-stu-id="273ac-107">The following code example demonstrates how to use <xref:System.Windows.Forms.ToolStrip> controls to create a composite control that mimics the **Navigation Pane** provided by Microsoft® Outlook®.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StackView#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StackView#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="273ac-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="273ac-108">Compiling the Code</span></span>  
 <span data-ttu-id="273ac-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="273ac-109">This example requires:</span></span>  
  
- <span data-ttu-id="273ac-110">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="273ac-110">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="273ac-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="273ac-111">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="273ac-112">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="273ac-112">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
- [<span data-ttu-id="273ac-113">Guide pratique pour Fournir des éléments de Menu Standard à un formulaire</span><span class="sxs-lookup"><span data-stu-id="273ac-113">How to: Provide Standard Menu Items to a Form</span></span>](how-to-provide-standard-menu-items-to-a-form.md)
