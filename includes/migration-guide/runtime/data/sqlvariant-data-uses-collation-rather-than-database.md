---
ms.openlocfilehash: e7a5a95a5d13f3396d396ad0d74a19a0efa3a967
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235273"
---
### <a name="sqlvariant-data-uses-sqlvariant-collation-rather-than-database-collation"></a>Les données Sql_variant utilisent le classement sql_variant plutôt que le classement de la base de données

|   |   |
|---|---|
|Détails|<code>sql_variant</code> Les données utilisent le classement <code>sql_variant</code> plutôt que le classement de la base de données.|
|Suggestion|Cette modification permet de répondre à une éventuelle altération de données si le classement de la base de données est différent du classement <code>sql_variant</code>. Les applications qui s'appuient sur les données endommagées peuvent éventuellement échouer.|
|Portée|Transparent|
|Version|4.5|
|Type|Runtime|
