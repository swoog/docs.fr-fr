---
title: 'Procédure : lier des contrôles Windows Forms à des valeurs de base de données DBNull'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BindingSource component [Windows Forms], binding to DBNull values
- examples [Windows Forms], BindingSource component
- controls [Windows Forms], binding to DBNull values
ms.assetid: 96494e6f-5f40-4f83-af97-bbd7192c2af8
ms.openlocfilehash: cc3dde0db3dad6faff548951ff06a39d23248d53
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137759"
---
# <a name="how-to-bind-windows-forms-controls-to-dbnull-database-values"></a><span data-ttu-id="be4c7-102">Procédure : lier des contrôles Windows Forms à des valeurs de base de données DBNull</span><span class="sxs-lookup"><span data-stu-id="be4c7-102">How to: Bind Windows Forms Controls to DBNull Database Values</span></span>
<span data-ttu-id="be4c7-103">Quand vous liez des contrôles Windows Forms à une source de données et que celle-ci retourne une valeur <xref:System.DBNull>, vous pouvez substituer une valeur appropriée sans gérer, mettre en forme ou analyser des événements.</span><span class="sxs-lookup"><span data-stu-id="be4c7-103">When you bind Windows Forms controls to a data source and the data source returns a <xref:System.DBNull> value, you can substitute an appropriate value without handling, formatting, or parsing events.</span></span> <span data-ttu-id="be4c7-104">La propriété <xref:System.Windows.Forms.Binding.NullValue%2A> convertira <xref:System.DBNull> en un objet spécifié lors de la mise en forme ou de l'analyse des valeurs de la source de données.</span><span class="sxs-lookup"><span data-stu-id="be4c7-104">The <xref:System.Windows.Forms.Binding.NullValue%2A> property will convert <xref:System.DBNull> to a specified object when formatting or parsing the data source values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="be4c7-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="be4c7-105">Example</span></span>  
 <span data-ttu-id="be4c7-106">Les exemples suivants montrent comment lier une valeur <xref:System.DBNull> dans deux situations différentes.</span><span class="sxs-lookup"><span data-stu-id="be4c7-106">The following example demonstrates how to bind a <xref:System.DBNull> value in two different situations.</span></span> <span data-ttu-id="be4c7-107">Le premier montre comment définir <xref:System.Windows.Forms.Binding.NullValue%2A> pour une propriété de chaîne ; le second montre comment définir <xref:System.Windows.Forms.Binding.NullValue%2A> pour une propriété d'image.</span><span class="sxs-lookup"><span data-stu-id="be4c7-107">The first demonstrates how to set the <xref:System.Windows.Forms.Binding.NullValue%2A> for a string property; the second demonstrates how to set the <xref:System.Windows.Forms.Binding.NullValue%2A> for an image property.</span></span>  
  
 [!code-csharp[System.Windows.Forms.BindingDBNull#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingDBNull/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingDBNull#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingDBNull/VB/form1.vb#1)]  
  
 <span data-ttu-id="be4c7-108">Les types de la propriété liée et de la propriété <xref:System.Windows.Forms.Binding.NullValue%2A> doivent être identiques, sinon une erreur se produit et aucune autre valeur <xref:System.Windows.Forms.Binding.NullValue%2A> n'est traitée.</span><span class="sxs-lookup"><span data-stu-id="be4c7-108">The types of the bound property and the <xref:System.Windows.Forms.Binding.NullValue%2A> property must be the same or an error will result, and no further <xref:System.Windows.Forms.Binding.NullValue%2A> values will be processed.</span></span> <span data-ttu-id="be4c7-109">Dans cette situation, aucune exception n'est levée.</span><span class="sxs-lookup"><span data-stu-id="be4c7-109">In this situation, an exception will not be thrown.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="be4c7-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="be4c7-110">Compiling the Code</span></span>  
 <span data-ttu-id="be4c7-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="be4c7-111">This example requires:</span></span>  
  
-   <span data-ttu-id="be4c7-112">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="be4c7-112">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="be4c7-113">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="be4c7-113">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="be4c7-114">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="be4c7-114">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be4c7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4c7-115">See also</span></span>

- [<span data-ttu-id="be4c7-116">Composant BindingSource</span><span class="sxs-lookup"><span data-stu-id="be4c7-116">BindingSource Component</span></span>](bindingsource-component.md)
- [<span data-ttu-id="be4c7-117">Procédure : gérer les erreurs et les exceptions qui se produisent avec Databinding</span><span class="sxs-lookup"><span data-stu-id="be4c7-117">How to: Handle Errors and Exceptions that Occur with Databinding</span></span>](how-to-handle-errors-and-exceptions-that-occur-with-databinding.md)
- [<span data-ttu-id="be4c7-118">Procédure : lier un contrôle Windows Forms à un type</span><span class="sxs-lookup"><span data-stu-id="be4c7-118">How to: Bind a Windows Forms Control to a Type</span></span>](how-to-bind-a-windows-forms-control-to-a-type.md)
