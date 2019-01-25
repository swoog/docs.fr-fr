---
title: 'Procédure : Déclencher des Notifications de modification à l’aide de la méthode ResetItem de BindingSource'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- change notifications [Windows Forms], raising
- data binding [Windows Forms], change notifications
- BindingSource component [Windows Forms], raising change notifications with
- data sources [Windows Forms], detecting changes
- change notifications
ms.assetid: ab8b4096-37ff-4e30-aabc-de79a2f2e972
ms.openlocfilehash: 50d2203638363831d236a6add7c6f4ba4fbebf4b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644815"
---
# <a name="how-to-raise-change-notifications-using-the-bindingsource-resetitem-method"></a><span data-ttu-id="a0b66-102">Procédure : Déclencher des Notifications de modification à l’aide de la méthode ResetItem de BindingSource</span><span class="sxs-lookup"><span data-stu-id="a0b66-102">How to: Raise Change Notifications Using the BindingSource ResetItem Method</span></span>
<span data-ttu-id="a0b66-103">Certaines sources de données de vos contrôles ne déclenchent pas de notifications de modifications quand des éléments sont modifiés, ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="a0b66-103">Some data sources for your controls do not raise change notifications when items are changed, added, or deleted.</span></span> <span data-ttu-id="a0b66-104">Avec le composant <xref:System.Windows.Forms.BindingSource>, vous pouvez établir une liaison à ces sources de données et déclencher une notification de modification à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="a0b66-104">With the <xref:System.Windows.Forms.BindingSource> component, you can bind to such data sources and raise a change notification from your code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a0b66-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0b66-105">Example</span></span>  
 <span data-ttu-id="a0b66-106">Cet écran montre comment utiliser un composant <xref:System.Windows.Forms.BindingSource> pour lier une liste à un contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="a0b66-106">This form demonstrates using a <xref:System.Windows.Forms.BindingSource> component to bind a list to a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="a0b66-107">La liste ne déclenche pas de notifications de modifications. La méthode <xref:System.Windows.Forms.BindingSource.ResetItem%2A> sur le <xref:System.Windows.Forms.BindingSource> est donc appelée quand un élément de la liste est modifié.</span><span class="sxs-lookup"><span data-stu-id="a0b66-107">The list does not raise change notifications, so the <xref:System.Windows.Forms.BindingSource.ResetItem%2A> method on the <xref:System.Windows.Forms.BindingSource> is called when an item in the list is changed.</span></span> <span data-ttu-id="a0b66-108">.</span><span class="sxs-lookup"><span data-stu-id="a0b66-108">.</span></span>  
  
 [!code-cpp[System.Windows.Forms.DataConnector.ResetItem#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetItem/CPP/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.DataConnector.ResetItem#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetItem/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.ResetItem#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetItem/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a0b66-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="a0b66-109">Compiling the Code</span></span>  
 <span data-ttu-id="a0b66-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="a0b66-110">This example requires:</span></span>  
  
-   <span data-ttu-id="a0b66-111">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="a0b66-111">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="a0b66-112">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="a0b66-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="a0b66-113">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="a0b66-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="a0b66-114">Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="a0b66-114">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0b66-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0b66-115">See also</span></span>
- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="a0b66-116">BindingSource, composant</span><span class="sxs-lookup"><span data-stu-id="a0b66-116">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)
- [<span data-ttu-id="a0b66-117">Guide pratique pour Lier un contrôle de formulaires Windows à un Type</span><span class="sxs-lookup"><span data-stu-id="a0b66-117">How to: Bind a Windows Forms Control to a Type</span></span>](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
