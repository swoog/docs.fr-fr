---
title: 'Atténuation : rendu de la fenêtre WPF'
ms.date: 03/30/2017
ms.assetid: 28ed6bf8-141b-4b73-a4e3-44a99fae5084
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d54751ae0492e25f824eee6362e0f3bca446d75e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59147626"
---
# <a name="mitigation-wpf-window-rendering"></a><span data-ttu-id="f8235-102">Atténuation : rendu de la fenêtre WPF</span><span class="sxs-lookup"><span data-stu-id="f8235-102">Mitigation: WPF Window Rendering</span></span>
<span data-ttu-id="f8235-103">Dans le [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] s'exécutant sur Windows 8 et versions ultérieures, la totalité de la fenêtre est restituée sans découpage lorsqu'elle s'étend au-delà d'un seul affichage dans un scénario à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="f8235-103">In the [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] running on Windows 8 and above, the entire window is rendered without clipping when it extends outside of single display in a multi-monitor scenario.</span></span>  
  
## <a name="impact"></a><span data-ttu-id="f8235-104">Impact</span><span class="sxs-lookup"><span data-stu-id="f8235-104">Impact</span></span>  
 <span data-ttu-id="f8235-105">En général, le rendu de toute une fenêtre sur plusieurs écrans sans découpage est le comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="f8235-105">In general, rendering an entire window across multiple monitors without clipping is the expected behavior.</span></span> <span data-ttu-id="f8235-106">Cependant, sur Windows 7 et versions antérieures, les fenêtres WPF sont tronquées lorsqu'elles s'étendent au-delà d'un seul affichage, car le rendu d'une partie de la fenêtre sur le second écran a un impact significatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="f8235-106">However, on Windows 7 and earlier versions, WPF windows are clipped when they extend beyond a single display because rendering a portion of the window on the second monitor has a significant performance impact.</span></span>  
  
 <span data-ttu-id="f8235-107">L'impact du rendu des fenêtres WPF sur les écrans sur Windows 8 et versions ultérieures n'est pas précisément quantifiable, car il dépend d'un grand nombre de facteurs.</span><span class="sxs-lookup"><span data-stu-id="f8235-107">The precise impact of rendering WPF windows across monitors on Windows 8 and above is not precisely quantifiable since it depends on a large number of factors.</span></span> <span data-ttu-id="f8235-108">Dans certains cas, il peut se produire un impact indésirable sur les performances, en particulier pour les utilisateurs qui exécutent des applications riches en graphisme et dont les fenêtres se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="f8235-108">In some cases, it may still produce an undesirable impact on performance, particularly for users who run graphics-intensive applications and have windows straddling monitors.</span></span> <span data-ttu-id="f8235-109">Dans d'autres cas, vous pouvez simplement vouloir un comportement cohérent entre les versions du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f8235-109">In other cases, you may simply want a consistent behavior across .NET Framework versions.</span></span>  
  
## <a name="mitigation"></a><span data-ttu-id="f8235-110">Atténuation</span><span class="sxs-lookup"><span data-stu-id="f8235-110">Mitigation</span></span>  
 <span data-ttu-id="f8235-111">Vous pouvez désactiver cette modification et rétablir le comportement précédent de découpage d'une fenêtre WPF lorsqu'elle s'étend au-delà d'un affichage unique.</span><span class="sxs-lookup"><span data-stu-id="f8235-111">You can disable this change and revert to the previous behavior of clipping a WPF window when it extends beyond a single display.</span></span> <span data-ttu-id="f8235-112">Il existe deux façons d'effectuer cette opération :</span><span class="sxs-lookup"><span data-stu-id="f8235-112">There are two ways to do this:</span></span>  
  
-   <span data-ttu-id="f8235-113">En ajoutant l'élément `<EnableMultiMonitorDisplayClipping>` à la section `<appSettings>` du fichier de configuration de votre application, vous pouvez activer ou désactiver ce comportement sur les applications qui s'exécutent sur Windows 8 ou versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f8235-113">By adding the `<EnableMultiMonitorDisplayClipping>` element to the `<appSettings>` section of your application configuration file, you can disable or enable this behavior on apps running on Windows 8 or later.</span></span> <span data-ttu-id="f8235-114">Par exemple, la section de configuration suivante désactive le rendu sans découpage :</span><span class="sxs-lookup"><span data-stu-id="f8235-114">For example, the following configuration section disables rendering without clipping:</span></span>  
  
    ```xml  
    <appSettings>  
        <add key="EnableMultiMonitorDisplayClipping" value="true"/>  
      </appSettings>  
    ```  
  
     <span data-ttu-id="f8235-115">Le paramètre de configuration `<EnableMultiMonitorDisplayClipping>` peut avoir l'une des deux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8235-115">The `<EnableMultiMonitorDisplayClipping>` configuration setting can have either of two values:</span></span>  
  
    -   <span data-ttu-id="f8235-116">`true`, pour activer le découpage des fenêtres selon les limites de l'écran pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="f8235-116">`true`, to enable clipping of windows to monitor bounds during rendering.</span></span>  
  
    -   <span data-ttu-id="f8235-117">`false`, pour désactiver le découpage des fenêtres selon les limites de l'écran pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="f8235-117">`false`, to disable clipping of windows to monitor bounds during rendering.</span></span>  
  
-   <span data-ttu-id="f8235-118">En définissant la propriété <xref:System.Windows.CoreCompatibilityPreferences.EnableMultiMonitorDisplayClipping%2A> avec la valeur `true` au démarrage de l'application.</span><span class="sxs-lookup"><span data-stu-id="f8235-118">By setting the <xref:System.Windows.CoreCompatibilityPreferences.EnableMultiMonitorDisplayClipping%2A> property to `true` at app startup.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8235-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8235-119">See also</span></span>

- [<span data-ttu-id="f8235-120">Modifications du runtime</span><span class="sxs-lookup"><span data-stu-id="f8235-120">Runtime Changes</span></span>](../../../docs/framework/migration-guide/runtime-changes-in-the-net-framework-4-6.md)
