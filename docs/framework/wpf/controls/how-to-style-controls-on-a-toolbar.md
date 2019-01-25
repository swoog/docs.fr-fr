---
title: "Procédure : Donner un style aux contrôles d'une barre d'outils"
ms.date: 03/30/2017
helpviewer_keywords:
- styling controls on toolbar [WPF]
- toolbars [WPF]
- customizing controls on toolbar [WPF]
ms.assetid: ba6ae056-d6a9-4c24-90f8-467ab0bc0b1a
ms.openlocfilehash: 097bb23a41ba68bf9c121a53920f19694508348b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544859"
---
# <a name="how-to-style-controls-on-a-toolbar"></a><span data-ttu-id="7bd26-102">Procédure : Donner un style aux contrôles d'une barre d'outils</span><span class="sxs-lookup"><span data-stu-id="7bd26-102">How to: Style Controls on a ToolBar</span></span>
<span data-ttu-id="7bd26-103">Le <xref:System.Windows.Controls.ToolBar> définit <xref:System.Windows.ResourceKey> objets pour spécifier le style des contrôles dans le <xref:System.Windows.Controls.ToolBar>.</span><span class="sxs-lookup"><span data-stu-id="7bd26-103">The <xref:System.Windows.Controls.ToolBar> defines <xref:System.Windows.ResourceKey> objects to specify the style of controls within the <xref:System.Windows.Controls.ToolBar>.</span></span>  <span data-ttu-id="7bd26-104">Style à un contrôle dans un <xref:System.Windows.Controls.ToolBar>, définissez le `x:key` attribut de style à un <xref:System.Windows.ResourceKey> défini dans <xref:System.Windows.Controls.ToolBar>.</span><span class="sxs-lookup"><span data-stu-id="7bd26-104">To style a control in a <xref:System.Windows.Controls.ToolBar>, set the `x:key` attribute of the style to a <xref:System.Windows.ResourceKey> defined in <xref:System.Windows.Controls.ToolBar>.</span></span>  
  
 <span data-ttu-id="7bd26-105">Le <xref:System.Windows.Controls.ToolBar> définit les éléments suivants <xref:System.Windows.ResourceKey> objets :</span><span class="sxs-lookup"><span data-stu-id="7bd26-105">The <xref:System.Windows.Controls.ToolBar> defines the following <xref:System.Windows.ResourceKey> objects:</span></span>  
  
-   <xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.CheckBoxStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.ComboBoxStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.MenuStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.RadioButtonStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.SeparatorStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.TextBoxStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.ToggleButtonStyleKey%2A>  
  
## <a name="example"></a><span data-ttu-id="7bd26-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="7bd26-106">Example</span></span>  
 <span data-ttu-id="7bd26-107">L’exemple suivant définit les styles pour les contrôles au sein d’un <xref:System.Windows.Controls.ToolBar>.</span><span class="sxs-lookup"><span data-stu-id="7bd26-107">The following example defines styles for the controls within a <xref:System.Windows.Controls.ToolBar>.</span></span>  
  
 [!code-xaml[ToolBar_snip#ToolBarAllStyles](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbarallstyles)]  
[!code-xaml[ToolBar_snip#ToolBar](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbar)]  
  
## <a name="see-also"></a><span data-ttu-id="7bd26-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bd26-108">See also</span></span>
- [<span data-ttu-id="7bd26-109">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="7bd26-109">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
