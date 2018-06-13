---
title: 'Comment : imprimer un Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, printing
- printing [Windows Forms]
- printing a form
- printing [Windows Forms], printing a form
ms.assetid: c8dff5f8-f56a-4c07-ae31-64643b31f8fc
ms.openlocfilehash: 42940654a0754ac3616ca7983af07d20607f480f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33522267"
---
# <a name="how-to-print-a-windows-form"></a><span data-ttu-id="1cde2-102">Comment : imprimer un Windows Form</span><span class="sxs-lookup"><span data-stu-id="1cde2-102">How to: Print a Windows Form</span></span>
<span data-ttu-id="1cde2-103">Dans le cadre du processus de développement, vous généralement souhaiterez imprimer une copie de votre Windows Form.</span><span class="sxs-lookup"><span data-stu-id="1cde2-103">As part of the development process, you typically will want to print a copy of your Windows Form.</span></span> <span data-ttu-id="1cde2-104">L’exemple de code suivant montre comment imprimer une copie de l’écran actuel à l’aide de la <xref:System.Drawing.Graphics.CopyFromScreen%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="1cde2-104">The following code example shows how to print a copy of the current form by using the <xref:System.Drawing.Graphics.CopyFromScreen%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1cde2-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="1cde2-105">Example</span></span>  
 [!code-csharp[System.Drawing.Graphics.CopyFromScreen#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Graphics.CopyFromScreen/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Graphics.CopyFromScreen#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Graphics.CopyFromScreen/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1cde2-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="1cde2-106">Compiling the Code</span></span>  
 <span data-ttu-id="1cde2-107">Il s’agit d’un exemple de code complet qui contient un `Main` (méthode).</span><span class="sxs-lookup"><span data-stu-id="1cde2-107">This is a complete code example that contains a `Main` method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="1cde2-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="1cde2-108">Robust Programming</span></span>  
 <span data-ttu-id="1cde2-109">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="1cde2-109">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="1cde2-110">Vous n’avez pas l’autorisation d’accéder à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1cde2-110">You do not have permission to access the printer.</span></span>  
  
-   <span data-ttu-id="1cde2-111">Aucune imprimante n’est installée.</span><span class="sxs-lookup"><span data-stu-id="1cde2-111">There is no printer installed.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="1cde2-112">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="1cde2-112">.NET Framework Security</span></span>  
 <span data-ttu-id="1cde2-113">Pour exécuter cet exemple de code, vous devez disposer d’autorisation d’accéder à l’imprimante que vous utilisez avec votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1cde2-113">In order to run this code example, you must have permission to access the printer you use with your computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cde2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cde2-114">See Also</span></span>  
 <xref:System.Drawing.Printing.PrintDocument>  
 [<span data-ttu-id="1cde2-115">Guide pratique pour rendre des images avec GDI+</span><span class="sxs-lookup"><span data-stu-id="1cde2-115">How to: Render Images with GDI+</span></span>](../../../../docs/framework/winforms/advanced/how-to-render-images-with-gdi.md)  
 [<span data-ttu-id="1cde2-116">Comment : imprimer des graphiques dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1cde2-116">How to: Print Graphics in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-print-graphics-in-windows-forms.md)
