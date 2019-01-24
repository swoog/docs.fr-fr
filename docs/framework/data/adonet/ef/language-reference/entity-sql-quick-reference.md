---
title: Aide-mémoire Entity SQL
ms.date: 03/30/2017
ms.assetid: e53dad9e-5e83-426e-abb4-be3e78e3d6dc
ms.openlocfilehash: 20d8d1cb1e4b5cbf37dffcce6a7e79c2a4c265d3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539401"
---
# <a name="entity-sql-quick-reference"></a><span data-ttu-id="85d80-102">Aide-mémoire Entity SQL</span><span class="sxs-lookup"><span data-stu-id="85d80-102">Entity SQL Quick Reference</span></span>
<span data-ttu-id="85d80-103">Cette rubrique fournit un aide-mémoire sur les requêtes [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span><span class="sxs-lookup"><span data-stu-id="85d80-103">This topic provides a quick reference to [!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries.</span></span> <span data-ttu-id="85d80-104">Les requêtes dans cette rubrique sont basées sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="85d80-104">The queries in this topic are based on the AdventureWorks Sales model.</span></span>  
  
## <a name="literals"></a><span data-ttu-id="85d80-105">Littéraux</span><span class="sxs-lookup"><span data-stu-id="85d80-105">Literals</span></span>  
  
### <a name="string"></a><span data-ttu-id="85d80-106">Chaîne</span><span class="sxs-lookup"><span data-stu-id="85d80-106">String</span></span>  
 <span data-ttu-id="85d80-107">Les chaînes de caractères littérales peuvent être au format Unicode ou non-Unicode.</span><span class="sxs-lookup"><span data-stu-id="85d80-107">There are Unicode and non-Unicode character string literals.</span></span> <span data-ttu-id="85d80-108">Chaînes Unicode sont précédées de N. Par exemple, `N'hello'`.</span><span class="sxs-lookup"><span data-stu-id="85d80-108">Unicode strings are prepended with N. For example, `N'hello'`.</span></span>  
  
 <span data-ttu-id="85d80-109">Exemple de littéral de chaîne non-Unicode :</span><span class="sxs-lookup"><span data-stu-id="85d80-109">The following is an example of a Non-Unicode string literal:</span></span>  
  
```  
'hello'  
--same as  
"hello"  
```  
  
 <span data-ttu-id="85d80-110">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-110">Output:</span></span>  
  
|<span data-ttu-id="85d80-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-111">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-112">hello</span><span class="sxs-lookup"><span data-stu-id="85d80-112">hello</span></span>|  
  
### <a name="datetime"></a><span data-ttu-id="85d80-113">DateTime</span><span class="sxs-lookup"><span data-stu-id="85d80-113">DateTime</span></span>  
 <span data-ttu-id="85d80-114">Dans les littéraux DateTime, les parties date et heure sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="85d80-114">In DateTime literals, both date and time parts are mandatory.</span></span> <span data-ttu-id="85d80-115">Il n'existe pas de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="85d80-115">There are no default values.</span></span>  
  
 <span data-ttu-id="85d80-116">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-116">Example:</span></span>  
  
```  
DATETIME '2006-12-25 01:01:00.000'   
--same as  
DATETIME '2006-12-25 01:01'  
```  
  
 <span data-ttu-id="85d80-117">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-117">Output:</span></span>  
  
|<span data-ttu-id="85d80-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-118">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-119">25.12.06 01:01:00</span><span class="sxs-lookup"><span data-stu-id="85d80-119">12/25/2006 1:01:00 AM</span></span>|  
  
### <a name="integer"></a><span data-ttu-id="85d80-120">Integer</span><span class="sxs-lookup"><span data-stu-id="85d80-120">Integer</span></span>  
 <span data-ttu-id="85d80-121">Les littéraux d'entiers peuvent être de type Int32 (123), UInt32 (123U), Int64 (123L) et UInt64 (123UL).</span><span class="sxs-lookup"><span data-stu-id="85d80-121">Integer literals can be of type Int32 (123), UInt32 (123U), Int64 (123L), and UInt64 (123UL).</span></span>  
  
 <span data-ttu-id="85d80-122">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-122">Example:</span></span>  
  
```  
--a collection of integers  
{1, 2, 3}  
```  
  
 <span data-ttu-id="85d80-123">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-123">Output:</span></span>  
  
|<span data-ttu-id="85d80-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-124">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-125">1</span><span class="sxs-lookup"><span data-stu-id="85d80-125">1</span></span>|  
|<span data-ttu-id="85d80-126">2</span><span class="sxs-lookup"><span data-stu-id="85d80-126">2</span></span>|  
|<span data-ttu-id="85d80-127">3</span><span class="sxs-lookup"><span data-stu-id="85d80-127">3</span></span>|  
  
### <a name="other"></a><span data-ttu-id="85d80-128">Autre</span><span class="sxs-lookup"><span data-stu-id="85d80-128">Other</span></span>  
 <span data-ttu-id="85d80-129">Les autres littéraux pris en charge par [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont Guid, Binary, Float/Double, Decimal et la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="85d80-129">Other literals supported by [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are Guid, Binary, Float/Double, Decimal, and `null`.</span></span> <span data-ttu-id="85d80-130">Les littéraux NULL dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont considérés compatibles avec tous les autres types dans le modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="85d80-130">Null literals in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are considered to be compatible with every other type in the conceptual model.</span></span>  
  
## <a name="type-constructors"></a><span data-ttu-id="85d80-131">Constructeurs de type</span><span class="sxs-lookup"><span data-stu-id="85d80-131">Type Constructors</span></span>  
  
### <a name="row"></a><span data-ttu-id="85d80-132">ROW</span><span class="sxs-lookup"><span data-stu-id="85d80-132">ROW</span></span>  
 <span data-ttu-id="85d80-133">[LIGNE](../../../../../../docs/framework/data/adonet/ef/language-reference/row-entity-sql.md) construit une valeur anonyme, structurellement typée de (enregistrement) comme dans : `ROW(1 AS myNumber, ‘Name’ AS myName).`</span><span class="sxs-lookup"><span data-stu-id="85d80-133">[ROW](../../../../../../docs/framework/data/adonet/ef/language-reference/row-entity-sql.md) constructs an anonymous, structurally-typed (record) value as in: `ROW(1 AS myNumber, ‘Name’ AS myName).`</span></span>  
  
 <span data-ttu-id="85d80-134">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-134">Example:</span></span>  
  
```  
SELECT VALUE row (product.ProductID as ProductID, product.Name   
    as ProductName) FROM AdventureWorksEntities.Product AS product  
```  
  
 <span data-ttu-id="85d80-135">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-135">Output:</span></span>  
  
|<span data-ttu-id="85d80-136">ProductID</span><span class="sxs-lookup"><span data-stu-id="85d80-136">ProductID</span></span>|<span data-ttu-id="85d80-137">Nom</span><span class="sxs-lookup"><span data-stu-id="85d80-137">Name</span></span>|  
|---------------|----------|  
|<span data-ttu-id="85d80-138">1</span><span class="sxs-lookup"><span data-stu-id="85d80-138">1</span></span>|<span data-ttu-id="85d80-139">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="85d80-139">Adjustable Race</span></span>|  
|<span data-ttu-id="85d80-140">879</span><span class="sxs-lookup"><span data-stu-id="85d80-140">879</span></span>|<span data-ttu-id="85d80-141">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="85d80-141">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="85d80-142">712</span><span class="sxs-lookup"><span data-stu-id="85d80-142">712</span></span>|<span data-ttu-id="85d80-143">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="85d80-143">AWC Logo Cap</span></span>|  
|<span data-ttu-id="85d80-144">...</span><span class="sxs-lookup"><span data-stu-id="85d80-144">...</span></span>|<span data-ttu-id="85d80-145">...</span><span class="sxs-lookup"><span data-stu-id="85d80-145">...</span></span>|  
  
### <a name="multiset"></a><span data-ttu-id="85d80-146">MULTISET</span><span class="sxs-lookup"><span data-stu-id="85d80-146">MULTISET</span></span>  
 <span data-ttu-id="85d80-147">[MULTISET](../../../../../../docs/framework/data/adonet/ef/language-reference/multiset-entity-sql.md) construit des collections, telles que :</span><span class="sxs-lookup"><span data-stu-id="85d80-147">[MULTISET](../../../../../../docs/framework/data/adonet/ef/language-reference/multiset-entity-sql.md) constructs collections, such as:</span></span>  
  
 <span data-ttu-id="85d80-148">`MULTISET(1,2,2,3)` `--same as`-`{1,2,2,3}.`</span><span class="sxs-lookup"><span data-stu-id="85d80-148">`MULTISET(1,2,2,3)` `--same as`-`{1,2,2,3}.`</span></span>  
  
 <span data-ttu-id="85d80-149">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-149">Example:</span></span>  
  
```  
SELECT VALUE product FROM AdventureWorksEntities.Product AS product WHERE product.ListPrice IN MultiSet (125, 300)  
```  
  
 <span data-ttu-id="85d80-150">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-150">Output:</span></span>  
  
|<span data-ttu-id="85d80-151">ProductID</span><span class="sxs-lookup"><span data-stu-id="85d80-151">ProductID</span></span>|<span data-ttu-id="85d80-152">Nom</span><span class="sxs-lookup"><span data-stu-id="85d80-152">Name</span></span>|<span data-ttu-id="85d80-153">ProductNumber</span><span class="sxs-lookup"><span data-stu-id="85d80-153">ProductNumber</span></span>|<span data-ttu-id="85d80-154">…</span><span class="sxs-lookup"><span data-stu-id="85d80-154">…</span></span>|  
|---------------|----------|-------------------|-------|  
|<span data-ttu-id="85d80-155">842</span><span class="sxs-lookup"><span data-stu-id="85d80-155">842</span></span>|<span data-ttu-id="85d80-156">Touring-Panniers, Large</span><span class="sxs-lookup"><span data-stu-id="85d80-156">Touring-Panniers, Large</span></span>|<span data-ttu-id="85d80-157">PA-T100</span><span class="sxs-lookup"><span data-stu-id="85d80-157">PA-T100</span></span>|<span data-ttu-id="85d80-158">…</span><span class="sxs-lookup"><span data-stu-id="85d80-158">…</span></span>|  
  
### <a name="object"></a><span data-ttu-id="85d80-159">Object</span><span class="sxs-lookup"><span data-stu-id="85d80-159">Object</span></span>  
 <span data-ttu-id="85d80-160">[Nommé le constructeur de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/named-type-constructor-entity-sql.md) construit les objets définis par l’utilisateur (nommés) comme `person("abc", 12)`.</span><span class="sxs-lookup"><span data-stu-id="85d80-160">[Named Type Constructor](../../../../../../docs/framework/data/adonet/ef/language-reference/named-type-constructor-entity-sql.md) constructs (named) user-defined objects, such as `person("abc", 12)`.</span></span>  
  
 <span data-ttu-id="85d80-161">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-161">Example:</span></span>  
  
```  
SELECT VALUE AdventureWorksModel.SalesOrderDetail (o.SalesOrderDetailID, o.CarrierTrackingNumber, o.OrderQty,   
o.ProductID, o.SpecialOfferID, o.UnitPrice, o.UnitPriceDiscount,   
o.rowguid, o.ModifiedDate) FROM AdventureWorksEntities.SalesOrderDetail   
AS o  
```  
  
 <span data-ttu-id="85d80-162">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-162">Output:</span></span>  
  
|<span data-ttu-id="85d80-163">SalesOrderDetailID</span><span class="sxs-lookup"><span data-stu-id="85d80-163">SalesOrderDetailID</span></span>|<span data-ttu-id="85d80-164">CarrierTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="85d80-164">CarrierTrackingNumber</span></span>|<span data-ttu-id="85d80-165">OrderQty</span><span class="sxs-lookup"><span data-stu-id="85d80-165">OrderQty</span></span>|<span data-ttu-id="85d80-166">ProductID</span><span class="sxs-lookup"><span data-stu-id="85d80-166">ProductID</span></span>|<span data-ttu-id="85d80-167">...</span><span class="sxs-lookup"><span data-stu-id="85d80-167">...</span></span>|  
|------------------------|---------------------------|--------------|---------------|---------|  
|<span data-ttu-id="85d80-168">1</span><span class="sxs-lookup"><span data-stu-id="85d80-168">1</span></span>|<span data-ttu-id="85d80-169">4911-403C-98</span><span class="sxs-lookup"><span data-stu-id="85d80-169">4911-403C-98</span></span>|<span data-ttu-id="85d80-170">1</span><span class="sxs-lookup"><span data-stu-id="85d80-170">1</span></span>|<span data-ttu-id="85d80-171">776</span><span class="sxs-lookup"><span data-stu-id="85d80-171">776</span></span>|<span data-ttu-id="85d80-172">...</span><span class="sxs-lookup"><span data-stu-id="85d80-172">...</span></span>|  
|<span data-ttu-id="85d80-173">2</span><span class="sxs-lookup"><span data-stu-id="85d80-173">2</span></span>|<span data-ttu-id="85d80-174">4911-403C-98</span><span class="sxs-lookup"><span data-stu-id="85d80-174">4911-403C-98</span></span>|<span data-ttu-id="85d80-175">3</span><span class="sxs-lookup"><span data-stu-id="85d80-175">3</span></span>|<span data-ttu-id="85d80-176">777</span><span class="sxs-lookup"><span data-stu-id="85d80-176">777</span></span>|<span data-ttu-id="85d80-177">...</span><span class="sxs-lookup"><span data-stu-id="85d80-177">...</span></span>|  
|<span data-ttu-id="85d80-178">...</span><span class="sxs-lookup"><span data-stu-id="85d80-178">...</span></span>|<span data-ttu-id="85d80-179">...</span><span class="sxs-lookup"><span data-stu-id="85d80-179">...</span></span>|<span data-ttu-id="85d80-180">...</span><span class="sxs-lookup"><span data-stu-id="85d80-180">...</span></span>|<span data-ttu-id="85d80-181">...</span><span class="sxs-lookup"><span data-stu-id="85d80-181">...</span></span>|<span data-ttu-id="85d80-182">...</span><span class="sxs-lookup"><span data-stu-id="85d80-182">...</span></span>|  
  
## <a name="references"></a><span data-ttu-id="85d80-183">Références</span><span class="sxs-lookup"><span data-stu-id="85d80-183">References</span></span>  
  
### <a name="ref"></a><span data-ttu-id="85d80-184">REF</span><span class="sxs-lookup"><span data-stu-id="85d80-184">REF</span></span>  
 <span data-ttu-id="85d80-185">[REF](../../../../../../docs/framework/data/adonet/ef/language-reference/ref-entity-sql.md) crée une référence à une instance de type d’entité.</span><span class="sxs-lookup"><span data-stu-id="85d80-185">[REF](../../../../../../docs/framework/data/adonet/ef/language-reference/ref-entity-sql.md) creates a reference to an entity type instance.</span></span> <span data-ttu-id="85d80-186">Par exemple, la requête suivante retourne les références à chaque entité Order dans le jeu d'entités Orders :</span><span class="sxs-lookup"><span data-stu-id="85d80-186">For example, the following query returns references to each Order entity in the Orders entity set:</span></span>  
  
```  
SELECT REF(o) AS OrderID FROM Orders AS o  
```  
  
 <span data-ttu-id="85d80-187">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-187">Output:</span></span>  
  
|<span data-ttu-id="85d80-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-188">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-189">1</span><span class="sxs-lookup"><span data-stu-id="85d80-189">1</span></span>|  
|<span data-ttu-id="85d80-190">2</span><span class="sxs-lookup"><span data-stu-id="85d80-190">2</span></span>|  
|<span data-ttu-id="85d80-191">3</span><span class="sxs-lookup"><span data-stu-id="85d80-191">3</span></span>|  
|<span data-ttu-id="85d80-192">...</span><span class="sxs-lookup"><span data-stu-id="85d80-192">...</span></span>|  
  
 <span data-ttu-id="85d80-193">L'exemple suivant utilise l'opérateur d'extraction de propriété (.) pour accéder à une propriété d'entité.</span><span class="sxs-lookup"><span data-stu-id="85d80-193">The following example uses the property extraction operator (.) to access a property of an entity.</span></span> <span data-ttu-id="85d80-194">Lors de l'utilisation de l'opérateur d'extraction de propriété, la référence est automatiquement supprimée.</span><span class="sxs-lookup"><span data-stu-id="85d80-194">When the property extraction operator is used, the reference is automatically dereferenced.</span></span>  
  
 <span data-ttu-id="85d80-195">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-195">Example:</span></span>  
  
```  
SELECT VALUE REF(p).Name FROM   
    AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="85d80-196">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-196">Output:</span></span>  
  
|<span data-ttu-id="85d80-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-197">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-198">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="85d80-198">Adjustable Race</span></span>|  
|<span data-ttu-id="85d80-199">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="85d80-199">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="85d80-200">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="85d80-200">AWC Logo Cap</span></span>|  
|<span data-ttu-id="85d80-201">...</span><span class="sxs-lookup"><span data-stu-id="85d80-201">...</span></span>|  
  
### <a name="deref"></a><span data-ttu-id="85d80-202">DEREF</span><span class="sxs-lookup"><span data-stu-id="85d80-202">DEREF</span></span>  
 <span data-ttu-id="85d80-203">[DEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/deref-entity-sql.md) déréférence une valeur de référence et génère le résultat de ce déréférencement.</span><span class="sxs-lookup"><span data-stu-id="85d80-203">[DEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/deref-entity-sql.md) dereferences a reference value and produces the result of that dereference.</span></span> <span data-ttu-id="85d80-204">Par exemple, la requête suivante génère les entités Order pour chaque élément Order du jeu d'entités Orders : `SELECT DEREF(o2.r) FROM (SELECT REF(o) AS r FROM LOB.Orders AS o) AS o2`.</span><span class="sxs-lookup"><span data-stu-id="85d80-204">For example, the following query produces the Order entities for each Order in the Orders entity set: `SELECT DEREF(o2.r) FROM (SELECT REF(o) AS r FROM LOB.Orders AS o) AS o2`..</span></span>  
  
 <span data-ttu-id="85d80-205">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-205">Example:</span></span>  
  
```  
SELECT VALUE DEREF(REF(p)).Name FROM   
    AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="85d80-206">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-206">Output:</span></span>  
  
|<span data-ttu-id="85d80-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-207">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-208">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="85d80-208">Adjustable Race</span></span>|  
|<span data-ttu-id="85d80-209">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="85d80-209">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="85d80-210">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="85d80-210">AWC Logo Cap</span></span>|  
|<span data-ttu-id="85d80-211">...</span><span class="sxs-lookup"><span data-stu-id="85d80-211">...</span></span>|  
  
### <a name="createref-and-key"></a><span data-ttu-id="85d80-212">CREATEREF et KEY</span><span class="sxs-lookup"><span data-stu-id="85d80-212">CREATEREF AND KEY</span></span>  
 <span data-ttu-id="85d80-213">[CREATEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/createref-entity-sql.md) crée une référence qui passe une clé.</span><span class="sxs-lookup"><span data-stu-id="85d80-213">[CREATEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/createref-entity-sql.md) creates a reference passing a key.</span></span> <span data-ttu-id="85d80-214">[CLÉ](../../../../../../docs/framework/data/adonet/ef/language-reference/key-entity-sql.md) extrait la partie clé d’une expression avec référence de type.</span><span class="sxs-lookup"><span data-stu-id="85d80-214">[KEY](../../../../../../docs/framework/data/adonet/ef/language-reference/key-entity-sql.md) extracts the key portion of an expression with type reference.</span></span>  
  
 <span data-ttu-id="85d80-215">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-215">Example:</span></span>  
  
```  
SELECT VALUE Key(CreateRef(AdventureWorksEntities.Product, row(p.ProductID)))   
    FROM AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="85d80-216">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-216">Output:</span></span>  
  
|<span data-ttu-id="85d80-217">ProductID</span><span class="sxs-lookup"><span data-stu-id="85d80-217">ProductID</span></span>|  
|---------------|  
|<span data-ttu-id="85d80-218">980</span><span class="sxs-lookup"><span data-stu-id="85d80-218">980</span></span>|  
|<span data-ttu-id="85d80-219">365</span><span class="sxs-lookup"><span data-stu-id="85d80-219">365</span></span>|  
|<span data-ttu-id="85d80-220">771</span><span class="sxs-lookup"><span data-stu-id="85d80-220">771</span></span>|  
|<span data-ttu-id="85d80-221">...</span><span class="sxs-lookup"><span data-stu-id="85d80-221">...</span></span>|  
  
## <a name="functions"></a><span data-ttu-id="85d80-222">Fonctions</span><span class="sxs-lookup"><span data-stu-id="85d80-222">Functions</span></span>  
  
### <a name="canonical"></a><span data-ttu-id="85d80-223">Canoniques</span><span class="sxs-lookup"><span data-stu-id="85d80-223">Canonical</span></span>  
 <span data-ttu-id="85d80-224">L’espace de noms [fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md) est Edm, comme dans `Edm.Length("string")`.</span><span class="sxs-lookup"><span data-stu-id="85d80-224">The namespace for [canonical functions](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md) is Edm, as in `Edm.Length("string")`.</span></span> <span data-ttu-id="85d80-225">Vous n'avez pas besoin de spécifier l'espace de noms sauf si un autre espace de noms est importé et qu'il contient une fonction portant le même nom qu'une fonction canonique.</span><span class="sxs-lookup"><span data-stu-id="85d80-225">You do not have to specify the namespace unless another namespace is imported that contains a function with the same name as a canonical function.</span></span> <span data-ttu-id="85d80-226">Si deux espaces de noms partagent la même fonction, l'utilisateur doit spécifier le nom complet.</span><span class="sxs-lookup"><span data-stu-id="85d80-226">If two namespaces have the same function, the user should specific the full name.</span></span>  
  
 <span data-ttu-id="85d80-227">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-227">Example:</span></span>  
  
```  
SELECT Length(c. FirstName) As NameLen FROM   
    AdventureWorksEntities.Contact AS c   
    WHERE c.ContactID BETWEEN 10 AND 12  
```  
  
 <span data-ttu-id="85d80-228">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-228">Output:</span></span>  
  
|<span data-ttu-id="85d80-229">NameLen</span><span class="sxs-lookup"><span data-stu-id="85d80-229">NameLen</span></span>|  
|-------------|  
|<span data-ttu-id="85d80-230">6</span><span class="sxs-lookup"><span data-stu-id="85d80-230">6</span></span>|  
|<span data-ttu-id="85d80-231">6</span><span class="sxs-lookup"><span data-stu-id="85d80-231">6</span></span>|  
|<span data-ttu-id="85d80-232">5</span><span class="sxs-lookup"><span data-stu-id="85d80-232">5</span></span>|  
  
### <a name="microsoft-provider-specific"></a><span data-ttu-id="85d80-233">Spécifiques au fournisseur Microsoft</span><span class="sxs-lookup"><span data-stu-id="85d80-233">Microsoft Provider-Specific</span></span>  
 <span data-ttu-id="85d80-234">[Fonctions spécifiques au fournisseur de Microsoft](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md) se trouvent dans le `SqlServer` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="85d80-234">[Microsoft provider-specific functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md) are in the `SqlServer` namespace.</span></span>  
  
 <span data-ttu-id="85d80-235">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-235">Example:</span></span>  
  
```  
SELECT SqlServer.LEN(c.EmailAddress) As EmailLen FROM   
    AdventureWorksEntities.Contact AS c WHERE   
    c.ContactID BETWEEN 10 AND 12  
```  
  
 <span data-ttu-id="85d80-236">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-236">Output:</span></span>  
  
|<span data-ttu-id="85d80-237">EmailLen</span><span class="sxs-lookup"><span data-stu-id="85d80-237">EmailLen</span></span>|  
|--------------|  
|<span data-ttu-id="85d80-238">27</span><span class="sxs-lookup"><span data-stu-id="85d80-238">27</span></span>|  
|<span data-ttu-id="85d80-239">27</span><span class="sxs-lookup"><span data-stu-id="85d80-239">27</span></span>|  
|<span data-ttu-id="85d80-240">26</span><span class="sxs-lookup"><span data-stu-id="85d80-240">26</span></span>|  
  
## <a name="namespaces"></a><span data-ttu-id="85d80-241">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="85d80-241">Namespaces</span></span>  
 <span data-ttu-id="85d80-242">[À l’aide de](../../../../../../docs/framework/data/adonet/ef/language-reference/using-entity-sql.md) spécifie les espaces de noms utilisés dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="85d80-242">[USING](../../../../../../docs/framework/data/adonet/ef/language-reference/using-entity-sql.md) specifies namespaces used in a query expression.</span></span>  
  
 <span data-ttu-id="85d80-243">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-243">Example:</span></span>  
  
```  
using SqlServer; LOWER('AA');  
```  
  
 <span data-ttu-id="85d80-244">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-244">Output:</span></span>  
  
|<span data-ttu-id="85d80-245">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-245">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-246">aa</span><span class="sxs-lookup"><span data-stu-id="85d80-246">aa</span></span>|  
  
## <a name="paging"></a><span data-ttu-id="85d80-247">Pagination</span><span class="sxs-lookup"><span data-stu-id="85d80-247">Paging</span></span>  
 <span data-ttu-id="85d80-248">La pagination peut être exprimée en déclarant un [SKIP](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md) et [limite](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md) sous-clauses pour le [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md) clause.</span><span class="sxs-lookup"><span data-stu-id="85d80-248">Paging can be expressed by declaring a [SKIP](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md) and [LIMIT](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md) sub-clauses to the [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md) clause.</span></span>  
  
 <span data-ttu-id="85d80-249">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-249">Example:</span></span>  
  
```  
SELECT c.ContactID as ID, c.LastName as Name FROM   
    AdventureWorks.Contact AS c ORDER BY c.ContactID SKIP 9 LIMIT 3;  
```  
  
 <span data-ttu-id="85d80-250">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-250">Output:</span></span>  
  
|<span data-ttu-id="85d80-251">ID</span><span class="sxs-lookup"><span data-stu-id="85d80-251">ID</span></span>|<span data-ttu-id="85d80-252">Nom</span><span class="sxs-lookup"><span data-stu-id="85d80-252">Name</span></span>|  
|--------|----------|  
|<span data-ttu-id="85d80-253">10</span><span class="sxs-lookup"><span data-stu-id="85d80-253">10</span></span>|<span data-ttu-id="85d80-254">Adina</span><span class="sxs-lookup"><span data-stu-id="85d80-254">Adina</span></span>|  
|<span data-ttu-id="85d80-255">11</span><span class="sxs-lookup"><span data-stu-id="85d80-255">11</span></span>|<span data-ttu-id="85d80-256">Agcaoili</span><span class="sxs-lookup"><span data-stu-id="85d80-256">Agcaoili</span></span>|  
|<span data-ttu-id="85d80-257">12</span><span class="sxs-lookup"><span data-stu-id="85d80-257">12</span></span>|<span data-ttu-id="85d80-258">Aguilar</span><span class="sxs-lookup"><span data-stu-id="85d80-258">Aguilar</span></span>|  
  
## <a name="grouping"></a><span data-ttu-id="85d80-259">Regroupement</span><span class="sxs-lookup"><span data-stu-id="85d80-259">Grouping</span></span>  
 <span data-ttu-id="85d80-260">[REGROUPEMENT par](../../../../../../docs/framework/data/adonet/ef/language-reference/group-by-entity-sql.md) indique les groupes dans les objets retournés par une requête ([sélectionnez](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md)) expression doivent être placés.</span><span class="sxs-lookup"><span data-stu-id="85d80-260">[GROUPING BY](../../../../../../docs/framework/data/adonet/ef/language-reference/group-by-entity-sql.md) specifies groups into which objects returned by a query ([SELECT](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md)) expression are to be placed.</span></span>  
  
 <span data-ttu-id="85d80-261">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-261">Example:</span></span>  
  
```  
SELECT VALUE name FROM AdventureWorksEntities.Product as P   
    GROUP BY P.Name HAVING MAX(P.ListPrice) > 5  
```  
  
 <span data-ttu-id="85d80-262">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-262">Output:</span></span>  
  
|<span data-ttu-id="85d80-263">name</span><span class="sxs-lookup"><span data-stu-id="85d80-263">name</span></span>|  
|----------|  
|<span data-ttu-id="85d80-264">LL Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="85d80-264">LL Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="85d80-265">ML Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="85d80-265">ML Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="85d80-266">HL Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="85d80-266">HL Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="85d80-267">...</span><span class="sxs-lookup"><span data-stu-id="85d80-267">...</span></span>|  
  
## <a name="navigation"></a><span data-ttu-id="85d80-268">Navigation</span><span class="sxs-lookup"><span data-stu-id="85d80-268">Navigation</span></span>  
 <span data-ttu-id="85d80-269">L'opérateur de navigation de relations vous permet de parcourir la relation entre une entité (terminaison From) et une autre entité (terminaison To).</span><span class="sxs-lookup"><span data-stu-id="85d80-269">The relationship navigation operator allows you to navigate over the relationship from one entity (from end) to another (to end).</span></span> <span data-ttu-id="85d80-270">[NAVIGATE](../../../../../../docs/framework/data/adonet/ef/language-reference/navigate-entity-sql.md) accepte le type de relation qualifié comme \<espace de noms >.\< nom de type de relation >.</span><span class="sxs-lookup"><span data-stu-id="85d80-270">[NAVIGATE](../../../../../../docs/framework/data/adonet/ef/language-reference/navigate-entity-sql.md) takes the relationship type qualified as \<namespace>.\<relationship type name>.</span></span> <span data-ttu-id="85d80-271">Accédez retourne Ref\<T > Si la cardinalité de la terminaison to est 1.</span><span class="sxs-lookup"><span data-stu-id="85d80-271">Navigate returns Ref\<T> if the cardinality of the to end is 1.</span></span> <span data-ttu-id="85d80-272">Si la cardinalité de la terminaison to est n, la Collection < Ref\<T >> sera retourné.</span><span class="sxs-lookup"><span data-stu-id="85d80-272">If the cardinality of the to end is n, the Collection<Ref\<T>> will be returned.</span></span>  
  
 <span data-ttu-id="85d80-273">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-273">Example:</span></span>  
  
```  
SELECT a.AddressID, (SELECT VALUE DEREF(v) FROM   
    NAVIGATE(a, AdventureWorksModel.FK_SalesOrderHeader_Address_BillToAddressID) AS v)   
    FROM AdventureWorksEntities.Address AS a  
```  
  
 <span data-ttu-id="85d80-274">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-274">Output:</span></span>  
  
|<span data-ttu-id="85d80-275">AddressID</span><span class="sxs-lookup"><span data-stu-id="85d80-275">AddressID</span></span>|  
|---------------|  
|<span data-ttu-id="85d80-276">1</span><span class="sxs-lookup"><span data-stu-id="85d80-276">1</span></span>|  
|<span data-ttu-id="85d80-277">2</span><span class="sxs-lookup"><span data-stu-id="85d80-277">2</span></span>|  
|<span data-ttu-id="85d80-278">3</span><span class="sxs-lookup"><span data-stu-id="85d80-278">3</span></span>|  
|<span data-ttu-id="85d80-279">...</span><span class="sxs-lookup"><span data-stu-id="85d80-279">...</span></span>|  
  
## <a name="select-value-and-select"></a><span data-ttu-id="85d80-280">SELECT VALUE et SELECT</span><span class="sxs-lookup"><span data-stu-id="85d80-280">SELECT VALUE AND SELECT</span></span>  
  
### <a name="select-value"></a><span data-ttu-id="85d80-281">SELECT VALUE</span><span class="sxs-lookup"><span data-stu-id="85d80-281">SELECT VALUE</span></span>  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="85d80-282">fournit la clause SELECT VALUE pour ignorer la construction de ligne implicite.</span><span class="sxs-lookup"><span data-stu-id="85d80-282">provides the SELECT VALUE clause to skip the implicit row construction.</span></span> <span data-ttu-id="85d80-283">Un seul élément peut être spécifié dans une clause SELECT VALUE.</span><span class="sxs-lookup"><span data-stu-id="85d80-283">Only one item can be specified in a SELECT VALUE clause.</span></span> <span data-ttu-id="85d80-284">Lorsqu’une telle clause est utilisée, aucun wrapper de ligne n’est construit autour des éléments dans la clause SELECT, et une collection de la forme souhaitée peut être générée, par exemple : `SELECT VALUE a`.</span><span class="sxs-lookup"><span data-stu-id="85d80-284">When such a clause is used, no row wrapper is constructed around the items in the SELECT clause, and a collection of the desired shape can be produced, for example: `SELECT VALUE a`.</span></span>  
  
 <span data-ttu-id="85d80-285">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-285">Example:</span></span>  
  
```  
SELECT VALUE p.Name FROM AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="85d80-286">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-286">Output:</span></span>  
  
|<span data-ttu-id="85d80-287">Nom</span><span class="sxs-lookup"><span data-stu-id="85d80-287">Name</span></span>|  
|----------|  
|<span data-ttu-id="85d80-288">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="85d80-288">Adjustable Race</span></span>|  
|<span data-ttu-id="85d80-289">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="85d80-289">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="85d80-290">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="85d80-290">AWC Logo Cap</span></span>|  
|<span data-ttu-id="85d80-291">...</span><span class="sxs-lookup"><span data-stu-id="85d80-291">...</span></span>|  
  
### <a name="select"></a><span data-ttu-id="85d80-292">SELECT</span><span class="sxs-lookup"><span data-stu-id="85d80-292">SELECT</span></span>  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="85d80-293">fournit également le constructeur de ligne pour construire des lignes arbitraires.</span><span class="sxs-lookup"><span data-stu-id="85d80-293">also provides the row constructor to construct arbitrary rows.</span></span> <span data-ttu-id="85d80-294">SELECT extrait un ou plusieurs éléments de la projection et produit un enregistrement de données avec des champs, par exemple : `SELECT a, b, c`.</span><span class="sxs-lookup"><span data-stu-id="85d80-294">SELECT takes one or more elements in the projection and results in a data record with fields, for example: `SELECT a, b, c`.</span></span>  
  
 <span data-ttu-id="85d80-295">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-295">Example:</span></span>  
  
 <span data-ttu-id="85d80-296">SELECT p.Name, p.ProductID FROM AdventureWorksEntities.Product as p Output:</span><span class="sxs-lookup"><span data-stu-id="85d80-296">SELECT p.Name, p.ProductID FROM AdventureWorksEntities.Product as p Output:</span></span>  
  
|<span data-ttu-id="85d80-297">Nom</span><span class="sxs-lookup"><span data-stu-id="85d80-297">Name</span></span>|<span data-ttu-id="85d80-298">ProductID</span><span class="sxs-lookup"><span data-stu-id="85d80-298">ProductID</span></span>|  
|----------|---------------|  
|<span data-ttu-id="85d80-299">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="85d80-299">Adjustable Race</span></span>|<span data-ttu-id="85d80-300">1</span><span class="sxs-lookup"><span data-stu-id="85d80-300">1</span></span>|  
|<span data-ttu-id="85d80-301">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="85d80-301">All-Purpose Bike Stand</span></span>|<span data-ttu-id="85d80-302">879</span><span class="sxs-lookup"><span data-stu-id="85d80-302">879</span></span>|  
|<span data-ttu-id="85d80-303">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="85d80-303">AWC Logo Cap</span></span>|<span data-ttu-id="85d80-304">712</span><span class="sxs-lookup"><span data-stu-id="85d80-304">712</span></span>|  
|<span data-ttu-id="85d80-305">...</span><span class="sxs-lookup"><span data-stu-id="85d80-305">...</span></span>|<span data-ttu-id="85d80-306">...</span><span class="sxs-lookup"><span data-stu-id="85d80-306">...</span></span>|  
  
## <a name="case-expression"></a><span data-ttu-id="85d80-307">Expression CASE</span><span class="sxs-lookup"><span data-stu-id="85d80-307">CASE EXPRESSION</span></span>  
 <span data-ttu-id="85d80-308">Le [cas expression](../../../../../../docs/framework/data/adonet/ef/language-reference/case-entity-sql.md) évalue un ensemble d’expressions booléennes pour déterminer le résultat.</span><span class="sxs-lookup"><span data-stu-id="85d80-308">The [case expression](../../../../../../docs/framework/data/adonet/ef/language-reference/case-entity-sql.md) evaluates a set of Boolean expressions to determine the result.</span></span>  
  
 <span data-ttu-id="85d80-309">Exemple :</span><span class="sxs-lookup"><span data-stu-id="85d80-309">Example:</span></span>  
  
```  
CASE WHEN AVG({25,12,11}) < 100 THEN TRUE ELSE FALSE END  
```  
  
 <span data-ttu-id="85d80-310">Sortie :</span><span class="sxs-lookup"><span data-stu-id="85d80-310">Output:</span></span>  
  
|<span data-ttu-id="85d80-311">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d80-311">Value</span></span>|  
|-----------|  
|<span data-ttu-id="85d80-312">true</span><span class="sxs-lookup"><span data-stu-id="85d80-312">TRUE</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="85d80-313">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85d80-313">See also</span></span>
- [<span data-ttu-id="85d80-314">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="85d80-314">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [<span data-ttu-id="85d80-315">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="85d80-315">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
