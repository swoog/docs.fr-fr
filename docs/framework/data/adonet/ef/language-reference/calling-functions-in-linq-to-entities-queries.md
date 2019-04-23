---
title: Appel de fonctions dans les requêtes LINQ to Entities
ms.date: 03/30/2017
ms.assetid: 12a525a9-727c-4464-a0c7-71a0ef541792
ms.openlocfilehash: 6fa1a7204a91a62c30e8683c449cc2be44132b4f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59312083"
---
# <a name="calling-functions-in-linq-to-entities-queries"></a><span data-ttu-id="c6e58-102">Appel de fonctions dans les requêtes LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="c6e58-102">Calling Functions in LINQ to Entities Queries</span></span>
<span data-ttu-id="c6e58-103">Les rubriques de cette section expliquent comment appeler des fonctions dans les requêtes LINQ to Entities.</span><span class="sxs-lookup"><span data-stu-id="c6e58-103">The topics in this section describe how to call functions in LINQ to Entities queries.</span></span>  
  
 <span data-ttu-id="c6e58-104">Les classes <xref:System.Data.Objects.EntityFunctions> et <xref:System.Data.Objects.SqlClient.SqlFunctions> donnent accès à des fonctions canoniques et de base de données dans le cadre d'Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="c6e58-104">The <xref:System.Data.Objects.EntityFunctions> and <xref:System.Data.Objects.SqlClient.SqlFunctions> classes provide access to canonical and database functions as part of the Entity Framework.</span></span> <span data-ttu-id="c6e58-105">Pour plus d'informations, voir [Procédure : Appeler des fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md) et [Comment : Appeler des fonctions de base de données](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c6e58-105">For more information, see [How to: Call Canonical Functions](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md) and [How to: Call Database Functions](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md).</span></span>  
  
 <span data-ttu-id="c6e58-106">L'appel d'une fonction personnalisée passe par trois étapes de base obligatoires :</span><span class="sxs-lookup"><span data-stu-id="c6e58-106">The process for calling a custom function requires three basic steps:</span></span>  
  
1. <span data-ttu-id="c6e58-107">Définissez une fonction dans votre modèle conceptuel ou déclarez-la dans votre modèle de stockage.</span><span class="sxs-lookup"><span data-stu-id="c6e58-107">Define a function in your conceptual model or declare a function in your storage model.</span></span>  
  
2. <span data-ttu-id="c6e58-108">Ajoutez une méthode à votre application et mappez-la à la fonction du modèle avec un objet <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute>.</span><span class="sxs-lookup"><span data-stu-id="c6e58-108">Add a method to your application and map it to the function in the model with an <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute>.</span></span>  
  
3. <span data-ttu-id="c6e58-109">Appelez la fonction dans une requête LINQ to Entities.</span><span class="sxs-lookup"><span data-stu-id="c6e58-109">Call the function in a LINQ to Entities query.</span></span>  
  
 <span data-ttu-id="c6e58-110">Pour plus d'informations, consultez les rubriques de cette section.</span><span class="sxs-lookup"><span data-stu-id="c6e58-110">For more information, see the topics in this section.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c6e58-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c6e58-111">In This Section</span></span>  
 [<span data-ttu-id="c6e58-112">Guide pratique pour Appeler des fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="c6e58-112">How to: Call Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md)  
  
 [<span data-ttu-id="c6e58-113">Guide pratique pour Appeler des fonctions de base de données</span><span class="sxs-lookup"><span data-stu-id="c6e58-113">How to: Call Database Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md)  
  
 [<span data-ttu-id="c6e58-114">Guide pratique pour Appeler des fonctions de base de données personnalisée</span><span class="sxs-lookup"><span data-stu-id="c6e58-114">How to: Call Custom Database Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-custom-database-functions.md)  
  
 [<span data-ttu-id="c6e58-115">Guide pratique pour Appeler des fonctions définies par le modèle dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="c6e58-115">How to: Call Model-Defined Functions in Queries</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-in-queries.md)  
  
 [<span data-ttu-id="c6e58-116">Guide pratique pour Appeler des fonctions définies par modèle comme méthodes d’objet</span><span class="sxs-lookup"><span data-stu-id="c6e58-116">How to: Call Model-Defined Functions as Object Methods</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-as-object-methods.md)  
  
## <a name="see-also"></a><span data-ttu-id="c6e58-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6e58-117">See also</span></span>

- [<span data-ttu-id="c6e58-118">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="c6e58-118">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
- [<span data-ttu-id="c6e58-119">Fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="c6e58-119">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
- <span data-ttu-id="c6e58-120">[vue d’ensemble du fichier .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c6e58-120">[.edmx File Overview](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))</span></span>
- <span data-ttu-id="c6e58-121">[Guide pratique pour Définir des fonctions personnalisées dans le modèle conceptuel](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456812(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c6e58-121">[How to: Define Custom Functions in the Conceptual Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456812(v=vs.100))</span></span>
