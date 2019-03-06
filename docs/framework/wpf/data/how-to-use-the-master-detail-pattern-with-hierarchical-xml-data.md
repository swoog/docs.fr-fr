---
title: 'Procédure : Utiliser le modèle maître/détail avec des données XML hiérarchiques'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: eb8dbdd8-5871-42bb-a16b-04e655fea677
ms.openlocfilehash: 2b1ed34fe363f44a3a9eb80dc56d721868329717
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378104"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-xml-data"></a>Procédure : Utiliser le modèle maître/détail avec des données XML hiérarchiques
Cet exemple montre comment implémenter le scénario maître / détail avec [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] données.  
  
## <a name="example"></a>Exemple  
 Cet exemple est la [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] version des données de l’exemple abordé dans [utiliser le modèle maître / détail avec des données hiérarchiques](how-to-use-the-master-detail-pattern-with-hierarchical-data.md). Dans cet exemple, les données sont à partir du fichier `League.xml`. Notez comment le troisième <xref:System.Windows.Controls.ListBox> contrôle effectue le suivi des modifications de sélection dans la seconde <xref:System.Windows.Controls.ListBox> en le liant à son <xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A> propriété.  
  
 [!code-xaml[MasterDetailXml#HowTo1](~/samples/snippets/csharp/VS_Snippets_Wpf/MasterDetailXml/CS/Window1.xaml#howto1)]  
[!code-xaml[MasterDetailXml#HowTo2](~/samples/snippets/csharp/VS_Snippets_Wpf/MasterDetailXml/CS/Window1.xaml#howto2)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.HierarchicalDataTemplate>
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
