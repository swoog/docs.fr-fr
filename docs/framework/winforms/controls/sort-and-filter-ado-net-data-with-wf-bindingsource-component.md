---
title: 'Procédure : trier et filtrer des données ADO.NET avec le composant BindingSource de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sorting data
- data sorting [Windows Forms], ADO.NET
- data [Windows Forms], filtering
- BindingSource component [Windows Forms], sorting and filtering data
- filtering [Windows Forms], ADO.NET
- data [Windows Forms], sorting
- ADO.NET [Windows Forms]
ms.assetid: 6c206daf-d706-4602-9dbe-435343052063
ms.openlocfilehash: d270155fa1e6b61d8537096a07a4b93fa3b79b35
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882194"
---
# <a name="how-to-sort-and-filter-adonet-data-with-the-windows-forms-bindingsource-component"></a>Procédure : trier et filtrer des données ADO.NET avec le composant BindingSource de Windows Forms
Vous pouvez exposer le tri et filtrage de <xref:System.Windows.Forms.BindingSource> contrôler via le <xref:System.Windows.Forms.BindingSource.Sort%2A> et <xref:System.Windows.Forms.BindingSource.Filter%2A> propriétés. Vous pouvez appliquer un tri simple lorsque la source de données sous-jacent est un <xref:System.ComponentModel.IBindingList>, et vous pouvez appliquer le filtrage et tri avancé lorsque la source de données est un <xref:System.ComponentModel.IBindingListView>. Le <xref:System.Windows.Forms.BindingSource.Sort%2A> propriété requiert une syntaxe ADO.NET standard : une chaîne représentant le nom d’une colonne de données dans la source de données suivie `ASC` ou `DESC` pour indiquer si la liste doit être triée dans l’ordre croissant ou décroissant. Vous pouvez définir le tri avancé ou un tri sur plusieurs colonnes en séparant chaque colonne par une virgule de séparation. Le <xref:System.Windows.Forms.BindingSource.Filter%2A> propriété prend une expression de chaîne.  
  
> [!NOTE]
>  Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).  
  
### <a name="to-filter-data-with-the-bindingsource"></a>Pour filtrer les données avec le composant BindingSource  
  
- Définir le <xref:System.Windows.Forms.BindingSource.Filter%2A> propriété à l’expression que vous souhaitez.  
  
     Dans l’exemple de code suivant, l’expression est un nom de colonne suivi par la valeur souhaitée pour la colonne.  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#11)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#11)]  
  
### <a name="to-sort-data-with-the-bindingsource"></a>Pour trier les données avec le composant BindingSource  
  
1. Définir le <xref:System.Windows.Forms.BindingSource.Sort%2A> propriété le nom de colonne que vous souhaitez suivie `ASC` ou `DESC` pour indiquer le croissant ou décroissant.  
  
2. Séparez plusieurs colonnes par une virgule.  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#12)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#12)]  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant charge les données à partir de la table Customers de la base de données Northwind dans un <xref:System.Windows.Forms.DataGridView> contrôler et filtre et trie les données affichées.  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Pour exécuter cet exemple, collez le code dans un formulaire qui contient un <xref:System.Windows.Forms.BindingSource> nommé `BindingSource1` et un <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1`. Gérer le <xref:System.Windows.Forms.Form.Load> événement pour le formulaire et appelez `InitializeSortedFilteredBindingSource` dans la méthode de gestionnaire d’événements load.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.BindingSource.Sort%2A>
- <xref:System.Windows.Forms.BindingSource.Filter%2A>
- [Guide pratique pour Installer les bases de données exemple](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/8b6y4c7s(v=vs.120))
- [BindingSource, composant](bindingsource-component.md)
