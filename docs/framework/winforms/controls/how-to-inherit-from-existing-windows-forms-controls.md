---
title: 'Comment : hériter de contrôles Windows Forms existants'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- custom controls [Windows Forms], inheritance
ms.assetid: 1e1fc8ea-c615-4cf0-a356-16d6df7444ab
ms.openlocfilehash: f19b207c840994ffa3aa364135583b5daeb26827
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43890458"
---
# <a name="how-to-inherit-from-existing-windows-forms-controls"></a><span data-ttu-id="4959c-102">Comment : hériter de contrôles Windows Forms existants</span><span class="sxs-lookup"><span data-stu-id="4959c-102">How to: Inherit from Existing Windows Forms Controls</span></span>
<span data-ttu-id="4959c-103">Si vous souhaitez étendre les fonctionnalités d’un contrôle existant, vous pouvez créer un contrôle dérivé d’un contrôle existant par héritage.</span><span class="sxs-lookup"><span data-stu-id="4959c-103">If you want to extend the functionality of an existing control, you can create a control derived from an existing control through inheritance.</span></span> <span data-ttu-id="4959c-104">Lorsque vous héritez d’un contrôle existant, vous héritez de toutes les fonctionnalités et propriétés visuelles de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="4959c-104">When inheriting from an existing control, you inherit all of the functionality and visual properties of that control.</span></span> <span data-ttu-id="4959c-105">Par exemple, si vous avez créé un contrôle hérité de <xref:System.Windows.Forms.Button>, votre aura l’aspect et le comportement standard <xref:System.Windows.Forms.Button> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4959c-105">For example, if you were creating a control that inherited from <xref:System.Windows.Forms.Button>, your new control would look and act exactly like a standard <xref:System.Windows.Forms.Button> control.</span></span> <span data-ttu-id="4959c-106">Vous pourrez ensuite étendre ou modifier les fonctionnalités de votre nouveau contrôle en implémentant des méthodes et des propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4959c-106">You could then extend or modify the functionality of your new control through the implementation of custom methods and properties.</span></span> <span data-ttu-id="4959c-107">Dans certains cas, vous pouvez également modifier l’apparence visuelle du contrôle hérité en substituant ses <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4959c-107">In some controls, you can also change the visual appearance of your inherited control by overriding its <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4959c-108">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="4959c-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="4959c-109">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="4959c-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="4959c-110">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="4959c-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-an-inherited-control"></a><span data-ttu-id="4959c-111">Pour créer un contrôle hérité</span><span class="sxs-lookup"><span data-stu-id="4959c-111">To create an inherited control</span></span>  
  
1.  <span data-ttu-id="4959c-112">Créez un projet d’**application Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="4959c-112">Create a new **Windows Forms Application** project.</span></span>  
  
2.  <span data-ttu-id="4959c-113">Dans le menu **Projet**, sélectionnez **Ajouter un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="4959c-113">From the **Project** menu, choose **Add New Item**.</span></span>  
  
     <span data-ttu-id="4959c-114">La boîte de dialogue **Ajouter un nouvel élément** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4959c-114">The **Add New Item** dialog box appears.</span></span>  
  
3.  <span data-ttu-id="4959c-115">Dans la boîte de dialogue **Ajouter un nouvel élément**, double-cliquez sur **Contrôle personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="4959c-115">In the **Add New Item** dialog box, double-click **Custom Control**.</span></span>  
  
     <span data-ttu-id="4959c-116">Un contrôle personnalisé est ajouté à votre projet.</span><span class="sxs-lookup"><span data-stu-id="4959c-116">A new custom control is added to your project.</span></span>  
  
4.  <span data-ttu-id="4959c-117">Si vous utilisez Visual Basic, en haut de l’**Explorateur de solutions**, cliquez sur **Afficher tous les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="4959c-117">If you using Visual Basic, at the top of **Solution Explorer**, click **Show All Files**.</span></span> <span data-ttu-id="4959c-118">Développez CustomControl1.vb, puis ouvrez CustomControl1.Designer.vb dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4959c-118">Expand CustomControl1.vb and then open CustomControl1.Designer.vb in the Code Editor.</span></span>  
  
5.  <span data-ttu-id="4959c-119">Si vous utilisez C#, ouvrez CustomControl1.cs dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4959c-119">If you are using C#, open CustomControl1.cs in the Code Editor.</span></span>  
  
6.  <span data-ttu-id="4959c-120">Recherchez la déclaration de classe qui hérite de <xref:System.Windows.Forms.Control>.</span><span class="sxs-lookup"><span data-stu-id="4959c-120">Locate the class declaration, which inherits from <xref:System.Windows.Forms.Control>.</span></span>  
  
7.  <span data-ttu-id="4959c-121">Remplacez la classe de base par le contrôle dont vous voulez hériter.</span><span class="sxs-lookup"><span data-stu-id="4959c-121">Change the base class to the control that you want to inherit from.</span></span>  
  
     <span data-ttu-id="4959c-122">Par exemple, si vous voulez hériter <xref:System.Windows.Forms.Button>, modifiez la déclaration de classe à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="4959c-122">For example, if you want to inherit from <xref:System.Windows.Forms.Button>, change the class declaration to the following:</span></span>  
  
    ```vb  
    Partial Class CustomControl1  
        Inherits System.Windows.Forms.Button  
    ```  
  
    ```csharp  
    public partial class CustomControl1 : System.Windows.Forms.Button  
    ```  
  
8.  <span data-ttu-id="4959c-123">Si vous utilisez Visual Basic, enregistrez et fermez CustomControl1.Designer.vb.</span><span class="sxs-lookup"><span data-stu-id="4959c-123">If you are using Visual Basic, save and close CustomControl1.Designer.vb.</span></span> <span data-ttu-id="4959c-124">Ouvrez CustomControl1.vb dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4959c-124">Open CustomControl1.vb in the Code Editor.</span></span>  
  
9. <span data-ttu-id="4959c-125">Implémentez les méthodes ou propriétés personnalisées que votre contrôle intégrera.</span><span class="sxs-lookup"><span data-stu-id="4959c-125">Implement any custom methods or properties that your control will incorporate.</span></span>  
  
10. <span data-ttu-id="4959c-126">Si vous souhaitez modifier l’aspect graphique de votre contrôle, substituez le <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4959c-126">If you want to modify the graphical appearance of your control, override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="4959c-127">Substitution de <xref:System.Windows.Forms.Control.OnPaint%2A> vous autorisera pas à modifier l’apparence de tous les contrôles.</span><span class="sxs-lookup"><span data-stu-id="4959c-127">Overriding <xref:System.Windows.Forms.Control.OnPaint%2A> will not allow you to modify the appearance of all controls.</span></span> <span data-ttu-id="4959c-128">Les contrôles dont tout la peinture effectuée par Windows (par exemple, <xref:System.Windows.Forms.TextBox>) appellent jamais leur <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode) et n’utiliseront donc jamais le code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4959c-128">Those controls that have all of their painting done by Windows (for example, <xref:System.Windows.Forms.TextBox>) never call their <xref:System.Windows.Forms.Control.OnPaint%2A> method, and thus will never use the custom code.</span></span> <span data-ttu-id="4959c-129">Reportez-vous à la documentation d’aide pour le contrôle particulier que vous souhaitez modifier pour vérifier si le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="4959c-129">Refer to the Help documentation for the particular control you want to modify to see if the <xref:System.Windows.Forms.Control.OnPaint%2A> method is available.</span></span> <span data-ttu-id="4959c-130">Pour obtenir la liste de tous les contrôles Windows Forms, consultez [Contrôles à utiliser dans les Windows Forms](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="4959c-130">For a list of all the Windows Form Controls, see [Controls to Use on Windows Forms](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md).</span></span> <span data-ttu-id="4959c-131">Si un contrôle n’a pas <xref:System.Windows.Forms.Control.OnPaint%2A> répertorié comme une méthode membre, vous ne pouvez pas modifier son apparence en substituant cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4959c-131">If a control does not have <xref:System.Windows.Forms.Control.OnPaint%2A> listed as a member method, you cannot alter its appearance by overriding this method.</span></span> <span data-ttu-id="4959c-132">Pour plus d’informations sur la peinture personnalisée, consultez [Peinture et rendu personnalisés des contrôles](../../../../docs/framework/winforms/controls/custom-control-painting-and-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="4959c-132">For more information about custom painting, see [Custom Control Painting and Rendering](../../../../docs/framework/winforms/controls/custom-control-painting-and-rendering.md).</span></span>  
  
    ```vb  
    Protected Overrides Sub OnPaint(ByVal e As _  
       System.Windows.Forms.PaintEventArgs)  
       MyBase.OnPaint(e)  
       ' Insert code to do custom painting.   
       ' If you want to completely change the appearance of your control,  
       ' do not call MyBase.OnPaint(e).  
    End Sub  
    ```  
  
    ```csharp  
    protected override void OnPaint(PaintEventArgs pe)  
    {  
       base.OnPaint(pe);  
       // Insert code to do custom painting.  
       // If you want to completely change the appearance of your control,  
       // do not call base.OnPaint(pe).  
    }  
    ```  
  
11. <span data-ttu-id="4959c-133">Enregistrez et testez votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="4959c-133">Save and test your control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4959c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4959c-134">See Also</span></span>  
 [<span data-ttu-id="4959c-135">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="4959c-135">Varieties of Custom Controls</span></span>](../../../../docs/framework/winforms/controls/varieties-of-custom-controls.md)  
 [<span data-ttu-id="4959c-136">Guide pratique pour hériter de la classe du contrôle</span><span class="sxs-lookup"><span data-stu-id="4959c-136">How to: Inherit from the Control Class</span></span>](../../../../docs/framework/winforms/controls/how-to-inherit-from-the-control-class.md)  
 [<span data-ttu-id="4959c-137">Comment : hériter de la classe UserControl</span><span class="sxs-lookup"><span data-stu-id="4959c-137">How to: Inherit from the UserControl Class</span></span>](../../../../docs/framework/winforms/controls/how-to-inherit-from-the-usercontrol-class.md)  
 [<span data-ttu-id="4959c-138">Guide pratique pour créer des contrôles pour des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4959c-138">How to: Author Controls for Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-author-controls-for-windows-forms.md)  
 [<span data-ttu-id="4959c-139">Dépannage des gestionnaires d’événements hérités en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4959c-139">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)  
 [<span data-ttu-id="4959c-140">Procédure pas à pas : héritage à partir d'un contrôle Windows Forms à l'aide de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4959c-140">Walkthrough: Inheriting from a Windows Forms Control with Visual Basic</span></span>](../../../../docs/framework/winforms/controls/walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)  
 [<span data-ttu-id="4959c-141">Procédure pas à pas : héritage d’un contrôle Windows Forms à l’aide de Visual C#</span><span class="sxs-lookup"><span data-stu-id="4959c-141">Walkthrough: Inheriting from a Windows Forms Control with Visual C#</span></span>](../../../../docs/framework/winforms/controls/walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)
