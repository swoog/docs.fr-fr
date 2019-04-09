---
title: 'Procédure : Exécuter une requête paramétrable Entity SQL avec EntityCommand'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e93fea43-7e03-4d7d-9fee-2517b8b88cba
ms.openlocfilehash: 252d04ce96e222526bfd3d3e0b798f1c5edd2c8b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079706"
---
# <a name="how-to-execute-a-parameterized-entity-sql-query-using-entitycommand"></a>Procédure : Exécuter une requête paramétrable Entity SQL avec EntityCommand
Cette rubrique montre comment exécuter un [!INCLUDE[esql](../../../../../includes/esql-md.md)] requête comportant des paramètres à l’aide un <xref:System.Data.EntityClient.EntityCommand> objet.  
  
### <a name="to-run-the-code-in-this-example"></a>Pour exécuter le code de cet exemple  
  
1.  Ajouter le [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) à votre projet et configurez votre projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Pour plus d'informations, voir [Procédure : Utilisez l’Assistant Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).  
  
2.  Dans la page de codes de votre application, ajoutez les instructions `using` (`Imports` en Visual Basic) suivantes :  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment construire une chaîne de requête comportant deux paramètres. Il crée ensuite un objet <xref:System.Data.EntityClient.EntityCommand>, ajoute deux paramètres à la collection <xref:System.Data.EntityClient.EntityParameter> de cet objet <xref:System.Data.EntityClient.EntityCommand>, puis itère au sein de la collection d’éléments `Contact`.  
  
 [!code-csharp[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#parameterizedquerywithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#parameterizedquerywithentitycommand)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : Exécuter une requête paramétrable](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))
- [Langage d'Entity SQL](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
