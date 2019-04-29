---
title: Sémantique de comparaison (Entity SQL)
ms.date: 03/30/2017
ms.assetid: b36ce28a-2fe4-4236-b782-e5f7c054deae
ms.openlocfilehash: 6b4c4177ebd6c45e00a1ac7774e40a43e0c14a74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61605964"
---
# <a name="comparison-semantics-entity-sql"></a><span data-ttu-id="824cd-102">Sémantique de comparaison (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="824cd-102">Comparison Semantics (Entity SQL)</span></span>
<span data-ttu-id="824cd-103">L'exécution des opérateurs [!INCLUDE[esql](../../../../../../includes/esql-md.md)] suivants implique une comparaison d'instances de type :</span><span class="sxs-lookup"><span data-stu-id="824cd-103">Performing any of the following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] operators involves comparison of type instances:</span></span>  
  
## <a name="explicit-comparison"></a><span data-ttu-id="824cd-104">Comparaison explicite</span><span class="sxs-lookup"><span data-stu-id="824cd-104">Explicit comparison</span></span>  
 <span data-ttu-id="824cd-105">Opérations d'égalité :</span><span class="sxs-lookup"><span data-stu-id="824cd-105">Equality operations:</span></span>  
  
- =  
  
- <span data-ttu-id="824cd-106">!=</span><span class="sxs-lookup"><span data-stu-id="824cd-106">!=</span></span>  
  
 <span data-ttu-id="824cd-107">Opérations de classement :</span><span class="sxs-lookup"><span data-stu-id="824cd-107">Ordering operations:</span></span>  
  
- <  
  
- \<=  
  
- \>  
  
- \>=  
  
 <span data-ttu-id="824cd-108">Opérations relatives à la possibilité de valeurs NULL :</span><span class="sxs-lookup"><span data-stu-id="824cd-108">Nullability operations:</span></span>  
  
- <span data-ttu-id="824cd-109">IS NULL</span><span class="sxs-lookup"><span data-stu-id="824cd-109">IS NULL</span></span>  
  
- <span data-ttu-id="824cd-110">IS NOT NULL</span><span class="sxs-lookup"><span data-stu-id="824cd-110">IS NOT NULL</span></span>  
  
## <a name="explicit-distinction"></a><span data-ttu-id="824cd-111">Distinction explicite</span><span class="sxs-lookup"><span data-stu-id="824cd-111">Explicit distinction</span></span>  
 <span data-ttu-id="824cd-112">Distinction d'égalité :</span><span class="sxs-lookup"><span data-stu-id="824cd-112">Equality distinction:</span></span>  
  
- <span data-ttu-id="824cd-113">DISTINCT</span><span class="sxs-lookup"><span data-stu-id="824cd-113">DISTINCT</span></span>  
  
- <span data-ttu-id="824cd-114">GROUP BY</span><span class="sxs-lookup"><span data-stu-id="824cd-114">GROUP BY</span></span>  
  
 <span data-ttu-id="824cd-115">Distinction de classement :</span><span class="sxs-lookup"><span data-stu-id="824cd-115">Ordering distinction:</span></span>  
  
- <span data-ttu-id="824cd-116">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="824cd-116">ORDER BY</span></span>  
  
## <a name="implicit-distinction"></a><span data-ttu-id="824cd-117">Distinction implicite</span><span class="sxs-lookup"><span data-stu-id="824cd-117">Implicit distinction</span></span>  
 <span data-ttu-id="824cd-118">Opérations et prédicats de définition (égalité) :</span><span class="sxs-lookup"><span data-stu-id="824cd-118">Set operations and predicates (equality):</span></span>  
  
- <span data-ttu-id="824cd-119">UNION</span><span class="sxs-lookup"><span data-stu-id="824cd-119">UNION</span></span>  
  
- <span data-ttu-id="824cd-120">INTERSECT</span><span class="sxs-lookup"><span data-stu-id="824cd-120">INTERSECT</span></span>  
  
- <span data-ttu-id="824cd-121">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="824cd-121">EXCEPT</span></span>  
  
- <span data-ttu-id="824cd-122">SET</span><span class="sxs-lookup"><span data-stu-id="824cd-122">SET</span></span>  
  
- <span data-ttu-id="824cd-123">OVERLAPS</span><span class="sxs-lookup"><span data-stu-id="824cd-123">OVERLAPS</span></span>  
  
 <span data-ttu-id="824cd-124">Prédicats d'élément (égalité) :</span><span class="sxs-lookup"><span data-stu-id="824cd-124">Item predicates (equality):</span></span>  
  
- <span data-ttu-id="824cd-125">IN</span><span class="sxs-lookup"><span data-stu-id="824cd-125">IN</span></span>  
  
## <a name="supported-combinations"></a><span data-ttu-id="824cd-126">Combinaisons prises en charge</span><span class="sxs-lookup"><span data-stu-id="824cd-126">Supported Combinations</span></span>  
 <span data-ttu-id="824cd-127">Le tableau suivant répertorie toutes les combinaisons prises en charge des opérateurs de comparaison pour chaque type :</span><span class="sxs-lookup"><span data-stu-id="824cd-127">The following table shows all the supported combinations of comparison operators for each kind of type:</span></span>  
  
|<span data-ttu-id="824cd-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="824cd-128">**Type**</span></span>|**=**<br /><br /> <span data-ttu-id="824cd-129">**\!=**</span><span class="sxs-lookup"><span data-stu-id="824cd-129">**!=**</span></span>|<span data-ttu-id="824cd-130">**GROUP BY**</span><span class="sxs-lookup"><span data-stu-id="824cd-130">**GROUP BY**</span></span><br /><br /> <span data-ttu-id="824cd-131">**DISTINCT**</span><span class="sxs-lookup"><span data-stu-id="824cd-131">**DISTINCT**</span></span>|<span data-ttu-id="824cd-132">**UNION**</span><span class="sxs-lookup"><span data-stu-id="824cd-132">**UNION**</span></span><br /><br /> <span data-ttu-id="824cd-133">**INTERSECT**</span><span class="sxs-lookup"><span data-stu-id="824cd-133">**INTERSECT**</span></span><br /><br /> <span data-ttu-id="824cd-134">**EXCEPT**</span><span class="sxs-lookup"><span data-stu-id="824cd-134">**EXCEPT**</span></span><br /><br /> <span data-ttu-id="824cd-135">**SET**</span><span class="sxs-lookup"><span data-stu-id="824cd-135">**SET**</span></span><br /><br /> <span data-ttu-id="824cd-136">**OVERLAPS**</span><span class="sxs-lookup"><span data-stu-id="824cd-136">**OVERLAPS**</span></span>|<span data-ttu-id="824cd-137">**IN**</span><span class="sxs-lookup"><span data-stu-id="824cd-137">**IN**</span></span>|<span data-ttu-id="824cd-138">**<   <=**</span><span class="sxs-lookup"><span data-stu-id="824cd-138">**<   <=**</span></span><br /><br /> <span data-ttu-id="824cd-139">**>   >=**</span><span class="sxs-lookup"><span data-stu-id="824cd-139">**>   >=**</span></span>|<span data-ttu-id="824cd-140">**ORDER BY**</span><span class="sxs-lookup"><span data-stu-id="824cd-140">**ORDER BY**</span></span>|<span data-ttu-id="824cd-141">**A LA VALEUR NULL**</span><span class="sxs-lookup"><span data-stu-id="824cd-141">**IS NULL**</span></span><br /><br /> <span data-ttu-id="824cd-142">**N’EST PAS NULL**</span><span class="sxs-lookup"><span data-stu-id="824cd-142">**IS NOT NULL**</span></span>|  
|-|-|-|-|-|-|-|-|  
|<span data-ttu-id="824cd-143">Type d'entité</span><span class="sxs-lookup"><span data-stu-id="824cd-143">Entity type</span></span>|<span data-ttu-id="824cd-144">Ref<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-144">Ref<sup>1</sup></span></span>|<span data-ttu-id="824cd-145">Toutes les propriétés<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-145">All properties<sup>2</sup></span></span>|<span data-ttu-id="824cd-146">Toutes les propriétés<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-146">All properties<sup>2</sup></span></span>|<span data-ttu-id="824cd-147">Toutes les propriétés<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-147">All properties<sup>2</sup></span></span>|<span data-ttu-id="824cd-148">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-148">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-149">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-149">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-150">Ref<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-150">Ref<sup>1</sup></span></span>|  
|<span data-ttu-id="824cd-151">Type complexe</span><span class="sxs-lookup"><span data-stu-id="824cd-151">Complex type</span></span>|<span data-ttu-id="824cd-152">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-152">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-153">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-153">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-154">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-154">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-155">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-155">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-156">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-156">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-157">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-157">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-158">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-158">Throw<sup>3</sup></span></span>|  
|<span data-ttu-id="824cd-159">Ligne</span><span class="sxs-lookup"><span data-stu-id="824cd-159">Row</span></span>|<span data-ttu-id="824cd-160">Toutes les propriétés<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-160">All properties<sup>4</sup></span></span>|<span data-ttu-id="824cd-161">Toutes les propriétés<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-161">All properties<sup>4</sup></span></span>|<span data-ttu-id="824cd-162">Toutes les propriétés<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-162">All properties<sup>4</sup></span></span>|<span data-ttu-id="824cd-163">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-163">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-164">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-164">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-165">Toutes les propriétés<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-165">All properties<sup>4</sup></span></span>|<span data-ttu-id="824cd-166">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-166">Throw<sup>3</sup></span></span>|  
|<span data-ttu-id="824cd-167">Type primitif</span><span class="sxs-lookup"><span data-stu-id="824cd-167">Primitive type</span></span>|<span data-ttu-id="824cd-168">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-168">Provider-specific</span></span>|<span data-ttu-id="824cd-169">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-169">Provider-specific</span></span>|<span data-ttu-id="824cd-170">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-170">Provider-specific</span></span>|<span data-ttu-id="824cd-171">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-171">Provider-specific</span></span>|<span data-ttu-id="824cd-172">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-172">Provider-specific</span></span>|<span data-ttu-id="824cd-173">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-173">Provider-specific</span></span>|<span data-ttu-id="824cd-174">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="824cd-174">Provider-specific</span></span>|  
|<span data-ttu-id="824cd-175">Multiset</span><span class="sxs-lookup"><span data-stu-id="824cd-175">Multiset</span></span>|<span data-ttu-id="824cd-176">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-176">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-177">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-177">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-178">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-178">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-179">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-179">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-180">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-180">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-181">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-181">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-182">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-182">Throw<sup>3</sup></span></span>|  
|<span data-ttu-id="824cd-183">Ref</span><span class="sxs-lookup"><span data-stu-id="824cd-183">Ref</span></span>|<span data-ttu-id="824cd-184">Oui<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-184">Yes<sup>5</sup></span></span>|<span data-ttu-id="824cd-185">Oui<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-185">Yes<sup>5</sup></span></span>|<span data-ttu-id="824cd-186">Oui<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-186">Yes<sup>5</sup></span></span>|<span data-ttu-id="824cd-187">Oui<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-187">Yes<sup>5</sup></span></span>|<span data-ttu-id="824cd-188">Throw</span><span class="sxs-lookup"><span data-stu-id="824cd-188">Throw</span></span>|<span data-ttu-id="824cd-189">Throw</span><span class="sxs-lookup"><span data-stu-id="824cd-189">Throw</span></span>|<span data-ttu-id="824cd-190">Oui<sup>5</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-190">Yes<sup>5</sup></span></span>|  
|<span data-ttu-id="824cd-191">Association</span><span class="sxs-lookup"><span data-stu-id="824cd-191">Association</span></span><br /><br /> <span data-ttu-id="824cd-192">type</span><span class="sxs-lookup"><span data-stu-id="824cd-192">type</span></span>|<span data-ttu-id="824cd-193">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-193">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-194">Throw</span><span class="sxs-lookup"><span data-stu-id="824cd-194">Throw</span></span>|<span data-ttu-id="824cd-195">Throw</span><span class="sxs-lookup"><span data-stu-id="824cd-195">Throw</span></span>|<span data-ttu-id="824cd-196">Throw</span><span class="sxs-lookup"><span data-stu-id="824cd-196">Throw</span></span>|<span data-ttu-id="824cd-197">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-197">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-198">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-198">Throw<sup>3</sup></span></span>|<span data-ttu-id="824cd-199">Throw<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-199">Throw<sup>3</sup></span></span>|  
  
 <span data-ttu-id="824cd-200"><sup>1</sup>les références des instances du type d’entité donnée sont comparées implicitement, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="824cd-200"><sup>1</sup>The references of the given entity type instances are implicitly compared, as shown in the following example:</span></span>  
  
```  
SELECT p1, p2   
FROM AdventureWorksEntities.Product AS p1   
     JOIN AdventureWorksEntities.Product AS p2   
WHERE p1 != p2 OR p1 IS NULL  
```  
  
 <span data-ttu-id="824cd-201">Une instance d'entité ne peut pas être comparée à une référence explicite.</span><span class="sxs-lookup"><span data-stu-id="824cd-201">An entity instance cannot be compared to an explicit reference.</span></span> <span data-ttu-id="824cd-202">Lors d'une telle tentative, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="824cd-202">If this is attempted, an exception is thrown.</span></span> <span data-ttu-id="824cd-203">Par exemple, la requête suivante lève une exception :</span><span class="sxs-lookup"><span data-stu-id="824cd-203">For example, the following query will throw an exception:</span></span>  
  
```  
SELECT p1, p2   
FROM AdventureWorksEntities.Product AS p1   
     JOIN AdventureWorksEntities.Product AS p2   
WHERE p1 != REF(p2)  
```  
  
 <span data-ttu-id="824cd-204"><sup>2</sup>propriétés de types complexes sont aplanies avant d’être envoyés au magasin, afin de pouvoir être comparées (tant que toutes leurs propriétés peuvent être comparées).</span><span class="sxs-lookup"><span data-stu-id="824cd-204"><sup>2</sup>Properties of complex types are flattened out before being sent to the store, so they become comparable (as long as all their properties are comparable).</span></span> <span data-ttu-id="824cd-205">Consultez également <sup>4.</sup></span><span class="sxs-lookup"><span data-stu-id="824cd-205">Also see <sup>4.</sup></span></span>  
  
 <span data-ttu-id="824cd-206"><sup>3</sup>runtime de l’Entity Framework détecte le cas non pris en charge et lève une exception explicite sans engager le fournisseur/magasin.</span><span class="sxs-lookup"><span data-stu-id="824cd-206"><sup>3</sup>The Entity Framework runtime detects the unsupported case and throws a meaningful exception without engaging the provider/store.</span></span>  
  
 <span data-ttu-id="824cd-207"><sup>4</sup>une tentative est faite pour comparer toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="824cd-207"><sup>4</sup>An attempt is made to compare all properties.</span></span> <span data-ttu-id="824cd-208">Si une propriété est d'un type non comparable, tel que text, ntext ou image, une exception de serveur peut être levée.</span><span class="sxs-lookup"><span data-stu-id="824cd-208">If there is a property that is of a non-comparable type, such as text, ntext, or image, a server exception might be thrown.</span></span>  
  
 <span data-ttu-id="824cd-209"><sup>5</sup>tous les éléments individuels des références sont comparés (Cela inclut le nom de jeu d’entités et de toutes les propriétés de clé du type d’entité).</span><span class="sxs-lookup"><span data-stu-id="824cd-209"><sup>5</sup>All individual elements of the references are compared (this includes the entity set name and all the key properties of the entity type).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="824cd-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="824cd-210">See also</span></span>

- [<span data-ttu-id="824cd-211">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="824cd-211">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
