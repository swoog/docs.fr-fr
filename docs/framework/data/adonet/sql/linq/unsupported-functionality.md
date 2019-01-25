---
title: Fonctionnalité non prise en charge
ms.date: 03/30/2017
ms.assetid: e480cfb5-697e-42c8-bed5-9264c945c4f9
ms.openlocfilehash: 5022c9011c2aac5b3272e359f991c40236a5673f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686699"
---
# <a name="unsupported-functionality"></a><span data-ttu-id="581cc-102">Fonctionnalité non prise en charge</span><span class="sxs-lookup"><span data-stu-id="581cc-102">Unsupported Functionality</span></span>
<span data-ttu-id="581cc-103">Dans LINQ to SQL, les fonctionnalités SQL suivantes ne peuvent pas être exposées via la traduction de constructions du Common Language Runtime (CLR) et .NET Framework existantes :</span><span class="sxs-lookup"><span data-stu-id="581cc-103">In LINQ to SQL, the following SQL functionality cannot be exposed through translation of existing common language runtime (CLR) and .NET Framework constructs:</span></span>  
  
-   `STDDEV`  
  
-   `LIKE`  
  
     <span data-ttu-id="581cc-104">Bien que `LIKE` ne soit pas prise en charge par le biais de la traduction directe, il existe des fonctionnalités similaires dans la classe <xref:System.Data.Linq.SqlClient.SqlMethods>.</span><span class="sxs-lookup"><span data-stu-id="581cc-104">Although `LIKE` is not supported through direct translation, similar functionality exists in the <xref:System.Data.Linq.SqlClient.SqlMethods> class.</span></span> <span data-ttu-id="581cc-105">Pour plus d'informations, consultez <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="581cc-105">For more information, see <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.</span></span>  
  
-   `DATEDIFF`  
  
     <span data-ttu-id="581cc-106">LINQ to SQL a une prise en charge limitée de `DATEDIFF`.</span><span class="sxs-lookup"><span data-stu-id="581cc-106">LINQ to SQL has limited support for `DATEDIFF`.</span></span> <span data-ttu-id="581cc-107">Il existe des fonctionnalités similaires dans la classe <xref:System.Data.Linq.SqlClient.SqlMethods>.</span><span class="sxs-lookup"><span data-stu-id="581cc-107">Similar functionality exists in the <xref:System.Data.Linq.SqlClient.SqlMethods> class.</span></span>  
  
-   `ROUND`  
  
     <span data-ttu-id="581cc-108">LINQ to SQL a une prise en charge limitée de `ROUND`.</span><span class="sxs-lookup"><span data-stu-id="581cc-108">LINQ to SQL has limited support for `ROUND`.</span></span> <span data-ttu-id="581cc-109">Pour plus d’informations, consultez [System.Math, méthodes](system-math-methods.md).</span><span class="sxs-lookup"><span data-stu-id="581cc-109">For more information, see [System.Math Methods](system-math-methods.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="581cc-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="581cc-110">See also</span></span>
- [<span data-ttu-id="581cc-111">Fonctions et types de données</span><span class="sxs-lookup"><span data-stu-id="581cc-111">Data Types and Functions</span></span>](data-types-and-functions.md)
