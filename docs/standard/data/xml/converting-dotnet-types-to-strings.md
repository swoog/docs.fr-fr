---
title: Conversion de types .NET Framework en chaînes
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: dc2e2b65-f623-4dc3-938b-d2a054d6832c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59e288a756a022763bae2235964a8b25a9d72bd1
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2018
ms.locfileid: "47399646"
---
# <a name="converting-net-framework-types-to-strings"></a>Conversion de types .NET Framework en chaînes
Si vous voulez convertir un type .NET Framework en chaîne, utilisez la méthode **ToString**. La méthode **ToString** retourne une représentation sous forme de chaîne du type passé. Le tableau suivant répertorie les types .NET Framework qui retournent une chaîne dans un format qui mappe aux spécifications de schéma XML (XSD).  
  
|Type .NET Framework|Type de chaîne de retour|  
|-------------------------|--------------------------|  
|Booléen|"true", "false"|  
|Single.PositiveInfinity|"INF"|  
|Single.NegativeInfinity|"-INF"|  
|Double.PositiveInfinity|"INF"|  
|Double.NegativeInfinity|"-INF"|  
|DateTime|Le format est yyyy-MM-ddTHH:mm:sszzzzzz et ses sous-ensembles.|  
|TimeSpan|Le format est PnYnMnTnHnMnS. Par exemple, `P2Y10M15DT10H30M20S` est la durée de 2 années, 10 mois, 15 jours, 10 heures, 30 minutes et 20 secondes.|  
  
## <a name="see-also"></a>Voir aussi

- [Conversion des types de données XML](../../../../docs/standard/data/xml/conversion-of-xml-data-types.md)  
- [Conversion de chaînes en types de données .NET Framework](../../../../docs/standard/data/xml/converting-strings-to-dotnet-data-types.md)
