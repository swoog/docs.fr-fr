---
title: Rechercher et mettre un texte en surbrillance à l'aide d'UI Automation
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text, highlighting
- finding text
- text, finding
- UI automation, highlighting text
- UI automation, finding text
- highlighting text
ms.assetid: b77693f5-87bb-4b29-a297-05ff882e2044
ms.openlocfilehash: fafd3fc7345f94d3907163ff9dcf0ab293f85f3f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609955"
---
# <a name="find-and-highlight-text-using-ui-automation"></a>Rechercher et mettre un texte en surbrillance à l'aide d'UI Automation
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Cette rubrique montre comment séquentiellement rechercher et mettre en surbrillance chaque occurrence d’une chaîne dans le contenu d’un contrôle de texte en utilisant [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)].  
  
## <a name="example"></a>Exemple  
 L’exemple suivant obtient un <xref:System.Windows.Automation.TextPattern> objet à partir d’un contrôle de texte. Un <xref:System.Windows.Automation.Text.TextPatternRange> objet représentant le contenu textuel du document entier, est ensuite créé à l’aide de la <xref:System.Windows.Automation.TextPattern.DocumentRange%2A> propriété de ce <xref:System.Windows.Automation.TextPattern>. Deux autres <xref:System.Windows.Automation.Text.TextPatternRange> objets sont ensuite créées pour la recherche séquentielle et mettre en évidence les fonctionnalités.  
  
[!code-csharp[FindText#StartApp](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#startapp)]
[!code-vb[FindText#StartApp](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#startapp)]  
[!code-csharp[FindText#FindTextProvider](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#findtextprovider)]
[!code-vb[FindText#FindTextProvider](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#findtextprovider)]  
[!code-csharp[FindText#SearchTarget](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#searchtarget)]
[!code-vb[FindText#SearchTarget](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#searchtarget)]  
  
## <a name="see-also"></a>Voir aussi

- [Rechercher et mettre en surbrillance le texte à l’aide d’UI Automation](../../../docs/framework/ui-automation/find-and-highlight-text-using-ui-automation.md)
