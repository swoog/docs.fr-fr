---
title: Formuler des projections
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 745742df-0eda-479b-83f8-29bd8a80db96
caps.latest.revision: 2
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: d8215a016face76b8a258d694a36657be327b5e0
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="formulate-projections"></a><span data-ttu-id="73c80-102">Formuler des projections</span><span class="sxs-lookup"><span data-stu-id="73c80-102">Formulate Projections</span></span>
<span data-ttu-id="73c80-103">Les exemples suivants montrent comment les `select` instruction en c# et `Select` instruction en Visual Basic peut être combinée avec d’autres fonctionnalités pour former des projections de requête.</span><span class="sxs-lookup"><span data-stu-id="73c80-103">The following examples show how the `select` statement in C# and `Select` statement in Visual Basic can be combined with other features to form query projections.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73c80-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-104">Example</span></span>  
 <span data-ttu-id="73c80-105">L’exemple suivant utilise le `Select` clause dans Visual Basic (`select` clause en c#) pour retourner une séquence de noms de contact pour `Customers`.</span><span class="sxs-lookup"><span data-stu-id="73c80-105">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) to return a sequence of contact names for `Customers`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#57](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#57)]
 [!code-vb[DLinqQueryExamples#57](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#57)]  
  
## <a name="example"></a><span data-ttu-id="73c80-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-106">Example</span></span>  
 <span data-ttu-id="73c80-107">L’exemple suivant utilise le `Select` clause dans Visual Basic (`select` clause en c#) et *types anonymes* pour retourner une séquence de noms de contact et numéros de téléphone pour `Customers`.</span><span class="sxs-lookup"><span data-stu-id="73c80-107">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a sequence of contact names and telephone numbers for `Customers`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#58](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#58)]
 [!code-vb[DLinqQueryExamples#58](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#58)]  
  
## <a name="example"></a><span data-ttu-id="73c80-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-108">Example</span></span>  
 <span data-ttu-id="73c80-109">L’exemple suivant utilise le `Select` clause dans Visual Basic (`select` clause en c#) et *types anonymes* pour retourner une séquence de noms et numéros de téléphone pour les employés.</span><span class="sxs-lookup"><span data-stu-id="73c80-109">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a sequence of names and telephone numbers for employees.</span></span> <span data-ttu-id="73c80-110">Le `FirstName` et `LastName` les champs sont combinés en un seul champ (`Name`) et le `HomePhone` champ a été renommé en `Phone` dans la séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="73c80-110">The `FirstName` and `LastName` fields are combined into a single field (`Name`), and the `HomePhone` field is renamed to `Phone` in the resulting sequence.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#59](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#59)]
 [!code-vb[DLinqQueryExamples#59](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#59)]  
  
## <a name="example"></a><span data-ttu-id="73c80-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-111">Example</span></span>  
 <span data-ttu-id="73c80-112">L’exemple suivant utilise le `Select` clause dans Visual Basic (`select` clause en c#) et *types anonymes* pour retourner une séquence de tous les `ProductID`s et une valeur calculée nommée `HalfPrice`.</span><span class="sxs-lookup"><span data-stu-id="73c80-112">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a sequence of all `ProductID`s and a calculated value named `HalfPrice`.</span></span> <span data-ttu-id="73c80-113">Cette valeur correspond à `UnitPrice` divisé par 2.</span><span class="sxs-lookup"><span data-stu-id="73c80-113">This value is set to the `UnitPrice` divided by 2.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#60](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#60)]
 [!code-vb[DLinqQueryExamples#60](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#60)]  
  
## <a name="example"></a><span data-ttu-id="73c80-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-114">Example</span></span>  
 <span data-ttu-id="73c80-115">L’exemple suivant utilise le `Select` clause dans Visual Basic (`select` clause en c#) et un *instruction conditionnelle* pour retourner une séquence de nom de produit et la disponibilité des produits.</span><span class="sxs-lookup"><span data-stu-id="73c80-115">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and a *conditional statement* to return a sequence of product name and product availability.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#61](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#61)]
 [!code-vb[DLinqQueryExamples#61](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#61)]  
  
## <a name="example"></a><span data-ttu-id="73c80-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-116">Example</span></span>  
 <span data-ttu-id="73c80-117">L’exemple suivant utilise un Visual Basic `Select` clause (`select` clause en c#) et un *type connu* (Name) pour retourner une séquence de noms d’employés.</span><span class="sxs-lookup"><span data-stu-id="73c80-117">The following example uses a Visual Basic `Select` clause (`select` clause in C#) and a *known type* (Name) to return a sequence of the names of employees.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#62](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#62)]
 [!code-vb[DLinqQueryExamples#62](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#62)]  
  
## <a name="example"></a><span data-ttu-id="73c80-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-118">Example</span></span>  
 <span data-ttu-id="73c80-119">L’exemple suivant utilise `Select` et `Where` en Visual Basic (`select` et `where` en c#) pour retourner un *séquence filtrée* de noms de contact pour les clients de Londres.</span><span class="sxs-lookup"><span data-stu-id="73c80-119">The following example uses `Select` and `Where` in Visual Basic (`select` and `where` in C#) to return a *filtered sequence* of contact names for customers in London.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#63](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#63)]
 [!code-vb[DLinqQueryExamples#63](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#63)]  
  
## <a name="example"></a><span data-ttu-id="73c80-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-120">Example</span></span>  
 <span data-ttu-id="73c80-121">L’exemple suivant utilise un `Select` clause dans Visual Basic (`select` clause en c#) et *types anonymes* pour renvoyer un *en forme de sous-ensemble* des données sur les clients.</span><span class="sxs-lookup"><span data-stu-id="73c80-121">The following example uses a `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a *shaped subset* of the data about customers.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#64](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#64)]
 [!code-vb[DLinqQueryExamples#64](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#64)]  
  
## <a name="example"></a><span data-ttu-id="73c80-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="73c80-122">Example</span></span>  
 <span data-ttu-id="73c80-123">L'exemple suivant utilise des requêtes imbriquées pour retourner les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="73c80-123">The following example uses nested queries to return the following results:</span></span>  
  
-   <span data-ttu-id="73c80-124">Séquence de toutes les commandes et des `OrderID` correspondants.</span><span class="sxs-lookup"><span data-stu-id="73c80-124">A sequence of all orders and their corresponding `OrderID`s.</span></span>  
  
-   <span data-ttu-id="73c80-125">Sous-séquence des éléments dans la commande pour laquelle il existe une remise.</span><span class="sxs-lookup"><span data-stu-id="73c80-125">A subsequence of the items in the order for which there is a discount.</span></span>  
  
-   <span data-ttu-id="73c80-126">Montant enregistré si le coût d'expédition n'est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="73c80-126">The amount of money saved if the cost of shipping is not included.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#65](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#65)]
 [!code-vb[DLinqQueryExamples#65](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#65)]  
  
## <a name="see-also"></a><span data-ttu-id="73c80-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73c80-127">See Also</span></span>  
 [<span data-ttu-id="73c80-128">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="73c80-128">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
