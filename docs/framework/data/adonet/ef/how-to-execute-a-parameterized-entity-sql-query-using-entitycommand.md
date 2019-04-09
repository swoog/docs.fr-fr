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
# <a name="how-to-execute-a-parameterized-entity-sql-query-using-entitycommand"></a><span data-ttu-id="e6e89-102">Procédure : Exécuter une requête paramétrable Entity SQL avec EntityCommand</span><span class="sxs-lookup"><span data-stu-id="e6e89-102">How to: Execute a Parameterized Entity SQL Query Using EntityCommand</span></span>
<span data-ttu-id="e6e89-103">Cette rubrique montre comment exécuter un [!INCLUDE[esql](../../../../../includes/esql-md.md)] requête comportant des paramètres à l’aide un <xref:System.Data.EntityClient.EntityCommand> objet.</span><span class="sxs-lookup"><span data-stu-id="e6e89-103">This topic shows how to execute an [!INCLUDE[esql](../../../../../includes/esql-md.md)] query that has parameters by using an <xref:System.Data.EntityClient.EntityCommand> object.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="e6e89-104">Pour exécuter le code de cet exemple</span><span class="sxs-lookup"><span data-stu-id="e6e89-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="e6e89-105">Ajouter le [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) à votre projet et configurez votre projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e6e89-105">Add the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="e6e89-106">Pour plus d'informations, voir [Procédure : Utilisez l’Assistant Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e6e89-106">For more information, see [How to: Use the Entity Data Model Wizard](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span></span>  
  
2.  <span data-ttu-id="e6e89-107">Dans la page de codes de votre application, ajoutez les instructions `using` (`Imports` en Visual Basic) suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6e89-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="e6e89-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="e6e89-108">Example</span></span>  
 <span data-ttu-id="e6e89-109">L'exemple suivant montre comment construire une chaîne de requête comportant deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="e6e89-109">The following example shows how to construct a query string with two parameters.</span></span> <span data-ttu-id="e6e89-110">Il crée ensuite un objet <xref:System.Data.EntityClient.EntityCommand>, ajoute deux paramètres à la collection <xref:System.Data.EntityClient.EntityParameter> de cet objet <xref:System.Data.EntityClient.EntityCommand>, puis itère au sein de la collection d’éléments `Contact`.</span><span class="sxs-lookup"><span data-stu-id="e6e89-110">It then creates an <xref:System.Data.EntityClient.EntityCommand>, adds two parameters to the <xref:System.Data.EntityClient.EntityParameter> collection of that <xref:System.Data.EntityClient.EntityCommand>, and iterates through the collection of `Contact` items.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#parameterizedquerywithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#parameterizedquerywithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="e6e89-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6e89-111">See also</span></span>

- [<span data-ttu-id="e6e89-112">Procédure : Exécuter une requête paramétrable</span><span class="sxs-lookup"><span data-stu-id="e6e89-112">How to: Execute a Parameterized Query</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))
- [<span data-ttu-id="e6e89-113">Langage d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="e6e89-113">Entity SQL Language</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
