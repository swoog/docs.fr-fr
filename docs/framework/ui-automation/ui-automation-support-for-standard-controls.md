---
title: Prise en charge d'UI Automation pour les contrôles standard
ms.date: 03/30/2017
helpviewer_keywords:
- controls, UI Automation support for
- UI Automation, support for standard controls
ms.assetid: 3770ea8a-2655-4add-9c59-fe0610ad5084
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: cbfb640a068a2c1178d321480ee3a112db07b6ac
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519987"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="1cfd2-102">Prise en charge d'UI Automation pour les contrôles standard</span><span class="sxs-lookup"><span data-stu-id="1cfd2-102">UI Automation Support for Standard Controls</span></span>
> [!NOTE]
>  <span data-ttu-id="1cfd2-103">Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="1cfd2-104">Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="1cfd2-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="1cfd2-105">Cette rubrique contient des informations sur la prise en charge d’ [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] pour les contrôles standard dans les applications développées pour les infrastructures [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)]et [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="1cfd2-105">This topic contains information about [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] support for standard controls in applications developed for the [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)], and [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] frameworks.</span></span>  
  
<a name="Windows_Presentation_Foundation_Controls"></a>   
## <a name="windows-presentation-foundation-controls"></a><span data-ttu-id="1cfd2-106">Contrôles Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="1cfd2-106">Windows Presentation Foundation Controls</span></span>  
 <span data-ttu-id="1cfd2-107">Tous les éléments du contrôle [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] qui fournissent des informations ou une prise en charge pour l’interaction utilisateur disposent d’une prise en charge native complète de [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span><span class="sxs-lookup"><span data-stu-id="1cfd2-107">All [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] control elements that provide information or support for user interaction have full native support for [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="1cfd2-108">D’autres éléments, tels que les panneaux, ne sont pas visibles par [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span><span class="sxs-lookup"><span data-stu-id="1cfd2-108">Other elements, such as panels, are not visible to [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span>  
  
<a name="Win32_Controls"></a>   
## <a name="win32-controls"></a><span data-ttu-id="1cfd2-109">Contrôles Win32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-109">Win32 Controls</span></span>  
 <span data-ttu-id="1cfd2-110">La plupart des contrôles [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] sont exposés à [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] via des fournisseurs côté client dans UIAutomationClientsideProviders.dll.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-110">Most [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="1cfd2-111">Cet assembly est inscrit automatiquement pour être utilisé avec les applications clientes UI Automation.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-111">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="1cfd2-112">La prise en charge complète n’est fournie que pour les contrôles de la version 6 de ComCtrl32.dll (disponible avec [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] et les versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="1cfd2-112">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] and later).</span></span>  
  
 <span data-ttu-id="1cfd2-113">Les contrôles suivants sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-113">The following controls are supported.</span></span>  
  
|<span data-ttu-id="1cfd2-114">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="1cfd2-114">Class name</span></span>|<span data-ttu-id="1cfd2-115">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-115">Control Type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="1cfd2-116">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-116">Button</span></span>|<span data-ttu-id="1cfd2-117">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-117">Button</span></span>|  
|<span data-ttu-id="1cfd2-118">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-118">Button</span></span>|<span data-ttu-id="1cfd2-119">RadioButton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-119">RadioButton</span></span>|  
|<span data-ttu-id="1cfd2-120">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-120">Button</span></span>|<span data-ttu-id="1cfd2-121">Regrouper</span><span class="sxs-lookup"><span data-stu-id="1cfd2-121">Group</span></span>|  
|<span data-ttu-id="1cfd2-122">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-122">Button</span></span>|<span data-ttu-id="1cfd2-123">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="1cfd2-123">CheckBox</span></span>|  
|<span data-ttu-id="1cfd2-124">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-124">Button</span></span>|<span data-ttu-id="1cfd2-125">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="1cfd2-125">Hyperlink</span></span>|  
|<span data-ttu-id="1cfd2-126">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-126">Button</span></span>|<span data-ttu-id="1cfd2-127">SplitButton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-127">SplitButton</span></span>|  
|<span data-ttu-id="1cfd2-128">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-128">Button</span></span>|<span data-ttu-id="1cfd2-129">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="1cfd2-129">CheckBox</span></span>|  
|<span data-ttu-id="1cfd2-130">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-130">ComboBoxEx32</span></span>|<span data-ttu-id="1cfd2-131">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-131">ComboBox</span></span>|  
|<span data-ttu-id="1cfd2-132">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-132">ComboBox</span></span>|<span data-ttu-id="1cfd2-133">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-133">ComboBox</span></span>|  
|<span data-ttu-id="1cfd2-134">Modifier</span><span class="sxs-lookup"><span data-stu-id="1cfd2-134">Edit</span></span>|<span data-ttu-id="1cfd2-135">Document</span><span class="sxs-lookup"><span data-stu-id="1cfd2-135">Document</span></span>|  
|<span data-ttu-id="1cfd2-136">Modifier</span><span class="sxs-lookup"><span data-stu-id="1cfd2-136">Edit</span></span>|<span data-ttu-id="1cfd2-137">Modifier</span><span class="sxs-lookup"><span data-stu-id="1cfd2-137">Edit</span></span>|  
|<span data-ttu-id="1cfd2-138">SysLink</span><span class="sxs-lookup"><span data-stu-id="1cfd2-138">SysLink</span></span>|<span data-ttu-id="1cfd2-139">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="1cfd2-139">Hyperlink</span></span>|  
|<span data-ttu-id="1cfd2-140">Statique</span><span class="sxs-lookup"><span data-stu-id="1cfd2-140">Static</span></span>|<span data-ttu-id="1cfd2-141">Texte</span><span class="sxs-lookup"><span data-stu-id="1cfd2-141">Text</span></span>|  
|<span data-ttu-id="1cfd2-142">Statique</span><span class="sxs-lookup"><span data-stu-id="1cfd2-142">Static</span></span>|<span data-ttu-id="1cfd2-143">Image</span><span class="sxs-lookup"><span data-stu-id="1cfd2-143">Image</span></span>|  
|<span data-ttu-id="1cfd2-144">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-144">SysIPAddress32</span></span>|<span data-ttu-id="1cfd2-145">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="1cfd2-145">Custom</span></span>|  
|<span data-ttu-id="1cfd2-146">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-146">SysHeader32</span></span>|<span data-ttu-id="1cfd2-147">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="1cfd2-147">Header/HeaderItem</span></span>|  
|<span data-ttu-id="1cfd2-148">SysListView32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-148">SysListView32</span></span>|<span data-ttu-id="1cfd2-149">DataGrid</span><span class="sxs-lookup"><span data-stu-id="1cfd2-149">DataGrid</span></span>|  
|<span data-ttu-id="1cfd2-150">SysListView32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-150">SysListView32</span></span>|<span data-ttu-id="1cfd2-151">Liste</span><span class="sxs-lookup"><span data-stu-id="1cfd2-151">List</span></span>|  
|<span data-ttu-id="1cfd2-152">ListBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-152">ListBox</span></span>|<span data-ttu-id="1cfd2-153">Liste</span><span class="sxs-lookup"><span data-stu-id="1cfd2-153">List</span></span>|  
|<span data-ttu-id="1cfd2-154">ListBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-154">ListBox</span></span>|<span data-ttu-id="1cfd2-155">ListItem</span><span class="sxs-lookup"><span data-stu-id="1cfd2-155">ListItem</span></span>|  
|<span data-ttu-id="1cfd2-156">#32768</span><span class="sxs-lookup"><span data-stu-id="1cfd2-156">#32768</span></span>|<span data-ttu-id="1cfd2-157">Menu</span><span class="sxs-lookup"><span data-stu-id="1cfd2-157">Menu</span></span>|  
|<span data-ttu-id="1cfd2-158">#32768</span><span class="sxs-lookup"><span data-stu-id="1cfd2-158">#32768</span></span>|<span data-ttu-id="1cfd2-159">MenuItem</span><span class="sxs-lookup"><span data-stu-id="1cfd2-159">MenuItem</span></span>|  
|<span data-ttu-id="1cfd2-160">msctls_progress32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-160">msctls_progress32</span></span>|<span data-ttu-id="1cfd2-161">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="1cfd2-161">ProgressBar</span></span>|  
|<span data-ttu-id="1cfd2-162">RichEdit</span><span class="sxs-lookup"><span data-stu-id="1cfd2-162">RichEdit</span></span>|<span data-ttu-id="1cfd2-163">Document.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-163">Document.</span></span> <span data-ttu-id="1cfd2-164">Consultez la remarque.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-164">See note.</span></span>|  
|<span data-ttu-id="1cfd2-165">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="1cfd2-165">RichEdit20A</span></span>|<span data-ttu-id="1cfd2-166">Document</span><span class="sxs-lookup"><span data-stu-id="1cfd2-166">Document</span></span>|  
|<span data-ttu-id="1cfd2-167">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="1cfd2-167">RichEdit20W</span></span>|<span data-ttu-id="1cfd2-168">Document</span><span class="sxs-lookup"><span data-stu-id="1cfd2-168">Document</span></span>|  
|<span data-ttu-id="1cfd2-169">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="1cfd2-169">RichEdit50W</span></span>|<span data-ttu-id="1cfd2-170">Document</span><span class="sxs-lookup"><span data-stu-id="1cfd2-170">Document</span></span>|  
|<span data-ttu-id="1cfd2-171">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-171">ScrollBar</span></span>|<span data-ttu-id="1cfd2-172">Curseur</span><span class="sxs-lookup"><span data-stu-id="1cfd2-172">Slider</span></span>|  
|<span data-ttu-id="1cfd2-173">msctls_trackbar32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-173">msctls_trackbar32</span></span>|<span data-ttu-id="1cfd2-174">Curseur</span><span class="sxs-lookup"><span data-stu-id="1cfd2-174">Slider</span></span>|  
|<span data-ttu-id="1cfd2-175">msctls_updown32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-175">msctls_updown32</span></span>|<span data-ttu-id="1cfd2-176">Spinner</span><span class="sxs-lookup"><span data-stu-id="1cfd2-176">Spinner</span></span>|  
|<span data-ttu-id="1cfd2-177">msctls_statusbar32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-177">msctls_statusbar32</span></span>|<span data-ttu-id="1cfd2-178">StatusBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-178">StatusBar</span></span>|  
|<span data-ttu-id="1cfd2-179">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-179">SysTabControl32</span></span>|<span data-ttu-id="1cfd2-180">Onglet</span><span class="sxs-lookup"><span data-stu-id="1cfd2-180">Tab</span></span>|  
|<span data-ttu-id="1cfd2-181">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-181">SysTabControl32</span></span>|<span data-ttu-id="1cfd2-182">TabItem</span><span class="sxs-lookup"><span data-stu-id="1cfd2-182">TabItem</span></span>|  
|<span data-ttu-id="1cfd2-183">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-183">ToolbarWindow32</span></span>|<span data-ttu-id="1cfd2-184">ToolBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-184">ToolBar</span></span>|  
|<span data-ttu-id="1cfd2-185">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-185">ToolbarWindow32</span></span>|<span data-ttu-id="1cfd2-186">MenuItem</span><span class="sxs-lookup"><span data-stu-id="1cfd2-186">MenuItem</span></span>|  
|<span data-ttu-id="1cfd2-187">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-187">ToolbarWindow32</span></span>|<span data-ttu-id="1cfd2-188">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-188">Button</span></span>|  
|<span data-ttu-id="1cfd2-189">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-189">ToolbarWindow32</span></span>|<span data-ttu-id="1cfd2-190">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="1cfd2-190">CheckBox</span></span>|  
|<span data-ttu-id="1cfd2-191">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-191">ToolbarWindow32</span></span>|<span data-ttu-id="1cfd2-192">RadioButton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-192">RadioButton</span></span>|  
|<span data-ttu-id="1cfd2-193">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-193">ToolbarWindow32</span></span>|<span data-ttu-id="1cfd2-194">Séparateur</span><span class="sxs-lookup"><span data-stu-id="1cfd2-194">Separator</span></span>|  
|<span data-ttu-id="1cfd2-195">tooltips_class32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-195">tooltips_class32</span></span>|<span data-ttu-id="1cfd2-196">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-196">ToolTip</span></span>|  
|<span data-ttu-id="1cfd2-197">#32774</span><span class="sxs-lookup"><span data-stu-id="1cfd2-197">#32774</span></span>|<span data-ttu-id="1cfd2-198">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-198">ToolTip</span></span>|  
|<span data-ttu-id="1cfd2-199">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-199">ReBarWindow32</span></span>|<span data-ttu-id="1cfd2-200">ToolBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-200">Toolbar</span></span>|  
|<span data-ttu-id="1cfd2-201">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-201">SysTreeView32</span></span>|<span data-ttu-id="1cfd2-202">Arborescence</span><span class="sxs-lookup"><span data-stu-id="1cfd2-202">Tree</span></span>|  
|<span data-ttu-id="1cfd2-203">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-203">SysTreeView32</span></span>|<span data-ttu-id="1cfd2-204">TreeItem</span><span class="sxs-lookup"><span data-stu-id="1cfd2-204">TreeItem</span></span>|  
  
 <span data-ttu-id="1cfd2-205">**Remarque** Le contrôle RichEdit est pris en charge uniquement pour les versions fournies avec [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] (dans RichEd20.dll version 3.1 et version ultérieure, ainsi que dans MsftEdit.dll version 4.1 et version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="1cfd2-205">**Note** The RichEdit control is supported only for versions shipped with [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>  
  
 <span data-ttu-id="1cfd2-206">Les contrôles suivants ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-206">The following controls are not supported.</span></span>  
  
|<span data-ttu-id="1cfd2-207">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="1cfd2-207">Class name</span></span>|<span data-ttu-id="1cfd2-208">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-208">Control type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="1cfd2-209">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-209">SysAnimate32</span></span>|<span data-ttu-id="1cfd2-210">Image</span><span class="sxs-lookup"><span data-stu-id="1cfd2-210">Image</span></span>|  
|<span data-ttu-id="1cfd2-211">SysPager</span><span class="sxs-lookup"><span data-stu-id="1cfd2-211">SysPager</span></span>|<span data-ttu-id="1cfd2-212">Spinner</span><span class="sxs-lookup"><span data-stu-id="1cfd2-212">Spinner</span></span>|  
|<span data-ttu-id="1cfd2-213">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-213">SysDateTimePick32</span></span>|<span data-ttu-id="1cfd2-214">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="1cfd2-214">Custom</span></span>|  
|<span data-ttu-id="1cfd2-215">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="1cfd2-215">SysMonthCal32</span></span>|<span data-ttu-id="1cfd2-216">Calendrier</span><span class="sxs-lookup"><span data-stu-id="1cfd2-216">Calendar</span></span>|  
|<span data-ttu-id="1cfd2-217">MS_WINNOTE</span><span class="sxs-lookup"><span data-stu-id="1cfd2-217">MS_WINNOTE</span></span>|<span data-ttu-id="1cfd2-218">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-218">Tooltip</span></span>|  
|<span data-ttu-id="1cfd2-219">VBBubble</span><span class="sxs-lookup"><span data-stu-id="1cfd2-219">VBBubble</span></span>|<span data-ttu-id="1cfd2-220">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-220">Tooltip</span></span>|  
|<span data-ttu-id="1cfd2-221">ScrollBar (quand il est utilisé comme contrôle autonome)</span><span class="sxs-lookup"><span data-stu-id="1cfd2-221">ScrollBar (when used as a standalone control)</span></span>|<span data-ttu-id="1cfd2-222">Curseur</span><span class="sxs-lookup"><span data-stu-id="1cfd2-222">Slider</span></span>|  
|<span data-ttu-id="1cfd2-223">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="1cfd2-223">SuperGrid</span></span>|<span data-ttu-id="1cfd2-224">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="1cfd2-224">Custom</span></span>|  
  
<a name="Windows_Forms_Controls"></a>   
## <a name="windows-forms-controls"></a><span data-ttu-id="1cfd2-225">contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1cfd2-225">Windows Forms Controls</span></span>  
 <span data-ttu-id="1cfd2-226">Contrôles Windows Forms sont exposés à [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] via des fournisseurs côté client dans UIAutomationClientsideProviders.dll.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-226">Windows Forms controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="1cfd2-227">Cet assembly est inscrit automatiquement pour être utilisé avec les applications clientes UI Automation.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-227">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="1cfd2-228">En règle générale, les contrôles Windows Forms qui sont des wrappers managés pour [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] contrôles communs sont pris en charge par [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span><span class="sxs-lookup"><span data-stu-id="1cfd2-228">Typically, Windows Forms controls that are managed wrappers for [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] common controls are supported by [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="1cfd2-229">Les contrôles suivants sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-229">The following controls are supported.</span></span>  
  
|<span data-ttu-id="1cfd2-230">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="1cfd2-230">Class Name</span></span>|  
|----------------|  
|<span data-ttu-id="1cfd2-231">Bouton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-231">Button</span></span>|  
|<span data-ttu-id="1cfd2-232">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="1cfd2-232">CheckBox</span></span>|  
|<span data-ttu-id="1cfd2-233">CheckedListBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-233">CheckedListBox</span></span>|  
|<span data-ttu-id="1cfd2-234">ColorDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-234">ColorDialog</span></span>|  
|<span data-ttu-id="1cfd2-235">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-235">ComboBox</span></span>|  
|<span data-ttu-id="1cfd2-236">FolderBrowser</span><span class="sxs-lookup"><span data-stu-id="1cfd2-236">FolderBrowser</span></span>|  
|<span data-ttu-id="1cfd2-237">FontDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-237">FontDialog</span></span>|  
|<span data-ttu-id="1cfd2-238">GroupBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-238">GroupBox</span></span>|  
|<span data-ttu-id="1cfd2-239">HscrollBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-239">HscrollBar</span></span>|  
|<span data-ttu-id="1cfd2-240">ImageList</span><span class="sxs-lookup"><span data-stu-id="1cfd2-240">ImageList</span></span>|  
|<span data-ttu-id="1cfd2-241">Label</span><span class="sxs-lookup"><span data-stu-id="1cfd2-241">Label</span></span>|  
|<span data-ttu-id="1cfd2-242">ListBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-242">ListBox</span></span>|  
|<span data-ttu-id="1cfd2-243">Affichage de liste</span><span class="sxs-lookup"><span data-stu-id="1cfd2-243">ListView</span></span>|  
|<span data-ttu-id="1cfd2-244">MainMenu/ContextMenu</span><span class="sxs-lookup"><span data-stu-id="1cfd2-244">MainMenu/ContextMenu</span></span>|  
|<span data-ttu-id="1cfd2-245">MonthCalendar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-245">MonthCalendar</span></span>|  
|<span data-ttu-id="1cfd2-246">NotifyIcon</span><span class="sxs-lookup"><span data-stu-id="1cfd2-246">NotifyIcon</span></span>|  
|<span data-ttu-id="1cfd2-247">OpenFileDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-247">OpenFileDialog</span></span>|  
|<span data-ttu-id="1cfd2-248">PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-248">PageSetupDialog</span></span>|  
|<span data-ttu-id="1cfd2-249">PrintDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-249">PrintDialog</span></span>|  
|<span data-ttu-id="1cfd2-250">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="1cfd2-250">ProgressBar</span></span>|  
|<span data-ttu-id="1cfd2-251">RadioButton</span><span class="sxs-lookup"><span data-stu-id="1cfd2-251">RadioButton</span></span>|  
|<span data-ttu-id="1cfd2-252">RichTextBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-252">RichTextBox</span></span>|  
|<span data-ttu-id="1cfd2-253">SaveFileDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-253">SaveFileDialog</span></span>|  
|<span data-ttu-id="1cfd2-254">ScrollableControl</span><span class="sxs-lookup"><span data-stu-id="1cfd2-254">ScrollableControl</span></span>|  
|<span data-ttu-id="1cfd2-255">SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="1cfd2-255">SoundPlayer</span></span>|  
|<span data-ttu-id="1cfd2-256">StatusBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-256">StatusBar</span></span>|  
|<span data-ttu-id="1cfd2-257">TabControl/TabPage</span><span class="sxs-lookup"><span data-stu-id="1cfd2-257">TabControl/TabPage</span></span>|  
|<span data-ttu-id="1cfd2-258">TextBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-258">TextBox</span></span>|  
|<span data-ttu-id="1cfd2-259">Minuterie</span><span class="sxs-lookup"><span data-stu-id="1cfd2-259">Timer</span></span>|  
|<span data-ttu-id="1cfd2-260">ToolBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-260">Toolbar</span></span>|  
|<span data-ttu-id="1cfd2-261">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-261">ToolTip</span></span>|  
|<span data-ttu-id="1cfd2-262">TrackBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-262">TrackBar</span></span>|  
|<span data-ttu-id="1cfd2-263">TreeView</span><span class="sxs-lookup"><span data-stu-id="1cfd2-263">TreeView</span></span>|  
|<span data-ttu-id="1cfd2-264">VscrollBar</span><span class="sxs-lookup"><span data-stu-id="1cfd2-264">VscrollBar</span></span>|  
|<span data-ttu-id="1cfd2-265">Navigateur web</span><span class="sxs-lookup"><span data-stu-id="1cfd2-265">WebBrowser</span></span>|  
  
 <span data-ttu-id="1cfd2-266">Les contrôles suivants sont exposés à [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] uniquement via leur prise en charge de [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)].</span><span class="sxs-lookup"><span data-stu-id="1cfd2-266">The following controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] only through their support for [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)].</span></span> <span data-ttu-id="1cfd2-267">Certaines fonctionnalités ne sont peut-être pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="1cfd2-267">Some functionality may not be available.</span></span>  
  
|<span data-ttu-id="1cfd2-268">Nom du contrôle</span><span class="sxs-lookup"><span data-stu-id="1cfd2-268">Control Name</span></span>|  
|------------------|  
|<span data-ttu-id="1cfd2-269">BindingSource</span><span class="sxs-lookup"><span data-stu-id="1cfd2-269">BindingSource</span></span>|  
|<span data-ttu-id="1cfd2-270">DataGrid</span><span class="sxs-lookup"><span data-stu-id="1cfd2-270">DataGrid</span></span>|  
|<span data-ttu-id="1cfd2-271">DataGridView</span><span class="sxs-lookup"><span data-stu-id="1cfd2-271">DataGridView</span></span>|  
|<span data-ttu-id="1cfd2-272">DataNavigator</span><span class="sxs-lookup"><span data-stu-id="1cfd2-272">DataNavigator</span></span>|  
|<span data-ttu-id="1cfd2-273">DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="1cfd2-273">DomainUpDown</span></span>|  
|<span data-ttu-id="1cfd2-274">ErrorProvider</span><span class="sxs-lookup"><span data-stu-id="1cfd2-274">ErrorProvider</span></span>|  
|<span data-ttu-id="1cfd2-275">FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="1cfd2-275">FlowLayoutPanel</span></span>|  
|<span data-ttu-id="1cfd2-276">Formulaire</span><span class="sxs-lookup"><span data-stu-id="1cfd2-276">Form</span></span>|  
|<span data-ttu-id="1cfd2-277">LinkLabel</span><span class="sxs-lookup"><span data-stu-id="1cfd2-277">LinkLabel</span></span>|  
|<span data-ttu-id="1cfd2-278">HelpProvider</span><span class="sxs-lookup"><span data-stu-id="1cfd2-278">HelpProvider</span></span>|  
|<span data-ttu-id="1cfd2-279">MaskedTextBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-279">MaskedTextBox</span></span>|  
|<span data-ttu-id="1cfd2-280">MenuStrip/ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="1cfd2-280">MenuStrip/ContextMenuStrip</span></span>|  
|<span data-ttu-id="1cfd2-281">NumericUpDown</span><span class="sxs-lookup"><span data-stu-id="1cfd2-281">NumericUpDown</span></span>|  
|<span data-ttu-id="1cfd2-282">Volet</span><span class="sxs-lookup"><span data-stu-id="1cfd2-282">Panel</span></span>|  
|<span data-ttu-id="1cfd2-283">PictureBox</span><span class="sxs-lookup"><span data-stu-id="1cfd2-283">PictureBox</span></span>|  
|<span data-ttu-id="1cfd2-284">PrintDocument</span><span class="sxs-lookup"><span data-stu-id="1cfd2-284">PrintDocument</span></span>|  
|<span data-ttu-id="1cfd2-285">PrintPreviewControl</span><span class="sxs-lookup"><span data-stu-id="1cfd2-285">PrintPreview-Control</span></span>|  
|<span data-ttu-id="1cfd2-286">PrintPreviewDialog</span><span class="sxs-lookup"><span data-stu-id="1cfd2-286">PrintPreview-Dialog</span></span>|  
|<span data-ttu-id="1cfd2-287">PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="1cfd2-287">PropertyGrid</span></span>|  
|<span data-ttu-id="1cfd2-288">UserControl</span><span class="sxs-lookup"><span data-stu-id="1cfd2-288">UserControl</span></span>|  
|<span data-ttu-id="1cfd2-289">ToolStrip</span><span class="sxs-lookup"><span data-stu-id="1cfd2-289">ToolStrip</span></span>|  
|<span data-ttu-id="1cfd2-290">TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="1cfd2-290">TableLayoutPanel</span></span>|  
|<span data-ttu-id="1cfd2-291">SplitContainer/SplitterPanel</span><span class="sxs-lookup"><span data-stu-id="1cfd2-291">SplitContainer/SplitterPanel</span></span>|  
|<span data-ttu-id="1cfd2-292">Séparateur</span><span class="sxs-lookup"><span data-stu-id="1cfd2-292">Splitter</span></span>|  
|<span data-ttu-id="1cfd2-293">RaftingContainer</span><span class="sxs-lookup"><span data-stu-id="1cfd2-293">RaftingContainer</span></span>|  
|<span data-ttu-id="1cfd2-294">StatusStrip</span><span class="sxs-lookup"><span data-stu-id="1cfd2-294">StatusStrip</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1cfd2-295">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cfd2-295">See Also</span></span>  
 [<span data-ttu-id="1cfd2-296">Types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="1cfd2-296">UI Automation Control Types</span></span>](../../../docs/framework/ui-automation/ui-automation-control-types.md)
