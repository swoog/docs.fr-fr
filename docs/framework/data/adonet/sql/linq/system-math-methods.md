---
title: System.Math, méthodes
ms.date: 03/30/2017
ms.assetid: 0f299521-6f41-4720-bd70-67c93fc50948
ms.openlocfilehash: 1dae31b30962505c07c198f3bd35fceb8f400efb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59141711"
---
# <a name="systemmath-methods"></a><span data-ttu-id="8da38-102">System.Math, méthodes</span><span class="sxs-lookup"><span data-stu-id="8da38-102">System.Math Methods</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="8da38-103">ne prend pas en charge les méthodes <xref:System.Math> suivantes.</span><span class="sxs-lookup"><span data-stu-id="8da38-103">does not support the following <xref:System.Math> methods.</span></span>  
  
-   <xref:System.Math.DivRem%28System.Int32%2CSystem.Int32%2CSystem.Int32%40%29?displayProperty=nameWithType>  
  
-   <xref:System.Math.DivRem%28System.Int64%2CSystem.Int64%2CSystem.Int64%40%29?displayProperty=nameWithType>  
  
-   <xref:System.Math.IEEERemainder%28System.Double%2CSystem.Double%29?displayProperty=nameWithType>  
  
## <a name="differences-from-net"></a><span data-ttu-id="8da38-104">Différences par rapport à .NET</span><span class="sxs-lookup"><span data-stu-id="8da38-104">Differences from .NET</span></span>  
 <span data-ttu-id="8da38-105">Le .NET Framework présente une sémantique d'arrondi différente de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8da38-105">The .NET Framework has different rounding semantics from SQL Server.</span></span> <span data-ttu-id="8da38-106">Le <xref:System.Math.Round%2A> méthode dans le .NET Framework effectue *l’arrondi bancaire*, où les nombres qui se termine par.5 sont arrondies à la plus proche de chiffre pair, au lieu d’au chiffre supérieur suivant.</span><span class="sxs-lookup"><span data-stu-id="8da38-106">The <xref:System.Math.Round%2A> method in the .NET Framework performs *Banker's rounding*, where numbers that ends in .5 round to the nearest even digit instead of to the next higher digit.</span></span> <span data-ttu-id="8da38-107">Par exemple, 2,5 est arrondi à 2 et 3,5 à 4.</span><span class="sxs-lookup"><span data-stu-id="8da38-107">For example, 2.5 rounds to 2, while 3.5 rounds to 4.</span></span> <span data-ttu-id="8da38-108">Cette technique permet d’éviter les écarts systématiques vers des valeurs supérieures dans les transactions de données importantes.</span><span class="sxs-lookup"><span data-stu-id="8da38-108">(This technique helps avoid systematic bias toward higher values in large data transactions.)</span></span>  
  
 <span data-ttu-id="8da38-109">Dans SQL, la fonction `ROUND` arrondit toujours vers le chiffre supérieur.</span><span class="sxs-lookup"><span data-stu-id="8da38-109">In SQL, the `ROUND` function instead always rounds away from 0.</span></span> <span data-ttu-id="8da38-110">Ainsi, 2,5 est arrondi à 3 (contre 2 dans le .NET Framework).</span><span class="sxs-lookup"><span data-stu-id="8da38-110">Therefore 2.5 rounds to 3, contrasted with its rounding to 2 in the .NET Framework.</span></span>  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="8da38-111">passe par la sémantique `ROUND` de SQL et ne tente pas d'implémenter l'arrondi bancaire.</span><span class="sxs-lookup"><span data-stu-id="8da38-111">passes through to the SQL `ROUND` semantics and does not try to implement Banker's rounding.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8da38-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8da38-112">See also</span></span>

- [<span data-ttu-id="8da38-113">Fonctions et types de données</span><span class="sxs-lookup"><span data-stu-id="8da38-113">Data Types and Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
