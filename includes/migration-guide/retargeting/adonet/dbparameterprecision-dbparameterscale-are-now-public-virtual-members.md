---
ms.openlocfilehash: 1721d32f8cdc9b6ea4b4732e38afa56a8a532600
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234730"
---
### <a name="dbparameterprecision-and-dbparameterscale-are-now-public-virtual-members"></a>DbParameter.Precision et DbParameter.Scale sont maintenant des membres virtuels publics

|   |   |
|---|---|
|Détails|<xref:System.Data.Common.DbParameter.Precision> et <xref:System.Data.Common.DbParameter.Scale> sont implémentées en tant que propriétés virtuelles publiques. Elles remplacent les implémentations d'interface explicites correspondantes, <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> et <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.|
|Suggestion|Lorsque vous régénérez un fournisseur de base de données ADO.NET, vous devez désormais appliquer le mot clé « override » aux propriétés Precision et Scale. Cette opération est nécessaire uniquement si vous régénérez les composants. Les fichiers binaires existants continuent de fonctionner.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Data.Common.DbParameter.Precision?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbParameter.Scale?displayProperty=nameWithType></li></ul>|
