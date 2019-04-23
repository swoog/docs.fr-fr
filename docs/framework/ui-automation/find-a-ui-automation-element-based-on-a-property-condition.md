---
title: Rechercher un élément UI Automation basé sur une condition de propriété
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements, finding by property conditions
- UI Automation, finding elements by property conditions
ms.assetid: 3acaee5a-6ce8-4c3e-81c8-67e59eb74477
ms.openlocfilehash: a5e775c69a4dd520d8148bfc790cc00428d9d15e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175511"
---
# <a name="find-a-ui-automation-element-based-on-a-property-condition"></a>Rechercher un élément UI Automation basé sur une condition de propriété
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Cette rubrique contient des exemples de code qui montre comment localiser un élément dans le [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence selon une ou plusieurs propriétés spécifiques.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, un ensemble de conditions de propriété sont spécifiés qui identifient un élément particulier (ou éléments) qui vous intéresse dans la <xref:System.Windows.Automation.AutomationElement> arborescence. Une recherche de tous les éléments correspondants est ensuite exécutée avec le <xref:System.Windows.Automation.AutomationElement.FindAll%2A> méthode qui incorpore une série de <xref:System.Windows.Automation.AndCondition> opérations booléennes pour limiter le nombre d’éléments correspondants.  
  
> [!NOTE]
>  Lors de la recherche à partir de la <xref:System.Windows.Automation.AutomationElement.RootElement%2A>, vous devez essayer d’obtenir uniquement les enfants directs. Une recherche des descendants peut itérer au sein des centaines ou des milliers d’éléments, ce qui peut provoquer un dépassement de capacité de pile. Si vous tentez d’obtenir un élément spécifique de niveau inférieur, vous devez commencer votre recherche à partir de la fenêtre d’application ou d’un conteneur de niveau inférieur.  
  
 [!code-csharp[InvokePatternApp#1100](../../../samples/snippets/csharp/VS_Snippets_Wpf/InvokePatternApp/CSharp/InvokePatternApp.cs#1100)]
 [!code-vb[InvokePatternApp#1100](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InvokePatternApp/VisualBasic/Client.vb#1100)]  
  
## <a name="see-also"></a>Voir aussi

- [InvokePattern et ExpandCollapsePattern Menu exemple d’élément](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms771636(v=vs.90))
- [Obtention d’éléments UI Automation](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)
- [Utiliser la propriété AutomationID](../../../docs/framework/ui-automation/use-the-automationid-property.md)
