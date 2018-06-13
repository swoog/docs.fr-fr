---
title: Fonctions définies par l'utilisateur
ms.date: 03/30/2017
ms.assetid: 3304c9b2-5c7a-4a95-9d45-4f260dcb606e
ms.openlocfilehash: f1222d9332d365c9c3c6ca2aa28cbb48e92c04e0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33363598"
---
# <a name="user-defined-functions"></a><span data-ttu-id="b508a-102">Fonctions définies par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="b508a-102">User-Defined Functions</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="b508a-103"> utilise des méthodes dans votre modèle objet pour représenter des fonctions définies par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b508a-103"> uses methods in your object model to represent user-defined functions.</span></span> <span data-ttu-id="b508a-104">Vous désignez des méthodes comme des fonctions en appliquant l'attribut <xref:System.Data.Linq.Mapping.FunctionAttribute> et, si nécessaire, l'attribut <xref:System.Data.Linq.Mapping.ParameterAttribute>.</span><span class="sxs-lookup"><span data-stu-id="b508a-104">You designate methods as functions by applying the <xref:System.Data.Linq.Mapping.FunctionAttribute> attribute and, where required, the <xref:System.Data.Linq.Mapping.ParameterAttribute> attribute.</span></span> <span data-ttu-id="b508a-105">Pour plus d’informations, consultez [le modèle LINQ to SQL objet](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="b508a-105">For more information, see [The LINQ to SQL Object Model](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md).</span></span>  
  
 <span data-ttu-id="b508a-106">Pour éviter une exception <xref:System.InvalidOperationException>, les fonctions définies par l'utilisateur dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] doivent prendre l'une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b508a-106">To avoid an <xref:System.InvalidOperationException>, user-defined functions in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] must be in one of the following forms:</span></span>  
  
-   <span data-ttu-id="b508a-107">Fonction encapsulée comme un appel de méthode disposant des attributs de mappage appropriés.</span><span class="sxs-lookup"><span data-stu-id="b508a-107">A function wrapped as a method call having the correct mapping attributes.</span></span> <span data-ttu-id="b508a-108">Pour plus d’informations, consultez [mappage basé sur l’attribut](../../../../../../docs/framework/data/adonet/sql/linq/attribute-based-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="b508a-108">For more information, see [Attribute-Based Mapping](../../../../../../docs/framework/data/adonet/sql/linq/attribute-based-mapping.md).</span></span>  
  
-   <span data-ttu-id="b508a-109">Méthode SQL statique spécifique à [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b508a-109">A static SQL method specific to [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>  
  
-   <span data-ttu-id="b508a-110">Fonction prise en charge par une méthode [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b508a-110">A function supported by a [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)] method.</span></span>  
  
 <span data-ttu-id="b508a-111">Les rubriques de cette section montrent comment former et appeler ces méthodes dans votre application si vous écrivez vous-même le code.</span><span class="sxs-lookup"><span data-stu-id="b508a-111">The topics in this section show how to form and call these methods in your application if you write the code yourself.</span></span> <span data-ttu-id="b508a-112">Les développeurs qui utilisent Visual Studio utilisent généralement le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour mapper des fonctions définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b508a-112">Developers using Visual Studio would typically use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to map user-defined functions.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b508a-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b508a-113">In This Section</span></span>  
 [<span data-ttu-id="b508a-114">Guide pratique pour utiliser des fonctions scalaires définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b508a-114">How to: Use Scalar-Valued User-Defined Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-scalar-valued-user-defined-functions.md)  
 <span data-ttu-id="b508a-115">Décrit comment implémenter une fonction qui retourne des valeurs scalaires.</span><span class="sxs-lookup"><span data-stu-id="b508a-115">Describes how to implement a function that returns scalar values.</span></span>  
  
 [<span data-ttu-id="b508a-116">Guide pratique pour utiliser des fonctions table définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b508a-116">How to: Use Table-Valued User-Defined Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-table-valued-user-defined-functions.md)  
 <span data-ttu-id="b508a-117">Décrit comment implémenter une fonction qui retourne des valeurs de table.</span><span class="sxs-lookup"><span data-stu-id="b508a-117">Describes how to implement a function that returns table values.</span></span>  
  
 [<span data-ttu-id="b508a-118">Guide pratique pour appeler des fonctions inline définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b508a-118">How to: Call User-Defined Functions Inline</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-call-user-defined-functions-inline.md)  
 <span data-ttu-id="b508a-119">Décrit comment passer des appels inline à des fonctions et les différences d'exécution lorsque l'appel est rendu inline.</span><span class="sxs-lookup"><span data-stu-id="b508a-119">Describes how to make inline calls to functions and the differences in execution when the call is made inline.</span></span>
