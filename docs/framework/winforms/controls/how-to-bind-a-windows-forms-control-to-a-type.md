---
title: 'Procédure : lier un contrôle Windows Forms à un type'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], binding to a type
- BindingSource component [Windows Forms], binding to a type
- types [Windows Forms], binding controls to
ms.assetid: 94faeebb-d2bc-45d6-86d7-96a42661b43d
ms.openlocfilehash: 93cf9844a1c5b9d6eb052c94c2309cbff1f4ad56
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64612385"
---
# <a name="how-to-bind-a-windows-forms-control-to-a-type"></a><span data-ttu-id="e944c-102">Procédure : lier un contrôle Windows Forms à un type</span><span class="sxs-lookup"><span data-stu-id="e944c-102">How to: Bind a Windows Forms Control to a Type</span></span>
<span data-ttu-id="e944c-103">Quand vous créez des contrôles qui interagissent avec des données, vous devez parfois lier un contrôle à un type plutôt qu'à un objet.</span><span class="sxs-lookup"><span data-stu-id="e944c-103">When you are building controls that interact with data, you will sometimes find it necessary to bind a control to a type, rather than an object.</span></span> <span data-ttu-id="e944c-104">Cette situation se présente surtout au moment du design, quand les données peuvent ne pas être disponibles mais que vos contrôles liés aux données ont quand même besoin d'afficher des informations à partir de l'interface publique d'un type.</span><span class="sxs-lookup"><span data-stu-id="e944c-104">This situation arises especially at design time, when data may not be available, but your data-bound controls still need to display information from a type's public interface.</span></span> <span data-ttu-id="e944c-105">Par exemple, vous pouvez lier un contrôle <xref:System.Windows.Forms.DataGridView> à un objet exposé par un service web et vouloir que le contrôle <xref:System.Windows.Forms.DataGridView> étiquette ses colonnes au moment du design avec les noms de membres d'un type personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e944c-105">For example, you may bind a <xref:System.Windows.Forms.DataGridView> control to an object exposed by a Web service and want the <xref:System.Windows.Forms.DataGridView> control to label its columns at design time with the member names of a custom type.</span></span>  
  
 <span data-ttu-id="e944c-106">Vous pouvez facilement lier un contrôle à un type avec le composant <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="e944c-106">You can easily bind a control to a type with the <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e944c-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="e944c-107">Example</span></span>  
 <span data-ttu-id="e944c-108">L'exemple de code suivant montre comment lier un contrôle <xref:System.Windows.Forms.DataGridView> à un type personnalisé à l'aide d'un composant <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="e944c-108">The following code example demonstrates how to bind a <xref:System.Windows.Forms.DataGridView> control to a custom type by using a <xref:System.Windows.Forms.BindingSource> component.</span></span> <span data-ttu-id="e944c-109">Lors de l'exécution de l'exemple, vous remarquerez que le <xref:System.Windows.Forms.DataGridView> a étiqueté les colonnes qui reflètent les propriétés d'un objet `Customer`, avant que le contrôle soit rempli avec des données.</span><span class="sxs-lookup"><span data-stu-id="e944c-109">When you run the example, you'll notice the <xref:System.Windows.Forms.DataGridView> has labeled columns that reflect the properties of a `Customer` object, before the control is populated with data.</span></span> <span data-ttu-id="e944c-110">L'exemple comporte un bouton Add Customer pour ajouter des données au contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="e944c-110">The example has an Add Customer button to add data to the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="e944c-111">Quand vous cliquez sur le bouton, un nouvel objet `Customer` est ajouté à <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="e944c-111">When you click the button, a new `Customer` object is added to the <xref:System.Windows.Forms.BindingSource>.</span></span> <span data-ttu-id="e944c-112">Dans un scénario réel, les données peuvent être obtenues par un appel à un service web ou autre source de données.</span><span class="sxs-lookup"><span data-stu-id="e944c-112">In a real-world scenario, the data might be obtained by a call to a Web service or other data source.</span></span>  
  
 [!code-csharp[System.Windows.Forms.DataConnector.BindingToType#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.BindingToType/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.BindingToType#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.BindingToType/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e944c-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e944c-113">Compiling the Code</span></span>  
 <span data-ttu-id="e944c-114">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="e944c-114">This example requires:</span></span>  
  
- <span data-ttu-id="e944c-115">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="e944c-115">References to the System and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="e944c-116">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="e944c-116">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="e944c-117">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="e944c-117">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e944c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e944c-118">See also</span></span>

- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="e944c-119">BindingSource, composant</span><span class="sxs-lookup"><span data-stu-id="e944c-119">BindingSource Component</span></span>](bindingsource-component.md)
