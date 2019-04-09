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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59196461"
---
# <a name="developing-a-composite-windows-forms-control"></a><span data-ttu-id="6a2fe-102">Développement d'un contrôle Windows Forms composite</span><span class="sxs-lookup"><span data-stu-id="6a2fe-102">Developing a Composite Windows Forms Control</span></span>
<span data-ttu-id="6a2fe-103">Vous pouvez développer un contrôle Windows Forms composite en combinant d'autres contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="6a2fe-103">You can develop a composite Windows Forms control by combining other Windows Forms controls.</span></span> <span data-ttu-id="6a2fe-104">Les contrôles composites qui dérivent <xref:System.Web.UI.UserControl> sont appelés contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a2fe-104">Composite controls that derive from <xref:System.Web.UI.UserControl> are called user controls.</span></span> <span data-ttu-id="6a2fe-105">La classe de base, <xref:System.Windows.Forms.UserControl>, fournit le routage clavier pour les contrôles enfants, ce qui permet de garantir que les contrôles enfants peuvent recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="6a2fe-105">The base class, <xref:System.Windows.Forms.UserControl>, provides keyboard routing for the child controls, thus ensuring that child controls can receive focus.</span></span> <span data-ttu-id="6a2fe-106">Pour obtenir un exemple d’un contrôle utilisateur, consultez le <xref:System.Windows.Forms.UserControl> exemple [Comment : Appliquer des attributs dans les contrôles Windows Forms](how-to-apply-attributes-in-windows-forms-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6a2fe-106">For an example of a user control, see the <xref:System.Windows.Forms.UserControl> sample in [How to: Apply Attributes in Windows Forms Controls](how-to-apply-attributes-in-windows-forms-controls.md).</span></span>  
  
 <span data-ttu-id="6a2fe-107">Le Concepteur Windows Forms dans Visual Studio fournit la prise en charge au moment du design pour la création de contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a2fe-107">The Windows Forms designer in Visual Studio provides rich design-time support for authoring user controls.</span></span>  
  
-   [<span data-ttu-id="6a2fe-108">Procédure : afficher un contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils</span><span class="sxs-lookup"><span data-stu-id="6a2fe-108">How to: Display a Control in the Choose Toolbox Items Dialog Box</span></span>](how-to-display-a-control-in-the-choose-toolbox-items-dialog-box.md)  
  
-   [<span data-ttu-id="6a2fe-109">Procédure pas à pas : Sérialisation des collections de types standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="6a2fe-109">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)  
  
-   [<span data-ttu-id="6a2fe-110">Procédure pas à pas : Héritage d'un contrôle Windows Forms à l'aide de Visual C#</span><span class="sxs-lookup"><span data-stu-id="6a2fe-110">Walkthrough: Inheriting from a Windows Forms Control with Visual C#</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)  
  
-   [<span data-ttu-id="6a2fe-111">Procédure : fournir une image bitmap de boîte à outils pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="6a2fe-111">How to: Provide a Toolbox Bitmap for a Control</span></span>](how-to-provide-a-toolbox-bitmap-for-a-control.md)  
  
-   [<span data-ttu-id="6a2fe-112">Procédure : hériter de contrôles Windows Forms existants</span><span class="sxs-lookup"><span data-stu-id="6a2fe-112">How to: Inherit from Existing Windows Forms Controls</span></span>](how-to-inherit-from-existing-windows-forms-controls.md)  
  
-   [<span data-ttu-id="6a2fe-113">Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design</span><span class="sxs-lookup"><span data-stu-id="6a2fe-113">Walkthrough: Debugging Custom Windows Forms Controls at Design Time</span></span>](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md)  
  
-   [<span data-ttu-id="6a2fe-114">Procédure : hériter de la classe Control</span><span class="sxs-lookup"><span data-stu-id="6a2fe-114">How to: Inherit from the Control Class</span></span>](how-to-inherit-from-the-control-class.md)  
  
-   [<span data-ttu-id="6a2fe-115">Procédure : tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="6a2fe-115">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
  
-   [<span data-ttu-id="6a2fe-116">Procédure : aligner un contrôle sur les bords des formulaires au moment du design</span><span class="sxs-lookup"><span data-stu-id="6a2fe-116">How to: Align a Control to the Edges of Forms at Design Time</span></span>](how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)  
  
-   [<span data-ttu-id="6a2fe-117">Procédure : hériter de la classe UserControl</span><span class="sxs-lookup"><span data-stu-id="6a2fe-117">How to: Inherit from the UserControl Class</span></span>](how-to-inherit-from-the-usercontrol-class.md)  
  
-   [<span data-ttu-id="6a2fe-118">Procédure : créer des contrôles pour Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6a2fe-118">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)  
  
-   [<span data-ttu-id="6a2fe-119">Procédure : créer des contrôles composites</span><span class="sxs-lookup"><span data-stu-id="6a2fe-119">How to: Author Composite Controls</span></span>](how-to-author-composite-controls.md)  
  
-   [<span data-ttu-id="6a2fe-120">Procédure pas à pas : création d’un contrôle composite avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6a2fe-120">Walkthrough: Authoring a Composite Control with Visual Basic</span></span>](walkthrough-authoring-a-composite-control-with-visual-basic.md)  
  
-   [<span data-ttu-id="6a2fe-121">Procédure pas à pas : Création d'un contrôle composite à l'aide de Visual C#</span><span class="sxs-lookup"><span data-stu-id="6a2fe-121">Walkthrough: Authoring a Composite Control with Visual C#</span></span>](walkthrough-authoring-a-composite-control-with-visual-csharp.md)  
  
-   [<span data-ttu-id="6a2fe-122">Procédure pas à pas : héritage d’un contrôle Windows Forms avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6a2fe-122">Walkthrough: Inheriting from a Windows Forms Control with Visual Basic</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)  
  
-   [<span data-ttu-id="6a2fe-123">Procédure pas à pas : création d’un contrôle Windows Forms qui tire parti des fonctionnalités au moment du design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6a2fe-123">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)  
  
-   [<span data-ttu-id="6a2fe-124">Procédure : Créer un contrôle Windows Forms tire parti des fonctionnalités de conception</span><span class="sxs-lookup"><span data-stu-id="6a2fe-124">How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features</span></span>](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))  
  
## <a name="see-also"></a><span data-ttu-id="6a2fe-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a2fe-125">See also</span></span>

- [<span data-ttu-id="6a2fe-126">Procédure : appliquer des attributs dans des contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6a2fe-126">How to: Apply Attributes in Windows Forms Controls</span></span>](how-to-apply-attributes-in-windows-forms-controls.md)
- [<span data-ttu-id="6a2fe-127">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="6a2fe-127">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="6a2fe-128">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="6a2fe-128">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
