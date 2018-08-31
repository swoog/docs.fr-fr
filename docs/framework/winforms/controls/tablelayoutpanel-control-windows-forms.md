---
title: TableLayoutPanel, contrôle (Windows Forms)
ms.date: 03/30/2017
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- layout [Windows Forms]
- controls [Windows Forms], sizing
- sizing [Windows Forms], automatic
- layout [Windows Forms], TableLayoutPanel control
- automatic sizing
ms.assetid: f55175c6-424e-4782-a86e-3f79c1550235
ms.openlocfilehash: 671553b496520f2c2ac3fea90b1514a6cdf1764a
ms.sourcegitcommit: a368166a51e5204c0224fbf5e46476e3ed122817
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "43331759"
---
# <a name="tablelayoutpanel-control-windows-forms"></a><span data-ttu-id="96f6a-102">TableLayoutPanel, contrôle (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="96f6a-102">TableLayoutPanel Control (Windows Forms)</span></span>
<span data-ttu-id="96f6a-103">Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> réorganise son contenu dans une grille.</span><span class="sxs-lookup"><span data-stu-id="96f6a-103">The <xref:System.Windows.Forms.TableLayoutPanel> control arranges its contents in a grid.</span></span> <span data-ttu-id="96f6a-104">La disposition étant effectuée au moment du design et au moment de l'exécution, elle peut changer dynamiquement quand l'environnement d'application change.</span><span class="sxs-lookup"><span data-stu-id="96f6a-104">Because the layout is performed both at design time and run time, it can change dynamically as the application environment changes.</span></span> <span data-ttu-id="96f6a-105">Cela permet de redimensionner proportionnellement les contrôles du panneau, pour pouvoir répondre à des modifications telles que le redimensionnement du contrôle parent ou le changement de longueur de texte en raison de la localisation.</span><span class="sxs-lookup"><span data-stu-id="96f6a-105">This gives the controls in the panel the ability to proportionally resize, so it can respond to changes such as the parent control resizing or text length changing due to localization.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="96f6a-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="96f6a-106">In This Section</span></span>  
 [<span data-ttu-id="96f6a-107">Vue d’ensemble du contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-107">TableLayoutPanel Control Overview</span></span>](../../../../docs/framework/winforms/controls/tablelayoutpanel-control-overview.md)  
 <span data-ttu-id="96f6a-108">Présente les concepts généraux du contrôle <xref:System.Windows.Forms.TableLayoutPanel>, ce qui vous permet de créer une disposition avec des lignes et des colonnes.</span><span class="sxs-lookup"><span data-stu-id="96f6a-108">Introduces the general concepts of the <xref:System.Windows.Forms.TableLayoutPanel> control, which allows you to create a layout with rows and columns.</span></span>  
  
 [<span data-ttu-id="96f6a-109">Meilleures pratiques pour le contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-109">Best Practices for the TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/best-practices-for-the-tablelayoutpanel-control.md)  
 <span data-ttu-id="96f6a-110">Fournit des recommandations pour vous aider à tirer le meilleur parti des fonctionnalités de disposition du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="96f6a-110">Outlines recommendations to help you get the most out of the layout features of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>  
  
 [<span data-ttu-id="96f6a-111">Comportement du redimensionnement automatique dans le contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-111">AutoSize Behavior in the TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/autosize-behavior-in-the-tablelayoutpanel-control.md)  
 <span data-ttu-id="96f6a-112">Explique la manière dont le contrôle <xref:System.Windows.Forms.TableLayoutPanel> prend en charge le comportement de dimensionnement automatique.</span><span class="sxs-lookup"><span data-stu-id="96f6a-112">Explains the ways in which the <xref:System.Windows.Forms.TableLayoutPanel> control supports automatic sizing behavior.</span></span>  
  
 [<span data-ttu-id="96f6a-113">Guide pratique pour ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-113">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 <span data-ttu-id="96f6a-114">Montre comment ancrer des contrôles enfants dans un contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="96f6a-114">Shows how to anchor and dock child controls in a <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>  
  
 [<span data-ttu-id="96f6a-115">Guide pratique pour créer une présentation Windows Forms qui répond bien à la localisation</span><span class="sxs-lookup"><span data-stu-id="96f6a-115">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>](../../../../docs/framework/winforms/controls/how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)  
 <span data-ttu-id="96f6a-116">Montre comment utiliser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour créer un formulaire qui réponde bien à la localisation.</span><span class="sxs-lookup"><span data-stu-id="96f6a-116">Demonstrates using a <xref:System.Windows.Forms.TableLayoutPanel> control to build a form that responds well to localization.</span></span>  
  
 [<span data-ttu-id="96f6a-117">Guide pratique pour créer un Windows Form redimensionnable pour l'entrée de données</span><span class="sxs-lookup"><span data-stu-id="96f6a-117">How to: Create a Resizable Windows Form for Data Entry</span></span>](../../../../docs/framework/winforms/controls/how-to-create-a-resizable-windows-form-for-data-entry.md)  
 <span data-ttu-id="96f6a-118">Montre comment utiliser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour créer un formulaire qui réponde bien au redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="96f6a-118">Demonstrates using a <xref:System.Windows.Forms.TableLayoutPanel> control to build a form that responds well to resizing.</span></span>  
  
1.  [<span data-ttu-id="96f6a-119">Comment : aligner et étirer un contrôle dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-119">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [<span data-ttu-id="96f6a-120">Comment : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-120">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
3.  [<span data-ttu-id="96f6a-121">Comment : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="96f6a-121">How to: Edit Columns and Rows in a TableLayoutPanel Control</span></span>](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
4.  <span data-ttu-id="96f6a-122">[Procédure pas à pas : organisation des contrôles dans les Windows Forms à l’aide d’un TableLayoutPanel](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="96f6a-122">[Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))</span></span>  
  
## <a name="reference"></a><span data-ttu-id="96f6a-123">Référence</span><span class="sxs-lookup"><span data-stu-id="96f6a-123">Reference</span></span>  
 <xref:System.Windows.Forms.TableLayoutPanel>  
 <span data-ttu-id="96f6a-124">Fournit la documentation de référence pour le contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="96f6a-124">Provides reference documentation for the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>  
  
 <xref:System.Windows.Forms.TableLayoutSettings>  
 <span data-ttu-id="96f6a-125">Fournit une documentation de référence pour le type <xref:System.Windows.Forms.TableLayoutSettings>.</span><span class="sxs-lookup"><span data-stu-id="96f6a-125">Provides reference documentation for the <xref:System.Windows.Forms.TableLayoutSettings> type.</span></span>  
  
 <xref:System.Windows.Forms.FlowLayoutPanel>  
 <span data-ttu-id="96f6a-126">Fournit la documentation de référence pour le contrôle <xref:System.Windows.Forms.FlowLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="96f6a-126">Provides reference documentation for the <xref:System.Windows.Forms.FlowLayoutPanel> control.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="96f6a-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96f6a-127">Related Sections</span></span>  
 [<span data-ttu-id="96f6a-128">Localisation</span><span class="sxs-lookup"><span data-stu-id="96f6a-128">Localization</span></span>](../../../../docs/standard/globalization-localization/localization.md)  
 <span data-ttu-id="96f6a-129">Fournit une vue d'ensemble des rubriques relatives à la localisation.</span><span class="sxs-lookup"><span data-stu-id="96f6a-129">Provides an overview of topics relating to localization.</span></span>  
  
 <span data-ttu-id="96f6a-130">Consultez également [Localizing Applications](https://msdn.microsoft.com/library/z68135h5\(v=vs.110\)) ou [localisation d’Applications](https://msdn.microsoft.com/library/z68135h5\(v=vs.120\))</span><span class="sxs-lookup"><span data-stu-id="96f6a-130">Also see [Localizing Applications](https://msdn.microsoft.com/library/z68135h5\(v=vs.110\)) or [Localizing Applications](https://msdn.microsoft.com/library/z68135h5\(v=vs.120\))</span></span>
