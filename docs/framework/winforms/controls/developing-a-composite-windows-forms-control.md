---
title: Développement d'un contrôle Windows Forms composite
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], composite controls
- composite controls [Windows Forms]
- composite controls [Windows Forms], Windows Forms
- controls [Windows Forms], composite
ms.assetid: d086f2a3-baa3-4e09-b40c-a5bb3cfc51a6
ms.openlocfilehash: 82d76c1656ff14c6d1c9bbbb1c79ec3a30708a90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54635713"
---
# <a name="developing-a-composite-windows-forms-control"></a><span data-ttu-id="067d0-102">Développement d'un contrôle Windows Forms composite</span><span class="sxs-lookup"><span data-stu-id="067d0-102">Developing a Composite Windows Forms Control</span></span>
<span data-ttu-id="067d0-103">Vous pouvez développer un contrôle Windows Forms composite en combinant d'autres contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="067d0-103">You can develop a composite Windows Forms control by combining other Windows Forms controls.</span></span> <span data-ttu-id="067d0-104">Les contrôles composites qui dérivent <xref:System.Web.UI.UserControl> sont appelés contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="067d0-104">Composite controls that derive from <xref:System.Web.UI.UserControl> are called user controls.</span></span> <span data-ttu-id="067d0-105">La classe de base, <xref:System.Windows.Forms.UserControl>, fournit le routage clavier pour les contrôles enfants, ce qui permet de garantir que les contrôles enfants peuvent recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="067d0-105">The base class, <xref:System.Windows.Forms.UserControl>, provides keyboard routing for the child controls, thus ensuring that child controls can receive focus.</span></span> <span data-ttu-id="067d0-106">Pour obtenir un exemple d’un contrôle utilisateur, consultez le <xref:System.Windows.Forms.UserControl> exemple [Comment : Appliquer des attributs dans les contrôles Windows Forms](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md).</span><span class="sxs-lookup"><span data-stu-id="067d0-106">For an example of a user control, see the <xref:System.Windows.Forms.UserControl> sample in [How to: Apply Attributes in Windows Forms Controls](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md).</span></span>  
  
 <span data-ttu-id="067d0-107">Le Concepteur Windows Forms dans Visual Studio fournit la prise en charge au moment du design pour la création de contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="067d0-107">The Windows Forms designer in Visual Studio provides rich design-time support for authoring user controls.</span></span>  
  
-   <span data-ttu-id="067d0-108">[Guide pratique pour Afficher un contrôle dans la boîte de dialogue de boîte à outils éléments choisir](https://msdn.microsoft.com/library/9yxtkx75\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-108">[How to: Display a Control in the Choose Toolbox Items Dialog Box](https://msdn.microsoft.com/library/9yxtkx75\(v=vs.110\))</span></span>  
  
-   [<span data-ttu-id="067d0-109">Procédure pas à pas : Sérialisation des Collections de Types Standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="067d0-109">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)  
  
-   <span data-ttu-id="067d0-110">[Procédure pas à pas : Héritage à partir d’un Windows Forms contrôle visuel C# ](https://msdn.microsoft.com/library/09476da0-8d4c-4a4c-b969-649519dfb438))</span><span class="sxs-lookup"><span data-stu-id="067d0-110">[Walkthrough: Inheriting from a Windows Forms Control with Visual C#](https://msdn.microsoft.com/library/09476da0-8d4c-4a4c-b969-649519dfb438))</span></span>  
  
-   <span data-ttu-id="067d0-111">[Guide pratique pour Fournir une Bitmap de boîte à outils pour un contrôle](https://msdn.microsoft.com/library/4wk1wc0a\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-111">[How to: Provide a Toolbox Bitmap for a Control](https://msdn.microsoft.com/library/4wk1wc0a\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-112">[Guide pratique pour Windows existant hériter de contrôles de formulaires](https://msdn.microsoft.com/library/7h62478z\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-112">[How to: Inherit from Existing Windows Forms Controls](https://msdn.microsoft.com/library/7h62478z\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-113">[Procédure pas à pas : Débogage des contrôles Windows Forms personnalisés au moment du design](https://msdn.microsoft.com/library/5ytx0z24\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-113">[Walkthrough: Debugging Custom Windows Forms Controls at Design Time](https://msdn.microsoft.com/library/5ytx0z24\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-114">[Guide pratique pour Héritez de la classe de contrôle](https://msdn.microsoft.com/library/skcysbt2\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-114">[How to: Inherit from the Control Class](https://msdn.microsoft.com/library/skcysbt2\(v=vs.110\))</span></span>  
  
-   [<span data-ttu-id="067d0-115">Guide pratique pour Tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="067d0-115">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
  
-   <span data-ttu-id="067d0-116">[Guide pratique pour Aligner un contrôle sur les bords des formulaires au moment du Design](https://msdn.microsoft.com/library/1fxyb15b\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-116">[How to: Align a Control to the Edges of Forms at Design Time](https://msdn.microsoft.com/library/1fxyb15b\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-117">[Guide pratique pour Hériter de la classe UserControl](https://msdn.microsoft.com/library/00ctb4z0\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-117">[How to: Inherit from the UserControl Class](https://msdn.microsoft.com/library/00ctb4z0\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-118">[Guide pratique pour Créer des contrôles pour les Windows Forms](https://msdn.microsoft.com/library/bs3yhkh7\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-118">[How to: Author Controls for Windows Forms](https://msdn.microsoft.com/library/bs3yhkh7\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-119">[Guide pratique pour Créer des contrôles composites](https://msdn.microsoft.com/library/3sf86w5h\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-119">[How to: Author Composite Controls](https://msdn.microsoft.com/library/3sf86w5h\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-120">[Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic](https://msdn.microsoft.com/library/c316f119\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-120">[Walkthrough: Authoring a Composite Control with Visual Basic](https://msdn.microsoft.com/library/c316f119\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-121">[Procédure pas à pas : Création d’un contrôle Composite avec Visual C# ](https://msdn.microsoft.com/library/f88481a8-c746-4a36-9479-374ce5f2e91f))</span><span class="sxs-lookup"><span data-stu-id="067d0-121">[Walkthrough: Authoring a Composite Control with Visual C#](https://msdn.microsoft.com/library/f88481a8-c746-4a36-9479-374ce5f2e91f))</span></span>  
  
-   <span data-ttu-id="067d0-122">[Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec Visual Basic](https://msdn.microsoft.com/library/w2a8y03d\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-122">[Walkthrough: Inheriting from a Windows Forms Control with Visual Basic](https://msdn.microsoft.com/library/w2a8y03d\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-123">[Guide pratique pour Créer un contrôle Windows Forms tire parti des fonctionnalités de conception](https://msdn.microsoft.com/library/307hck25\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="067d0-123">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://msdn.microsoft.com/library/307hck25\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="067d0-124">[Guide pratique pour Créer un contrôle Windows Forms tire parti des fonctionnalités de conception](https://msdn.microsoft.com/library/307hck25\(v=vs.120\))</span><span class="sxs-lookup"><span data-stu-id="067d0-124">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://msdn.microsoft.com/library/307hck25\(v=vs.120\))</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="067d0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="067d0-125">See also</span></span>
- [<span data-ttu-id="067d0-126">Guide pratique pour Appliquer des attributs dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="067d0-126">How to: Apply Attributes in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md)
- [<span data-ttu-id="067d0-127">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="067d0-127">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="067d0-128">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="067d0-128">Varieties of Custom Controls</span></span>](../../../../docs/framework/winforms/controls/varieties-of-custom-controls.md)
