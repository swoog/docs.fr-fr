---
title: Implémentation du modèle de contrôle ScrollItem d’UI Automation
ms.date: 03/30/2017
helpviewer_keywords:
- control patterns, Scroll Item
- UI Automation, Scroll Item control pattern
- Scroll Item control pattern
ms.assetid: 903bab5c-80c1-44d7-bdc2-0a418893b987
ms.openlocfilehash: 377b383cb6dc583ab5b3ad9479f03eb552c5babe
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64651855"
---
# <a name="implementing-the-ui-automation-scrollitem-control-pattern"></a><span data-ttu-id="4acab-102">Implémentation du modèle de contrôle ScrollItem d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="4acab-102">Implementing the UI Automation ScrollItem Control Pattern</span></span>
> [!NOTE]
>  <span data-ttu-id="4acab-103">Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="4acab-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="4acab-104">Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="4acab-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="4acab-105">Cette rubrique présente les conventions et directives à respecter pour implémenter <xref:System.Windows.Automation.Provider.IScrollItemProvider>, notamment les informations sur les propriétés, les méthodes et les événements.</span><span class="sxs-lookup"><span data-stu-id="4acab-105">This topic introduces guidelines and conventions for implementing the <xref:System.Windows.Automation.Provider.IScrollItemProvider>, including information about properties, methods, and events.</span></span> <span data-ttu-id="4acab-106">Des liens vers des références supplémentaires sont répertoriés à la fin de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="4acab-106">Links to additional references are listed at the end of the topic.</span></span>  
  
 <span data-ttu-id="4acab-107">Le modèle de contrôle <xref:System.Windows.Automation.ScrollItemPattern> est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent <xref:System.Windows.Automation.Provider.IScrollProvider>.</span><span class="sxs-lookup"><span data-stu-id="4acab-107">The <xref:System.Windows.Automation.ScrollItemPattern> control pattern is used to support individual child controls of containers that implement <xref:System.Windows.Automation.Provider.IScrollProvider>.</span></span> <span data-ttu-id="4acab-108">Ce modèle de contrôle agit comme un canal de communication entre un contrôle enfant et son conteneur pour garantir que le conteneur est en mesure de modifier le contenu (ou la zone) actuellement visible dans sa fenêtre d’affichage pour afficher le contrôle enfant.</span><span class="sxs-lookup"><span data-stu-id="4acab-108">This control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="4acab-109">Pour obtenir des exemples de contrôles implémentant ce modèle de contrôle, consultez [Control Pattern Mapping for UI Automation Clients](../../../docs/framework/ui-automation/control-pattern-mapping-for-ui-automation-clients.md).</span><span class="sxs-lookup"><span data-stu-id="4acab-109">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](../../../docs/framework/ui-automation/control-pattern-mapping-for-ui-automation-clients.md).</span></span>  
  
<a name="Implementation_Guidelines_and_Conventions"></a>   
## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="4acab-110">Conventions et recommandations en matière d'implémentation</span><span class="sxs-lookup"><span data-stu-id="4acab-110">Implementation Guidelines and Conventions</span></span>  
 <span data-ttu-id="4acab-111">Quand vous implémentez le modèle de contrôle Scroll Item, notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4acab-111">When implementing the Scroll Item control pattern, note the following guidelines and conventions:</span></span>  
  
- <span data-ttu-id="4acab-112">Les éléments contenus dans un contrôle Window ou Canvas ne sont pas tenus d’implémenter l’interface IScrollItemProvider.</span><span class="sxs-lookup"><span data-stu-id="4acab-112">Items contained within a Window or Canvas control are not required to implement the IScrollItemProvider interface.</span></span> <span data-ttu-id="4acab-113">Cependant, comme alternative, ils doivent exposer un emplacement valide pour <xref:System.Windows.Automation.AutomationElementIdentifiers.BoundingRectangleProperty>.</span><span class="sxs-lookup"><span data-stu-id="4acab-113">As an alternative, however, they must expose a valid location for the <xref:System.Windows.Automation.AutomationElementIdentifiers.BoundingRectangleProperty>.</span></span> <span data-ttu-id="4acab-114">Ainsi, une application cliente UI Automation peut utiliser les méthodes de modèle de contrôle <xref:System.Windows.Automation.ScrollPattern> sur le conteneur pour afficher l’élément enfant.</span><span class="sxs-lookup"><span data-stu-id="4acab-114">This will allow a UI Automation client application to use the <xref:System.Windows.Automation.ScrollPattern> control pattern methods on the container to display the child item.</span></span>  
  
<a name="Required_Members_for_IScrollItemProvider"></a>   
## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="4acab-115">Membres requis pour IScrollItemProvider</span><span class="sxs-lookup"><span data-stu-id="4acab-115">Required Members for IScrollItemProvider</span></span>  
 <span data-ttu-id="4acab-116">La méthode suivante est requise pour l’implémentation de l’interface IScrollProvider.</span><span class="sxs-lookup"><span data-stu-id="4acab-116">The following method is required for implementing the IScrollProvider interface.</span></span>  
  
|<span data-ttu-id="4acab-117">Membres requis</span><span class="sxs-lookup"><span data-stu-id="4acab-117">Required members</span></span>|<span data-ttu-id="4acab-118">Type de membre</span><span class="sxs-lookup"><span data-stu-id="4acab-118">Member type</span></span>|<span data-ttu-id="4acab-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4acab-119">Notes</span></span>|  
|----------------------|-----------------|-----------|  
|<xref:System.Windows.Automation.Provider.IScrollItemProvider.ScrollIntoView%2A>|<span data-ttu-id="4acab-120">-Méthode</span><span class="sxs-lookup"><span data-stu-id="4acab-120">-   Method</span></span>|<span data-ttu-id="4acab-121">None</span><span class="sxs-lookup"><span data-stu-id="4acab-121">None</span></span>|  
  
 <span data-ttu-id="4acab-122">Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.</span><span class="sxs-lookup"><span data-stu-id="4acab-122">This control pattern has no associated properties or events.</span></span>  
  
<a name="Exceptions"></a>   
## <a name="exceptions"></a><span data-ttu-id="4acab-123">Exceptions</span><span class="sxs-lookup"><span data-stu-id="4acab-123">Exceptions</span></span>  
 <span data-ttu-id="4acab-124">Les fournisseurs doivent lever les exceptions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4acab-124">Providers must throw the following exceptions.</span></span>  
  
|<span data-ttu-id="4acab-125">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="4acab-125">Exception Type</span></span>|<span data-ttu-id="4acab-126">Condition</span><span class="sxs-lookup"><span data-stu-id="4acab-126">Condition</span></span>|  
|--------------------|---------------|  
|<xref:System.InvalidOperationException>|<span data-ttu-id="4acab-127">Si un élément ne peut pas être l’objet d’un défilement dans la vue :</span><span class="sxs-lookup"><span data-stu-id="4acab-127">If an item cannot be scrolled into view:</span></span><br /><br /> -   <xref:System.Windows.Automation.ScrollItemPattern.ScrollIntoView%2A>|  
  
## <a name="see-also"></a><span data-ttu-id="4acab-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4acab-128">See also</span></span>

- [<span data-ttu-id="4acab-129">Vue d’ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="4acab-129">UI Automation Control Patterns Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-control-patterns-overview.md)
- [<span data-ttu-id="4acab-130">Prendre en charge des modèles de contrôle dans un fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="4acab-130">Support Control Patterns in a UI Automation Provider</span></span>](../../../docs/framework/ui-automation/support-control-patterns-in-a-ui-automation-provider.md)
- [<span data-ttu-id="4acab-131">Modèles de contrôle UI Automation pour les clients</span><span class="sxs-lookup"><span data-stu-id="4acab-131">UI Automation Control Patterns for Clients</span></span>](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)
- [<span data-ttu-id="4acab-132">Présentation de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="4acab-132">UI Automation Tree Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-tree-overview.md)
- [<span data-ttu-id="4acab-133">Utiliser la mise en cache dans UI Automation</span><span class="sxs-lookup"><span data-stu-id="4acab-133">Use Caching in UI Automation</span></span>](../../../docs/framework/ui-automation/use-caching-in-ui-automation.md)
