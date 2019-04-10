---
title: BETWEEN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4dcdd754-ae01-4e78-bf28-8a117fb2b73e
ms.openlocfilehash: eae4387bcd5cbaf381ebf7169b6bc54d60328377
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59309301"
---
# <a name="between-entity-sql"></a><span data-ttu-id="554dc-102">BETWEEN (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="554dc-102">BETWEEN (Entity SQL)</span></span>
<span data-ttu-id="554dc-103">Détermine si une expression a pour résultat une valeur contenue dans une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="554dc-103">Determines whether an expression results in a value in a specified range.</span></span> <span data-ttu-id="554dc-104">Le [!INCLUDE[esql](../../../../../../includes/esql-md.md)] entre l’expression a les mêmes fonctionnalités que l’expression Transact-SQL BETWEEN.</span><span class="sxs-lookup"><span data-stu-id="554dc-104">The [!INCLUDE[esql](../../../../../../includes/esql-md.md)] BETWEEN expression has the same functionality as the Transact-SQL BETWEEN expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="554dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="554dc-105">Syntax</span></span>  
  
```  
expression [ NOT ] BETWEEN begin_expression AND end_expression    
```  
  
## <a name="arguments"></a><span data-ttu-id="554dc-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="554dc-106">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="554dc-107">Toute expression valide à tester dans la plage définie par `begin_expression` et `end_expression`.</span><span class="sxs-lookup"><span data-stu-id="554dc-107">Any valid expression to test for in the range defined by `begin_expression` and `end_expression`.</span></span> `expression` <span data-ttu-id="554dc-108">doit être du même type que les deux `begin_expression` et `end_expression`.</span><span class="sxs-lookup"><span data-stu-id="554dc-108">must be the same type as both `begin_expression` and `end_expression`.</span></span>  
  
 `begin_expression`  
 <span data-ttu-id="554dc-109">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="554dc-109">Any valid expression.</span></span> `begin_expression` <span data-ttu-id="554dc-110">doit être du même type que les deux `expression` et `end_expression`.</span><span class="sxs-lookup"><span data-stu-id="554dc-110">must be the same type as both `expression` and `end_expression`.</span></span> `begin_expression` <span data-ttu-id="554dc-111">doit être inférieur à `end_expression`, sinon la valeur de retour sera niée.</span><span class="sxs-lookup"><span data-stu-id="554dc-111">should be less than `end_expression`, else the return value will be negated.</span></span>  
  
 `end_expression`  
 <span data-ttu-id="554dc-112">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="554dc-112">Any valid expression.</span></span> `end_expression` <span data-ttu-id="554dc-113">doit être du même type que les deux `expression` et `begin_expression`.</span><span class="sxs-lookup"><span data-stu-id="554dc-113">must be the same type as both `expression` and `begin_expression`.</span></span>  
  
 <span data-ttu-id="554dc-114">NOT</span><span class="sxs-lookup"><span data-stu-id="554dc-114">NOT</span></span>  
 <span data-ttu-id="554dc-115">Indique que le résultat de BETWEEN est inversé.</span><span class="sxs-lookup"><span data-stu-id="554dc-115">Specifies that the result of BETWEEN be negated.</span></span>  
  
 <span data-ttu-id="554dc-116">AND</span><span class="sxs-lookup"><span data-stu-id="554dc-116">AND</span></span>  
 <span data-ttu-id="554dc-117">Espace réservé qui indique que `expression` doit se trouver dans la plage définie par `begin_expression` et `end_expression`.</span><span class="sxs-lookup"><span data-stu-id="554dc-117">Acts as a placeholder that indicates `expression` should be within the range indicated by `begin_expression` and `end_expression`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="554dc-118">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="554dc-118">Return Value</span></span>  
 `true` <span data-ttu-id="554dc-119">Si `expression` est comprise entre la plage indiquée par `begin_expression` et `end_expression`; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="554dc-119">if `expression` is between the range indicated by `begin_expression` and `end_expression`; otherwise, `false`.</span></span> `null` <span data-ttu-id="554dc-120">est retourné si `expression` est `null` ou si `begin_expression` ou `end_expression` est `null`.</span><span class="sxs-lookup"><span data-stu-id="554dc-120">will be returned if `expression` is `null` or if `begin_expression` or `end_expression` is `null`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="554dc-121">Notes</span><span class="sxs-lookup"><span data-stu-id="554dc-121">Remarks</span></span>  
 <span data-ttu-id="554dc-122">Pour spécifier un intervalle exclusif, utilisez le signe supérieur à (>) et inférieur à (<) opérateurs place de BETWEEN.</span><span class="sxs-lookup"><span data-stu-id="554dc-122">To specify an exclusive range, use the greater than (>) and less than (<) operators instead of BETWEEN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="554dc-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="554dc-123">Example</span></span>  
 <span data-ttu-id="554dc-124">La requête Entity SQL ci-dessous utilise l'opérateur BETWEEN pour déterminer si une expression génère une valeur située dans une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="554dc-124">The following Entity SQL query uses BETWEEN operator to determine whether an expression results in a value in a specified range.</span></span> <span data-ttu-id="554dc-125">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="554dc-125">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="554dc-126">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="554dc-126">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="554dc-127">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="554dc-127">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="554dc-128">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="554dc-128">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#BETWEEN](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#between)]  
  
## <a name="see-also"></a><span data-ttu-id="554dc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="554dc-129">See also</span></span>

- [<span data-ttu-id="554dc-130">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="554dc-130">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
