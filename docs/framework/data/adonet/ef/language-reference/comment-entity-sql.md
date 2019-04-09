---
title: -- (Commentaire) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5d9de735-2099-47f1-b7e7-60856f494924
ms.openlocfilehash: 40a0ee8f6bc2cf8fae5779ecb3d103c77dde161b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137174"
---
# <a name="---comment-entity-sql"></a><span data-ttu-id="77395-102">-- (Commentaire) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="77395-102">-- (Comment) (Entity SQL)</span></span>
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="77395-103">les requêtes peuvent contenir des commentaires.</span><span class="sxs-lookup"><span data-stu-id="77395-103">queries can contain comments.</span></span> <span data-ttu-id="77395-104">Deux tirets (`--`) marquent le début d'une ligne de commentaire.</span><span class="sxs-lookup"><span data-stu-id="77395-104">Two dashes (`--`) start a comment line.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77395-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77395-105">Syntax</span></span>  
  
```  
-- text_of_comment  
```  
  
## <a name="arguments"></a><span data-ttu-id="77395-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="77395-106">Arguments</span></span>  
 `text_of_comment`  
 <span data-ttu-id="77395-107">Chaîne de caractères contenant le texte du commentaire.</span><span class="sxs-lookup"><span data-stu-id="77395-107">Is the character string that contains the text of the comment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="77395-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="77395-108">Example</span></span>  
 <span data-ttu-id="77395-109">La requête Entity SQL ci-dessous montre comment utiliser les commentaires.</span><span class="sxs-lookup"><span data-stu-id="77395-109">The following Entity SQL query demonstrates how to use comments.</span></span> <span data-ttu-id="77395-110">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="77395-110">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="77395-111">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="77395-111">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="77395-112">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="77395-112">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="77395-113">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="77395-113">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#COMMENT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#comment)]  
  
## <a name="see-also"></a><span data-ttu-id="77395-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77395-114">See also</span></span>

- [<span data-ttu-id="77395-115">Vue d'ensemble d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="77395-115">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
- [<span data-ttu-id="77395-116">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="77395-116">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
