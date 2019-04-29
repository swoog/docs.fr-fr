---
title: Obtention d'une valeur unique à partir d'une base de données
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b38526cd-a62a-48cb-822a-e91dfa68e02d
ms.openlocfilehash: 5eb81fd2a64f06f1252f71e251e58df568e7407c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772071"
---
# <a name="obtaining-a-single-value-from-a-database"></a>Obtention d'une valeur unique à partir d'une base de données
Vous aurez peut-être besoin de retourner des informations de base de données qui sont simplement une valeur unique plutôt qu'une table ou un flux de données. Par exemple, vous souhaitez retourner le résultat d’une fonction d’agrégation telles que COUNT (\*), SUM (price) ou AVG (Quantity). Le **commande** objet offre la possibilité de retourner des valeurs uniques à l’aide de la **ExecuteScalar** (méthode). Le **ExecuteScalar** méthode est retournée, comme une valeur scalaire, la valeur de la première colonne de la première ligne du jeu de résultats.  
  
 L'exemple de code suivant insère une nouvelle valeur dans la base de données en utilisant un objet <xref:System.Data.SqlClient.SqlCommand>. La méthode <xref:System.Data.SqlClient.SqlCommand.ExecuteScalar%2A> est utilisée pour retourner la valeur de la colonne d'identité de l'enregistrement inséré.  
  
 [!code-csharp[DataWorks SqlCommand.ExecuteScalar#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlCommand.ExecuteScalar/CS/source.cs#1)]
 [!code-vb[DataWorks SqlCommand.ExecuteScalar#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlCommand.ExecuteScalar/VB/source.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [Exécution d’une commande](../../../../docs/framework/data/adonet/executing-a-command.md)
- [DbConnection, DbCommand et DbException](../../../../docs/framework/data/adonet/dbconnection-dbcommand-and-dbexception.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
