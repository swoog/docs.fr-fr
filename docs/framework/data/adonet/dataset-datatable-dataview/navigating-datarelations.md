---
title: Parcours des DataRelations
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e5e673f4-9b44-45ae-aaea-c504d1cc5d3e
ms.openlocfilehash: 0f19e08aba36d2e93033fb944efe848d4e1125e8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732776"
---
# <a name="navigating-datarelations"></a>Parcours des DataRelations
L'une des principales fonctions d'un objet <xref:System.Data.DataRelation> est de permettre de passer d'un objet <xref:System.Data.DataTable> à un autre à l'intérieur d'un objet <xref:System.Data.DataSet>. Cela vous permet de récupérer tous les connexe <xref:System.Data.DataRow> les objets **DataTable** lorsqu’un **DataRow** à partir d’un connexes **DataTable**. Par exemple, après avoir établi un **DataRelation** entre une table de clients et une table de commandes, vous pouvez récupérer toutes les lignes de commande pour une ligne de client spécifique à l’aide **GetChildRows**.  
  
 L’exemple de code suivant crée un **DataRelation** entre le **clients** table et le **commandes** table d’un **DataSet** et retourne toutes les commandes pour chaque client.  
  
 [!code-csharp[DataWorks Data.DataTableRelation#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks Data.DataTableRelation/CS/source.cs#1)]
 [!code-vb[DataWorks Data.DataTableRelation#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks Data.DataTableRelation/VB/source.vb#1)]  
  
 L'exemple suivant s'appuie sur le précédent, en créant des relations entre quatre tables et en explorant ces relations. Comme dans l’exemple précédent, **CustomerID** se rapporte la **clients** de la table vers le **commandes** table. Pour chaque client dans le **clients** table, toutes les lignes enfants de la **commandes** table sont déterminées, afin de retourner le nombre de commandes passées par un client et leurs **OrderID** valeurs.  
  
 L’exemple développé retourne également les valeurs à partir de la **OrderDetails** et **produits** tables. Le **commandes** table est associée à la **OrderDetails** à l’aide de la table **OrderID** pour déterminer, pour chaque commande client, de quels produits et quantités commandées. Étant donné que le **OrderDetails** table contient uniquement le **ProductID** d’un produit commandé, **OrderDetails** est liée à **produits** à l’aide de **ProductID** afin de retourner le **ProductName**. Dans cette relation, le **produits** est la table parente et la **Order Details** table est l’enfant. Par conséquent, lors de l’itération via la **OrderDetails** table, **GetParentRow** est appelée pour extraire la **ProductName** valeur.  
  
 Notez que lorsque le **DataRelation** est créé pour le **clients** et **commandes** tables, aucune valeur n’est spécifiée pour le **createConstraints**indicateur (la valeur par défaut est **true**). Cela suppose que toutes les les lignes dans le **commandes** table ont une **CustomerID** valeur qui existe dans le parent **clients** table. Si un **CustomerID** existe dans le **commandes** table qui n’existe pas dans le **clients** table, un <xref:System.Data.ForeignKeyConstraint> provoque une exception levée.  
  
 Lorsque la colonne enfant peut contenir des valeurs de la colonne parent ne contient-elle pas, définissez le **createConstraints** indicateur **false** lors de l’ajout du **DataRelation**. Dans l’exemple, le **createConstraints** indicateur a la valeur **false** pour le **DataRelation** entre le **commandes** table et le  **OrderDetails** table. Cela permet à l’application retourner tous les enregistrements à partir de la **OrderDetails** table et uniquement un sous-ensemble d’enregistrements à partir de la **commandes** table sans générer une exception au moment de l’exécution. La sortie de l’exemple développé se présente comme suit.  
  
```  
Customer ID: NORTS  
  Order ID: 10517  
        Order Date: 4/24/1997 12:00:00 AM  
           Product: Filo Mix  
          Quantity: 6  
           Product: Raclette Courdavault  
          Quantity: 4  
           Product: Outback Lager  
          Quantity: 6  
  Order ID: 11057  
        Order Date: 4/29/1998 12:00:00 AM  
           Product: Outback Lager  
          Quantity: 3  
```  
  
 L’exemple de code suivant est un exemple développé où les valeurs à partir de la **OrderDetails** et **produits** les tables sont retournées, avec uniquement un sous-ensemble des enregistrements dans la **commandes**table qui est retournée.  
  
 [!code-csharp[DataWorks Data.DataTableNavigation#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks Data.DataTableNavigation/CS/source.cs#1)]
 [!code-vb[DataWorks Data.DataTableNavigation#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks Data.DataTableNavigation/VB/source.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
