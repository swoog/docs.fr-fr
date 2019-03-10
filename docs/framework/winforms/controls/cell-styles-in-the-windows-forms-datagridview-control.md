---
title: Styles de cellules dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], cell styles
- cells [Windows Forms], styles
- data grids [Windows Forms], cell styles
ms.assetid: dbb75ed6-8804-4232-8382-f9920c2e380c
ms.openlocfilehash: a22fc29d2cab21977c0411a440b847b426fb5915
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57712273"
---
# <a name="cell-styles-in-the-windows-forms-datagridview-control"></a>Styles de cellules dans le contrôle DataGridView Windows Forms
Chaque cellule dans le <xref:System.Windows.Forms.DataGridView> contrôle peut avoir son propre style, telles que le format de texte, couleur d’arrière-plan, couleur de premier plan et police. En général, toutefois, plusieurs cellules partagent les caractéristiques de style particulier.  
  
 Groupes de cellules qui partagent des styles peuvent inclure toutes les cellules de particuliers lignes ou colonnes, toutes les cellules qui contiennent des valeurs particulières ou toutes les cellules dans le contrôle. Étant donné que ces groupes se chevauchent, chaque cellule peut obtenir ses informations de style à partir de plusieurs endroits. Par exemple, vous pouvez choisir chaque cellule un <xref:System.Windows.Forms.DataGridView> contrôle à utiliser la même police, mais uniquement les cellules des colonnes de devise à utiliser le format monétaire et uniquement les cellules de devises contenant des nombres négatifs pour utiliser une couleur de premier plan rouge.  
  
## <a name="the-datagridviewcellstyle-class"></a>La classe DataGridViewCellStyle  
 Le <xref:System.Windows.Forms.DataGridViewCellStyle> classe contient les propriétés suivantes relatives au style visuel :  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.BackColor%2A> et <xref:System.Windows.Forms.DataGridViewCellStyle.ForeColor%2A>  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.SelectionBackColor%2A> et <xref:System.Windows.Forms.DataGridViewCellStyle.SelectionForeColor%2A>  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.Font%2A>  
  
 Cette classe contient également les propriétés suivantes liées à la mise en forme :  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> et <xref:System.Windows.Forms.DataGridViewCellStyle.FormatProvider%2A>  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.NullValue%2A> et <xref:System.Windows.Forms.DataGridViewCellStyle.DataSourceNullValue%2A>  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.WrapMode%2A>  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.Alignment%2A>  
  
-   <xref:System.Windows.Forms.DataGridViewCellStyle.Padding%2A>  
  
 Pour plus d’informations sur ces propriétés et d’autres propriétés de style de cellule, consultez la <xref:System.Windows.Forms.DataGridViewCellStyle> documentation de référence et les rubriques répertoriées dans la section Voir aussi.  
  
## <a name="using-datagridviewcellstyle-objects"></a>À l’aide d’objets DataGridViewCellStyle  
 Vous pouvez récupérer <xref:System.Windows.Forms.DataGridViewCellStyle> objets de différentes propriétés de la <xref:System.Windows.Forms.DataGridView>, <xref:System.Windows.Forms.DataGridViewColumn>, <xref:System.Windows.Forms.DataGridViewRow>, et <xref:System.Windows.Forms.DataGridViewCell> classes et leurs classes dérivées. Si une de ces propriétés n’a pas encore été définie, récupérer sa valeur créera un nouveau <xref:System.Windows.Forms.DataGridViewCellStyle> objet. Vous pouvez également instancier votre propre <xref:System.Windows.Forms.DataGridViewCellStyle> les objets et les assigner à ces propriétés.  
  
 Vous pouvez éviter la duplication inutile des informations de style en partageant <xref:System.Windows.Forms.DataGridViewCellStyle> objets entre plusieurs <xref:System.Windows.Forms.DataGridView> éléments. Étant donné que les styles définis au contrôle, de la colonne et de la ligne effectuant un filtrage chaque niveau au niveau cellule, vous pouvez également éviter la duplication de style en définissant uniquement les propriétés de style à chaque niveau qui diffèrent des niveaux au-dessus. Cette opération est décrite plus en détail dans la section qui suit.  
  
 Le tableau suivant répertorie les principales propriétés qui obtient ou définit la <xref:System.Windows.Forms.DataGridViewCellStyle> objets.  
  
|Propriété|Classes|Description|  
|--------------|-------------|-----------------|  
|`DefaultCellStyle`|<xref:System.Windows.Forms.DataGridView>, <xref:System.Windows.Forms.DataGridViewColumn>, <xref:System.Windows.Forms.DataGridViewRow>et les classes dérivées|Obtient ou définit les styles par défaut utilisés par toutes les cellules dans l’ensemble du contrôle (y compris les cellules d’en-tête), dans une colonne ou dans une ligne.|  
|<xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A>|<xref:System.Windows.Forms.DataGridView>|Obtient ou définit les styles de cellules par défaut utilisés par toutes les lignes dans le contrôle. Cela n’inclut pas de cellules d’en-tête.|  
|<xref:System.Windows.Forms.DataGridView.AlternatingRowsDefaultCellStyle%2A>|<xref:System.Windows.Forms.DataGridView>|Obtient ou définit les styles de cellules par défaut utilisés par les lignes en alternance dans le contrôle. Utilisé pour créer un effet de type livre comptable.|  
|<xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A>|<xref:System.Windows.Forms.DataGridView>|Obtient ou définit les styles de cellules par défaut utilisés par les en-têtes de lignes du contrôle. Remplacé par le thème actuel si les styles visuels sont activés.|  
|<xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A>|<xref:System.Windows.Forms.DataGridView>|Obtient ou définit les styles de cellules par défaut utilisés par les en-têtes de colonne du contrôle. Remplacé par le thème actuel si les styles visuels sont activés.|  
|<xref:System.Windows.Forms.DataGridViewCell.Style%2A>|<xref:System.Windows.Forms.DataGridViewCell> et classes dérivées|Obtient ou définit des styles spécifiés au niveau de la cellule. Ces styles remplacent celles héritées des niveaux supérieurs.|  
|`InheritedStyle`|<xref:System.Windows.Forms.DataGridViewCell>, <xref:System.Windows.Forms.DataGridViewRow>, <xref:System.Windows.Forms.DataGridViewColumn>et les classes dérivées|Obtient tous les styles actuellement appliqués à la cellule, une ligne ou une colonne, y compris les styles hérités des niveaux supérieurs.|  
  
 Comme mentionné ci-dessus, l’obtention de la valeur d’une propriété de style automatiquement instancie un nouveau <xref:System.Windows.Forms.DataGridViewCellStyle> de l’objet si la propriété n’a pas été définie précédemment. Pour éviter de créer ces objets inutilement, les classes de ligne et de colonne ont une <xref:System.Windows.Forms.DataGridViewBand.HasDefaultCellStyle%2A> propriété que vous pouvez vérifier pour déterminer si le <xref:System.Windows.Forms.DataGridViewBand.DefaultCellStyle%2A> propriété a été définie. De même, les classes de cellule ont un <xref:System.Windows.Forms.DataGridViewCell.HasStyle%2A> propriété qui indique si le <xref:System.Windows.Forms.DataGridViewCell.Style%2A> propriété a été définie.  
  
 Chacune des propriétés de style associé à un *PropertyName* `Changed` événement sur le <xref:System.Windows.Forms.DataGridView> contrôle. Pour la ligne, colonne et les propriétés de cellule, le nom de l’événement commence par «`Row`«, »`Column`», ou «`Cell`» (par exemple, <xref:System.Windows.Forms.DataGridView.RowDefaultCellStyleChanged>). Chacun de ces événements se produit lorsque la propriété de style correspondante est définie à un autre <xref:System.Windows.Forms.DataGridViewCellStyle> objet. Ces événements ne se produisent pas lorsque vous récupérez un <xref:System.Windows.Forms.DataGridViewCellStyle> de l’objet à partir d’une propriété de style et modifier ses valeurs de propriété. Pour répondre aux modifications apportées aux objets de style de la cellule eux-mêmes, gérez le <xref:System.Windows.Forms.DataGridView.CellStyleContentChanged> événement.  
  
## <a name="style-inheritance"></a>Héritage de style  
 Chaque <xref:System.Windows.Forms.DataGridViewCell> obtient son apparence à partir de son <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A> propriété. Le <xref:System.Windows.Forms.DataGridViewCellStyle> objet retourné par cette propriété hérite ses valeurs d’une hiérarchie de propriétés de type <xref:System.Windows.Forms.DataGridViewCellStyle>. Ces propriétés sont répertoriées ci-dessous dans l’ordre dans lequel le <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A> pour les cellules d’en-tête obtient ses valeurs.  
  
1.  <xref:System.Windows.Forms.DataGridViewCell.Style%2A?displayProperty=nameWithType>  
  
2.  <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
3.  <xref:System.Windows.Forms.DataGridView.AlternatingRowsDefaultCellStyle%2A?displayProperty=nameWithType> (uniquement pour les cellules des lignes avec des numéros d’index impairs)  
  
4.  <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A?displayProperty=nameWithType>  
  
5.  <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
6.  <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
 Pour les cellules d’en-tête de ligne et de colonne, le <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A> propriété est remplie par les valeurs de la liste suivante des propriétés de source dans l’ordre indiqué.  
  
1.  <xref:System.Windows.Forms.DataGridViewCell.Style%2A?displayProperty=nameWithType>  
  
2.  <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A?displayProperty=nameWithType> ou <xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A?displayProperty=nameWithType>  
  
3.  <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
 Le diagramme suivant illustre ce processus.  
  
 ![Propriétés du type DataGridViewCellStyle](./media/cell-styles-in-the-windows-forms-datagridview-control/datagridviewcells-inheritance-diagram.gif "DataGridViewCells diagramme d’héritage")  
  
 Vous pouvez également accéder styles hérités par des colonnes et des lignes spécifiques. La colonne <xref:System.Windows.Forms.DataGridViewColumn.InheritedStyle%2A> propriété hérite ses valeurs des propriétés suivantes.  
  
1.  <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
2.  <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
 La ligne <xref:System.Windows.Forms.DataGridViewRow.InheritedStyle%2A> propriété hérite ses valeurs des propriétés suivantes.  
  
1.  <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
2.  <xref:System.Windows.Forms.DataGridView.AlternatingRowsDefaultCellStyle%2A?displayProperty=nameWithType> (uniquement pour les cellules des lignes avec des numéros d’index impairs)  
  
3.  <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A?displayProperty=nameWithType>  
  
4.  <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>  
  
 Pour chaque propriété dans un <xref:System.Windows.Forms.DataGridViewCellStyle> objet retourné par une `InheritedStyle` propriété, la valeur de propriété est obtenue à partir du premier style de cellule dans la liste appropriée qui possède la propriété correspondante définie sur une valeur autre que la <xref:System.Windows.Forms.DataGridViewCellStyle> classe les valeurs par défaut.  
  
 Le tableau suivant illustre comment la <xref:System.Windows.Forms.DataGridViewCellStyle.ForeColor%2A> valeur de propriété pour une cellule d’exemple est héritée de sa colonne conteneur.  
  
|propriété de type `DataGridViewCellStyle`|Exemple `ForeColor` valeur pour l’objet récupéré|  
|----------------------------------------------|----------------------------------------------------|  
|<xref:System.Windows.Forms.DataGridViewCell.Style%2A?displayProperty=nameWithType>|<xref:System.Drawing.Color.Empty?displayProperty=nameWithType>|  
|<xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A?displayProperty=nameWithType>|<xref:System.Drawing.Color.Red%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Forms.DataGridView.AlternatingRowsDefaultCellStyle%2A?displayProperty=nameWithType>|<xref:System.Drawing.Color.Empty?displayProperty=nameWithType>|  
|<xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A?displayProperty=nameWithType>|<xref:System.Drawing.Color.Empty?displayProperty=nameWithType>|  
|<xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A?displayProperty=nameWithType>|<xref:System.Drawing.Color.DarkBlue%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>|<xref:System.Drawing.Color.Black%2A?displayProperty=nameWithType>|  
  
 Dans ce cas, le <xref:System.Drawing.Color.Red%2A?displayProperty=nameWithType> valeur à partir de la ligne de la cellule est la première valeur réelle de la liste. Cela devient le <xref:System.Windows.Forms.DataGridViewCellStyle.ForeColor%2A> valeur de propriété de la cellule <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A>.  
  
 Le diagramme suivant illustre comment les différents <xref:System.Windows.Forms.DataGridViewCellStyle> propriétés peuvent hériter leurs valeurs d’emplacements différents.  
  
 ![Propriété du DataGridView&#45;héritage de la valeur](./media/cell-styles-in-the-windows-forms-datagridview-control/datagridviewcells-value-inheritance-diagram.gif "diagramme de l’héritage de valeur DataGridViewCells")  
  
 En tirant parti de l’héritage de style, vous pouvez fournir des styles appropriés pour l’ensemble du contrôle sans avoir à spécifier les mêmes informations à plusieurs endroits.  
  
 Bien que les cellules d’en-tête participent à l’héritage de style comme décrit, les objets retournés par le <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A> et <xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A> propriétés de la <xref:System.Windows.Forms.DataGridView> contrôle ont des valeurs de propriété initiales qui remplacent les valeurs de propriété de l’objet retourné par le <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A> propriété. Si vous souhaitez que les propriétés définies pour l’objet retourné par la <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A> propriété à appliquer aux en-têtes de lignes et de colonnes, vous devez définir les propriétés correspondantes des objets retournés par le <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A> et <xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A> indiqué de propriétés pour les valeurs par défaut pour le <xref:System.Windows.Forms.DataGridViewCellStyle> classe.  
  
> [!NOTE]
>  Si les styles visuels sont activés, les en-têtes de ligne et de colonne (à l’exception de la <xref:System.Windows.Forms.DataGridView.TopLeftHeaderCell%2A>) sont automatiquement un style du thème actuel, en substituant tous les styles spécifiés par ces propriétés.  
  
 Le <xref:System.Windows.Forms.DataGridViewButtonColumn>, <xref:System.Windows.Forms.DataGridViewImageColumn>, et <xref:System.Windows.Forms.DataGridViewCheckBoxColumn> types initialisent également quelques valeurs de l’objet retourné par la colonne <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A> propriété. Pour plus d’informations, consultez la documentation de référence pour ces types.  
  
## <a name="setting-styles-dynamically"></a>Définition dynamique des Styles  
 Pour personnaliser les styles de cellules avec des valeurs particulières, implémentez un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> événement. Gestionnaires pour cet événement reçoivent un argument de la <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs> type. Cet objet contient des propriétés qui vous permettent de déterminer la valeur de la cellule mise en forme, ainsi que son emplacement dans le <xref:System.Windows.Forms.DataGridView> contrôle. Cet objet contient également un <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs.CellStyle%2A> propriété qui est initialisée à la valeur de la <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A> propriété de la cellule en cours de mise en forme. Vous pouvez modifier les propriétés de style de cellule pour spécifier les informations de style appropriées à l’emplacement et la valeur de la cellule.  
  
> [!NOTE]
>  Le <xref:System.Windows.Forms.DataGridView.RowPrePaint> et <xref:System.Windows.Forms.DataGridView.RowPostPaint> événements reçoivent également un <xref:System.Windows.Forms.DataGridViewCellStyle> données d’objet de l’événement, mais dans leur casse, il s’agit d’une copie de la ligne <xref:System.Windows.Forms.DataGridViewRow.InheritedStyle%2A> propriété en lecture seule et les modifications apportées n’affectent pas le contrôle.  
  
 Vous pouvez également modifier dynamiquement les styles de cellules individuelles en réponse aux événements tels que le <xref:System.Windows.Forms.DataGridView.CellMouseEnter?displayProperty=nameWithType> et <xref:System.Windows.Forms.DataGridView.CellMouseLeave> événements. Par exemple, dans un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellMouseEnter> événement, vous pouvez stocker la valeur actuelle de la couleur d’arrière-plan de cellule (récupérée par le biais de la cellule <xref:System.Windows.Forms.DataGridViewCell.Style%2A> propriété), puis affectez-lui une nouvelle couleur qui met en surbrillance la cellule lorsque la souris passe dessus. Dans un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellMouseLeave> événement, vous pouvez ensuite restaurer la couleur d’arrière-plan la valeur d’origine.  
  
> [!NOTE]
>  La mise en cache les valeurs stockées dans la cellule <xref:System.Windows.Forms.DataGridViewCell.Style%2A> propriété est importante même si une valeur de style particulier est définie. Si vous remplacez temporairement un paramètre de style, restaurant à son état initial « non défini » permet de s’assurer que la cellule reviens à hériter le paramètre de style à un niveau supérieur. Si vous avez besoin déterminer le style réel en vigueur pour une cellule, quel que soit le style est hérité ou non, utilisez la cellule <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A> propriété.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Windows.Forms.DataGridView.AlternatingRowsDefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewBand.InheritedStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewRow.InheritedStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.InheritedStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewBand.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCell.Style%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellStyleContentChanged?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType>
- [Mises en forme et styles de base dans le contrôle DataGridView Windows Forms](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Définir des Styles de cellules par défaut pour le contrôle de DataGridView Windows Forms](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)
- [Mise en forme de données dans le contrôle DataGridView Windows Forms](data-formatting-in-the-windows-forms-datagridview-control.md)
