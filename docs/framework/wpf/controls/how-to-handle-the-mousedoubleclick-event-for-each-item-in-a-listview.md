---
title: "Procédure : Gérer l'événement MouseDoubleClick pour chaque élément d'un ListView"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView controls [WPF], MouseDoubleClick event
ms.assetid: 81b39369-655a-4585-ac58-4640e5bb8fed
ms.openlocfilehash: a4a93ffdf7c9cf2737c41a7fd196d8cfff716ea1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57377196"
---
# <a name="how-to-handle-the-mousedoubleclick-event-for-each-item-in-a-listview"></a>Procédure : Gérer l'événement MouseDoubleClick pour chaque élément d'un ListView
Pour gérer un événement pour un élément dans un <xref:System.Windows.Controls.ListView>, vous devez ajouter un gestionnaire d’événements à chaque <xref:System.Windows.Controls.ListViewItem>. Quand un <xref:System.Windows.Controls.ListView> est lié à une source de données, vous ne créez pas explicitement un <xref:System.Windows.Controls.ListViewItem>, mais vous pouvez gérer l’événement pour chaque élément en ajoutant un <xref:System.Windows.EventSetter> à un style d’un <xref:System.Windows.Controls.ListViewItem>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une limite de données <xref:System.Windows.Controls.ListView> et crée un <xref:System.Windows.Style> pour ajouter un gestionnaire d’événements dans chaque <xref:System.Windows.Controls.ListViewItem>.  
  
 [!code-xaml[ListViewHowTos#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#1)]  
[!code-xaml[ListViewHowTos#5](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#5)]  
[!code-xaml[ListViewHowTos#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#2)]  
  
 L’exemple suivant gère le <xref:System.Windows.Controls.Control.MouseDoubleClick> événement.  
  
 [!code-csharp[ListViewHowTos#6](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml.cs#6)]
 [!code-vb[ListViewHowTos#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewHowTos/VisualBasic/Window1.xaml.vb#6)]  
  
> [!NOTE]
>  Bien qu’il soit plus courante consiste à lier un <xref:System.Windows.Controls.ListView> à une source de données, vous pouvez utiliser un style pour ajouter un gestionnaire d’événements dans chaque <xref:System.Windows.Controls.ListViewItem> dans un non-lié aux données <xref:System.Windows.Controls.ListView> que vous créiez explicitement une <xref:System.Windows.Controls.ListViewItem>.  Pour plus d’informations sur explicitement et implicitement créé <xref:System.Windows.Controls.ListViewItem> contrôles, consultez <xref:System.Windows.Controls.ItemsControl>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Xml.XmlElement>
- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Application d’un style et création de modèles](styling-and-templating.md)
- [Effectuer une liaison à des données XML à l’aide d’un XMLDataProvider et de requêtes XPath](../data/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [Vue d’ensemble de ListView](listview-overview.md)
