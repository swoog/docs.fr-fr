---
title: System.String, méthodes
ms.date: 03/30/2017
ms.assetid: ce307f14-87e6-4816-8694-8a4147f6b784
ms.openlocfilehash: 569010c36296e18487eb52527d3df0cc0b97cf06
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618120"
---
# <a name="systemstring-methods"></a>System.String, méthodes
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ne prend pas en charge les méthodes <xref:System.String> suivantes.  
  
## <a name="unsupported-systemstring-methods-in-general"></a>Méthodes System.String non prises en charge en général  
 Méthodes <xref:System.String> non prises en charge en général :  
  
-   Surcharges prenant en charge la culture (méthodes qui prennent un `CultureInfo`  /  `StringComparison`  /  `IFormatProvider`).  
  
-   Méthodes qui acceptent ou génèrent un tableau de `char`.  
  
## <a name="unsupported-systemstring-static-methods"></a>Méthodes statiques System.String non prises en charge  
  
|Méthodes statiques System.String non prises en charge|  
|----------------------------------------------|  
|<xref:System.String.Copy%28System.String%29?displayProperty=nameWithType>|  
|<xref:System.String.Compare%28System.String%2CSystem.String%2CSystem.Boolean%29?displayProperty=nameWithType>|  
|<xref:System.String.Compare%28System.String%2CSystem.String%2CSystem.Boolean%2CSystem.Globalization.CultureInfo%29?displayProperty=nameWithType>|  
|<xref:System.String.Compare%28System.String%2CSystem.Int32%2CSystem.String%2CSystem.Int32%2CSystem.Int32%29?displayProperty=nameWithType>|  
|<xref:System.String.Compare%28System.String%2CSystem.Int32%2CSystem.String%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%29?displayProperty=nameWithType>|  
|<xref:System.String.Compare%28System.String%2CSystem.Int32%2CSystem.String%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%2CSystem.Globalization.CultureInfo%29?displayProperty=nameWithType>|  
|<xref:System.String.CompareOrdinal%28System.String%2CSystem.String%29?displayProperty=nameWithType>|  
|<xref:System.String.CompareOrdinal%28System.String%2CSystem.Int32%2CSystem.String%2CSystem.Int32%2CSystem.Int32%29?displayProperty=nameWithType>|  
|<xref:System.String.Format%2A?displayProperty=nameWithType>|  
|<xref:System.String.Join%2A?displayProperty=nameWithType>|  
  
## <a name="unsupported-systemstring-non-static-methods"></a>Méthodes non statiques System.String non prises en charge  
  
|Méthodes non statiques System.String non prises en charge|  
|---------------------------------------------------|  
|<xref:System.String.IndexOfAny%28System.Char%5B%5D%29?displayProperty=nameWithType>|  
|<xref:System.String.Split%2A?displayProperty=nameWithType>|  
|<xref:System.String.ToCharArray?displayProperty=nameWithType>|  
|<xref:System.String.ToUpper%28System.Globalization.CultureInfo%29?displayProperty=nameWithType>|  
|<xref:System.String.TrimEnd%28System.Char%5B%5D%29?displayProperty=nameWithType>|  
|<xref:System.String.TrimStart%28System.Char%5B%5D%29?displayProperty=nameWithType>|  
  
## <a name="differences-from-net"></a>Différences par rapport à .NET  
  
-   Les requêtes n'expliquent pas les classements SQL Server qui peuvent être appliqués sur le serveur, et par conséquent, fournissent par défaut des comparaisons dépendantes de la culture qui ne respectent pas la casse. Ce comportement diffère de la sémantique par défaut sensible à la casse du .NET Framework.  
  
-   Lorsque `LastIndexOf` retourne 0, la chaîne est `NULL` ou la position trouvée est 0.  
  
-   Des résultats inattendus peuvent être retournés de la concaténation ou d'autres opérations sur les chaînes de longueur fixe (`CHAR`, `NCHAR`), car le remplissage de ces types s'effectue automatiquement dans la base de données.  
  
-   Comme de nombreuses méthodes, telles que `Replace`, `ToLower`, `ToUpper` et l'indexeur de caractère, n'ont aucune traduction valide pour les colonnes `TEXT` ou `NTEXT` et XML, `SqlExceptions` se produit si la traduction se produit normalement. Ce comportement est considéré comme acceptable pour ces types. Toutefois, toutes les opérations de chaînes doivent correspondre à la sémantique Common Language Runtime (CLR) pour `VARCHAR`, `NVARCHAR`, `VARCHAR(max)` et `NVARCHAR(max)`.  
  
## <a name="see-also"></a>Voir aussi
- [Fonctions et types de données](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
