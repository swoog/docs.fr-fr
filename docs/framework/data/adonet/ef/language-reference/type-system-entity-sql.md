---
title: System, type (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 818a505b-a196-41dd-aaac-2ccd5f7a2f1a
ms.openlocfilehash: 0afeffd3ad180d6cc6175010140754e279988b38
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134561"
---
# <a name="type-system-entity-sql"></a><span data-ttu-id="9acfd-102">System, type (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="9acfd-102">Type System (Entity SQL)</span></span>
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="9acfd-103">prend en charge un nombre de types :</span><span class="sxs-lookup"><span data-stu-id="9acfd-103">supports a number of types:</span></span>  
  
-   <span data-ttu-id="9acfd-104">Types primitifs (simples) tels que `Int32` et</span><span class="sxs-lookup"><span data-stu-id="9acfd-104">Primitive (simple) types such as `Int32` and</span></span> `String.`  
  
-   <span data-ttu-id="9acfd-105">Les types nominaux qui sont définis dans le schéma, tels que <xref:System.Data.Metadata.Edm.EntityType>, <xref:System.Data.Metadata.Edm.ComplexType> et <xref:System.Data.Metadata.Edm.RelationshipType>.</span><span class="sxs-lookup"><span data-stu-id="9acfd-105">Nominal types that are defined in the schema, such as <xref:System.Data.Metadata.Edm.EntityType>, <xref:System.Data.Metadata.Edm.ComplexType>, and <xref:System.Data.Metadata.Edm.RelationshipType>.</span></span>  
  
-   <span data-ttu-id="9acfd-106">Les types anonymes qui ne sont pas définis explicitement dans le schéma : <xref:System.Data.Metadata.Edm.CollectionType>, <xref:System.Data.Metadata.Edm.RowType> et <xref:System.Data.Metadata.Edm.RefType>.</span><span class="sxs-lookup"><span data-stu-id="9acfd-106">Anonymous types that are not defined in the schema explicitly: <xref:System.Data.Metadata.Edm.CollectionType>, <xref:System.Data.Metadata.Edm.RowType>, and <xref:System.Data.Metadata.Edm.RefType>.</span></span>  
  
 <span data-ttu-id="9acfd-107">Cette section décrit les types anonymes qui ne sont pas définis explicitement dans le schéma mais qui sont prises en charge par Entity SQL.</span><span class="sxs-lookup"><span data-stu-id="9acfd-107">This section discusses the anonymous types that are not defined in the schema explicitly but are supported by Entity SQL.</span></span> <span data-ttu-id="9acfd-108">Pour plus d’informations sur les types primitifs et nominaux, voir [Types du modèle conceptuel (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#conceptual-model-types-csdl).</span><span class="sxs-lookup"><span data-stu-id="9acfd-108">For information on primitive and nominal types, see [Conceptual Model Types (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#conceptual-model-types-csdl).</span></span>  
  
## <a name="rows"></a><span data-ttu-id="9acfd-109">Lignes</span><span class="sxs-lookup"><span data-stu-id="9acfd-109">Rows</span></span>  
 <span data-ttu-id="9acfd-110">La structure d'une ligne dépend de la séquence de membres typés et nommés que la ligne contient.</span><span class="sxs-lookup"><span data-stu-id="9acfd-110">The structure of a row depends on the sequence of typed and named members that the row consists of.</span></span> <span data-ttu-id="9acfd-111">Un type de ligne n'a aucune identité et ne peut pas faire l'objet d'un héritage.</span><span class="sxs-lookup"><span data-stu-id="9acfd-111">A row type has no identity and cannot be inherited from.</span></span> <span data-ttu-id="9acfd-112">Les instances du même type de ligne sont équivalentes si les membres sont respectivement équivalents.</span><span class="sxs-lookup"><span data-stu-id="9acfd-112">Instances of the same row type are equivalent if the members are respectively equivalent.</span></span> <span data-ttu-id="9acfd-113">Les lignes n'ont aucun comportement au-delà de leur équivalence structurelle et n'ont aucun équivalent dans le Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="9acfd-113">Rows have no behavior beyond their structural equivalence and have no equivalent in the common language runtime.</span></span> <span data-ttu-id="9acfd-114">Les requêtes peuvent donner des structures qui contiennent des lignes ou des collections de lignes.</span><span class="sxs-lookup"><span data-stu-id="9acfd-114">Queries can result in structures that contain rows or collections of rows.</span></span> <span data-ttu-id="9acfd-115">La liaison d’API entre les requêtes [!INCLUDE[esql](../../../../../../includes/esql-md.md)] et le langage hôte définit la façon dont les lignes sont réalisées dans la requête qui a produit le résultat.</span><span class="sxs-lookup"><span data-stu-id="9acfd-115">The API binding between the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries and the host language defines how rows are realized in the query that produced the result.</span></span> <span data-ttu-id="9acfd-116">Pour plus d’informations sur la façon de construire une instance de la ligne, consultez [Types construction](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="9acfd-116">For information on how to construct a row instance, see [Constructing Types](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span></span>  
  
## <a name="collections"></a><span data-ttu-id="9acfd-117">Collections</span><span class="sxs-lookup"><span data-stu-id="9acfd-117">Collections</span></span>  
 <span data-ttu-id="9acfd-118">Les types de collections représentent zéro instance ou plus d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="9acfd-118">Collection types represent zero or more instances of other objects.</span></span> <span data-ttu-id="9acfd-119">Pour plus d’informations sur la façon de construire une collection, consultez [Types construction](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="9acfd-119">For information on how to construct collection, see [Constructing Types](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span></span>  
  
## <a name="references"></a><span data-ttu-id="9acfd-120">Références</span><span class="sxs-lookup"><span data-stu-id="9acfd-120">References</span></span>  
 <span data-ttu-id="9acfd-121">Une référence est un pointeur logique vers une entité spécifique dans un jeu d'entités spécifique.</span><span class="sxs-lookup"><span data-stu-id="9acfd-121">A reference is a logical pointer to a specific entity in a specific entity set.</span></span>  
  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="9acfd-122">prend en charge les opérateurs suivants pour construire, déconstruire et parcourir les références :</span><span class="sxs-lookup"><span data-stu-id="9acfd-122">supports the following operators to construct, deconstruct, and navigate through references:</span></span>  
  
-   [<span data-ttu-id="9acfd-123">REF</span><span class="sxs-lookup"><span data-stu-id="9acfd-123">REF</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/ref-entity-sql.md)  
  
-   [<span data-ttu-id="9acfd-124">CREATEREF</span><span class="sxs-lookup"><span data-stu-id="9acfd-124">CREATEREF</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/createref-entity-sql.md)  
  
-   [<span data-ttu-id="9acfd-125">KEY</span><span class="sxs-lookup"><span data-stu-id="9acfd-125">KEY</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/key-entity-sql.md)  
  
-   [<span data-ttu-id="9acfd-126">DEREF</span><span class="sxs-lookup"><span data-stu-id="9acfd-126">DEREF</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/deref-entity-sql.md)  
  
 <span data-ttu-id="9acfd-127">Vous pouvez explorer une référence en utilisant l'opérateur `.` (point) d'accès au membre.</span><span class="sxs-lookup"><span data-stu-id="9acfd-127">You can navigate through a reference by using the member access (dot) operator(`.`).</span></span> <span data-ttu-id="9acfd-128">L'extrait de code suivant extrait la propriété ID (de Order) en explorant la propriété r (référence).</span><span class="sxs-lookup"><span data-stu-id="9acfd-128">The following snippet extracts the Id property (of Order) by navigating through the r (reference) property.</span></span>  
  
```  
select o2.r.Id   
from (select ref(o) as r from LOB.Orders as o) as o2   
```  
  
 <span data-ttu-id="9acfd-129">Si la valeur de la référence est Null, si la cible de la référence n'existe pas, le résultat est null.</span><span class="sxs-lookup"><span data-stu-id="9acfd-129">If the reference value is null, or if the target of the reference does not exist, the result is null.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9acfd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9acfd-130">See also</span></span>

- [<span data-ttu-id="9acfd-131">Vue d'ensemble d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="9acfd-131">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
- [<span data-ttu-id="9acfd-132">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="9acfd-132">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [<span data-ttu-id="9acfd-133">CAST</span><span class="sxs-lookup"><span data-stu-id="9acfd-133">CAST</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/cast-entity-sql.md)
- [<span data-ttu-id="9acfd-134">Spécifications CSDL, SSDL et MSL</span><span class="sxs-lookup"><span data-stu-id="9acfd-134">CSDL, SSDL, and MSL Specifications</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/csdl-ssdl-and-msl-specifications.md)
