---
title: MULTISET (Entity SQL)
ms.date: 03/30/2017
ms.assetid: eb90a377-e47a-43a5-b308-e993b6d611e6
ms.openlocfilehash: df194a26b36ba50d7b55c3dda6053c883ba9b228
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32762921"
---
# <a name="multiset-entity-sql"></a><span data-ttu-id="74439-102">MULTISET (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="74439-102">MULTISET (Entity SQL)</span></span>
<span data-ttu-id="74439-103">Crée une instance d'un multiensemble à partir d'une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="74439-103">Creates an instance of a multiset from a list of values.</span></span> <span data-ttu-id="74439-104">Toutes les valeurs du constructeur MULTISET doivent être d'un type `T`compatible.</span><span class="sxs-lookup"><span data-stu-id="74439-104">All the values in the MULTISET constructor must be of a compatible type `T`.</span></span> <span data-ttu-id="74439-105">Les constructeurs de multiensemble vides ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="74439-105">Empty multiset constructors are not allowed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74439-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74439-106">Syntax</span></span>  
  
```  
MULTISET ( expression [{, expression }] )  
or  
{ expression [{, expression }] }  
```  
  
## <a name="arguments"></a><span data-ttu-id="74439-107">Arguments</span><span class="sxs-lookup"><span data-stu-id="74439-107">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="74439-108">Toute liste de valeurs valide.</span><span class="sxs-lookup"><span data-stu-id="74439-108">Any valid list of values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="74439-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="74439-109">Return Value</span></span>  
 <span data-ttu-id="74439-110">Une collection de type MULTISET\<T >.</span><span class="sxs-lookup"><span data-stu-id="74439-110">A collection of type MULTISET\<T>.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="74439-111">Notes</span><span class="sxs-lookup"><span data-stu-id="74439-111">Remarks</span></span>  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="74439-112">propose trois types de constructeurs : constructeurs de ligne, constructeurs d'objets et constructeurs de multiensemble (ou de collection).</span><span class="sxs-lookup"><span data-stu-id="74439-112"> provides three kinds of constructors: row constructors, object constructors, and multiset (or collection) constructors.</span></span> <span data-ttu-id="74439-113">Pour plus d’informations, consultez [construction de Types](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="74439-113">For more information, see [Constructing Types](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span></span>  
  
 <span data-ttu-id="74439-114">Le constructeur de multiensemble crée une instance d'un multiensemble à partir d'une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="74439-114">The multiset constructor creates an instance of a multiset from a list of values.</span></span> <span data-ttu-id="74439-115">Toutes les valeurs du constructeur doivent être d'un type compatible.</span><span class="sxs-lookup"><span data-stu-id="74439-115">All the values in the constructor must be of a compatible type.</span></span>  
  
 <span data-ttu-id="74439-116">Par exemple, l'expression suivante crée un multiensemble d'entiers.</span><span class="sxs-lookup"><span data-stu-id="74439-116">For example, the following expression creates a multiset of integers.</span></span>  
  
 `MULTISET(1, 2, 3)`  
  
 `{1, 2, 3}`  
  
> [!NOTE]
>  <span data-ttu-id="74439-117">Les littéraux de multiensemble imbriqués ne sont pris en charge que lorsqu'un multiensemble d'encapsulation a un seul élément de multiensemble ; par exemple, `{{1, 2, 3}}`.</span><span class="sxs-lookup"><span data-stu-id="74439-117">Nested multiset literals are only supported when a wrapping mutiset has a single multiset element; for example, `{{1, 2, 3}}`.</span></span> <span data-ttu-id="74439-118">Lorsqu'un multiensemble d'encapsulation a plusieurs éléments de multiensemble (par exemple, `{{1, 2}, {3, 4}}`), ils ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="74439-118">When the wrapping multiset has multiple multiset elements (for example, `{{1, 2}, {3, 4}}`), nested multiset literals are not supported.</span></span>  
  
## <a name="example"></a><span data-ttu-id="74439-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="74439-119">Example</span></span>  
 <span data-ttu-id="74439-120">La requête Entity SQL suivante utilise l'opérateur MULTISET pour créer une instance d'un multiensemble à partir d'une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="74439-120">The following Entity SQL query uses the MULTISET operator to create an instance of a multiset from a list of values.</span></span> <span data-ttu-id="74439-121">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="74439-121">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="74439-122">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="74439-122">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="74439-123">Suivez la procédure indiquée dans [Comment : exécuter une requête qui retourne les résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="74439-123">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="74439-124">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="74439-124">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#MULTISET](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#multiset)]  
  
## <a name="see-also"></a><span data-ttu-id="74439-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74439-125">See Also</span></span>  
 [<span data-ttu-id="74439-126">Construction de types</span><span class="sxs-lookup"><span data-stu-id="74439-126">Constructing Types</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md)  
 [<span data-ttu-id="74439-127">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="74439-127">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
