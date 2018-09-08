---
title: 'Comment : gérer des erreurs et des exceptions qui se produisent avec Databinding'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- error handling [Windows Forms], examples
- data binding [Windows Forms], examples
- examples [Windows Forms], error handling
- error handling [Windows Forms], data binding
- data binding [Windows Forms], error handling
- BindingSource component [Windows Forms], handling errors and exceptions
ms.assetid: eddc5bad-9513-47df-ab28-f02d8dff7892
ms.openlocfilehash: d0bb41da69bf1cb87f052c11d3a7d1f1783320ad
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44196853"
---
# <a name="how-to-handle-errors-and-exceptions-that-occur-with-databinding"></a><span data-ttu-id="50903-102">Comment : gérer des erreurs et des exceptions qui se produisent avec Databinding</span><span class="sxs-lookup"><span data-stu-id="50903-102">How to: Handle Errors and Exceptions that Occur with Databinding</span></span>
<span data-ttu-id="50903-103">Souvent, les exceptions et les erreurs surviennent quand vous liez des objets métier sous-jacents aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="50903-103">Oftentimes exceptions and errors occur on the underlying business objects when you bind them to controls.</span></span> <span data-ttu-id="50903-104">Vous pouvez intercepter ces erreurs et ces exceptions, puis récupérer ou bien passer des informations d'erreur à l'utilisateur en gérant l'événement <xref:System.Windows.Forms.Binding.BindingComplete> pour un composant <xref:System.Windows.Forms.Binding>, <xref:System.Windows.Forms.BindingSource> ou <xref:System.Windows.Forms.CurrencyManager>.</span><span class="sxs-lookup"><span data-stu-id="50903-104">You can intercept these errors and exceptions and then either recover or pass the error information to the user by handling the <xref:System.Windows.Forms.Binding.BindingComplete> event for a particular <xref:System.Windows.Forms.Binding>, <xref:System.Windows.Forms.BindingSource>, or <xref:System.Windows.Forms.CurrencyManager> component.</span></span>  
  
## <a name="example"></a><span data-ttu-id="50903-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="50903-105">Example</span></span>  
 <span data-ttu-id="50903-106">Cet exemple de code montre comment gérer les erreurs et les exceptions qui se produisent pendant une opération de liaison de données.</span><span class="sxs-lookup"><span data-stu-id="50903-106">This code example demonstrates how to handle errors and exceptions that occur during a data-binding operation.</span></span> <span data-ttu-id="50903-107">Il montre comment intercepter des erreurs en gérant l'événement <xref:System.Windows.Forms.Binding.BindingComplete?displayProperty=nameWithType> des objets <xref:System.Windows.Forms.Binding>.</span><span class="sxs-lookup"><span data-stu-id="50903-107">It demonstrates how to intercept errors by handling the <xref:System.Windows.Forms.Binding.BindingComplete?displayProperty=nameWithType> event of the <xref:System.Windows.Forms.Binding> objects.</span></span> <span data-ttu-id="50903-108">Pour intercepter les erreurs et les exceptions en gérant cet événement, vous devez activer la mise en forme de la liaison.</span><span class="sxs-lookup"><span data-stu-id="50903-108">In order to intercept errors and exceptions by handling this event, you must enable formatting for the binding.</span></span> <span data-ttu-id="50903-109">Vous pouvez activer la mise en forme quand la liaison est construite ou ajoutée à la collection de liaison, ou bien en définissant la propriété <xref:System.Windows.Forms.Binding.FormattingEnabled%2A> sur `true`.</span><span class="sxs-lookup"><span data-stu-id="50903-109">You can enable formatting when the binding is constructed or added to the binding collection, or by setting the <xref:System.Windows.Forms.Binding.FormattingEnabled%2A> property to `true`.</span></span>  
  
 [!code-cpp[System.Windows.Forms.DataConnectorBindingComplete#3](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorBindingComplete/CPP/form1.cpp#3)]
 [!code-csharp[System.Windows.Forms.DataConnectorBindingComplete#3](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorBindingComplete/CS/form1.cs#3)]
 [!code-vb[System.Windows.Forms.DataConnectorBindingComplete#3](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorBindingComplete/VB/form1.vb#3)]  
  
 <span data-ttu-id="50903-110">Quand le code s'exécute et qu'une chaîne vide est entrée pour le nom du composant ou qu'une valeur inférieure à 100 est entrée pour le numéro du composant, un message s'affiche.</span><span class="sxs-lookup"><span data-stu-id="50903-110">When the code is running and an empty string is entered for the part name or a value less than 100 is entered for the part number, a message box appears.</span></span> <span data-ttu-id="50903-111">Ceci est la conséquence de la gestion de l'événement <xref:System.Windows.Forms.Binding.BindingComplete?displayProperty=nameWithType> pour ces liaisons de zone de texte.</span><span class="sxs-lookup"><span data-stu-id="50903-111">This is a result of handling the <xref:System.Windows.Forms.Binding.BindingComplete?displayProperty=nameWithType> event for these textbox bindings.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="50903-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="50903-112">Compiling the Code</span></span>  
 <span data-ttu-id="50903-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="50903-113">This example requires:</span></span>  
  
-   <span data-ttu-id="50903-114">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="50903-114">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="50903-115">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="50903-115">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="50903-116">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="50903-116">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="50903-117">Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="50903-117">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50903-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50903-118">See Also</span></span>  
 <xref:System.Windows.Forms.Binding.BindingComplete?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.BindingSource.BindingComplete?displayProperty=nameWithType>  
 [<span data-ttu-id="50903-119">BindingSource, composant</span><span class="sxs-lookup"><span data-stu-id="50903-119">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)
