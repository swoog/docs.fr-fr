---
title: Peinture et rendu personnalisés des contrôles
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], rendering
- custom controls [Windows Forms], painting
- user controls [Windows Forms], painting
ms.assetid: a09dbf76-0966-4cbf-a66a-2083ba98e068
ms.openlocfilehash: ec9002ffa4a7e2c82f59d52344764a01afe4c568
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011482"
---
# <a name="custom-control-painting-and-rendering"></a><span data-ttu-id="e859a-102">Peinture et rendu personnalisés des contrôles</span><span class="sxs-lookup"><span data-stu-id="e859a-102">Custom Control Painting and Rendering</span></span>
<span data-ttu-id="e859a-103">La peinture personnalisée des contrôles est une des nombreuses tâches complexes facilitées par le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e859a-103">Custom painting of controls is one of the many complicated tasks made easy by the .NET Framework.</span></span> <span data-ttu-id="e859a-104">Lorsque vous créez un contrôle personnalisé, vous disposez de nombreuses options concernant l’aspect graphique de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="e859a-104">When authoring a custom control, you have many options regarding your control's graphical appearance.</span></span> <span data-ttu-id="e859a-105">Si vous créez un contrôle qui hérite de la `Control`, vous devez fournir du code qui permet à votre contrôle afficher sa représentation sous forme graphique.</span><span class="sxs-lookup"><span data-stu-id="e859a-105">If you are authoring a control that inherits from the `Control`, you must provide code that allows your control to render its graphical representation.</span></span> <span data-ttu-id="e859a-106">Si vous créez un contrôle utilisateur en héritant de la `UserControl`, ou à partir d’un des contrôles Windows Forms, vous pouvez substituer la représentation graphique standard et fournir votre propre code graphique.</span><span class="sxs-lookup"><span data-stu-id="e859a-106">If you are creating a user control by inheriting from the `UserControl`, or are inheriting from one of the Windows Forms controls, you may override the standard graphical representation and provide your own graphics code.</span></span> <span data-ttu-id="e859a-107">Si vous souhaitez fournir un rendu personnalisé pour les contrôles constitutifs d’un `UserControl` vous créez, vos options sont plus limitées, tout en autorisant un large éventail de possibilités de graphiques pour vos applications et de contrôles.</span><span class="sxs-lookup"><span data-stu-id="e859a-107">If you want to provide custom rendering for the constituent controls of a `UserControl` you are authoring, your options become more limited, but still allow a wide range of graphical possibilities for your controls and applications.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e859a-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e859a-108">In This Section</span></span>  
 [<span data-ttu-id="e859a-109">Rendu d'un contrôle Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e859a-109">Rendering a Windows Forms Control</span></span>](rendering-a-windows-forms-control.md)  
 <span data-ttu-id="e859a-110">Montre comment programmer la logique qui affiche un contrôle.</span><span class="sxs-lookup"><span data-stu-id="e859a-110">Shows how to program the logic that displays a control.</span></span>  
  
 [<span data-ttu-id="e859a-111">Contrôles dessinés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e859a-111">User-Drawn Controls</span></span>](user-drawn-controls.md)  
 <span data-ttu-id="e859a-112">Donne une vue d’ensemble des étapes impliquées dans l’écriture et en remplaçant le code de rendu de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="e859a-112">Gives an overview of the steps involved in writing and overriding rendering code for your control.</span></span>  
  
 [<span data-ttu-id="e859a-113">Contrôles constitutifs</span><span class="sxs-lookup"><span data-stu-id="e859a-113">Constituent Controls</span></span>](constituent-controls.md)  
 <span data-ttu-id="e859a-114">Décrit comment implémenter le code de rendu personnalisées pour des contrôles constitutifs dans vos formulaires et contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e859a-114">Describes how to implement custom rendering code for constituent controls in your user controls and forms.</span></span>  
  
 [<span data-ttu-id="e859a-115">Guide pratique pour Rendre votre contrôle Invisible au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="e859a-115">How to: Make Your Control Invisible at Run Time</span></span>](how-to-make-your-control-invisible-at-run-time.md)  
 <span data-ttu-id="e859a-116">Montre comment utiliser le <xref:System.Windows.Forms.Control.Visible%2A> propriété à masquer et afficher un contrôle.</span><span class="sxs-lookup"><span data-stu-id="e859a-116">Shows how to use the <xref:System.Windows.Forms.Control.Visible%2A> property to hide and show a control.</span></span>  
  
 [<span data-ttu-id="e859a-117">Guide pratique pour Affecter un arrière-plan Transparent à votre contrôle</span><span class="sxs-lookup"><span data-stu-id="e859a-117">How to: Give Your Control a Transparent Background</span></span>](how-to-give-your-control-a-transparent-background.md)  
 <span data-ttu-id="e859a-118">Montre comment utiliser le <xref:System.Windows.Forms.Control.SetStyle%2A> méthode pour créer une couleur d’arrière-plan qui est opaque, transparente ou partiellement transparents.</span><span class="sxs-lookup"><span data-stu-id="e859a-118">Shows how to use the <xref:System.Windows.Forms.Control.SetStyle%2A> method to create a background color that is opaque, transparent, or partially transparent.</span></span>  
  
 [<span data-ttu-id="e859a-119">Rendu des contrôles avec les styles visuels</span><span class="sxs-lookup"><span data-stu-id="e859a-119">Rendering Controls with Visual Styles</span></span>](rendering-controls-with-visual-styles.md)  
 <span data-ttu-id="e859a-120">Montre comment restituer les contrôles à l’aide de styles visuels dans les systèmes d’exploitation qui les prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="e859a-120">Shows how to render controls using visual styles in operating systems that support them.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="e859a-121">Référence</span><span class="sxs-lookup"><span data-stu-id="e859a-121">Reference</span></span>  
 <xref:System.Windows.Forms.Control>  
 <span data-ttu-id="e859a-122">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="e859a-122">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.UserControl>  
 <span data-ttu-id="e859a-123">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="e859a-123">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.Control.OnPaint%2A>  
 <span data-ttu-id="e859a-124">Décrit cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e859a-124">Describes this method.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="e859a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e859a-125">Related Sections</span></span>  
 [<span data-ttu-id="e859a-126">Guide pratique pour Créer des objets graphiques pour le dessin</span><span class="sxs-lookup"><span data-stu-id="e859a-126">How to: Create Graphics Objects for Drawing</span></span>](../advanced/how-to-create-graphics-objects-for-drawing.md)  
 <span data-ttu-id="e859a-127">Introduit [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] fonctionnalités graphiques à partir d’un point de vue et donne de liens Visual Studio pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e859a-127">Introduces [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] graphics functionality from a Visual Studio perspective and gives links to more information.</span></span>  
  
 [<span data-ttu-id="e859a-128">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="e859a-128">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)  
 <span data-ttu-id="e859a-129">Décrit les types de contrôles personnalisés que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="e859a-129">Describes the kinds of custom controls you can author.</span></span>
