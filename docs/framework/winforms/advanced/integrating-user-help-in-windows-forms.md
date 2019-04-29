---
title: Intégration de l'aide d'utilisateur dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Help [Windows Forms], Windows Forms (using designer)
- Windows Forms, Help (using designer)
- HTML Help [Windows Forms], Windows Forms (using designer)
- Help [Windows Forms], Windows applications (using designer)
- forms. Help (using designer)
- Windows applications [Windows Forms], Help (using designer)
ms.assetid: a8563d25-8a75-4bc7-a024-f1870591b50f
ms.openlocfilehash: 207ceeafa2ea06340310577c636deb5ea1977aae
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61942920"
---
# <a name="integrating-user-help-in-windows-forms"></a><span data-ttu-id="9456e-102">Intégration de l'aide d'utilisateur dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9456e-102">Integrating User Help in Windows Forms</span></span>
<span data-ttu-id="9456e-103">Un aspect essentiel mais souvent négligé, de la création d’applications basées sur Windows est le système d’aide, car cela est où les utilisateurs pour obtenir une assistance fois de confusion.</span><span class="sxs-lookup"><span data-stu-id="9456e-103">An essential, but often overlooked, aspect of building Windows-based applications is the Help system, as this is where users turn for assistance in times of confusion.</span></span> <span data-ttu-id="9456e-104">Windows Forms prend en charge deux types différents d’aide, fourni par le [du composant HelpProvider](../controls/helpprovider-component-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="9456e-104">Windows Forms support two different types of Help, each provided by the [HelpProvider Component](../controls/helpprovider-component-windows-forms.md).</span></span> <span data-ttu-id="9456e-105">La première implique l’orientation de l’utilisateur à un fichier d’aide de code HTML ou HTML Help 1. *x* format ou ultérieur.</span><span class="sxs-lookup"><span data-stu-id="9456e-105">The first involves pointing the user to a Help file of either HTML or HTML Help 1.*x* or greater format.</span></span> <span data-ttu-id="9456e-106">Le second peut afficher brève « Qu’est-ce »-tapez Help sur chacun des contrôles. Cela est particulièrement utile sur les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9456e-106">The second can display brief "What's This"-type Help on individual controls; this is especially useful on dialog boxes.</span></span> <span data-ttu-id="9456e-107">Les deux types d’aide peuvent être utilisés sur le même formulaire.</span><span class="sxs-lookup"><span data-stu-id="9456e-107">Both types of Help can be used on the same form.</span></span>  
  
 <span data-ttu-id="9456e-108">En outre, le [composant ToolTip](../controls/tooltip-component-windows-forms.md) peut être utilisé pour fournir une aide individuelle pour les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9456e-108">Additionally, the [ToolTip Component](../controls/tooltip-component-windows-forms.md) can be used to provide individual Help for controls on Windows Forms.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9456e-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9456e-109">In This Section</span></span>  
 [<span data-ttu-id="9456e-110">Guide pratique pour Fournir une aide dans une Application Windows</span><span class="sxs-lookup"><span data-stu-id="9456e-110">How to: Provide Help in a Windows Application</span></span>](how-to-provide-help-in-a-windows-application.md)  
 <span data-ttu-id="9456e-111">Explique comment utiliser le `HelpProvider` composant pour lier des contrôles aux fichiers dans un système d’aide.</span><span class="sxs-lookup"><span data-stu-id="9456e-111">Explains how to use the `HelpProvider` component to link controls to files in a Help system.</span></span>  
  
 [<span data-ttu-id="9456e-112">Guide pratique pour Afficher l’aide contextuelle</span><span class="sxs-lookup"><span data-stu-id="9456e-112">How to: Display Pop-up Help</span></span>](how-to-display-pop-up-help.md)  
 <span data-ttu-id="9456e-113">Explique comment utiliser le `HelpProvider` composant pour afficher l’aide contextuelle dans les Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9456e-113">Explains how to use the `HelpProvider` component to show pop-up Help on Windows Forms.</span></span>  
  
 [<span data-ttu-id="9456e-114">Affichage sous forme d’info-bulles de l’aide relative aux contrôles</span><span class="sxs-lookup"><span data-stu-id="9456e-114">Control Help Using ToolTips</span></span>](control-help-using-tooltips.md)  
 <span data-ttu-id="9456e-115">Décrit l’utilisation de la `ToolTip` composant pour afficher l’aide spécifique du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9456e-115">Describes using the `ToolTip` component to show control-specific Help.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="9456e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9456e-116">Related Sections</span></span>  
 [<span data-ttu-id="9456e-117">HelpProvider, composant</span><span class="sxs-lookup"><span data-stu-id="9456e-117">HelpProvider Component</span></span>](../controls/helpprovider-component-windows-forms.md)  
 <span data-ttu-id="9456e-118">Explique les principes fondamentaux de la `HelpProvider` composant.</span><span class="sxs-lookup"><span data-stu-id="9456e-118">Explains the basics of the `HelpProvider` component.</span></span>  
  
 [<span data-ttu-id="9456e-119">ToolTip, composant</span><span class="sxs-lookup"><span data-stu-id="9456e-119">ToolTip Component</span></span>](../controls/tooltip-component-windows-forms.md)  
 <span data-ttu-id="9456e-120">Explique les principes fondamentaux de la `ToolTip` composant.</span><span class="sxs-lookup"><span data-stu-id="9456e-120">Explains the basics of the `ToolTip` component.</span></span>  
  
 [<span data-ttu-id="9456e-121">Vue d'ensemble des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9456e-121">Windows Forms Overview</span></span>](../windows-forms-overview.md)  
 <span data-ttu-id="9456e-122">Explique les principes fondamentaux de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9456e-122">Explains the basics of Windows Forms.</span></span>  
  
 [<span data-ttu-id="9456e-123">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9456e-123">Windows Forms</span></span>](../index.md)  
 <span data-ttu-id="9456e-124">Fournit une vue d’ensemble des Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9456e-124">Provides an overview of Windows Forms.</span></span>
