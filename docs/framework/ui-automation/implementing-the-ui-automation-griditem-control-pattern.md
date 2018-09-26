---
title: Implémentation du modèle de contrôle GridItem d'UI Automation
ms.date: 03/30/2017
helpviewer_keywords:
- control patterns, GridItem
- UI Automation GridItem control pattern
- GridItem control pattern
ms.assetid: bffbae08-fe2a-42fd-ab84-f37187518916
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 68de80e4a01de27c16c0ed85c4177c562d5e328b
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47089946"
---
# <a name="implementing-the-ui-automation-griditem-control-pattern"></a>Implémentation du modèle de contrôle GridItem d’UI Automation
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Cette rubrique présente les conventions de mise en œuvre et <xref:System.Windows.Automation.Provider.IGridItemProvider>, y compris des informations sur les propriétés. Des liens vers des références supplémentaires sont répertoriés à la fin de la vue d'ensemble.  
  
 Le <xref:System.Windows.Automation.GridItemPattern> modèle de contrôle est utilisé pour prendre en charge les contrôles enfants individuels de conteneurs qui implémentent <xref:System.Windows.Automation.Provider.IGridProvider>. Pour obtenir des exemples de contrôles implémentant ce modèle de contrôle, consultez [Control Pattern Mapping for UI Automation Clients](../../../docs/framework/ui-automation/control-pattern-mapping-for-ui-automation-clients.md).  
  
<a name="Implementation_Guidelines_and_Conventions"></a>   
## <a name="implementation-guidelines-and-conventions"></a>Conventions et recommandations en matière d'implémentation  
 Lors de l’implémentation <xref:System.Windows.Automation.Provider.IGridProvider>, notez les conventions et recommandations suivantes :  
  
-   Les coordonnées de grille ont une base zéro et la cellule supérieure gauche possède les coordonnées (0, 0).  
  
-   Cellules fusionnées signalent leurs <xref:System.Windows.Automation.Provider.IGridItemProvider.Row%2A> et <xref:System.Windows.Automation.Provider.IGridItemProvider.Column%2A> propriétés basées sur leur cellule d’ancrage sous-jacente, comme défini par le fournisseur UI Automation. En règle générale, il s’agit de la ligne la plus haute ou de la colonne la plus à gauche.  
  
-   <xref:System.Windows.Automation.Provider.IGridItemProvider> ne fournit pas de manipulation active de la grille telle que la fusion ou le fractionnement des cellules.  
  
-   Contrôles qui implémentent <xref:System.Windows.Automation.Provider.IGridItemProvider> peut généralement être parcouru (autrement dit, un client UI Automation peut déplacer vers les contrôles adjacents) à l’aide du clavier.  
  
<a name="Required_Members_for_IGridItemProvider"></a>   
## <a name="required-members-for-igriditemprovider"></a>Membres obligatoires pour IGridItemProvider  
 Les propriétés et méthodes suivantes sont nécessaires à l'implémentation d'<xref:System.Windows.Automation.Provider.IGridItemProvider>.  
  
|Membres requis|Type de membre|Notes|  
|----------------------|-----------------|-----------|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.Row%2A>|Propriété|Aucun.|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.Column%2A>|Propriété|Aucun.|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.RowSpan%2A>|Propriété|Aucun.|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.ColumnSpan%2A>|Propriété|Aucun.|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.ContainingGrid%2A>|Propriété|Aucun.|  
  
 Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.  
  
<a name="Exceptions"></a>   
## <a name="exceptions"></a>Exceptions  
 Ce modèle de contrôle n’est associé à aucune exception.  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble des modèles de contrôle UI Automation](../../../docs/framework/ui-automation/ui-automation-control-patterns-overview.md)  
 [Prendre en charge des modèles de contrôle dans un fournisseur UI Automation](../../../docs/framework/ui-automation/support-control-patterns-in-a-ui-automation-provider.md)  
 [Modèles de contrôle UI Automation pour les clients](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)  
 [Implémentation du modèle de contrôle Grid d’UI Automation](../../../docs/framework/ui-automation/implementing-the-ui-automation-grid-control-pattern.md)  
 [Présentation de l’arborescence UI Automation](../../../docs/framework/ui-automation/ui-automation-tree-overview.md)  
 [Utiliser la mise en cache dans UI Automation](../../../docs/framework/ui-automation/use-caching-in-ui-automation.md)
