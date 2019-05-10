---
title: 'Procédure : fournir des éléments de menu standard à un formulaire'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- menu items [Windows Forms], standard
- ToolStrip control [Windows Forms]
ms.assetid: 75db9126-e70c-4e81-921d-b83c0a4a9f50
ms.openlocfilehash: 530e4185b065c9483f112146c496860f2c8a52c1
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662320"
---
# <a name="how-to-provide-standard-menu-items-to-a-form"></a><span data-ttu-id="e5f1a-102">Procédure : fournir des éléments de menu standard à un formulaire</span><span class="sxs-lookup"><span data-stu-id="e5f1a-102">How to: Provide Standard Menu Items to a Form</span></span>
<span data-ttu-id="e5f1a-103">Vous pouvez fournir un menu standard pour vos formulaires avec le contrôle <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="e5f1a-103">You can provide a standard menu for your forms with the <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
 <span data-ttu-id="e5f1a-104">Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e5f1a-104">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="e5f1a-105">Consultez également [procédure pas à pas : En fournissant des éléments de Menu Standard à un formulaire](walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="e5f1a-105">Also see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e5f1a-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5f1a-106">Example</span></span>  
 <span data-ttu-id="e5f1a-107">L'exemple de code suivant montre comment utiliser un contrôle <xref:System.Windows.Forms.MenuStrip> pour créer un formulaire avec un menu standard.</span><span class="sxs-lookup"><span data-stu-id="e5f1a-107">The following code example demonstrates how to use a <xref:System.Windows.Forms.MenuStrip> control to create a form with a standard menu.</span></span> <span data-ttu-id="e5f1a-108">Les sélections d'élément de menu sont affichées dans un contrôle <xref:System.Windows.Forms.StatusStrip>.</span><span class="sxs-lookup"><span data-stu-id="e5f1a-108">Menu item selections are displayed in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e5f1a-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e5f1a-109">Compiling the Code</span></span>  
 <span data-ttu-id="e5f1a-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="e5f1a-110">This example requires:</span></span>  
  
- <span data-ttu-id="e5f1a-111">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="e5f1a-111">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="e5f1a-112">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="e5f1a-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="e5f1a-113">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="e5f1a-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5f1a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5f1a-114">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="e5f1a-115">MenuStrip, contrôle</span><span class="sxs-lookup"><span data-stu-id="e5f1a-115">MenuStrip Control</span></span>](menustrip-control-windows-forms.md)
