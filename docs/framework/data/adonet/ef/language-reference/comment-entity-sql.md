---
title: -- (Commentaire) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5d9de735-2099-47f1-b7e7-60856f494924
ms.openlocfilehash: 4b3c801999d520a775c1a7026c945c027145b59d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32764162"
---
# <a name="---comment-entity-sql"></a><span data-ttu-id="ed8f4-102">-- (Commentaire) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="ed8f4-102">-- (Comment) (Entity SQL)</span></span>
<span data-ttu-id="ed8f4-103">Les requêtes[!INCLUDE[esql](../../../../../../includes/esql-md.md)] peuvent contenir des commentaires.</span><span class="sxs-lookup"><span data-stu-id="ed8f4-103">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries can contain comments.</span></span> <span data-ttu-id="ed8f4-104">Deux tirets (`--`) marquent le début d'une ligne de commentaire.</span><span class="sxs-lookup"><span data-stu-id="ed8f4-104">Two dashes (`--`) start a comment line.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed8f4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed8f4-105">Syntax</span></span>  
  
```  
-- text_of_comment  
```  
  
## <a name="arguments"></a><span data-ttu-id="ed8f4-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="ed8f4-106">Arguments</span></span>  
 `text_of_comment`  
 <span data-ttu-id="ed8f4-107">Chaîne de caractères contenant le texte du commentaire.</span><span class="sxs-lookup"><span data-stu-id="ed8f4-107">Is the character string that contains the text of the comment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed8f4-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed8f4-108">Example</span></span>  
 <span data-ttu-id="ed8f4-109">La requête Entity SQL ci-dessous montre comment utiliser les commentaires.</span><span class="sxs-lookup"><span data-stu-id="ed8f4-109">The following Entity SQL query demonstrates how to use comments.</span></span> <span data-ttu-id="ed8f4-110">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="ed8f4-110">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="ed8f4-111">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ed8f4-111">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="ed8f4-112">Suivez la procédure indiquée dans [Guide pratique pour exécuter une requête qui retourne les résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="ed8f4-112">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="ed8f4-113">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="ed8f4-113">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#COMMENT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#comment)]  
  
## <a name="see-also"></a><span data-ttu-id="ed8f4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed8f4-114">See Also</span></span>  
 [<span data-ttu-id="ed8f4-115">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="ed8f4-115">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
 [<span data-ttu-id="ed8f4-116">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="ed8f4-116">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
