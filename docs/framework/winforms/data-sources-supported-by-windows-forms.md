---
title: Sources de données prises en charge par les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- collections [Windows Forms], binding to
- OLE DB providers [Windows Forms], Windows Forms
- DataTable class [Windows Forms], binding and Windows Forms
- Windows Forms, data binding
- DataView class [Windows Forms], binding and Windows Forms
- DataViewManager class [Windows Forms], binding and Windows Forms
- Windows Forms, source data
- arrays [Windows Forms]
- data sources [Windows Forms]
- data providers [Windows Forms]
- DataSet class [Windows Forms], binding and Windows Forms
- data [Windows Forms], data providers
ms.assetid: 3d2c43f6-462b-4d35-9c86-13e9afe012e1
ms.openlocfilehash: 0252259d92f08a0f871167fc7930818bab542cc5
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64626781"
---
# <a name="data-sources-supported-by-windows-forms"></a>Sources de données prises en charge par les Windows Forms
En règle générale, la liaison de données a été utilisée au sein d’applications pour tirer parti des données stockées dans les bases de données. Avec la liaison de données Windows Forms, vous pouvez accéder aux données à partir de bases de données, ainsi que des données dans d’autres structures, telles que des tableaux et collections, tant que certaines exigences minimales sont respectées.  
  
## <a name="structures-to-bind-to"></a>Structures à lier aux  
 Dans les Windows Forms, vous pouvez lier à une vaste gamme de structures, simple objets (liaison simple) à des listes complexes telles que les tables de données ADO.NET (liaison complexe). Pour la liaison simple, Windows Forms prend en charge la liaison aux propriétés publiques sur l’objet simple. Liaison de liste Windows Forms nécessite généralement que l’objet prend en charge la <xref:System.Collections.IList> interface ou le <xref:System.ComponentModel.IListSource> interface. En outre, si vous créez une liaison avec via un <xref:System.Windows.Forms.BindingSource> composant, vous pouvez lier à un objet qui prend en charge la <xref:System.Collections.IEnumerable> interface. Pour plus d’informations sur les interfaces participant à la liaison de données, consultez [Interfaces associées à la liaison de données](interfaces-related-to-data-binding.md).  
  
 La liste suivante présente les structures que vous pouvez lier à dans les Windows Forms.  
  
 <xref:System.Windows.Forms.BindingSource>  
 Un <xref:System.Windows.Forms.BindingSource> est la source de données Windows Forms courante qui fait Office de proxy entre une source de données et des contrôles Windows Forms. Le général <xref:System.Windows.Forms.BindingSource> modèle d’utilisation consiste à lier vos contrôles à la <xref:System.Windows.Forms.BindingSource> et lier le <xref:System.Windows.Forms.BindingSource> à la source de données (par exemple, une table de données ADO.NET ou un objet métier). Le <xref:System.Windows.Forms.BindingSource> fournit des services qui activent et améliorent le niveau de prise en charge de liaison de données. Par exemple, Windows Forms contrôles basés sur liste tel que le <xref:System.Windows.Forms.DataGridView> et <xref:System.Windows.Forms.ComboBox> ne prennent pas directement en charge la liaison à <xref:System.Collections.IEnumerable> des sources de données, toutefois, vous pouvez activer ce scénario par liaison via un <xref:System.Windows.Forms.BindingSource>. Dans ce cas, le <xref:System.Windows.Forms.BindingSource> convertira la source de données à un <xref:System.Collections.IList>.  
  
 Objets simples  
 Windows Forms prend en charge les propriétés de contrôle de liaison de données aux propriétés publiques sur l’instance d’un objet en utilisant le <xref:System.Windows.Forms.Binding> type. Windows Forms prend également en charge des contrôles de liste en fonction de liaison comme un <xref:System.Windows.Forms.ListControl> à un objet d’instance quand un <xref:System.Windows.Forms.BindingSource> est utilisé.  
  
 tableau ou collection  
 Pour agir comme source de données, une liste doit implémenter le <xref:System.Collections.IList> interface ; un exemple serait un tableau qui est une instance de la <xref:System.Array> classe. Pour plus d’informations sur les tableaux, consultez [Comment : Créer un tableau d’objets (Visual Basic)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/487y7874(v=vs.100)).  
  
 En général, vous devez utiliser <xref:System.ComponentModel.BindingList%601> lorsque vous créez des listes d’objets pour la liaison de données. <xref:System.ComponentModel.BindingList%601> est une version générique de le <xref:System.ComponentModel.IBindingList> interface. Le <xref:System.ComponentModel.IBindingList> interface étend la <xref:System.Collections.IList> interface en ajoutant des propriétés, méthodes et événements nécessaires pour la liaison de données bidirectionnelle.  
  
 <xref:System.Collections.IEnumerable>  
 Contrôles Windows Forms peuvent être liés à des sources de données qui prennent en charge uniquement le <xref:System.Collections.IEnumerable> si elles sont liées par le biais de l’interface un <xref:System.Windows.Forms.BindingSource> composant.  
  
 [!INCLUDE[vstecado](../../../includes/vstecado-md.md)] objets de données  
 [!INCLUDE[vstecado](../../../includes/vstecado-md.md)] Fournit des structures de données pouvant être lié à plusieurs. Chacune d’elle varie dans sa complexité et la complexité.  
  
- <xref:System.Data.DataColumn>. Un <xref:System.Data.DataColumn> est le bloc de construction fondamental d’un <xref:System.Data.DataTable>, car un nombre de colonnes comprendre une table. Chaque <xref:System.Data.DataColumn> a un <xref:System.Data.DataColumn.DataType%2A> propriété qui détermine le type de données figurant dans la colonne (par exemple, la marque d’une automobile dans une table décrivant des voitures). Vous pouvez créer une liaison simple un contrôle (comme un <xref:System.Windows.Forms.TextBox> du contrôle <xref:System.Windows.Forms.Control.Text%2A> propriété) à une colonne dans une table de données.  
  
- <xref:System.Data.DataTable>. Un <xref:System.Data.DataTable> est la représentation sous forme d’une table, avec des lignes et colonnes, dans [!INCLUDE[vstecado](../../../includes/vstecado-md.md)]. Une table de données contient deux collections : <xref:System.Data.DataColumn>, représentant les colonnes de données dans une table donnée (qui détermine les types de données qui peuvent être entrées dans cette table), et <xref:System.Data.DataRow>, représentant les lignes de données dans une table donnée. Vous pouvez complexe lier un contrôle pour les informations contenues dans une table de données (notamment la liaison la <xref:System.Windows.Forms.DataGridView> contrôle à une table de données). Toutefois, lorsque vous liez à un <xref:System.Data.DataTable>, vous êtes fait une liaison à la vue du tableau par défaut.  
  
- <xref:System.Data.DataView>. Un <xref:System.Data.DataView> est une vue personnalisée d’une table de données unique qui peut être filtrée ou triée. Une vue de données est les « instantané » utilisée par les contrôles liés complexes de données. Vous pouvez créer une liaison simple ou complexe lier aux données dans une vue de données, mais n’oubliez pas que vous liez à une « image » fixe de données plutôt que sur une source de données.  
  
- <xref:System.Data.DataSet>. Un <xref:System.Data.DataSet> est une collection de tables, relations et contraintes des données dans une base de données. Vous pouvez créer une liaison simple ou complexe lier aux données au sein d’un jeu de données, mais n’oubliez pas que vous liez à la valeur par défaut <xref:System.Data.DataViewManager> pour le <xref:System.Data.DataSet> (voir la puce suivante).  
  
- <xref:System.Data.DataViewManager>. Un <xref:System.Data.DataViewManager> est une vue personnalisée de l’ensemble du <xref:System.Data.DataSet>, analogue à un <xref:System.Data.DataView>, mais avec les relations incluses. Avec un <xref:System.Data.DataViewManager.DataViewSettings%2A> collection, vous pouvez définir des filtres par défaut et les options de tri pour toutes les vues qui le <xref:System.Data.DataViewManager> a pour une table donnée.  
  
## <a name="see-also"></a>Voir aussi

- [Notification de modifications dans la liaison de données Windows Forms](change-notification-in-windows-forms-data-binding.md)
- [Liaison de données et Windows Forms](data-binding-and-windows-forms.md)
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
