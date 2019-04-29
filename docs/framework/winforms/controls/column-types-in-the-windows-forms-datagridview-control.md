---
title: Types de colonnes dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- columns [Windows Forms], types
- DataGridView control [Windows Forms], column types
- data grids [Windows Forms], columns
ms.assetid: f0a0a9f1-8757-4bfd-891f-d7d12870dbed
ms.openlocfilehash: a33cf4cd865921c04ef10c7fccf3a67c3d22de73
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61956245"
---
# <a name="column-types-in-the-windows-forms-datagridview-control"></a>Types de colonnes dans le contrôle DataGridView Windows Forms
Le <xref:System.Windows.Forms.DataGridView> contrôle utilise plusieurs types de colonne pour afficher ses informations et permettre aux utilisateurs de modifier ou ajouter des informations.  
  
 Lorsque vous liez un <xref:System.Windows.Forms.DataGridView> contrôler et de définir le <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A> propriété `true`, colonnes sont générées automatiquement à l’aide des types de colonne par défaut appropriés pour les types de données contenus dans la source de données.  
  
 Vous pouvez également créer vous-même des instances des classes de la colonne et les ajouter à la collection retournée par la <xref:System.Windows.Forms.DataGridView.Columns%2A> propriété. Vous pouvez créer ces instances pour une utilisation en tant que colonnes indépendantes, ou vous pouvez les lier manuellement. Par exemple, les colonnes liées manuellement sont utiles lorsque vous souhaitez remplacer une colonne générée automatiquement d’un type avec une colonne d’un autre type.  
  
 Le tableau suivant décrit les différentes classes de colonne disponibles pour une utilisation dans le <xref:System.Windows.Forms.DataGridView> contrôle.  
  
|Classe|Description|  
|-----------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewTextBoxColumn>|Utilisé avec des valeurs textuelles. Généré automatiquement lors de la liaison pour les nombres et les chaînes.|  
|<xref:System.Windows.Forms.DataGridViewCheckBoxColumn>|Utilisé avec <xref:System.Boolean> et <xref:System.Windows.Forms.CheckState> valeurs. Généré automatiquement lors de la liaison à des valeurs de ces types.|  
|<xref:System.Windows.Forms.DataGridViewImageColumn>|Utilisé pour afficher des images. Généré automatiquement lors de la liaison aux tableaux d’octets, <xref:System.Drawing.Image> objets, ou <xref:System.Drawing.Icon> objets.|  
|<xref:System.Windows.Forms.DataGridViewButtonColumn>|Permet d’afficher des boutons dans les cellules. Pas générée automatiquement lors de la liaison. Généralement utilisé en tant que colonnes indépendantes.|  
|<xref:System.Windows.Forms.DataGridViewComboBoxColumn>|Utilisé pour afficher les listes déroulantes des cellules. Pas générée automatiquement lors de la liaison. En général lié aux données manuellement.|  
|<xref:System.Windows.Forms.DataGridViewLinkColumn>|Utilisé pour afficher les liens dans les cellules. Pas générée automatiquement lors de la liaison. En général lié aux données manuellement.|  
|Votre type de colonne personnalisé|Vous pouvez créer votre propre classe de la colonne en héritant la <xref:System.Windows.Forms.DataGridViewColumn> classe ou une de ses classes dérivées pour fournir une apparence personnalisée, comportement ou contrôles hébergés. Pour plus d'informations, voir [Procédure : Personnaliser des cellules et des colonnes dans le contrôle de DataGridView Windows Forms en étendant leur comportement et leur apparence](customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md)|  
  
 Ces types de colonnes sont décrites plus en détail dans les sections suivantes.  
  
## <a name="datagridviewtextboxcolumn"></a>DataGridViewTextBoxColumn  
 Le <xref:System.Windows.Forms.DataGridViewTextBoxColumn> est un type de colonne à usage général pour une utilisation avec les valeurs textuelles telles que des nombres et des chaînes. En mode de modification, un <xref:System.Windows.Forms.TextBox> contrôle s’affiche dans la cellule active, permettant aux utilisateurs de modifier la valeur de cellule.  
  
 Les valeurs de cellule sont automatiquement convertis en chaînes pour l’affichage. Valeurs entrées ou modifiées par l’utilisateur sont automatiquement analysés pour créer une valeur de cellule du type de données approprié. Vous pouvez personnaliser ces conversions en gérant la <xref:System.Windows.Forms.DataGridView.CellFormatting> et <xref:System.Windows.Forms.DataGridView.CellParsing> événements de la <xref:System.Windows.Forms.DataGridView> contrôle.  
  
 Le type de données de valeur de cellule d’une colonne est spécifié dans le <xref:System.Windows.Forms.DataGridViewColumn.ValueType%2A> propriété de la colonne.  
  
## <a name="datagridviewcheckboxcolumn"></a>DataGridViewCheckBoxColumn  
 Le <xref:System.Windows.Forms.DataGridViewCheckBoxColumn> est utilisé avec <xref:System.Boolean> et <xref:System.Windows.Forms.CheckState> valeurs. <xref:System.Boolean> affichage des valeurs en tant que les cases à cocher deux ou trois états, selon la valeur de la <xref:System.Windows.Forms.DataGridViewCheckBoxColumn.ThreeState%2A> propriété. Lorsque la colonne est liée à <xref:System.Windows.Forms.CheckState> valeurs, le <xref:System.Windows.Forms.DataGridViewCheckBoxColumn.ThreeState%2A> valeur de propriété est `true` par défaut.  
  
 En règle générale, les valeurs de cellule de case à cocher sont destinés au stockage, comme toutes les autres données, ou pour effectuer des opérations en bloc. Si vous souhaitez répondre immédiatement lorsque les utilisateurs cliquent sur une cellule de case à cocher, vous pouvez gérer le <xref:System.Windows.Forms.DataGridView.CellClick> événement, mais cet événement se produit avant la mise à jour de la valeur de cellule. Si vous avez besoin de la nouvelle valeur au moment du clic, une option consiste à calculer la valeur attendue sera basée sur la valeur actuelle. Une autre approche consiste à valider la modification immédiatement et à gérer le <xref:System.Windows.Forms.DataGridView.CellValueChanged> événement y répondre. Pour valider la modification de la suite d’un clic sur la cellule, vous devez gérer le <xref:System.Windows.Forms.DataGridView.CurrentCellDirtyStateChanged> événement. Dans le gestionnaire, si la cellule active est une cellule de case à cocher, appelez le <xref:System.Windows.Forms.DataGridView.CommitEdit%2A> (méthode) et passez le <xref:System.Windows.Forms.DataGridViewDataErrorContexts.Commit> valeur.  
  
## <a name="datagridviewimagecolumn"></a>DataGridViewImageColumn  
 Le <xref:System.Windows.Forms.DataGridViewImageColumn> est utilisé pour afficher des images. Colonnes de type image peuvent être remplis automatiquement à partir d’une source de données, remplies manuellement pour les colonnes indépendantes ou remplies dynamiquement dans un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellFormatting> événement.  
  
 Le remplissage automatique d’une colonne d’image à partir d’une source de données fonctionne avec les tableaux d’octets dans un large éventail de formats d’image, y compris tous les formats pris en charge par le <xref:System.Drawing.Image> classe et le format d’image OLE utilisé par Microsoft® Access et la base de données Northwind.  
  
 Remplissage d’une colonne d’image manuellement est utile lorsque vous souhaitez fournir les fonctionnalités d’un <xref:System.Windows.Forms.DataGridViewButtonColumn>, mais avec une apparence personnalisée. Vous pouvez gérer le <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType> événements pour répondre aux clics dans une cellule d’image.  
  
 Remplissage des cellules d’une colonne d’image dans un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellFormatting> événement est utile lorsque vous souhaitez fournir des images pour les valeurs calculées ou des valeurs dans des formats non-image. Par exemple, vous pouvez avoir une colonne de « À risque » avec les valeurs de chaîne telles que `"high"`, `"middle"`, et `"low"` que vous souhaitez afficher sous forme d’icônes. Alternativement, vous pouvez avoir une colonne de « Image » qui contient les emplacements des images qui doivent être chargés au lieu du contenu binaire des images.  
  
## <a name="datagridviewbuttoncolumn"></a>DataGridViewButtonColumn  
 Avec la <xref:System.Windows.Forms.DataGridViewButtonColumn>, vous pouvez afficher une colonne de cellules qui contiennent des boutons. Cela est utile lorsque vous souhaitez fournir un moyen facile pour vos utilisateurs à effectuer des actions sur des enregistrements particuliers, tels que de passer une commande ou l’affichage des enregistrements enfants dans une fenêtre distincte.  
  
 Colonnes de boutons ne sont pas générées automatiquement lors de la liaison de données un <xref:System.Windows.Forms.DataGridView> contrôle. Pour utiliser des colonnes de bouton, vous devez les créer manuellement et les ajouter à la collection retournée par la <xref:System.Windows.Forms.DataGridView.Columns%2A?displayProperty=nameWithType> propriété.  
  
 Vous pouvez répondre aux clics de l’utilisateur dans les cellules de boutons en gérant la <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType> événement.  
  
## <a name="datagridviewcomboboxcolumn"></a>DataGridViewComboBoxColumn  
 Avec la <xref:System.Windows.Forms.DataGridViewComboBoxColumn>, vous pouvez afficher une colonne de cellules qui contiennent des zones de liste déroulante. Cela est utile pour la saisie de données dans les champs peuvent contenir uniquement des valeurs particulières, telles que la colonne catégorie de la table Products dans la base de données Northwind.  
  
 Vous pouvez remplir la liste déroulante utilisée pour toutes les cellules de la même façon que vous devez remplir un <xref:System.Windows.Forms.ComboBox> la liste déroulante, soit manuellement par le biais de la collection retournée par la <xref:System.Windows.Forms.DataGridViewComboBoxColumn.Items%2A> propriété, ou en le liant à une source de données via le <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A>, <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DisplayMember%2A>, et <xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A> propriétés. Pour plus d’informations, consultez [contrôle ComboBox](combobox-control-windows-forms.md).  
  
 Vous pouvez lier les valeurs de cellule réelle à la source de données utilisée par le <xref:System.Windows.Forms.DataGridView> contrôle en définissant le <xref:System.Windows.Forms.DataGridViewColumn.DataPropertyName%2A> propriété de la <xref:System.Windows.Forms.DataGridViewComboBoxColumn?displayProperty=nameWithType>.  
  
 Colonnes de zone de liste déroulante ne sont pas générées automatiquement lors de la liaison de données un <xref:System.Windows.Forms.DataGridView> contrôle. Pour utiliser des colonnes de zone de liste déroulante, vous devez les créer manuellement et les ajouter à la collection retournée par la <xref:System.Windows.Forms.DataGridView.Columns%2A> propriété.  
  
## <a name="datagridviewlinkcolumn"></a>DataGridViewLinkColumn  
 Avec la <xref:System.Windows.Forms.DataGridViewLinkColumn>, vous pouvez afficher une colonne de cellules qui contiennent des liens hypertexte. Cela est utile pour les valeurs d’URL dans la source de données ou comme alternative à la colonne de boutons pour les comportements spéciaux, comme l’ouverture d’une fenêtre avec des enregistrements enfants.  
  
 Les colonnes de liens ne sont pas générées automatiquement lors de la liaison de données un <xref:System.Windows.Forms.DataGridView> contrôle. Pour utiliser des colonnes de liens, vous devez les créer manuellement et les ajouter à la collection retournée par la <xref:System.Windows.Forms.DataGridView.Columns%2A> propriété.  
  
 Vous pouvez répondre aux clics de l’utilisateur sur les liens en gérant la <xref:System.Windows.Forms.DataGridView.CellContentClick> événement. Cet événement se distingue le <xref:System.Windows.Forms.DataGridView.CellClick> et <xref:System.Windows.Forms.DataGridView.CellMouseClick> les événements qui se produisent lorsqu’un utilisateur clique sur n’importe où dans une cellule.  
  
 Le <xref:System.Windows.Forms.DataGridViewLinkColumn> classe fournit plusieurs propriétés pour modifier l’apparence des liens avant, pendant et après vous cliquez dessus.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- <xref:System.Windows.Forms.DataGridViewButtonColumn>
- <xref:System.Windows.Forms.DataGridViewCheckBoxColumn>
- <xref:System.Windows.Forms.DataGridViewComboBoxColumn>
- <xref:System.Windows.Forms.DataGridViewImageColumn>
- <xref:System.Windows.Forms.DataGridViewTextBoxColumn>
- <xref:System.Windows.Forms.DataGridViewLinkColumn>
- [DataGridView, contrôle](datagridview-control-windows-forms.md)
- [Guide pratique pour Afficher des Images dans les cellules du contrôle DataGridView Windows Forms](how-to-display-images-in-cells-of-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Travailler avec des colonnes de type Image dans le contrôle de DataGridView Windows Forms](how-to-work-with-image-columns-in-the-windows-forms-datagridview-control.md)
- [Personnalisation du contrôle DataGridView Windows Forms](customizing-the-windows-forms-datagridview-control.md)
