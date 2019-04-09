---
title: Espaces de noms (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 83991c21-60db-4af9-aca3-b416f6cae98e
ms.openlocfilehash: bef2fa96ce090a600155d68ecc3daea55b675840
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59185521"
---
# <a name="namespaces-entity-sql"></a>Espaces de noms (Entity SQL)
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] introduit les espaces de noms pour éviter les conflits de noms des identificateurs globaux tels que les noms de types, les jeux d’entités, les fonctions et ainsi de suite. La prise en charge de l’espace de noms dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)] est similaire à la prise en charge de l’espace de noms dans le [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)].  
  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] fournit deux formes de la clause USING : qualifiés (où un alias plus court est fourni pour l’espace de noms) des espaces de noms et les espaces de noms non qualifiés, comme illustré dans l’exemple suivant :  
  
 `USING System.Data;`  
  
 `USING tsql = System.Data;`  
  
## <a name="name-resolution-rules"></a>Règles de résolution de noms  
 Si un identificateur ne peut pas être résolu dans les portées locales, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] tente de localiser le nom dans les portées globales (les espaces de noms). [!INCLUDE[esql](../../../../../../includes/esql-md.md)] tout d’abord essaie de correspondre à l’identificateur (préfixe) avec l’un des espaces de noms qualifiés. S’il existe une correspondance, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] tente de résoudre le reste de l’identificateur dans l’espace de noms spécifié. Si aucune correspondance n'est trouvée, une exception est levée.  
  
 Ensuite, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] tente de rechercher tous les non qualifiés espaces de noms (spécifiés dans le prologue) pour l’identificateur. Si l'identificateur est localisé dans exactement un espace de noms, cet emplacement est retourné. Si plusieurs espaces de noms ont une correspondance pour cet identificateur, une exception est levée. Si aucun espace de noms ne peut être identifié pour l’identificateur, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] passe le nom à l’étendue externe suivante (le <xref:System.Data.Common.DbCommand> ou <xref:System.Data.Common.DbConnection> objet), comme illustré dans l’exemple suivant :  
  
```  
SELECT TREAT(p AS NamespaceName.Employee)  
FROM ContainerName.Person AS p  
WHERE p IS OF (NamespaceName.Employee)  
```  
  
## <a name="differences-from-the-net-framework"></a>Différences par rapport au .NET Framework  
 Dans le [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)], vous pouvez utiliser des espaces de noms partiellement qualifiés. [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ne permet pas cela.  
  
## <a name="adonet-usage"></a>Utilisation d'ADO.NET  
 Les requêtes sont exprimées par le biais d'objets <xref:System.Data.Common.DbCommand> ADO.NET. <xref:System.Data.Common.DbCommand> les objets peuvent être créés à partir <xref:System.Data.Common.DbConnection> objets. Il est également possible de spécifier des espaces de noms comme faisant partie des objets <xref:System.Data.Common.DbCommand> et <xref:System.Data.Common.DbConnection>. Si [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ne peut pas résoudre un identificateur dans la requête elle-même, les espaces de noms externes sont détectés (en fonction des règles similaires).  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Vue d'ensemble d'Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
