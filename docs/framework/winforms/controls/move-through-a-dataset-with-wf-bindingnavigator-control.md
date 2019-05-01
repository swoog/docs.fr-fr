---
title: 'Procédure : parcourir un jeu de données avec le contrôle BindingNavigator de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- datasets [Windows Forms], moving through
- BindingNavigator control [Windows Forms], moving through datasets
- examples [Windows Forms], BindingNavigator control
ms.assetid: 146d97be-3d97-400e-accb-860bbf47729d
ms.openlocfilehash: d76c2e5882c9df94674294da00ba446dfbfd2b3a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012735"
---
# <a name="how-to-move-through-a-dataset-with-the-windows-forms-bindingnavigator-control"></a><span data-ttu-id="f2d5a-102">Procédure : parcourir un jeu de données avec le contrôle BindingNavigator de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f2d5a-102">How to: Move Through a DataSet with the Windows Forms BindingNavigator Control</span></span>
<span data-ttu-id="f2d5a-103">Quand vous générez des applications pilotées par les données, vous devez souvent présenter des collections de données aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-103">As you build data-driven applications, you will often need to display collections of data to users.</span></span> <span data-ttu-id="f2d5a-104">Le contrôle <xref:System.Windows.Forms.BindingNavigator>, associé au composant <xref:System.Windows.Forms.BindingSource>, fournit une solution pratique et extensible pour parcourir une collection et afficher des éléments de façon séquentielle.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-104">The <xref:System.Windows.Forms.BindingNavigator> control, in conjunction with the <xref:System.Windows.Forms.BindingSource> component, provides a convenient and extensible solution for moving through a collection and displaying items sequentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f2d5a-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2d5a-105">Example</span></span>  
 <span data-ttu-id="f2d5a-106">L'exemple de code suivant montre comment utiliser un contrôle <xref:System.Windows.Forms.BindingNavigator> pour parcourir des données.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-106">The following code example demonstrates how to use a <xref:System.Windows.Forms.BindingNavigator> control to move through data.</span></span> <span data-ttu-id="f2d5a-107">Le jeu est contenu dans un <xref:System.Data.DataView>, qui est lié à un contrôle <xref:System.Windows.Forms.TextBox> avec un composant <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-107">The set is contained in a <xref:System.Data.DataView>, which is bound to a <xref:System.Windows.Forms.TextBox> control with a <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f2d5a-108">Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-108">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="f2d5a-109">L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-109">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="f2d5a-110">Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).</span><span class="sxs-lookup"><span data-stu-id="f2d5a-110">For more information, see [Protecting Connection Information](../../data/adonet/protecting-connection-information.md).</span></span>  
  
 [!code-csharp[System.Windows.Forms.DataNavigator#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataNavigator/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataNavigator#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataNavigator/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f2d5a-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f2d5a-111">Compiling the Code</span></span>  
 <span data-ttu-id="f2d5a-112">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="f2d5a-112">This example requires:</span></span>  
  
- <span data-ttu-id="f2d5a-113">Références aux assemblys System, System.Data, System.Drawing, System.Windows.Forms et System.Xml.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-113">References to the System, System.Data, System.Drawing, System.Windows.Forms and System.Xml assemblies.</span></span>  
  
 <span data-ttu-id="f2d5a-114">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="f2d5a-114">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="f2d5a-115">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="f2d5a-115">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2d5a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d5a-116">See also</span></span>

- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="f2d5a-117">BindingNavigator, contrôle</span><span class="sxs-lookup"><span data-stu-id="f2d5a-117">BindingNavigator Control</span></span>](bindingnavigator-control-windows-forms.md)
- [<span data-ttu-id="f2d5a-118">BindingSource, composant</span><span class="sxs-lookup"><span data-stu-id="f2d5a-118">BindingSource Component</span></span>](bindingsource-component.md)
- [<span data-ttu-id="f2d5a-119">Guide pratique pour Lier un contrôle de formulaires Windows à un Type</span><span class="sxs-lookup"><span data-stu-id="f2d5a-119">How to: Bind a Windows Forms Control to a Type</span></span>](how-to-bind-a-windows-forms-control-to-a-type.md)
