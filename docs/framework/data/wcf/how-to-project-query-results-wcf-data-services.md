---
title: 'Procédure : Résultats de requête de projet (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- projection [WCF Data Services]
- WCF Data Services, projection
- query projection [WCF Data Services]
- WCF Data Services, querying
ms.assetid: 474ac625-8770-43ba-8320-d3315ea9530f
ms.openlocfilehash: 4b0646c2ad45a86691b86b1dd5f112f598ee2dfd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59974787"
---
# <a name="how-to-project-query-results-wcf-data-services"></a>Procédure : Résultats de requête de projet (WCF Data Services)
La projection fournit un mécanisme permettant de réduire la quantité de données retournées par une requête en spécifiant que seules certaines propriétés d'une entité doivent être retournées dans la réponse. Vous pouvez effectuer des projections sur les résultats d’une [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] interroger à l’aide de la `$select` option de requête ou à l’aide de la [sélectionnez](~/docs/csharp/language-reference/keywords/select-clause.md) clause ([sélectionnez](~/docs/visual-basic/language-reference/queries/select-clause.md) en Visual Basic) dans une requête LINQ. Pour plus d’informations, consultez [interrogation du Service de données](../../../../docs/framework/data/wcf/querying-the-data-service-wcf-data-services.md).  
  
 L'exemple dans cette rubrique utilise l'exemple de service de données Northwind et des classes de service de données clientes générées automatiquement. Ce service et les classes de données client sont créés lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre une requête LINQ qui projette des entités Customers dans un nouveau type CustomerAddress, qui contient uniquement des propriétés spécifiques à l'adresse ainsi que la propriété d'identité. Cette classe `CustomerAddress` est définie sur le client et est attribuée de sorte que la bibliothèque cliente puisse le reconnaître comme un type d'entité.  
  
 [!code-csharp[Astoria Northwind Client#SelectCustomerAddress](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#selectcustomeraddress)]
 [!code-vb[Astoria Northwind Client#SelectCustomerAddress](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#selectcustomeraddress)]  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre une requête LINQ qui projette les entités Customers renvoyées dans un nouveau type CustomerAddressNonEntity, qui contient uniquement des propriétés spécifiques à l'adresse et aucune propriété d'identité. Cette classe `CustomerAddressNonEntity` est définie sur le client et n'est pas attribuée comme un type d'entité.  
  
 [!code-csharp[Astoria Northwind Client#SelectCustomerAddressNonEntity](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#selectcustomeraddressnonentity)]
 [!code-vb[Astoria Northwind Client#SelectCustomerAddressNonEntity](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#selectcustomeraddressnonentity)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre les définitions de la `CustomerAddress` et `CustomerAddressNonEntity` types qui sont utilisés dans les exemples précédents.  
  
 [!code-csharp[Astoria Northwind Client#CustomerAddressDefinition](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/customeraddress.cs#customeraddressdefinition)]
 [!code-vb[Astoria Northwind Client#CustomerAddressDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/customeraddress.vb#customeraddressdefinition)]
