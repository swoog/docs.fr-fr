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
# <a name="unsupported-functionality"></a>Fonctionnalité non prise en charge
Dans LINQ to SQL, les fonctionnalités SQL suivantes ne peuvent pas être exposées via la traduction de constructions du Common Language Runtime (CLR) et .NET Framework existantes :  
  
-   `STDDEV`  
  
-   `LIKE`  
  
     Bien que `LIKE` ne soit pas prise en charge par le biais de la traduction directe, il existe des fonctionnalités similaires dans la classe <xref:System.Data.Linq.SqlClient.SqlMethods>. Pour plus d'informations, consultez <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.  
  
-   `DATEDIFF`  
  
     LINQ to SQL a une prise en charge limitée de `DATEDIFF`. Il existe des fonctionnalités similaires dans la classe <xref:System.Data.Linq.SqlClient.SqlMethods>.  
  
-   `ROUND`  
  
     LINQ to SQL a une prise en charge limitée de `ROUND`. Pour plus d’informations, consultez [System.Math, méthodes](system-math-methods.md).  
  
## <a name="see-also"></a>Voir aussi
- [Fonctions et types de données](data-types-and-functions.md)
