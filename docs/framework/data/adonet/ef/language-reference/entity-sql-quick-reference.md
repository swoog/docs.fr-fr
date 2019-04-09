---
title: Aide-mémoire Entity SQL
ms.date: 03/30/2017
ms.assetid: e53dad9e-5e83-426e-abb4-be3e78e3d6dc
ms.openlocfilehash: b4e3eaf8abd82b63fa2663b47f878ecfa9584897
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207069"
---
# <a name="entity-sql-quick-reference"></a><span data-ttu-id="68949-102">Aide-mémoire Entity SQL</span><span class="sxs-lookup"><span data-stu-id="68949-102">Entity SQL Quick Reference</span></span>
<span data-ttu-id="68949-103">Cette rubrique fournit un aide-mémoire sur les requêtes [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68949-103">This topic provides a quick reference to [!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries.</span></span> <span data-ttu-id="68949-104">Les requêtes dans cette rubrique sont basées sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="68949-104">The queries in this topic are based on the AdventureWorks Sales model.</span></span>  
  
## <a name="literals"></a><span data-ttu-id="68949-105">Littéraux</span><span class="sxs-lookup"><span data-stu-id="68949-105">Literals</span></span>  
  
### <a name="string"></a><span data-ttu-id="68949-106">Chaîne</span><span class="sxs-lookup"><span data-stu-id="68949-106">String</span></span>  
 <span data-ttu-id="68949-107">Les chaînes de caractères littérales peuvent être au format Unicode ou non-Unicode.</span><span class="sxs-lookup"><span data-stu-id="68949-107">There are Unicode and non-Unicode character string literals.</span></span> <span data-ttu-id="68949-108">Chaînes Unicode sont précédées de N. Par exemple, `N'hello'`.</span><span class="sxs-lookup"><span data-stu-id="68949-108">Unicode strings are prepended with N. For example, `N'hello'`.</span></span>  
  
 <span data-ttu-id="68949-109">Exemple de littéral de chaîne non-Unicode :</span><span class="sxs-lookup"><span data-stu-id="68949-109">The following is an example of a Non-Unicode string literal:</span></span>  
  
```  
'hello'  
--same as  
"hello"  
```  
  
 <span data-ttu-id="68949-110">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-110">Output:</span></span>  
  
|<span data-ttu-id="68949-111">Value</span><span class="sxs-lookup"><span data-stu-id="68949-111">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-112">hello</span><span class="sxs-lookup"><span data-stu-id="68949-112">hello</span></span>|  
  
### <a name="datetime"></a><span data-ttu-id="68949-113">DateTime</span><span class="sxs-lookup"><span data-stu-id="68949-113">DateTime</span></span>  
 <span data-ttu-id="68949-114">Dans les littéraux DateTime, les parties date et heure sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="68949-114">In DateTime literals, both date and time parts are mandatory.</span></span> <span data-ttu-id="68949-115">Il n'existe pas de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="68949-115">There are no default values.</span></span>  
  
 <span data-ttu-id="68949-116">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-116">Example:</span></span>  
  
```  
DATETIME '2006-12-25 01:01:00.000'   
--same as  
DATETIME '2006-12-25 01:01'  
```  
  
 <span data-ttu-id="68949-117">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-117">Output:</span></span>  
  
|<span data-ttu-id="68949-118">Value</span><span class="sxs-lookup"><span data-stu-id="68949-118">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-119">12/25/2006 1:01:00 AM</span><span class="sxs-lookup"><span data-stu-id="68949-119">12/25/2006 1:01:00 AM</span></span>|  
  
### <a name="integer"></a><span data-ttu-id="68949-120">Entier</span><span class="sxs-lookup"><span data-stu-id="68949-120">Integer</span></span>  
 <span data-ttu-id="68949-121">Les littéraux d'entiers peuvent être de type Int32 (123), UInt32 (123U), Int64 (123L) et UInt64 (123UL).</span><span class="sxs-lookup"><span data-stu-id="68949-121">Integer literals can be of type Int32 (123), UInt32 (123U), Int64 (123L), and UInt64 (123UL).</span></span>  
  
 <span data-ttu-id="68949-122">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-122">Example:</span></span>  
  
```  
--a collection of integers  
{1, 2, 3}  
```  
  
 <span data-ttu-id="68949-123">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-123">Output:</span></span>  
  
|<span data-ttu-id="68949-124">Value</span><span class="sxs-lookup"><span data-stu-id="68949-124">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-125">1</span><span class="sxs-lookup"><span data-stu-id="68949-125">1</span></span>|  
|<span data-ttu-id="68949-126">2</span><span class="sxs-lookup"><span data-stu-id="68949-126">2</span></span>|  
|<span data-ttu-id="68949-127">3</span><span class="sxs-lookup"><span data-stu-id="68949-127">3</span></span>|  
  
### <a name="other"></a><span data-ttu-id="68949-128">Autre</span><span class="sxs-lookup"><span data-stu-id="68949-128">Other</span></span>  
 <span data-ttu-id="68949-129">Les autres littéraux pris en charge par [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont Guid, Binary, Float/Double, Decimal et la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="68949-129">Other literals supported by [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are Guid, Binary, Float/Double, Decimal, and `null`.</span></span> <span data-ttu-id="68949-130">Les littéraux NULL dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont considérés compatibles avec tous les autres types dans le modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="68949-130">Null literals in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are considered to be compatible with every other type in the conceptual model.</span></span>  
  
## <a name="type-constructors"></a><span data-ttu-id="68949-131">Constructeurs de type</span><span class="sxs-lookup"><span data-stu-id="68949-131">Type Constructors</span></span>  
  
### <a name="row"></a><span data-ttu-id="68949-132">ROW</span><span class="sxs-lookup"><span data-stu-id="68949-132">ROW</span></span>  
 <span data-ttu-id="68949-133">[LIGNE](../../../../../../docs/framework/data/adonet/ef/language-reference/row-entity-sql.md) construit une valeur anonyme, structurellement typée de (enregistrement) comme dans :</span><span class="sxs-lookup"><span data-stu-id="68949-133">[ROW](../../../../../../docs/framework/data/adonet/ef/language-reference/row-entity-sql.md) constructs an anonymous, structurally-typed (record) value as in:</span></span> `ROW(1 AS myNumber, ‘Name’ AS myName).`  
  
 <span data-ttu-id="68949-134">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-134">Example:</span></span>  
  
```  
SELECT VALUE row (product.ProductID as ProductID, product.Name   
    as ProductName) FROM AdventureWorksEntities.Product AS product  
```  
  
 <span data-ttu-id="68949-135">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-135">Output:</span></span>  
  
|<span data-ttu-id="68949-136">ProductID</span><span class="sxs-lookup"><span data-stu-id="68949-136">ProductID</span></span>|<span data-ttu-id="68949-137">Nom</span><span class="sxs-lookup"><span data-stu-id="68949-137">Name</span></span>|  
|---------------|----------|  
|<span data-ttu-id="68949-138">1</span><span class="sxs-lookup"><span data-stu-id="68949-138">1</span></span>|<span data-ttu-id="68949-139">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="68949-139">Adjustable Race</span></span>|  
|<span data-ttu-id="68949-140">879</span><span class="sxs-lookup"><span data-stu-id="68949-140">879</span></span>|<span data-ttu-id="68949-141">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="68949-141">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="68949-142">712</span><span class="sxs-lookup"><span data-stu-id="68949-142">712</span></span>|<span data-ttu-id="68949-143">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="68949-143">AWC Logo Cap</span></span>|  
|<span data-ttu-id="68949-144">...</span><span class="sxs-lookup"><span data-stu-id="68949-144">...</span></span>|<span data-ttu-id="68949-145">...</span><span class="sxs-lookup"><span data-stu-id="68949-145">...</span></span>|  
  
### <a name="multiset"></a><span data-ttu-id="68949-146">MULTISET</span><span class="sxs-lookup"><span data-stu-id="68949-146">MULTISET</span></span>  
 <span data-ttu-id="68949-147">[MULTISET](../../../../../../docs/framework/data/adonet/ef/language-reference/multiset-entity-sql.md) construit des collections, telles que :</span><span class="sxs-lookup"><span data-stu-id="68949-147">[MULTISET](../../../../../../docs/framework/data/adonet/ef/language-reference/multiset-entity-sql.md) constructs collections, such as:</span></span>  
  
 `MULTISET(1,2,2,3)` `--same as`-`{1,2,2,3}.`  
  
 <span data-ttu-id="68949-148">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-148">Example:</span></span>  
  
```  
SELECT VALUE product FROM AdventureWorksEntities.Product AS product WHERE product.ListPrice IN MultiSet (125, 300)  
```  
  
 <span data-ttu-id="68949-149">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-149">Output:</span></span>  
  
|<span data-ttu-id="68949-150">ProductID</span><span class="sxs-lookup"><span data-stu-id="68949-150">ProductID</span></span>|<span data-ttu-id="68949-151">Nom</span><span class="sxs-lookup"><span data-stu-id="68949-151">Name</span></span>|<span data-ttu-id="68949-152">ProductNumber</span><span class="sxs-lookup"><span data-stu-id="68949-152">ProductNumber</span></span>|<span data-ttu-id="68949-153">…</span><span class="sxs-lookup"><span data-stu-id="68949-153">…</span></span>|  
|---------------|----------|-------------------|-------|  
|<span data-ttu-id="68949-154">842</span><span class="sxs-lookup"><span data-stu-id="68949-154">842</span></span>|<span data-ttu-id="68949-155">Touring-Panniers, Large</span><span class="sxs-lookup"><span data-stu-id="68949-155">Touring-Panniers, Large</span></span>|<span data-ttu-id="68949-156">PA-T100</span><span class="sxs-lookup"><span data-stu-id="68949-156">PA-T100</span></span>|<span data-ttu-id="68949-157">…</span><span class="sxs-lookup"><span data-stu-id="68949-157">…</span></span>|  
  
### <a name="object"></a><span data-ttu-id="68949-158">Object</span><span class="sxs-lookup"><span data-stu-id="68949-158">Object</span></span>  
 <span data-ttu-id="68949-159">[Nommé le constructeur de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/named-type-constructor-entity-sql.md) construit les objets définis par l’utilisateur (nommés) comme `person("abc", 12)`.</span><span class="sxs-lookup"><span data-stu-id="68949-159">[Named Type Constructor](../../../../../../docs/framework/data/adonet/ef/language-reference/named-type-constructor-entity-sql.md) constructs (named) user-defined objects, such as `person("abc", 12)`.</span></span>  
  
 <span data-ttu-id="68949-160">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-160">Example:</span></span>  
  
```  
SELECT VALUE AdventureWorksModel.SalesOrderDetail (o.SalesOrderDetailID, o.CarrierTrackingNumber, o.OrderQty,   
o.ProductID, o.SpecialOfferID, o.UnitPrice, o.UnitPriceDiscount,   
o.rowguid, o.ModifiedDate) FROM AdventureWorksEntities.SalesOrderDetail   
AS o  
```  
  
 <span data-ttu-id="68949-161">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-161">Output:</span></span>  
  
|<span data-ttu-id="68949-162">SalesOrderDetailID</span><span class="sxs-lookup"><span data-stu-id="68949-162">SalesOrderDetailID</span></span>|<span data-ttu-id="68949-163">CarrierTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="68949-163">CarrierTrackingNumber</span></span>|<span data-ttu-id="68949-164">OrderQty</span><span class="sxs-lookup"><span data-stu-id="68949-164">OrderQty</span></span>|<span data-ttu-id="68949-165">ProductID</span><span class="sxs-lookup"><span data-stu-id="68949-165">ProductID</span></span>|<span data-ttu-id="68949-166">...</span><span class="sxs-lookup"><span data-stu-id="68949-166">...</span></span>|  
|------------------------|---------------------------|--------------|---------------|---------|  
|<span data-ttu-id="68949-167">1</span><span class="sxs-lookup"><span data-stu-id="68949-167">1</span></span>|<span data-ttu-id="68949-168">4911-403C-98</span><span class="sxs-lookup"><span data-stu-id="68949-168">4911-403C-98</span></span>|<span data-ttu-id="68949-169">1</span><span class="sxs-lookup"><span data-stu-id="68949-169">1</span></span>|<span data-ttu-id="68949-170">776</span><span class="sxs-lookup"><span data-stu-id="68949-170">776</span></span>|<span data-ttu-id="68949-171">...</span><span class="sxs-lookup"><span data-stu-id="68949-171">...</span></span>|  
|<span data-ttu-id="68949-172">2</span><span class="sxs-lookup"><span data-stu-id="68949-172">2</span></span>|<span data-ttu-id="68949-173">4911-403C-98</span><span class="sxs-lookup"><span data-stu-id="68949-173">4911-403C-98</span></span>|<span data-ttu-id="68949-174">3</span><span class="sxs-lookup"><span data-stu-id="68949-174">3</span></span>|<span data-ttu-id="68949-175">777</span><span class="sxs-lookup"><span data-stu-id="68949-175">777</span></span>|<span data-ttu-id="68949-176">...</span><span class="sxs-lookup"><span data-stu-id="68949-176">...</span></span>|  
|<span data-ttu-id="68949-177">...</span><span class="sxs-lookup"><span data-stu-id="68949-177">...</span></span>|<span data-ttu-id="68949-178">...</span><span class="sxs-lookup"><span data-stu-id="68949-178">...</span></span>|<span data-ttu-id="68949-179">...</span><span class="sxs-lookup"><span data-stu-id="68949-179">...</span></span>|<span data-ttu-id="68949-180">...</span><span class="sxs-lookup"><span data-stu-id="68949-180">...</span></span>|<span data-ttu-id="68949-181">...</span><span class="sxs-lookup"><span data-stu-id="68949-181">...</span></span>|  
  
## <a name="references"></a><span data-ttu-id="68949-182">Références</span><span class="sxs-lookup"><span data-stu-id="68949-182">References</span></span>  
  
### <a name="ref"></a><span data-ttu-id="68949-183">REF</span><span class="sxs-lookup"><span data-stu-id="68949-183">REF</span></span>  
 <span data-ttu-id="68949-184">[REF](../../../../../../docs/framework/data/adonet/ef/language-reference/ref-entity-sql.md) crée une référence à une instance de type d’entité.</span><span class="sxs-lookup"><span data-stu-id="68949-184">[REF](../../../../../../docs/framework/data/adonet/ef/language-reference/ref-entity-sql.md) creates a reference to an entity type instance.</span></span> <span data-ttu-id="68949-185">Par exemple, la requête suivante retourne les références à chaque entité Order dans le jeu d'entités Orders :</span><span class="sxs-lookup"><span data-stu-id="68949-185">For example, the following query returns references to each Order entity in the Orders entity set:</span></span>  
  
```  
SELECT REF(o) AS OrderID FROM Orders AS o  
```  
  
 <span data-ttu-id="68949-186">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-186">Output:</span></span>  
  
|<span data-ttu-id="68949-187">Value</span><span class="sxs-lookup"><span data-stu-id="68949-187">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-188">1</span><span class="sxs-lookup"><span data-stu-id="68949-188">1</span></span>|  
|<span data-ttu-id="68949-189">2</span><span class="sxs-lookup"><span data-stu-id="68949-189">2</span></span>|  
|<span data-ttu-id="68949-190">3</span><span class="sxs-lookup"><span data-stu-id="68949-190">3</span></span>|  
|<span data-ttu-id="68949-191">...</span><span class="sxs-lookup"><span data-stu-id="68949-191">...</span></span>|  
  
 <span data-ttu-id="68949-192">L'exemple suivant utilise l'opérateur d'extraction de propriété (.) pour accéder à une propriété d'entité.</span><span class="sxs-lookup"><span data-stu-id="68949-192">The following example uses the property extraction operator (.) to access a property of an entity.</span></span> <span data-ttu-id="68949-193">Lors de l'utilisation de l'opérateur d'extraction de propriété, la référence est automatiquement supprimée.</span><span class="sxs-lookup"><span data-stu-id="68949-193">When the property extraction operator is used, the reference is automatically dereferenced.</span></span>  
  
 <span data-ttu-id="68949-194">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-194">Example:</span></span>  
  
```  
SELECT VALUE REF(p).Name FROM   
    AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="68949-195">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-195">Output:</span></span>  
  
|<span data-ttu-id="68949-196">Value</span><span class="sxs-lookup"><span data-stu-id="68949-196">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-197">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="68949-197">Adjustable Race</span></span>|  
|<span data-ttu-id="68949-198">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="68949-198">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="68949-199">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="68949-199">AWC Logo Cap</span></span>|  
|<span data-ttu-id="68949-200">...</span><span class="sxs-lookup"><span data-stu-id="68949-200">...</span></span>|  
  
### <a name="deref"></a><span data-ttu-id="68949-201">DEREF</span><span class="sxs-lookup"><span data-stu-id="68949-201">DEREF</span></span>  
 <span data-ttu-id="68949-202">[DEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/deref-entity-sql.md) déréférence une valeur de référence et génère le résultat de ce déréférencement.</span><span class="sxs-lookup"><span data-stu-id="68949-202">[DEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/deref-entity-sql.md) dereferences a reference value and produces the result of that dereference.</span></span> <span data-ttu-id="68949-203">Par exemple, la requête suivante génère les entités Order pour chaque élément Order du jeu d'entités Orders : `SELECT DEREF(o2.r) FROM (SELECT REF(o) AS r FROM LOB.Orders AS o) AS o2`.</span><span class="sxs-lookup"><span data-stu-id="68949-203">For example, the following query produces the Order entities for each Order in the Orders entity set: `SELECT DEREF(o2.r) FROM (SELECT REF(o) AS r FROM LOB.Orders AS o) AS o2`..</span></span>  
  
 <span data-ttu-id="68949-204">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-204">Example:</span></span>  
  
```  
SELECT VALUE DEREF(REF(p)).Name FROM   
    AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="68949-205">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-205">Output:</span></span>  
  
|<span data-ttu-id="68949-206">Value</span><span class="sxs-lookup"><span data-stu-id="68949-206">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-207">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="68949-207">Adjustable Race</span></span>|  
|<span data-ttu-id="68949-208">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="68949-208">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="68949-209">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="68949-209">AWC Logo Cap</span></span>|  
|<span data-ttu-id="68949-210">...</span><span class="sxs-lookup"><span data-stu-id="68949-210">...</span></span>|  
  
### <a name="createref-and-key"></a><span data-ttu-id="68949-211">CREATEREF et KEY</span><span class="sxs-lookup"><span data-stu-id="68949-211">CREATEREF AND KEY</span></span>  
 <span data-ttu-id="68949-212">[CREATEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/createref-entity-sql.md) crée une référence qui passe une clé.</span><span class="sxs-lookup"><span data-stu-id="68949-212">[CREATEREF](../../../../../../docs/framework/data/adonet/ef/language-reference/createref-entity-sql.md) creates a reference passing a key.</span></span> <span data-ttu-id="68949-213">[CLÉ](../../../../../../docs/framework/data/adonet/ef/language-reference/key-entity-sql.md) extrait la partie clé d’une expression avec référence de type.</span><span class="sxs-lookup"><span data-stu-id="68949-213">[KEY](../../../../../../docs/framework/data/adonet/ef/language-reference/key-entity-sql.md) extracts the key portion of an expression with type reference.</span></span>  
  
 <span data-ttu-id="68949-214">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-214">Example:</span></span>  
  
```  
SELECT VALUE Key(CreateRef(AdventureWorksEntities.Product, row(p.ProductID)))   
    FROM AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="68949-215">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-215">Output:</span></span>  
  
|<span data-ttu-id="68949-216">ProductID</span><span class="sxs-lookup"><span data-stu-id="68949-216">ProductID</span></span>|  
|---------------|  
|<span data-ttu-id="68949-217">980</span><span class="sxs-lookup"><span data-stu-id="68949-217">980</span></span>|  
|<span data-ttu-id="68949-218">365</span><span class="sxs-lookup"><span data-stu-id="68949-218">365</span></span>|  
|<span data-ttu-id="68949-219">771</span><span class="sxs-lookup"><span data-stu-id="68949-219">771</span></span>|  
|<span data-ttu-id="68949-220">...</span><span class="sxs-lookup"><span data-stu-id="68949-220">...</span></span>|  
  
## <a name="functions"></a><span data-ttu-id="68949-221">Fonctions</span><span class="sxs-lookup"><span data-stu-id="68949-221">Functions</span></span>  
  
### <a name="canonical"></a><span data-ttu-id="68949-222">Canoniques</span><span class="sxs-lookup"><span data-stu-id="68949-222">Canonical</span></span>  
 <span data-ttu-id="68949-223">L’espace de noms [fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md) est Edm, comme dans `Edm.Length("string")`.</span><span class="sxs-lookup"><span data-stu-id="68949-223">The namespace for [canonical functions](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md) is Edm, as in `Edm.Length("string")`.</span></span> <span data-ttu-id="68949-224">Vous n'avez pas besoin de spécifier l'espace de noms sauf si un autre espace de noms est importé et qu'il contient une fonction portant le même nom qu'une fonction canonique.</span><span class="sxs-lookup"><span data-stu-id="68949-224">You do not have to specify the namespace unless another namespace is imported that contains a function with the same name as a canonical function.</span></span> <span data-ttu-id="68949-225">Si deux espaces de noms partagent la même fonction, l'utilisateur doit spécifier le nom complet.</span><span class="sxs-lookup"><span data-stu-id="68949-225">If two namespaces have the same function, the user should specific the full name.</span></span>  
  
 <span data-ttu-id="68949-226">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-226">Example:</span></span>  
  
```  
SELECT Length(c. FirstName) As NameLen FROM   
    AdventureWorksEntities.Contact AS c   
    WHERE c.ContactID BETWEEN 10 AND 12  
```  
  
 <span data-ttu-id="68949-227">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-227">Output:</span></span>  
  
|<span data-ttu-id="68949-228">NameLen</span><span class="sxs-lookup"><span data-stu-id="68949-228">NameLen</span></span>|  
|-------------|  
|<span data-ttu-id="68949-229">6</span><span class="sxs-lookup"><span data-stu-id="68949-229">6</span></span>|  
|<span data-ttu-id="68949-230">6</span><span class="sxs-lookup"><span data-stu-id="68949-230">6</span></span>|  
|<span data-ttu-id="68949-231">5</span><span class="sxs-lookup"><span data-stu-id="68949-231">5</span></span>|  
  
### <a name="microsoft-provider-specific"></a><span data-ttu-id="68949-232">Spécifiques au fournisseur Microsoft</span><span class="sxs-lookup"><span data-stu-id="68949-232">Microsoft Provider-Specific</span></span>  
 <span data-ttu-id="68949-233">[Fonctions spécifiques au fournisseur de Microsoft](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md) se trouvent dans le `SqlServer` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="68949-233">[Microsoft provider-specific functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md) are in the `SqlServer` namespace.</span></span>  
  
 <span data-ttu-id="68949-234">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-234">Example:</span></span>  
  
```  
SELECT SqlServer.LEN(c.EmailAddress) As EmailLen FROM   
    AdventureWorksEntities.Contact AS c WHERE   
    c.ContactID BETWEEN 10 AND 12  
```  
  
 <span data-ttu-id="68949-235">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-235">Output:</span></span>  
  
|<span data-ttu-id="68949-236">EmailLen</span><span class="sxs-lookup"><span data-stu-id="68949-236">EmailLen</span></span>|  
|--------------|  
|<span data-ttu-id="68949-237">27</span><span class="sxs-lookup"><span data-stu-id="68949-237">27</span></span>|  
|<span data-ttu-id="68949-238">27</span><span class="sxs-lookup"><span data-stu-id="68949-238">27</span></span>|  
|<span data-ttu-id="68949-239">26</span><span class="sxs-lookup"><span data-stu-id="68949-239">26</span></span>|  
  
## <a name="namespaces"></a><span data-ttu-id="68949-240">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="68949-240">Namespaces</span></span>  
 <span data-ttu-id="68949-241">[À l’aide de](../../../../../../docs/framework/data/adonet/ef/language-reference/using-entity-sql.md) spécifie les espaces de noms utilisés dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="68949-241">[USING](../../../../../../docs/framework/data/adonet/ef/language-reference/using-entity-sql.md) specifies namespaces used in a query expression.</span></span>  
  
 <span data-ttu-id="68949-242">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-242">Example:</span></span>  
  
```  
using SqlServer; LOWER('AA');  
```  
  
 <span data-ttu-id="68949-243">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-243">Output:</span></span>  
  
|<span data-ttu-id="68949-244">Value</span><span class="sxs-lookup"><span data-stu-id="68949-244">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-245">aa</span><span class="sxs-lookup"><span data-stu-id="68949-245">aa</span></span>|  
  
## <a name="paging"></a><span data-ttu-id="68949-246">Pagination</span><span class="sxs-lookup"><span data-stu-id="68949-246">Paging</span></span>  
 <span data-ttu-id="68949-247">La pagination peut être exprimée en déclarant un [SKIP](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md) et [limite](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md) sous-clauses pour le [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md) clause.</span><span class="sxs-lookup"><span data-stu-id="68949-247">Paging can be expressed by declaring a [SKIP](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md) and [LIMIT](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md) sub-clauses to the [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md) clause.</span></span>  
  
 <span data-ttu-id="68949-248">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-248">Example:</span></span>  
  
```  
SELECT c.ContactID as ID, c.LastName as Name FROM   
    AdventureWorks.Contact AS c ORDER BY c.ContactID SKIP 9 LIMIT 3;  
```  
  
 <span data-ttu-id="68949-249">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-249">Output:</span></span>  
  
|<span data-ttu-id="68949-250">Id</span><span class="sxs-lookup"><span data-stu-id="68949-250">ID</span></span>|<span data-ttu-id="68949-251">Nom</span><span class="sxs-lookup"><span data-stu-id="68949-251">Name</span></span>|  
|--------|----------|  
|<span data-ttu-id="68949-252">10</span><span class="sxs-lookup"><span data-stu-id="68949-252">10</span></span>|<span data-ttu-id="68949-253">Adina</span><span class="sxs-lookup"><span data-stu-id="68949-253">Adina</span></span>|  
|<span data-ttu-id="68949-254">11</span><span class="sxs-lookup"><span data-stu-id="68949-254">11</span></span>|<span data-ttu-id="68949-255">Agcaoili</span><span class="sxs-lookup"><span data-stu-id="68949-255">Agcaoili</span></span>|  
|<span data-ttu-id="68949-256">12</span><span class="sxs-lookup"><span data-stu-id="68949-256">12</span></span>|<span data-ttu-id="68949-257">Aguilar</span><span class="sxs-lookup"><span data-stu-id="68949-257">Aguilar</span></span>|  
  
## <a name="grouping"></a><span data-ttu-id="68949-258">Regroupement</span><span class="sxs-lookup"><span data-stu-id="68949-258">Grouping</span></span>  
 <span data-ttu-id="68949-259">[REGROUPEMENT par](../../../../../../docs/framework/data/adonet/ef/language-reference/group-by-entity-sql.md) indique les groupes dans les objets retournés par une requête ([sélectionnez](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md)) expression doivent être placés.</span><span class="sxs-lookup"><span data-stu-id="68949-259">[GROUPING BY](../../../../../../docs/framework/data/adonet/ef/language-reference/group-by-entity-sql.md) specifies groups into which objects returned by a query ([SELECT](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md)) expression are to be placed.</span></span>  
  
 <span data-ttu-id="68949-260">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-260">Example:</span></span>  
  
```  
SELECT VALUE name FROM AdventureWorksEntities.Product as P   
    GROUP BY P.Name HAVING MAX(P.ListPrice) > 5  
```  
  
 <span data-ttu-id="68949-261">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-261">Output:</span></span>  
  
|<span data-ttu-id="68949-262">name</span><span class="sxs-lookup"><span data-stu-id="68949-262">name</span></span>|  
|----------|  
|<span data-ttu-id="68949-263">LL Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="68949-263">LL Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="68949-264">ML Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="68949-264">ML Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="68949-265">HL Mountain Seat Assembly</span><span class="sxs-lookup"><span data-stu-id="68949-265">HL Mountain Seat Assembly</span></span>|  
|<span data-ttu-id="68949-266">...</span><span class="sxs-lookup"><span data-stu-id="68949-266">...</span></span>|  
  
## <a name="navigation"></a><span data-ttu-id="68949-267">Navigation</span><span class="sxs-lookup"><span data-stu-id="68949-267">Navigation</span></span>  
 <span data-ttu-id="68949-268">L'opérateur de navigation de relations vous permet de parcourir la relation entre une entité (terminaison From) et une autre entité (terminaison To).</span><span class="sxs-lookup"><span data-stu-id="68949-268">The relationship navigation operator allows you to navigate over the relationship from one entity (from end) to another (to end).</span></span> <span data-ttu-id="68949-269">[NAVIGATE](../../../../../../docs/framework/data/adonet/ef/language-reference/navigate-entity-sql.md) accepte le type de relation qualifié comme \<espace de noms >.\< nom de type de relation >.</span><span class="sxs-lookup"><span data-stu-id="68949-269">[NAVIGATE](../../../../../../docs/framework/data/adonet/ef/language-reference/navigate-entity-sql.md) takes the relationship type qualified as \<namespace>.\<relationship type name>.</span></span> <span data-ttu-id="68949-270">Accédez retourne Ref\<T > Si la cardinalité de la terminaison to est 1.</span><span class="sxs-lookup"><span data-stu-id="68949-270">Navigate returns Ref\<T> if the cardinality of the to end is 1.</span></span> <span data-ttu-id="68949-271">Si la cardinalité de la terminaison to est n, la Collection < Ref\<T >> sera retourné.</span><span class="sxs-lookup"><span data-stu-id="68949-271">If the cardinality of the to end is n, the Collection<Ref\<T>> will be returned.</span></span>  
  
 <span data-ttu-id="68949-272">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-272">Example:</span></span>  
  
```  
SELECT a.AddressID, (SELECT VALUE DEREF(v) FROM   
    NAVIGATE(a, AdventureWorksModel.FK_SalesOrderHeader_Address_BillToAddressID) AS v)   
    FROM AdventureWorksEntities.Address AS a  
```  
  
 <span data-ttu-id="68949-273">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-273">Output:</span></span>  
  
|<span data-ttu-id="68949-274">AddressID</span><span class="sxs-lookup"><span data-stu-id="68949-274">AddressID</span></span>|  
|---------------|  
|<span data-ttu-id="68949-275">1</span><span class="sxs-lookup"><span data-stu-id="68949-275">1</span></span>|  
|<span data-ttu-id="68949-276">2</span><span class="sxs-lookup"><span data-stu-id="68949-276">2</span></span>|  
|<span data-ttu-id="68949-277">3</span><span class="sxs-lookup"><span data-stu-id="68949-277">3</span></span>|  
|<span data-ttu-id="68949-278">...</span><span class="sxs-lookup"><span data-stu-id="68949-278">...</span></span>|  
  
## <a name="select-value-and-select"></a><span data-ttu-id="68949-279">SELECT VALUE et SELECT</span><span class="sxs-lookup"><span data-stu-id="68949-279">SELECT VALUE AND SELECT</span></span>  
  
### <a name="select-value"></a><span data-ttu-id="68949-280">SELECT VALUE</span><span class="sxs-lookup"><span data-stu-id="68949-280">SELECT VALUE</span></span>  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="68949-281">Fournit la clause SELECT VALUE pour ignorer la construction de ligne implicite.</span><span class="sxs-lookup"><span data-stu-id="68949-281">provides the SELECT VALUE clause to skip the implicit row construction.</span></span> <span data-ttu-id="68949-282">Un seul élément peut être spécifié dans une clause SELECT VALUE.</span><span class="sxs-lookup"><span data-stu-id="68949-282">Only one item can be specified in a SELECT VALUE clause.</span></span> <span data-ttu-id="68949-283">Lorsqu’une telle clause est utilisée, aucun wrapper de ligne n’est construit autour des éléments dans la clause SELECT, et une collection de la forme souhaitée peut être générée, par exemple : `SELECT VALUE a`.</span><span class="sxs-lookup"><span data-stu-id="68949-283">When such a clause is used, no row wrapper is constructed around the items in the SELECT clause, and a collection of the desired shape can be produced, for example: `SELECT VALUE a`.</span></span>  
  
 <span data-ttu-id="68949-284">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-284">Example:</span></span>  
  
```  
SELECT VALUE p.Name FROM AdventureWorksEntities.Product as p  
```  
  
 <span data-ttu-id="68949-285">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-285">Output:</span></span>  
  
|<span data-ttu-id="68949-286">Nom</span><span class="sxs-lookup"><span data-stu-id="68949-286">Name</span></span>|  
|----------|  
|<span data-ttu-id="68949-287">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="68949-287">Adjustable Race</span></span>|  
|<span data-ttu-id="68949-288">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="68949-288">All-Purpose Bike Stand</span></span>|  
|<span data-ttu-id="68949-289">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="68949-289">AWC Logo Cap</span></span>|  
|<span data-ttu-id="68949-290">...</span><span class="sxs-lookup"><span data-stu-id="68949-290">...</span></span>|  
  
### <a name="select"></a><span data-ttu-id="68949-291">SELECT</span><span class="sxs-lookup"><span data-stu-id="68949-291">SELECT</span></span>  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="68949-292">fournit également le constructeur row pour construire des lignes arbitraires.</span><span class="sxs-lookup"><span data-stu-id="68949-292">also provides the row constructor to construct arbitrary rows.</span></span> <span data-ttu-id="68949-293">SELECT extrait un ou plusieurs éléments de la projection et produit un enregistrement de données avec des champs, par exemple : `SELECT a, b, c`.</span><span class="sxs-lookup"><span data-stu-id="68949-293">SELECT takes one or more elements in the projection and results in a data record with fields, for example: `SELECT a, b, c`.</span></span>  
  
 <span data-ttu-id="68949-294">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-294">Example:</span></span>  
  
 <span data-ttu-id="68949-295">SELECT p.Name, p.ProductID FROM AdventureWorksEntities.Product as p Output:</span><span class="sxs-lookup"><span data-stu-id="68949-295">SELECT p.Name, p.ProductID FROM AdventureWorksEntities.Product as p Output:</span></span>  
  
|<span data-ttu-id="68949-296">Nom</span><span class="sxs-lookup"><span data-stu-id="68949-296">Name</span></span>|<span data-ttu-id="68949-297">ProductID</span><span class="sxs-lookup"><span data-stu-id="68949-297">ProductID</span></span>|  
|----------|---------------|  
|<span data-ttu-id="68949-298">Adjustable Race</span><span class="sxs-lookup"><span data-stu-id="68949-298">Adjustable Race</span></span>|<span data-ttu-id="68949-299">1</span><span class="sxs-lookup"><span data-stu-id="68949-299">1</span></span>|  
|<span data-ttu-id="68949-300">All-Purpose Bike Stand</span><span class="sxs-lookup"><span data-stu-id="68949-300">All-Purpose Bike Stand</span></span>|<span data-ttu-id="68949-301">879</span><span class="sxs-lookup"><span data-stu-id="68949-301">879</span></span>|  
|<span data-ttu-id="68949-302">AWC Logo Cap</span><span class="sxs-lookup"><span data-stu-id="68949-302">AWC Logo Cap</span></span>|<span data-ttu-id="68949-303">712</span><span class="sxs-lookup"><span data-stu-id="68949-303">712</span></span>|  
|<span data-ttu-id="68949-304">...</span><span class="sxs-lookup"><span data-stu-id="68949-304">...</span></span>|<span data-ttu-id="68949-305">...</span><span class="sxs-lookup"><span data-stu-id="68949-305">...</span></span>|  
  
## <a name="case-expression"></a><span data-ttu-id="68949-306">Expression CASE</span><span class="sxs-lookup"><span data-stu-id="68949-306">CASE EXPRESSION</span></span>  
 <span data-ttu-id="68949-307">Le [cas expression](../../../../../../docs/framework/data/adonet/ef/language-reference/case-entity-sql.md) évalue un ensemble d’expressions booléennes pour déterminer le résultat.</span><span class="sxs-lookup"><span data-stu-id="68949-307">The [case expression](../../../../../../docs/framework/data/adonet/ef/language-reference/case-entity-sql.md) evaluates a set of Boolean expressions to determine the result.</span></span>  
  
 <span data-ttu-id="68949-308">Exemple :</span><span class="sxs-lookup"><span data-stu-id="68949-308">Example:</span></span>  
  
```  
CASE WHEN AVG({25,12,11}) < 100 THEN TRUE ELSE FALSE END  
```  
  
 <span data-ttu-id="68949-309">Sortie :</span><span class="sxs-lookup"><span data-stu-id="68949-309">Output:</span></span>  
  
|<span data-ttu-id="68949-310">Value</span><span class="sxs-lookup"><span data-stu-id="68949-310">Value</span></span>|  
|-----------|  
|<span data-ttu-id="68949-311">TRUE</span><span class="sxs-lookup"><span data-stu-id="68949-311">TRUE</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="68949-312">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68949-312">See also</span></span>

- [<span data-ttu-id="68949-313">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="68949-313">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [<span data-ttu-id="68949-314">Vue d'ensemble d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="68949-314">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
