---
title: ISOF (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5b2b0d34-d0a7-4bcd-baf2-58aa8456d00b
ms.openlocfilehash: 097d6e7d452ee62a2c8934d2c5fcfdddbeaffc73
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195746"
---
# <a name="isof-entity-sql"></a><span data-ttu-id="63919-102">ISOF (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="63919-102">ISOF (Entity SQL)</span></span>
<span data-ttu-id="63919-103">Détermine si le type d'une expression appartient au type spécifié ou à l'un de ses sous-types.</span><span class="sxs-lookup"><span data-stu-id="63919-103">Determines whether the type of an expression is of the specified type or one of its subtypes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63919-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63919-104">Syntax</span></span>  
  
```  
expression IS [ NOT ] OF ( [ ONLY ] type )  
```  
  
## <a name="arguments"></a><span data-ttu-id="63919-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="63919-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="63919-106">Toute expression de requête valide pour en déterminer le type.</span><span class="sxs-lookup"><span data-stu-id="63919-106">Any valid query expression to determine the type of.</span></span>  
  
 <span data-ttu-id="63919-107">NOT</span><span class="sxs-lookup"><span data-stu-id="63919-107">NOT</span></span>  
 <span data-ttu-id="63919-108">Inverse le résultat EDM.Boolean de l'opérateur IS OF.</span><span class="sxs-lookup"><span data-stu-id="63919-108">Negates the EDM.Boolean result of IS OF.</span></span>  
  
 <span data-ttu-id="63919-109">ONLY</span><span class="sxs-lookup"><span data-stu-id="63919-109">ONLY</span></span>  
 <span data-ttu-id="63919-110">Indique que l'opérateur IS OF ne retourne `true` que si `expression` appartient au type `type` et non à l'un de ses sous-types.</span><span class="sxs-lookup"><span data-stu-id="63919-110">Specifies that IS OF returns `true` only if `expression` is of type `type` and not any of one its subtypes.</span></span>  
  
 `type`  
 <span data-ttu-id="63919-111">Type sur lequel tester `expression`.</span><span class="sxs-lookup"><span data-stu-id="63919-111">The type to test `expression` against.</span></span> <span data-ttu-id="63919-112">Le type doit être qualifié par un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="63919-112">The type must be namespace-qualified.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="63919-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="63919-113">Return Value</span></span>  
 `true` <span data-ttu-id="63919-114">Si `expression` est de type T et T sont un type de base, ou un type dérivé de `type`; null si `expression` est null lors de l’exécution ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="63919-114">if `expression` is of type T and T is either a base type, or a derived type of `type`; null if `expression` is null at runtime; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63919-115">Notes</span><span class="sxs-lookup"><span data-stu-id="63919-115">Remarks</span></span>  
 <span data-ttu-id="63919-116">Les expressions `expression IS NOT OF (type)` et `expression IS NOT OF (ONLY type)` sont syntaxiquement équivalente à `NOT (expression IS OF (type))` et `NOT (expression IS OF (ONLY type))`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="63919-116">The expressions `expression IS NOT OF (type)` and `expression IS NOT OF (ONLY type)` are syntactically equivalent to `NOT (expression IS OF (type))` and `NOT (expression IS OF (ONLY type))`, respectively.</span></span>  
  
 <span data-ttu-id="63919-117">Le tableau suivant indique le comportement de l'opérateur `IS OF` sur certains modèles courants et d'autres plus singuliers.</span><span class="sxs-lookup"><span data-stu-id="63919-117">The following table shows the behavior of `IS OF` operator over some typical- and corner patterns.</span></span> <span data-ttu-id="63919-118">Toutes les exceptions sont levées côté client avant que le fournisseur soit appelé :</span><span class="sxs-lookup"><span data-stu-id="63919-118">All exceptions are thrown from the client side before the provider gets invoked:</span></span>  
  
|<span data-ttu-id="63919-119">Motif</span><span class="sxs-lookup"><span data-stu-id="63919-119">Pattern</span></span>|<span data-ttu-id="63919-120">Comportement</span><span class="sxs-lookup"><span data-stu-id="63919-120">Behavior</span></span>|  
|-------------|--------------|  
|<span data-ttu-id="63919-121">null IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="63919-121">null IS OF (EntityType)</span></span>|<span data-ttu-id="63919-122">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-122">Throws</span></span>|  
|<span data-ttu-id="63919-123">null IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="63919-123">null IS OF (ComplexType)</span></span>|<span data-ttu-id="63919-124">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-124">Throws</span></span>|  
|<span data-ttu-id="63919-125">null IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="63919-125">null IS OF (RowType)</span></span>|<span data-ttu-id="63919-126">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-126">Throws</span></span>|  
|<span data-ttu-id="63919-127">TREAT (null AS EntityType) IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="63919-127">TREAT (null AS EntityType) IS OF (EntityType)</span></span>|<span data-ttu-id="63919-128">Retourne DBNull</span><span class="sxs-lookup"><span data-stu-id="63919-128">Returns DBNull</span></span>|  
|<span data-ttu-id="63919-129">TREAT (null AS ComplexType) IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="63919-129">TREAT (null AS ComplexType) IS OF (ComplexType)</span></span>|<span data-ttu-id="63919-130">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-130">Throws</span></span>|  
|<span data-ttu-id="63919-131">TREAT (null AS RowType) IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="63919-131">TREAT (null AS RowType) IS OF (RowType)</span></span>|<span data-ttu-id="63919-132">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-132">Throws</span></span>|  
|<span data-ttu-id="63919-133">EntityType IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="63919-133">EntityType IS OF (EntityType)</span></span>|<span data-ttu-id="63919-134">Retourne true/false</span><span class="sxs-lookup"><span data-stu-id="63919-134">Returns true/false</span></span>|  
|<span data-ttu-id="63919-135">ComplexType IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="63919-135">ComplexType IS OF (ComplexType)</span></span>|<span data-ttu-id="63919-136">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-136">Throws</span></span>|  
|<span data-ttu-id="63919-137">RowType IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="63919-137">RowType IS OF (RowType)</span></span>|<span data-ttu-id="63919-138">Exception</span><span class="sxs-lookup"><span data-stu-id="63919-138">Throws</span></span>|  
  
## <a name="example"></a><span data-ttu-id="63919-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="63919-139">Example</span></span>  
 <span data-ttu-id="63919-140">Ce qui suit [!INCLUDE[esql](../../../../../../includes/esql-md.md)] requête utilise l’opérateur IS OF pour déterminer le type d’une expression de requête, puis utilise l’opérateur TREAT pour convertir un objet du type Course en collection d’objets du type OnsiteCourse.</span><span class="sxs-lookup"><span data-stu-id="63919-140">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the IS OF operator to determine the type of a query expression, and then uses the TREAT operator to convert an object of the type Course to a collection of objects of the type OnsiteCourse.</span></span> <span data-ttu-id="63919-141">Cette requête est basée sur le modèle [School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="63919-141">The query is based on the [School Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)).</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#TREAT_ISOF](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#treat_isof)]  
  
## <a name="see-also"></a><span data-ttu-id="63919-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63919-142">See also</span></span>

- [<span data-ttu-id="63919-143">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="63919-143">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
