---
title: System.Math, méthodes
ms.date: 03/30/2017
ms.assetid: 0f299521-6f41-4720-bd70-67c93fc50948
ms.openlocfilehash: 1dae31b30962505c07c198f3bd35fceb8f400efb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59141711"
---
# <a name="systemmath-methods"></a>System.Math, méthodes
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ne prend pas en charge les éléments suivants <xref:System.Math> méthodes.  
  
-   <xref:System.Math.DivRem%28System.Int32%2CSystem.Int32%2CSystem.Int32%40%29?displayProperty=nameWithType>  
  
-   <xref:System.Math.DivRem%28System.Int64%2CSystem.Int64%2CSystem.Int64%40%29?displayProperty=nameWithType>  
  
-   <xref:System.Math.IEEERemainder%28System.Double%2CSystem.Double%29?displayProperty=nameWithType>  
  
## <a name="differences-from-net"></a>Différences par rapport à .NET  
 Le .NET Framework présente une sémantique d'arrondi différente de SQL Server. Le <xref:System.Math.Round%2A> méthode dans le .NET Framework effectue *l’arrondi bancaire*, où les nombres qui se termine par.5 sont arrondies à la plus proche de chiffre pair, au lieu d’au chiffre supérieur suivant. Par exemple, 2,5 est arrondi à 2 et 3,5 à 4. Cette technique permet d’éviter les écarts systématiques vers des valeurs supérieures dans les transactions de données importantes.  
  
 Dans SQL, la fonction `ROUND` arrondit toujours vers le chiffre supérieur. Ainsi, 2,5 est arrondi à 3 (contre 2 dans le .NET Framework).  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] passe par le biais de SQL `ROUND` sémantique et n’essaie pas d’implémenter l’arrondi bancaire.  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions et types de données](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
