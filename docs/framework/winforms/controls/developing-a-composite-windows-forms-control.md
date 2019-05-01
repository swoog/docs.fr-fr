---
title: Développement d'un contrôle Windows Forms composite
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], composite controls
- composite controls [Windows Forms]
- composite controls [Windows Forms], Windows Forms
- controls [Windows Forms], composite
ms.assetid: d086f2a3-baa3-4e09-b40c-a5bb3cfc51a6
ms.openlocfilehash: bfbb9091d40652bdd1ae277f3a77feefbccbf080
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972261"
---
# <a name="developing-a-composite-windows-forms-control"></a><span data-ttu-id="9f950-102">Développement d'un contrôle Windows Forms composite</span><span class="sxs-lookup"><span data-stu-id="9f950-102">Developing a Composite Windows Forms Control</span></span>
<span data-ttu-id="9f950-103">Vous pouvez développer un contrôle Windows Forms composite en combinant d'autres contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9f950-103">You can develop a composite Windows Forms control by combining other Windows Forms controls.</span></span> <span data-ttu-id="9f950-104">Les contrôles composites qui dérivent <xref:System.Web.UI.UserControl> sont appelés contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f950-104">Composite controls that derive from <xref:System.Web.UI.UserControl> are called user controls.</span></span> <span data-ttu-id="9f950-105">La classe de base, <xref:System.Windows.Forms.UserControl>, fournit le routage clavier pour les contrôles enfants, ce qui permet de garantir que les contrôles enfants peuvent recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="9f950-105">The base class, <xref:System.Windows.Forms.UserControl>, provides keyboard routing for the child controls, thus ensuring that child controls can receive focus.</span></span> <span data-ttu-id="9f950-106">Pour obtenir un exemple d’un contrôle utilisateur, consultez le <xref:System.Windows.Forms.UserControl> exemple [Comment : Appliquer des attributs dans les contrôles Windows Forms](how-to-apply-attributes-in-windows-forms-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9f950-106">For an example of a user control, see the <xref:System.Windows.Forms.UserControl> sample in [How to: Apply Attributes in Windows Forms Controls](how-to-apply-attributes-in-windows-forms-controls.md).</span></span>  
  
 <span data-ttu-id="9f950-107">Le Concepteur Windows Forms dans Visual Studio fournit la prise en charge au moment du design pour la création de contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f950-107">The Windows Forms designer in Visual Studio provides rich design-time support for authoring user controls.</span></span>  
  
- [<span data-ttu-id="9f950-108">Guide pratique pour Afficher un contrôle dans la boîte de dialogue de boîte à outils éléments choisir</span><span class="sxs-lookup"><span data-stu-id="9f950-108">How to: Display a Control in the Choose Toolbox Items Dialog Box</span></span>](how-to-display-a-control-in-the-choose-toolbox-items-dialog-box.md)  
  
- [<span data-ttu-id="9f950-109">Procédure pas à pas : Sérialisation des Collections de Types Standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="9f950-109">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)  
  
- [<span data-ttu-id="9f950-110">Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec VisualC#</span><span class="sxs-lookup"><span data-stu-id="9f950-110">Walkthrough: Inheriting from a Windows Forms Control with Visual C#</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)  
  
- [<span data-ttu-id="9f950-111">Guide pratique pour Fournir une Bitmap de boîte à outils pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="9f950-111">How to: Provide a Toolbox Bitmap for a Control</span></span>](how-to-provide-a-toolbox-bitmap-for-a-control.md)  
  
- [<span data-ttu-id="9f950-112">Guide pratique pour Windows existant hériter de contrôles de formulaires</span><span class="sxs-lookup"><span data-stu-id="9f950-112">How to: Inherit from Existing Windows Forms Controls</span></span>](how-to-inherit-from-existing-windows-forms-controls.md)  
  
- [<span data-ttu-id="9f950-113">Procédure pas à pas : Débogage des contrôles Windows Forms personnalisés au moment du design</span><span class="sxs-lookup"><span data-stu-id="9f950-113">Walkthrough: Debugging Custom Windows Forms Controls at Design Time</span></span>](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md)  
  
- [<span data-ttu-id="9f950-114">Guide pratique pour Héritez de la classe de contrôle</span><span class="sxs-lookup"><span data-stu-id="9f950-114">How to: Inherit from the Control Class</span></span>](how-to-inherit-from-the-control-class.md)  
  
- [<span data-ttu-id="9f950-115">Guide pratique pour Tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="9f950-115">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
  
- [<span data-ttu-id="9f950-116">Guide pratique pour Aligner un contrôle sur les bords des formulaires au moment du Design</span><span class="sxs-lookup"><span data-stu-id="9f950-116">How to: Align a Control to the Edges of Forms at Design Time</span></span>](how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)  
  
- [<span data-ttu-id="9f950-117">Guide pratique pour Hériter de la classe UserControl</span><span class="sxs-lookup"><span data-stu-id="9f950-117">How to: Inherit from the UserControl Class</span></span>](how-to-inherit-from-the-usercontrol-class.md)  
  
- [<span data-ttu-id="9f950-118">Guide pratique pour Créer des contrôles pour les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9f950-118">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)  
  
- [<span data-ttu-id="9f950-119">Guide pratique pour Créer des contrôles composites</span><span class="sxs-lookup"><span data-stu-id="9f950-119">How to: Author Composite Controls</span></span>](how-to-author-composite-controls.md)  
  
- [<span data-ttu-id="9f950-120">Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9f950-120">Walkthrough: Authoring a Composite Control with Visual Basic</span></span>](walkthrough-authoring-a-composite-control-with-visual-basic.md)  
  
- [<span data-ttu-id="9f950-121">Procédure pas à pas : Création d’un contrôle Composite avec VisualC#</span><span class="sxs-lookup"><span data-stu-id="9f950-121">Walkthrough: Authoring a Composite Control with Visual C#</span></span>](walkthrough-authoring-a-composite-control-with-visual-csharp.md)  
  
- [<span data-ttu-id="9f950-122">Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9f950-122">Walkthrough: Inheriting from a Windows Forms Control with Visual Basic</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)  
  
- [<span data-ttu-id="9f950-123">Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f950-123">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)  
  
- <span data-ttu-id="9f950-124">[Guide pratique pour Créer un contrôle Windows Forms tire parti des fonctionnalités de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="9f950-124">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f950-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f950-125">See also</span></span>

- [<span data-ttu-id="9f950-126">Guide pratique pour Appliquer des attributs dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9f950-126">How to: Apply Attributes in Windows Forms Controls</span></span>](how-to-apply-attributes-in-windows-forms-controls.md)
- [<span data-ttu-id="9f950-127">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="9f950-127">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="9f950-128">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="9f950-128">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
