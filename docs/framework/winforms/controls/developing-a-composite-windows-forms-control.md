---
title: Développement d'un contrôle Windows Forms composite
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], composite controls
- composite controls [Windows Forms]
- composite controls [Windows Forms], Windows Forms
- controls [Windows Forms], composite
ms.assetid: d086f2a3-baa3-4e09-b40c-a5bb3cfc51a6
ms.openlocfilehash: 24fbf17f02072b2d9922ca0998805b916afc41b6
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510158"
---
# <a name="developing-a-composite-windows-forms-control"></a><span data-ttu-id="52a0c-102">Développement d'un contrôle Windows Forms composite</span><span class="sxs-lookup"><span data-stu-id="52a0c-102">Developing a Composite Windows Forms Control</span></span>
<span data-ttu-id="52a0c-103">Vous pouvez développer un contrôle Windows Forms composite en combinant d'autres contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="52a0c-103">You can develop a composite Windows Forms control by combining other Windows Forms controls.</span></span> <span data-ttu-id="52a0c-104">Les contrôles composites qui dérivent <xref:System.Web.UI.UserControl> sont appelés contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52a0c-104">Composite controls that derive from <xref:System.Web.UI.UserControl> are called user controls.</span></span> <span data-ttu-id="52a0c-105">La classe de base, <xref:System.Windows.Forms.UserControl>, fournit le routage clavier pour les contrôles enfants, ce qui permet de garantir que les contrôles enfants peuvent recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="52a0c-105">The base class, <xref:System.Windows.Forms.UserControl>, provides keyboard routing for the child controls, thus ensuring that child controls can receive focus.</span></span> <span data-ttu-id="52a0c-106">Pour obtenir un exemple d’un contrôle utilisateur, consultez le <xref:System.Windows.Forms.UserControl> exemple [Comment : appliquer des attributs dans les contrôles Windows Forms](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md).</span><span class="sxs-lookup"><span data-stu-id="52a0c-106">For an example of a user control, see the <xref:System.Windows.Forms.UserControl> sample in [How to: Apply Attributes in Windows Forms Controls](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md).</span></span>  
  
 <span data-ttu-id="52a0c-107">Le Concepteur Windows Forms dans [!INCLUDE[vsprvsext](../../../../includes/vsprvsext-md.md)] fournit une prise en charge enrichie au moment du design pour la création de contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52a0c-107">The Windows Forms designer in [!INCLUDE[vsprvsext](../../../../includes/vsprvsext-md.md)] provides rich design-time support for authoring user controls.</span></span>  
  
-   <span data-ttu-id="52a0c-108">[Comment : afficher un contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils](https://msdn.microsoft.com/library/9yxtkx75\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-108">[How to: Display a Control in the Choose Toolbox Items Dialog Box](https://msdn.microsoft.com/library/9yxtkx75\(v=vs.110\))</span></span>  
  
-   [<span data-ttu-id="52a0c-109">Procédure pas à pas : sérialisation des collections de types standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="52a0c-109">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)  
  
-   <span data-ttu-id="52a0c-110">[Procédure pas à pas : héritage d’un contrôle Windows Forms à l’aide de Visual C#](https://msdn.microsoft.com/library/09476da0-8d4c-4a4c-b969-649519dfb438))</span><span class="sxs-lookup"><span data-stu-id="52a0c-110">[Walkthrough: Inheriting from a Windows Forms Control with Visual C#](https://msdn.microsoft.com/library/09476da0-8d4c-4a4c-b969-649519dfb438))</span></span>  
  
-   <span data-ttu-id="52a0c-111">[Comment : fournir une bitmap pour un contrôle en vue de l'afficher dans la boîte à outils](https://msdn.microsoft.com/library/4wk1wc0a\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-111">[How to: Provide a Toolbox Bitmap for a Control](https://msdn.microsoft.com/library/4wk1wc0a\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-112">[Guide pratique pour hériter de contrôles Windows Forms existants](https://msdn.microsoft.com/library/7h62478z\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-112">[How to: Inherit from Existing Windows Forms Controls](https://msdn.microsoft.com/library/7h62478z\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-113">[Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design](https://msdn.microsoft.com/library/5ytx0z24\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-113">[Walkthrough: Debugging Custom Windows Forms Controls at Design Time](https://msdn.microsoft.com/library/5ytx0z24\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-114">[Guide pratique pour hériter de la classe du contrôle](https://msdn.microsoft.com/library/skcysbt2\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-114">[How to: Inherit from the Control Class](https://msdn.microsoft.com/library/skcysbt2\(v=vs.110\))</span></span>  
  
-   [<span data-ttu-id="52a0c-115">Guide pratique pour tester le comportement d'un UserControl au moment de l'exécution</span><span class="sxs-lookup"><span data-stu-id="52a0c-115">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
  
-   <span data-ttu-id="52a0c-116">[Guide pratique pour aligner un contrôle sur les bords des formulaires au moment du design](https://msdn.microsoft.com/library/1fxyb15b\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-116">[How to: Align a Control to the Edges of Forms at Design Time](https://msdn.microsoft.com/library/1fxyb15b\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-117">[Comment : hériter de la classe UserControl](https://msdn.microsoft.com/library/00ctb4z0\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-117">[How to: Inherit from the UserControl Class](https://msdn.microsoft.com/library/00ctb4z0\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-118">[Guide pratique pour créer des contrôles pour des Windows Forms](https://msdn.microsoft.com/library/bs3yhkh7\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-118">[How to: Author Controls for Windows Forms](https://msdn.microsoft.com/library/bs3yhkh7\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-119">[Guide pratique pour créer des contrôles composites](https://msdn.microsoft.com/library/3sf86w5h\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-119">[How to: Author Composite Controls](https://msdn.microsoft.com/library/3sf86w5h\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-120">[Procédure pas à pas : création d'un contrôle composite à l'aide de Visual Basic](https://msdn.microsoft.com/library/c316f119\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-120">[Walkthrough: Authoring a Composite Control with Visual Basic](https://msdn.microsoft.com/library/c316f119\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-121">[Procédure pas à pas : création d’un contrôle composite à l’aide de Visual C#](https://msdn.microsoft.com/library/f88481a8-c746-4a36-9479-374ce5f2e91f))</span><span class="sxs-lookup"><span data-stu-id="52a0c-121">[Walkthrough: Authoring a Composite Control with Visual C#](https://msdn.microsoft.com/library/f88481a8-c746-4a36-9479-374ce5f2e91f))</span></span>  
  
-   <span data-ttu-id="52a0c-122">[Procédure pas à pas : héritage à partir d’un contrôle Windows Forms à l’aide de Visual Basic](https://msdn.microsoft.com/library/w2a8y03d\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-122">[Walkthrough: Inheriting from a Windows Forms Control with Visual Basic](https://msdn.microsoft.com/library/w2a8y03d\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-123">[Guide pratique pour créer un contrôle Windows Forms qui bénéficie des fonctionnalités au moment du design](https://msdn.microsoft.com/library/307hck25\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-123">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://msdn.microsoft.com/library/307hck25\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="52a0c-124">[Comment : créer un contrôle Windows Forms qui bénéficie des fonctionnalités au moment du design](https://msdn.microsoft.com/library/307hck25\(v=vs.120\))</span><span class="sxs-lookup"><span data-stu-id="52a0c-124">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://msdn.microsoft.com/library/307hck25\(v=vs.120\))</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52a0c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52a0c-125">See Also</span></span>  
 [<span data-ttu-id="52a0c-126">Guide pratique pour appliquer des attributs dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="52a0c-126">How to: Apply Attributes in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md)  
 [<span data-ttu-id="52a0c-127">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="52a0c-127">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)  
 [<span data-ttu-id="52a0c-128">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="52a0c-128">Varieties of Custom Controls</span></span>](../../../../docs/framework/winforms/controls/varieties-of-custom-controls.md)
