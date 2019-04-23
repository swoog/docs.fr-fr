---
title: Prise en charge d'UI Automation pour les contrôles standard
ms.date: 03/30/2017
helpviewer_keywords:
- controls, UI Automation support for
- UI Automation, support for standard controls
ms.assetid: 3770ea8a-2655-4add-9c59-fe0610ad5084
ms.openlocfilehash: 3fde9779205ea7d0902ddd99ed192f097a159d2c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59221477"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="62b64-102">Prise en charge d'UI Automation pour les contrôles standard</span><span class="sxs-lookup"><span data-stu-id="62b64-102">UI Automation Support for Standard Controls</span></span>
> [!NOTE]
>  <span data-ttu-id="62b64-103">Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="62b64-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="62b64-104">Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="62b64-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="62b64-105">Cette rubrique contient des informations sur la prise en charge d’ [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] pour les contrôles standard dans les applications développées pour les infrastructures [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)]et [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="62b64-105">This topic contains information about [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] support for standard controls in applications developed for the [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)], and [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] frameworks.</span></span>  
  
<a name="Windows_Presentation_Foundation_Controls"></a>   
## <a name="windows-presentation-foundation-controls"></a><span data-ttu-id="62b64-106">Contrôles Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="62b64-106">Windows Presentation Foundation Controls</span></span>  
 <span data-ttu-id="62b64-107">Tous les éléments du contrôle [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] qui fournissent des informations ou une prise en charge pour l’interaction utilisateur disposent d’une prise en charge native complète de [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span><span class="sxs-lookup"><span data-stu-id="62b64-107">All [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] control elements that provide information or support for user interaction have full native support for [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="62b64-108">D’autres éléments, tels que les panneaux, ne sont pas visibles par [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span><span class="sxs-lookup"><span data-stu-id="62b64-108">Other elements, such as panels, are not visible to [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span>  
  
<a name="Win32_Controls"></a>   
## <a name="win32-controls"></a><span data-ttu-id="62b64-109">Contrôles Win32</span><span class="sxs-lookup"><span data-stu-id="62b64-109">Win32 Controls</span></span>  
 <span data-ttu-id="62b64-110">La plupart des contrôles [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] sont exposés à [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] via des fournisseurs côté client dans UIAutomationClientsideProviders.dll.</span><span class="sxs-lookup"><span data-stu-id="62b64-110">Most [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="62b64-111">Cet assembly est inscrit automatiquement pour être utilisé avec les applications clientes UI Automation.</span><span class="sxs-lookup"><span data-stu-id="62b64-111">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="62b64-112">La prise en charge complète n’est fournie que pour les contrôles de la version 6 de ComCtrl32.dll (disponible avec [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] et les versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="62b64-112">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] and later).</span></span>  
  
 <span data-ttu-id="62b64-113">Les contrôles suivants sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="62b64-113">The following controls are supported.</span></span>  
  
|<span data-ttu-id="62b64-114">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="62b64-114">Class name</span></span>|<span data-ttu-id="62b64-115">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="62b64-115">Control Type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="62b64-116">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-116">Button</span></span>|<span data-ttu-id="62b64-117">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-117">Button</span></span>|  
|<span data-ttu-id="62b64-118">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-118">Button</span></span>|<span data-ttu-id="62b64-119">RadioButton</span><span class="sxs-lookup"><span data-stu-id="62b64-119">RadioButton</span></span>|  
|<span data-ttu-id="62b64-120">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-120">Button</span></span>|<span data-ttu-id="62b64-121">Regrouper</span><span class="sxs-lookup"><span data-stu-id="62b64-121">Group</span></span>|  
|<span data-ttu-id="62b64-122">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-122">Button</span></span>|<span data-ttu-id="62b64-123">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="62b64-123">CheckBox</span></span>|  
|<span data-ttu-id="62b64-124">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-124">Button</span></span>|<span data-ttu-id="62b64-125">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="62b64-125">Hyperlink</span></span>|  
|<span data-ttu-id="62b64-126">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-126">Button</span></span>|<span data-ttu-id="62b64-127">SplitButton</span><span class="sxs-lookup"><span data-stu-id="62b64-127">SplitButton</span></span>|  
|<span data-ttu-id="62b64-128">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-128">Button</span></span>|<span data-ttu-id="62b64-129">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="62b64-129">CheckBox</span></span>|  
|<span data-ttu-id="62b64-130">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="62b64-130">ComboBoxEx32</span></span>|<span data-ttu-id="62b64-131">ComboBox</span><span class="sxs-lookup"><span data-stu-id="62b64-131">ComboBox</span></span>|  
|<span data-ttu-id="62b64-132">ComboBox</span><span class="sxs-lookup"><span data-stu-id="62b64-132">ComboBox</span></span>|<span data-ttu-id="62b64-133">ComboBox</span><span class="sxs-lookup"><span data-stu-id="62b64-133">ComboBox</span></span>|  
|<span data-ttu-id="62b64-134">Modifier</span><span class="sxs-lookup"><span data-stu-id="62b64-134">Edit</span></span>|<span data-ttu-id="62b64-135">Document</span><span class="sxs-lookup"><span data-stu-id="62b64-135">Document</span></span>|  
|<span data-ttu-id="62b64-136">Modifier</span><span class="sxs-lookup"><span data-stu-id="62b64-136">Edit</span></span>|<span data-ttu-id="62b64-137">Modifier</span><span class="sxs-lookup"><span data-stu-id="62b64-137">Edit</span></span>|  
|<span data-ttu-id="62b64-138">SysLink</span><span class="sxs-lookup"><span data-stu-id="62b64-138">SysLink</span></span>|<span data-ttu-id="62b64-139">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="62b64-139">Hyperlink</span></span>|  
|<span data-ttu-id="62b64-140">Statique</span><span class="sxs-lookup"><span data-stu-id="62b64-140">Static</span></span>|<span data-ttu-id="62b64-141">Texte</span><span class="sxs-lookup"><span data-stu-id="62b64-141">Text</span></span>|  
|<span data-ttu-id="62b64-142">Statique</span><span class="sxs-lookup"><span data-stu-id="62b64-142">Static</span></span>|<span data-ttu-id="62b64-143">Image</span><span class="sxs-lookup"><span data-stu-id="62b64-143">Image</span></span>|  
|<span data-ttu-id="62b64-144">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="62b64-144">SysIPAddress32</span></span>|<span data-ttu-id="62b64-145">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="62b64-145">Custom</span></span>|  
|<span data-ttu-id="62b64-146">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="62b64-146">SysHeader32</span></span>|<span data-ttu-id="62b64-147">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="62b64-147">Header/HeaderItem</span></span>|  
|<span data-ttu-id="62b64-148">SysListView32</span><span class="sxs-lookup"><span data-stu-id="62b64-148">SysListView32</span></span>|<span data-ttu-id="62b64-149">DataGrid</span><span class="sxs-lookup"><span data-stu-id="62b64-149">DataGrid</span></span>|  
|<span data-ttu-id="62b64-150">SysListView32</span><span class="sxs-lookup"><span data-stu-id="62b64-150">SysListView32</span></span>|<span data-ttu-id="62b64-151">Liste</span><span class="sxs-lookup"><span data-stu-id="62b64-151">List</span></span>|  
|<span data-ttu-id="62b64-152">ListBox</span><span class="sxs-lookup"><span data-stu-id="62b64-152">ListBox</span></span>|<span data-ttu-id="62b64-153">Liste</span><span class="sxs-lookup"><span data-stu-id="62b64-153">List</span></span>|  
|<span data-ttu-id="62b64-154">ListBox</span><span class="sxs-lookup"><span data-stu-id="62b64-154">ListBox</span></span>|<span data-ttu-id="62b64-155">ListItem</span><span class="sxs-lookup"><span data-stu-id="62b64-155">ListItem</span></span>|  
|<span data-ttu-id="62b64-156">#32768</span><span class="sxs-lookup"><span data-stu-id="62b64-156">#32768</span></span>|<span data-ttu-id="62b64-157">Menu</span><span class="sxs-lookup"><span data-stu-id="62b64-157">Menu</span></span>|  
|<span data-ttu-id="62b64-158">#32768</span><span class="sxs-lookup"><span data-stu-id="62b64-158">#32768</span></span>|<span data-ttu-id="62b64-159">MenuItem</span><span class="sxs-lookup"><span data-stu-id="62b64-159">MenuItem</span></span>|  
|<span data-ttu-id="62b64-160">msctls_progress32</span><span class="sxs-lookup"><span data-stu-id="62b64-160">msctls_progress32</span></span>|<span data-ttu-id="62b64-161">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="62b64-161">ProgressBar</span></span>|  
|<span data-ttu-id="62b64-162">RichEdit</span><span class="sxs-lookup"><span data-stu-id="62b64-162">RichEdit</span></span>|<span data-ttu-id="62b64-163">Document.</span><span class="sxs-lookup"><span data-stu-id="62b64-163">Document.</span></span> <span data-ttu-id="62b64-164">Consultez la remarque.</span><span class="sxs-lookup"><span data-stu-id="62b64-164">See note.</span></span>|  
|<span data-ttu-id="62b64-165">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="62b64-165">RichEdit20A</span></span>|<span data-ttu-id="62b64-166">Document</span><span class="sxs-lookup"><span data-stu-id="62b64-166">Document</span></span>|  
|<span data-ttu-id="62b64-167">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="62b64-167">RichEdit20W</span></span>|<span data-ttu-id="62b64-168">Document</span><span class="sxs-lookup"><span data-stu-id="62b64-168">Document</span></span>|  
|<span data-ttu-id="62b64-169">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="62b64-169">RichEdit50W</span></span>|<span data-ttu-id="62b64-170">Document</span><span class="sxs-lookup"><span data-stu-id="62b64-170">Document</span></span>|  
|<span data-ttu-id="62b64-171">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="62b64-171">ScrollBar</span></span>|<span data-ttu-id="62b64-172">Curseur</span><span class="sxs-lookup"><span data-stu-id="62b64-172">Slider</span></span>|  
|<span data-ttu-id="62b64-173">msctls_trackbar32</span><span class="sxs-lookup"><span data-stu-id="62b64-173">msctls_trackbar32</span></span>|<span data-ttu-id="62b64-174">Curseur</span><span class="sxs-lookup"><span data-stu-id="62b64-174">Slider</span></span>|  
|<span data-ttu-id="62b64-175">msctls_updown32</span><span class="sxs-lookup"><span data-stu-id="62b64-175">msctls_updown32</span></span>|<span data-ttu-id="62b64-176">Spinner</span><span class="sxs-lookup"><span data-stu-id="62b64-176">Spinner</span></span>|  
|<span data-ttu-id="62b64-177">msctls_statusbar32</span><span class="sxs-lookup"><span data-stu-id="62b64-177">msctls_statusbar32</span></span>|<span data-ttu-id="62b64-178">StatusBar</span><span class="sxs-lookup"><span data-stu-id="62b64-178">StatusBar</span></span>|  
|<span data-ttu-id="62b64-179">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="62b64-179">SysTabControl32</span></span>|<span data-ttu-id="62b64-180">Onglet</span><span class="sxs-lookup"><span data-stu-id="62b64-180">Tab</span></span>|  
|<span data-ttu-id="62b64-181">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="62b64-181">SysTabControl32</span></span>|<span data-ttu-id="62b64-182">TabItem</span><span class="sxs-lookup"><span data-stu-id="62b64-182">TabItem</span></span>|  
|<span data-ttu-id="62b64-183">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-183">ToolbarWindow32</span></span>|<span data-ttu-id="62b64-184">ToolBar</span><span class="sxs-lookup"><span data-stu-id="62b64-184">ToolBar</span></span>|  
|<span data-ttu-id="62b64-185">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-185">ToolbarWindow32</span></span>|<span data-ttu-id="62b64-186">MenuItem</span><span class="sxs-lookup"><span data-stu-id="62b64-186">MenuItem</span></span>|  
|<span data-ttu-id="62b64-187">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-187">ToolbarWindow32</span></span>|<span data-ttu-id="62b64-188">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-188">Button</span></span>|  
|<span data-ttu-id="62b64-189">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-189">ToolbarWindow32</span></span>|<span data-ttu-id="62b64-190">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="62b64-190">CheckBox</span></span>|  
|<span data-ttu-id="62b64-191">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-191">ToolbarWindow32</span></span>|<span data-ttu-id="62b64-192">RadioButton</span><span class="sxs-lookup"><span data-stu-id="62b64-192">RadioButton</span></span>|  
|<span data-ttu-id="62b64-193">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-193">ToolbarWindow32</span></span>|<span data-ttu-id="62b64-194">Séparateur</span><span class="sxs-lookup"><span data-stu-id="62b64-194">Separator</span></span>|  
|<span data-ttu-id="62b64-195">tooltips_class32</span><span class="sxs-lookup"><span data-stu-id="62b64-195">tooltips_class32</span></span>|<span data-ttu-id="62b64-196">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="62b64-196">ToolTip</span></span>|  
|<span data-ttu-id="62b64-197">#32774</span><span class="sxs-lookup"><span data-stu-id="62b64-197">#32774</span></span>|<span data-ttu-id="62b64-198">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="62b64-198">ToolTip</span></span>|  
|<span data-ttu-id="62b64-199">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="62b64-199">ReBarWindow32</span></span>|<span data-ttu-id="62b64-200">ToolBar</span><span class="sxs-lookup"><span data-stu-id="62b64-200">Toolbar</span></span>|  
|<span data-ttu-id="62b64-201">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="62b64-201">SysTreeView32</span></span>|<span data-ttu-id="62b64-202">Arborescence</span><span class="sxs-lookup"><span data-stu-id="62b64-202">Tree</span></span>|  
|<span data-ttu-id="62b64-203">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="62b64-203">SysTreeView32</span></span>|<span data-ttu-id="62b64-204">TreeItem</span><span class="sxs-lookup"><span data-stu-id="62b64-204">TreeItem</span></span>|  
  
 <span data-ttu-id="62b64-205">**Remarque** Le contrôle RichEdit est pris en charge uniquement pour les versions fournies avec [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] (dans RichEd20.dll version 3.1 et version ultérieure, ainsi que dans MsftEdit.dll version 4.1 et version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="62b64-205">**Note** The RichEdit control is supported only for versions shipped with [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>  
  
 <span data-ttu-id="62b64-206">Les contrôles suivants ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="62b64-206">The following controls are not supported.</span></span>  
  
|<span data-ttu-id="62b64-207">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="62b64-207">Class name</span></span>|<span data-ttu-id="62b64-208">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="62b64-208">Control type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="62b64-209">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="62b64-209">SysAnimate32</span></span>|<span data-ttu-id="62b64-210">Image</span><span class="sxs-lookup"><span data-stu-id="62b64-210">Image</span></span>|  
|<span data-ttu-id="62b64-211">SysPager</span><span class="sxs-lookup"><span data-stu-id="62b64-211">SysPager</span></span>|<span data-ttu-id="62b64-212">Spinner</span><span class="sxs-lookup"><span data-stu-id="62b64-212">Spinner</span></span>|  
|<span data-ttu-id="62b64-213">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="62b64-213">SysDateTimePick32</span></span>|<span data-ttu-id="62b64-214">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="62b64-214">Custom</span></span>|  
|<span data-ttu-id="62b64-215">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="62b64-215">SysMonthCal32</span></span>|<span data-ttu-id="62b64-216">Calendrier</span><span class="sxs-lookup"><span data-stu-id="62b64-216">Calendar</span></span>|  
|<span data-ttu-id="62b64-217">MS_WINNOTE</span><span class="sxs-lookup"><span data-stu-id="62b64-217">MS_WINNOTE</span></span>|<span data-ttu-id="62b64-218">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="62b64-218">Tooltip</span></span>|  
|<span data-ttu-id="62b64-219">VBBubble</span><span class="sxs-lookup"><span data-stu-id="62b64-219">VBBubble</span></span>|<span data-ttu-id="62b64-220">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="62b64-220">Tooltip</span></span>|  
|<span data-ttu-id="62b64-221">ScrollBar (quand il est utilisé comme contrôle autonome)</span><span class="sxs-lookup"><span data-stu-id="62b64-221">ScrollBar (when used as a standalone control)</span></span>|<span data-ttu-id="62b64-222">Curseur</span><span class="sxs-lookup"><span data-stu-id="62b64-222">Slider</span></span>|  
|<span data-ttu-id="62b64-223">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="62b64-223">SuperGrid</span></span>|<span data-ttu-id="62b64-224">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="62b64-224">Custom</span></span>|  
  
<a name="Windows_Forms_Controls"></a>   
## <a name="windows-forms-controls"></a><span data-ttu-id="62b64-225">contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="62b64-225">Windows Forms Controls</span></span>  
 <span data-ttu-id="62b64-226">Contrôles Windows Forms sont exposés à [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] via des fournisseurs côté client dans UIAutomationClientsideProviders.dll.</span><span class="sxs-lookup"><span data-stu-id="62b64-226">Windows Forms controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="62b64-227">Cet assembly est inscrit automatiquement pour être utilisé avec les applications clientes UI Automation.</span><span class="sxs-lookup"><span data-stu-id="62b64-227">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="62b64-228">En règle générale, les contrôles Windows Forms qui sont des wrappers managés pour [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] contrôles communs sont pris en charge par [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span><span class="sxs-lookup"><span data-stu-id="62b64-228">Typically, Windows Forms controls that are managed wrappers for [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] common controls are supported by [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="62b64-229">Les contrôles suivants sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="62b64-229">The following controls are supported.</span></span>  
  
|<span data-ttu-id="62b64-230">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="62b64-230">Class Name</span></span>|  
|----------------|  
|<span data-ttu-id="62b64-231">Bouton</span><span class="sxs-lookup"><span data-stu-id="62b64-231">Button</span></span>|  
|<span data-ttu-id="62b64-232">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="62b64-232">CheckBox</span></span>|  
|<span data-ttu-id="62b64-233">CheckedListBox</span><span class="sxs-lookup"><span data-stu-id="62b64-233">CheckedListBox</span></span>|  
|<span data-ttu-id="62b64-234">ColorDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-234">ColorDialog</span></span>|  
|<span data-ttu-id="62b64-235">ComboBox</span><span class="sxs-lookup"><span data-stu-id="62b64-235">ComboBox</span></span>|  
|<span data-ttu-id="62b64-236">FolderBrowser</span><span class="sxs-lookup"><span data-stu-id="62b64-236">FolderBrowser</span></span>|  
|<span data-ttu-id="62b64-237">FontDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-237">FontDialog</span></span>|  
|<span data-ttu-id="62b64-238">GroupBox</span><span class="sxs-lookup"><span data-stu-id="62b64-238">GroupBox</span></span>|  
|<span data-ttu-id="62b64-239">HscrollBar</span><span class="sxs-lookup"><span data-stu-id="62b64-239">HscrollBar</span></span>|  
|<span data-ttu-id="62b64-240">ImageList</span><span class="sxs-lookup"><span data-stu-id="62b64-240">ImageList</span></span>|  
|<span data-ttu-id="62b64-241">Etiquette</span><span class="sxs-lookup"><span data-stu-id="62b64-241">Label</span></span>|  
|<span data-ttu-id="62b64-242">ListBox</span><span class="sxs-lookup"><span data-stu-id="62b64-242">ListBox</span></span>|  
|<span data-ttu-id="62b64-243">Affichage de liste</span><span class="sxs-lookup"><span data-stu-id="62b64-243">ListView</span></span>|  
|<span data-ttu-id="62b64-244">MainMenu/ContextMenu</span><span class="sxs-lookup"><span data-stu-id="62b64-244">MainMenu/ContextMenu</span></span>|  
|<span data-ttu-id="62b64-245">MonthCalendar</span><span class="sxs-lookup"><span data-stu-id="62b64-245">MonthCalendar</span></span>|  
|<span data-ttu-id="62b64-246">NotifyIcon</span><span class="sxs-lookup"><span data-stu-id="62b64-246">NotifyIcon</span></span>|  
|<span data-ttu-id="62b64-247">OpenFileDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-247">OpenFileDialog</span></span>|  
|<span data-ttu-id="62b64-248">PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-248">PageSetupDialog</span></span>|  
|<span data-ttu-id="62b64-249">PrintDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-249">PrintDialog</span></span>|  
|<span data-ttu-id="62b64-250">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="62b64-250">ProgressBar</span></span>|  
|<span data-ttu-id="62b64-251">RadioButton</span><span class="sxs-lookup"><span data-stu-id="62b64-251">RadioButton</span></span>|  
|<span data-ttu-id="62b64-252">RichTextBox</span><span class="sxs-lookup"><span data-stu-id="62b64-252">RichTextBox</span></span>|  
|<span data-ttu-id="62b64-253">SaveFileDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-253">SaveFileDialog</span></span>|  
|<span data-ttu-id="62b64-254">ScrollableControl</span><span class="sxs-lookup"><span data-stu-id="62b64-254">ScrollableControl</span></span>|  
|<span data-ttu-id="62b64-255">SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="62b64-255">SoundPlayer</span></span>|  
|<span data-ttu-id="62b64-256">StatusBar</span><span class="sxs-lookup"><span data-stu-id="62b64-256">StatusBar</span></span>|  
|<span data-ttu-id="62b64-257">TabControl/TabPage</span><span class="sxs-lookup"><span data-stu-id="62b64-257">TabControl/TabPage</span></span>|  
|<span data-ttu-id="62b64-258">TextBox</span><span class="sxs-lookup"><span data-stu-id="62b64-258">TextBox</span></span>|  
|<span data-ttu-id="62b64-259">Minuterie</span><span class="sxs-lookup"><span data-stu-id="62b64-259">Timer</span></span>|  
|<span data-ttu-id="62b64-260">ToolBar</span><span class="sxs-lookup"><span data-stu-id="62b64-260">Toolbar</span></span>|  
|<span data-ttu-id="62b64-261">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="62b64-261">ToolTip</span></span>|  
|<span data-ttu-id="62b64-262">TrackBar</span><span class="sxs-lookup"><span data-stu-id="62b64-262">TrackBar</span></span>|  
|<span data-ttu-id="62b64-263">TreeView</span><span class="sxs-lookup"><span data-stu-id="62b64-263">TreeView</span></span>|  
|<span data-ttu-id="62b64-264">VscrollBar</span><span class="sxs-lookup"><span data-stu-id="62b64-264">VscrollBar</span></span>|  
|<span data-ttu-id="62b64-265">Navigateur web</span><span class="sxs-lookup"><span data-stu-id="62b64-265">WebBrowser</span></span>|  
  
 <span data-ttu-id="62b64-266">Les contrôles suivants sont exposés à [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] uniquement via leur prise en charge de [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)].</span><span class="sxs-lookup"><span data-stu-id="62b64-266">The following controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] only through their support for [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)].</span></span> <span data-ttu-id="62b64-267">Certaines fonctionnalités ne sont peut-être pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="62b64-267">Some functionality may not be available.</span></span>  
  
|<span data-ttu-id="62b64-268">Nom du contrôle</span><span class="sxs-lookup"><span data-stu-id="62b64-268">Control Name</span></span>|  
|------------------|  
|<span data-ttu-id="62b64-269">BindingSource</span><span class="sxs-lookup"><span data-stu-id="62b64-269">BindingSource</span></span>|  
|<span data-ttu-id="62b64-270">DataGrid</span><span class="sxs-lookup"><span data-stu-id="62b64-270">DataGrid</span></span>|  
|<span data-ttu-id="62b64-271">DataGridView</span><span class="sxs-lookup"><span data-stu-id="62b64-271">DataGridView</span></span>|  
|<span data-ttu-id="62b64-272">DataNavigator</span><span class="sxs-lookup"><span data-stu-id="62b64-272">DataNavigator</span></span>|  
|<span data-ttu-id="62b64-273">DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="62b64-273">DomainUpDown</span></span>|  
|<span data-ttu-id="62b64-274">ErrorProvider</span><span class="sxs-lookup"><span data-stu-id="62b64-274">ErrorProvider</span></span>|  
|<span data-ttu-id="62b64-275">FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="62b64-275">FlowLayoutPanel</span></span>|  
|<span data-ttu-id="62b64-276">Formulaire</span><span class="sxs-lookup"><span data-stu-id="62b64-276">Form</span></span>|  
|<span data-ttu-id="62b64-277">LinkLabel</span><span class="sxs-lookup"><span data-stu-id="62b64-277">LinkLabel</span></span>|  
|<span data-ttu-id="62b64-278">HelpProvider</span><span class="sxs-lookup"><span data-stu-id="62b64-278">HelpProvider</span></span>|  
|<span data-ttu-id="62b64-279">MaskedTextBox</span><span class="sxs-lookup"><span data-stu-id="62b64-279">MaskedTextBox</span></span>|  
|<span data-ttu-id="62b64-280">MenuStrip/ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="62b64-280">MenuStrip/ContextMenuStrip</span></span>|  
|<span data-ttu-id="62b64-281">NumericUpDown</span><span class="sxs-lookup"><span data-stu-id="62b64-281">NumericUpDown</span></span>|  
|<span data-ttu-id="62b64-282">Volet</span><span class="sxs-lookup"><span data-stu-id="62b64-282">Panel</span></span>|  
|<span data-ttu-id="62b64-283">PictureBox</span><span class="sxs-lookup"><span data-stu-id="62b64-283">PictureBox</span></span>|  
|<span data-ttu-id="62b64-284">PrintDocument</span><span class="sxs-lookup"><span data-stu-id="62b64-284">PrintDocument</span></span>|  
|<span data-ttu-id="62b64-285">PrintPreviewControl</span><span class="sxs-lookup"><span data-stu-id="62b64-285">PrintPreview-Control</span></span>|  
|<span data-ttu-id="62b64-286">PrintPreviewDialog</span><span class="sxs-lookup"><span data-stu-id="62b64-286">PrintPreview-Dialog</span></span>|  
|<span data-ttu-id="62b64-287">PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="62b64-287">PropertyGrid</span></span>|  
|<span data-ttu-id="62b64-288">UserControl</span><span class="sxs-lookup"><span data-stu-id="62b64-288">UserControl</span></span>|  
|<span data-ttu-id="62b64-289">ToolStrip</span><span class="sxs-lookup"><span data-stu-id="62b64-289">ToolStrip</span></span>|  
|<span data-ttu-id="62b64-290">TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="62b64-290">TableLayoutPanel</span></span>|  
|<span data-ttu-id="62b64-291">SplitContainer/SplitterPanel</span><span class="sxs-lookup"><span data-stu-id="62b64-291">SplitContainer/SplitterPanel</span></span>|  
|<span data-ttu-id="62b64-292">Séparateur</span><span class="sxs-lookup"><span data-stu-id="62b64-292">Splitter</span></span>|  
|<span data-ttu-id="62b64-293">RaftingContainer</span><span class="sxs-lookup"><span data-stu-id="62b64-293">RaftingContainer</span></span>|  
|<span data-ttu-id="62b64-294">StatusStrip</span><span class="sxs-lookup"><span data-stu-id="62b64-294">StatusStrip</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="62b64-295">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b64-295">See also</span></span>

- [<span data-ttu-id="62b64-296">Types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="62b64-296">UI Automation Control Types</span></span>](../../../docs/framework/ui-automation/ui-automation-control-types.md)
