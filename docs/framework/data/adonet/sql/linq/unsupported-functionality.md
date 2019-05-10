---
title: Fonctionnalités non prises en charge
ms.date: 03/30/2017
ms.assetid: e480cfb5-697e-42c8-bed5-9264c945c4f9
ms.openlocfilehash: fb030a5f212be71d99b66f101e5e8411fbe4de33
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64618144"
---
# <a name="unsupported-functionality"></a>Fonctionnalités non prises en charge
Dans LINQ to SQL, les fonctionnalités SQL suivantes ne peuvent pas être exposées via la traduction de constructions du Common Language Runtime (CLR) et .NET Framework existantes :  
  
- `STDDEV`  
  
- `LIKE`  
  
     Bien que `LIKE` ne soit pas prise en charge par le biais de la traduction directe, il existe des fonctionnalités similaires dans la classe <xref:System.Data.Linq.SqlClient.SqlMethods>. Pour plus d'informations, consultez <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.  
  
- `DATEDIFF`  
  
     LINQ to SQL a une prise en charge limitée de `DATEDIFF`. Il existe des fonctionnalités similaires dans la classe <xref:System.Data.Linq.SqlClient.SqlMethods>.  
  
- `ROUND`  
  
     LINQ to SQL a une prise en charge limitée de `ROUND`. Pour plus d’informations, consultez [System.Math, méthodes](system-math-methods.md).  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions et types de données](data-types-and-functions.md)
