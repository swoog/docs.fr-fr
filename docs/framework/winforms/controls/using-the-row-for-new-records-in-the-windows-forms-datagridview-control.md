---
title: Utilisation de la ligne pour les nouveaux enregistrements dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], adding rows for new records
- rows [Windows Forms], new records
- DataGridView control [Windows Forms], data entry
ms.assetid: 6110f1ea-9794-442c-a98a-f104a1feeaf4
ms.openlocfilehash: 67c87b28f04b028f329663d6cf8215370a00ef2f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009168"
---
# <a name="using-the-row-for-new-records-in-the-windows-forms-datagridview-control"></a>Utilisation de la ligne pour les nouveaux enregistrements dans le contrôle DataGridView Windows Forms
Lorsque vous utilisez un <xref:System.Windows.Forms.DataGridView> pour la modification des données dans votre application, vous souhaiterez souvent donner aux utilisateurs la possibilité d’ajouter de nouvelles lignes de données au magasin de données. Le <xref:System.Windows.Forms.DataGridView> contrôle prend en charge cette fonctionnalité en fournissant une ligne pour les nouveaux enregistrements, qui est toujours affichée en tant que la dernière ligne. Elle est marquée avec un astérisque (*) dans son en-tête de ligne. Les sections suivantes décrivent certains éléments que vous devez envisager lorsque vous programmez avec la ligne pour les nouveaux enregistrements est activé.  
  
## <a name="displaying-the-row-for-new-records"></a>Affichage de la ligne pour les nouveaux enregistrements  
 Utilisez le <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> propriété pour indiquer si la ligne pour les nouveaux enregistrements s’affiche. La valeur par défaut de cette propriété est `true`.  
  
 Pour les données liées aux cas, la ligne des nouveaux enregistrements s’affichera si le <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> propriété du contrôle et le <xref:System.ComponentModel.IBindingList.AllowNew%2A?displayProperty=nameWithType> propriété de la source de données sont tous deux `true`. Si une est `false` la ligne n’est pas affichée.  
  
## <a name="populating-the-row-for-new-records-with-default-data"></a>Remplissage de la ligne pour les nouveaux enregistrements avec les données par défaut  
 Lorsque l’utilisateur sélectionne la ligne pour les nouveaux enregistrements que la ligne actuelle, le <xref:System.Windows.Forms.DataGridView> incrémente le <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> événement.  
  
 Cet événement permet d’accéder au nouveau <xref:System.Windows.Forms.DataGridViewRow> et vous permet de remplir la nouvelle ligne avec les données par défaut. Pour plus d'informations, voir [Procédure : Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms](specify-default-values-for-new-rows-in-the-datagrid.md)  
  
## <a name="the-rows-collection"></a>La Collection de lignes  
 La ligne des nouveaux enregistrements est contenue dans le <xref:System.Windows.Forms.DataGridView> du contrôle <xref:System.Windows.Forms.DataGridView.Rows%2A> collection mais se comporte différemment à deux égards :  
  
- Impossible de supprimer la ligne des nouveaux enregistrements de la <xref:System.Windows.Forms.DataGridView.Rows%2A> collection par programme. Un <xref:System.InvalidOperationException> est levée si cette opération est tentée. L’utilisateur ne peut pas également supprimer la ligne pour les nouveaux enregistrements. Le <xref:System.Windows.Forms.DataGridViewRowCollection.Clear%2A?displayProperty=nameWithType> méthode ne supprime pas cette ligne à partir de la <xref:System.Windows.Forms.DataGridView.Rows%2A> collection.  
  
- Aucune ligne ne peut être ajoutée après la ligne pour les nouveaux enregistrements. Un <xref:System.InvalidOperationException> est levée si cette opération est tentée. Par conséquent, la ligne des nouveaux enregistrements est toujours la dernière ligne dans le <xref:System.Windows.Forms.DataGridView> contrôle. Les méthodes sur <xref:System.Windows.Forms.DataGridViewRowCollection> qui ajoutent des lignes :<xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A>, <xref:System.Windows.Forms.DataGridViewRowCollection.AddCopy%2A>, et <xref:System.Windows.Forms.DataGridViewRowCollection.AddCopies%2A>— appellent toutes les méthodes d’insertion en interne lorsque la ligne pour les nouveaux enregistrements est présente.  
  
## <a name="visual-customization-of-the-row-for-new-records"></a>Personnalisation visuelle de la ligne pour les nouveaux enregistrements  
 Lorsque la ligne pour les nouveaux enregistrements est créée, elle est basée sur la ligne spécifiée par le <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> propriété. Les styles de cellules qui ne sont pas spécifiés pour cette ligne sont hérités d’autres propriétés. Pour plus d’informations sur l’héritage de style de cellule, consultez [Styles de cellules dans le contrôle DataGridView Windows Forms](cell-styles-in-the-windows-forms-datagridview-control.md).  
  
 Les valeurs initiales affichées par les cellules dans la ligne pour les nouveaux enregistrements sont extraites à partir de chaque cellule <xref:System.Windows.Forms.DataGridViewCell.DefaultNewRowValue%2A> propriété. Pour les cellules de type <xref:System.Windows.Forms.DataGridViewImageCell>, cette propriété retourne un espace réservé d’image. Sinon, cette propriété retourne `null`. Vous pouvez remplacer cette propriété pour retourner une valeur personnalisée. Toutefois, ces valeurs initiales peuvent être remplacées par un <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> Gestionnaire d’événements lorsque le focus entre dans la ligne pour les nouveaux enregistrements.  
  
 Les icônes standards pour l’en-tête de cette ligne, qui sont une flèche ou un astérisque, ne sont pas exposées publiquement. Si vous souhaitez personnaliser les icônes, vous devrez créer un personnalisé <xref:System.Windows.Forms.DataGridViewRowHeaderCell> classe.  
  
 Les icônes standard utilisent le <xref:System.Windows.Forms.DataGridViewCellStyle.ForeColor%2A> propriété de le <xref:System.Windows.Forms.DataGridViewCellStyle> en cours d’utilisation par la cellule d’en-tête de ligne. Les icônes standards ne sont pas rendus si n’est pas suffisamment d’espace pour les afficher complètement.  
  
 Si une valeur de chaîne est définie par la cellule d’en-tête de ligne, et si l’espace n’est pas suffisant pour le texte et l’icône, l’icône est d’abord supprimée.  
  
## <a name="sorting"></a>Tri  
 En mode indépendant, nouveaux enregistrements sont toujours ajoutés à la fin de la <xref:System.Windows.Forms.DataGridView> même si l’utilisateur les a triées le contenu de la <xref:System.Windows.Forms.DataGridView>. L’utilisateur doit appliquer encore le tri pour trier la ligne à la position correcte ; Ce comportement est semblable à celle de la <xref:System.Windows.Forms.ListView> contrôle.  
  
 Dans données de modes dépendants et virtuels, le comportement d’insertion lorsqu’un tri est appliqué sera dépendants de l’implémentation du modèle de données. Pour [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)], la ligne est immédiatement placée à la position correcte.  
  
## <a name="other-notes-on-the-row-for-new-records"></a>Autres remarques sur la ligne pour les nouveaux enregistrements  
 Vous ne pouvez pas définir le <xref:System.Windows.Forms.DataGridViewRow.Visible%2A> propriété de cette ligne à `false`. Un <xref:System.InvalidOperationException> est levée si cette opération est tentée.  
  
 La ligne pour les nouveaux enregistrements est toujours créée dans un état désélectionné.  
  
## <a name="virtual-mode"></a>Mode virtuel  
 Si vous implémentez le mode virtuel, vous devez suivre à quel moment une ligne pour les nouveaux enregistrements est nécessaire dans le modèle de données et quand annuler l’ajout de la ligne. L’implémentation exacte de cette fonctionnalité dépend de l’implémentation du modèle de données et sa sémantique de transaction, par exemple, si la validation étendue est au niveau de la cellule ou la ligne. Pour plus d’informations, consultez [Mode virtuel dans le contrôle DataGridView Windows Forms](virtual-mode-in-the-windows-forms-datagridview-control.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded?displayProperty=nameWithType>
- [Saisie de données dans le contrôle DataGridView Windows Forms](data-entry-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms](specify-default-values-for-new-rows-in-the-datagrid.md)
