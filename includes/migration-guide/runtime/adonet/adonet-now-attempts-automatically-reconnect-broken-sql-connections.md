---
ms.openlocfilehash: 4c65cd62b2d84ef2b852d10a04e5f6ce0cc82d3a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235389"
---
### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET tente maintenant de reconnecter automatiquement les connexions SQL rompues

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5.1, le .NET Framework tente de reconnecter automatiquement les connexions SQL rompues. Bien que cette opération améliore généralement la fiabilité des applications, il existe des cas particuliers où une application doit savoir que la connexion a été perdue afin de pouvoir prendre des mesures lors de la reconnexion.|
|Suggestion|Si cette fonctionnalité n’est pas souhaitable pour des raisons de compatibilité, elle peut être désactivée en affectant à la propriété <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> d’une chaîne de connexion (ou <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) la valeur 0.|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|
