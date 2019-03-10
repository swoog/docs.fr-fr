---
title: 'Procédure : Lier un contrôle de formulaires Windows à un Type à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], binding to a type
- BindingSource component [Windows Forms], binding to a type
- types [Windows Forms], binding controls to
ms.assetid: 5ab984b5-c2d0-4638-a572-1c84013e8746
ms.openlocfilehash: 29a28052b149f565e47a2e0366ed6845b83234ba
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57712095"
---
# <a name="how-to-bind-a-windows-forms-control-to-a-type-using-the-designer"></a><span data-ttu-id="57420-102">Procédure : Lier un contrôle de formulaires Windows à un Type à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="57420-102">How to: Bind a Windows Forms Control to a Type Using the Designer</span></span>
<span data-ttu-id="57420-103">Quand vous créez des contrôles qui interagissent avec des données, vous devez parfois lier un contrôle à un type plutôt qu’à un objet.</span><span class="sxs-lookup"><span data-stu-id="57420-103">When you are building controls that interact with data, you sometimes need to bind a control to a type, rather than an object.</span></span> <span data-ttu-id="57420-104">Cette situation se présente surtout au moment du design, quand les données peuvent ne pas être disponibles mais que vos contrôles liés aux données ont tout de même besoin d’afficher des informations à partir de l’interface publique d’un type.</span><span class="sxs-lookup"><span data-stu-id="57420-104">You typically need to bind a control to a type at design time, when data may not be available, but you still want your data-bound controls to display data from a type's public interface.</span></span> <span data-ttu-id="57420-105">Les procédures suivantes montrent comment créer un nouveau <xref:System.Windows.Forms.BindingSource> qui est lié à un type, puis comment lier une des propriétés du type pour le <xref:System.Windows.Forms.TextBox.Text%2A> propriété d’un <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="57420-105">The following procedures demonstrate how to create a new <xref:System.Windows.Forms.BindingSource> that is bound to a type, and then how to bind one of the type's properties to the <xref:System.Windows.Forms.TextBox.Text%2A> property of a <xref:System.Windows.Forms.TextBox>.</span></span>  
  
### <a name="to-bind-the-bindingsource-to-a-type"></a><span data-ttu-id="57420-106">Pour lier le BindingSource à un type</span><span class="sxs-lookup"><span data-stu-id="57420-106">To bind the BindingSource to a type</span></span>  
  
1.  <span data-ttu-id="57420-107">Créez un projet Windows Forms (**fichier** > **New** > **projet** > **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="57420-107">Create a Windows Forms project (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2.  <span data-ttu-id="57420-108">Dans **conception** afficher, faites glisser un <xref:System.Windows.Forms.BindingSource> composant vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="57420-108">In **Design** view, drag a <xref:System.Windows.Forms.BindingSource> component onto the form.</span></span>  
  
3.  <span data-ttu-id="57420-109">Dans le **propriétés** fenêtre, cliquez sur la flèche pour la <xref:System.Windows.Forms.BindingSource.DataSource%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="57420-109">In the **Properties** window, click the arrow for the <xref:System.Windows.Forms.BindingSource.DataSource%2A> property.</span></span>  
  
4.  <span data-ttu-id="57420-110">Dans l’**éditeur de types d’interface utilisateur DataSource**, cliquez sur **Ajouter la source de données du projet**.</span><span class="sxs-lookup"><span data-stu-id="57420-110">In the **DataSource UI Type Editor**, click **Add Project Data Source**.</span></span>  
  
5.  <span data-ttu-id="57420-111">Sur la page **Choisir un type de source de données**, sélectionnez **Objet**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="57420-111">On the **Choose a Data Source Type** page, select **Object** and click **Next**.</span></span>  
  
6.  <span data-ttu-id="57420-112">Sélectionnez le type à lier :</span><span class="sxs-lookup"><span data-stu-id="57420-112">Select the type to bind to:</span></span>  
  
    -   <span data-ttu-id="57420-113">Si le type avec lequel vous souhaitez établir une liaison se trouve dans le projet actuel, ou si l’assembly qui contient ce type est déjà ajouté en tant que référence, développez les nœuds pour rechercher le type souhaité et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="57420-113">If the type you want to bind to is in the current project, or the assembly that contains the type is already added as a reference, expand the nodes to find the type you want, and then select it.</span></span>  
  
         <span data-ttu-id="57420-114">ou</span><span class="sxs-lookup"><span data-stu-id="57420-114">-or-</span></span>  
  
    -   <span data-ttu-id="57420-115">Si le type avec lequel vous souhaitez établir une liaison se trouve actuellement dans un autre assembly, et non dans la liste de références, cliquez sur **Ajouter une référence**, puis cliquez sur l’onglet **Projets**. Sélectionnez le projet contenant l’objet métier de votre choix, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="57420-115">If the type you want to bind to is in another assembly, not currently in the list of references, click **Add Reference**, and then click the **Projects** tab. Select the project that contains the business object you want and click **OK**.</span></span> <span data-ttu-id="57420-116">Ce projet apparaît dans la liste des assemblys. Vous pouvez donc développer les nœuds pour rechercher le type que vous souhaitez, puis le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="57420-116">This project will appear in the list of assemblies, so you can expand the nodes to find the type you want, and then select it.</span></span>  
  
        > [!NOTE]
        >  <span data-ttu-id="57420-117">Pour effectuer une liaison avec un type présent dans une infrastructure ou un assembly Microsoft, décochez la case **Masquer les assemblys qui commencent par Microsoft ou System**.</span><span class="sxs-lookup"><span data-stu-id="57420-117">If you want to bind to a type in a framework or Microsoft assembly, clear the **Hide assemblies that begin with Microsoft or System** check box.</span></span>  
  
7.  <span data-ttu-id="57420-118">Cliquez sur **Suivant**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="57420-118">Click **Next**, and then click **Finish**.</span></span>  
  
### <a name="to-bind-the-control-to-the-bindingsource"></a><span data-ttu-id="57420-119">Pour lier le contrôle au BindingSource</span><span class="sxs-lookup"><span data-stu-id="57420-119">To bind the control to the BindingSource</span></span>  
  
1.  <span data-ttu-id="57420-120">Ajoutez un <xref:System.Windows.Forms.TextBox> au formulaire.</span><span class="sxs-lookup"><span data-stu-id="57420-120">Add a <xref:System.Windows.Forms.TextBox> to the form.</span></span>  
  
2.  <span data-ttu-id="57420-121">Dans la fenêtre **Propriétés**, développez le nœud **(DataBindings)**.</span><span class="sxs-lookup"><span data-stu-id="57420-121">In the **Properties** window, expand the **(DataBindings)** node.</span></span>  
  
3.  <span data-ttu-id="57420-122">Cliquez sur la flèche en regard du <xref:System.Windows.Forms.TextBox.Text%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="57420-122">Click the arrow next to the <xref:System.Windows.Forms.TextBox.Text%2A> property.</span></span>  
  
4.  <span data-ttu-id="57420-123">Dans le **éditeur de Type d’interface utilisateur DataSource**, développez le nœud pour le <xref:System.Windows.Forms.BindingSource> ajouté précédemment, puis sélectionnez la propriété du type lié que vous souhaitez lier à la <xref:System.Windows.Forms.TextBox.Text%2A> propriété de la <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="57420-123">In the **DataSource UI Type Editor**, expand the node for the <xref:System.Windows.Forms.BindingSource> added previously, and select the property of the bound type you want to bind to the <xref:System.Windows.Forms.TextBox.Text%2A> property of the <xref:System.Windows.Forms.TextBox>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57420-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57420-124">See also</span></span>
- [<span data-ttu-id="57420-125">BindingSource, composant</span><span class="sxs-lookup"><span data-stu-id="57420-125">BindingSource Component</span></span>](bindingsource-component.md)
- [<span data-ttu-id="57420-126">Guide pratique pour Lier un contrôle de formulaires Windows à un Type</span><span class="sxs-lookup"><span data-stu-id="57420-126">How to: Bind a Windows Forms Control to a Type</span></span>](how-to-bind-a-windows-forms-control-to-a-type.md)
- [<span data-ttu-id="57420-127">Lier des contrôles à des données dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="57420-127">Bind controls to data in Visual Studio</span></span>](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)
