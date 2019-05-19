---
title: Exécution côte à côte dans ADO.NET
ms.date: 03/30/2017
ms.assetid: 9f9ba96d-9f89-4f65-bb2f-6860879f4393
ms.openlocfilehash: d20d8e81d76284509d6fe733e4f283a9ab39cb00
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65877092"
---
# <a name="side-by-side-execution-in-adonet"></a>Exécution côte à côte dans ADO.NET
L’exécution côte à côte dans le .NET Framework est la possibilité d’exécuter une application sur un ordinateur qui possède plusieurs versions du .NET Framework installé, exclusivement à l’aide de la version pour laquelle l’application a été compilée. Pour plus d’informations sur la configuration de l’exécution côte à côte, consultez [l’exécution côte à côte](../../../../docs/framework/deployment/side-by-side-execution.md).  
  
 Une application compilée à l’aide d’une version du .NET Framework permettre s’exécuter sur une version différente du .NET Framework. Toutefois, nous recommandons que vous compilez une version de l’application pour chaque version installée du .NET Framework et les exécutez séparément. Dans les deux cas, soyez conscient des modifications dans ADO.NET entre les versions qui peuvent affecter la compatibilité ascendante ou descendante de votre application.  
  
## <a name="forward-compatibility-and-backward-compatibility"></a>Compatibilités descendante et ascendante  
 Compatibilité ascendante signifie qu’une application peut être compilée avec une version antérieure du .NET Framework, elle fonctionnera correctement avec une version ultérieure du .NET Framework. Code ADO.NET écrit pour le .NET Framework version 1.1 sera compatible avec les versions ultérieures.  
  
 La compatibilité descendante signifie qu’une application est compilée pour une version plus récente du .NET Framework, mais continue à s’exécuter sur des versions antérieures du .NET Framework sans aucune perte de fonctionnalité. Bien entendu, cela ne sera pas le cas pour les fonctionnalités introduites dans une nouvelle version du .NET Framework.  
  
## <a name="the-net-framework-data-provider-for-odbc"></a>Fournisseur de données .NET Framework pour ODBC  
 Depuis la version 1.1, le fournisseur de données .NET Framework pour ODBC (<xref:System.Data.Odbc>) est inclus dans le cadre du .NET Framework. Le fournisseur de données ODBC est disponible pour les développeurs .NET Framework version 1.0 sous forme de téléchargement Web à partir de la [Data Access and Storage Developer Center](https://go.microsoft.com/fwlink/?linkid=4173). L’espace de noms pour le fournisseur de données .NET Framework téléchargé pour ODBC est **Microsoft.Data.Odbc**.  
  
 Si vous avez une application développée pour le .NET Framework version 1.0 qui utilise le fournisseur de données ODBC pour se connecter à votre source de données, et que vous souhaitez exécuter cette application sur le .NET Framework version 1.1 ou une version ultérieure, vous devez mettre à jour l’espace de noms pour le dat ODBC un fournisseur à **System.Data.Odbc**. Vous devez ensuite le recompiler pour la version la plus récente du .NET Framework.  
  
 Si vous avez une application développée pour le .NET Framework version 2.0 ou version ultérieure qui utilise le fournisseur de données ODBC pour se connecter à votre source de données, et que vous souhaitez exécuter cette application sur le .NET Framework version 1.0, vous devez télécharger le fournisseur de données ODBC et l’installer sur le système de la version 1.0 de .NET Framework. Vous devez ensuite modifier l’espace de noms pour le fournisseur de données ODBC à **Microsoft.Data.Odbc**et recompiler l’application pour le .NET Framework version 1.0.  
  
## <a name="the-net-framework-data-provider-for-oracle"></a>Fournisseur de données .NET Framework pour Oracle  
 Depuis la version 1.1, le fournisseur de données .NET Framework pour Oracle (<xref:System.Data.OracleClient>) est inclus dans le cadre du .NET Framework. Le fournisseur de données est disponible pour les développeurs .NET Framework version 1.0 sous forme de téléchargement Web à partir de la [Data Access and Storage Developer Center](https://go.microsoft.com/fwlink/?linkid=4173).  
  
 Si vous avez une application développée pour le .NET Framework version 2.0 ou version ultérieure qui utilise le fournisseur de données pour se connecter à votre source de données, et que vous souhaitez exécuter cette application sur le .NET Framework version 1.0, vous devez télécharger le fournisseur de données et l’installer sur le .NE Système de la version 1.0 de Framework de T.  
  
## <a name="code-access-security"></a>Sécurité d'accès du code  
 Les fournisseurs de données .NET Framework dans le .NET Framework version 1.0 (<xref:System.Data.SqlClient>, <xref:System.Data.OleDb>) sont requis pour exécuter avec l’autorisation FullTrust. Toute tentative d’utiliser les fournisseurs de données .NET Framework k à partir de la version 1.0 du .NET Framework dans une zone avec une moindre causes d’autorisation FullTrust un <xref:System.Security.SecurityException>.  
  
 Toutefois, à compter de .NET Framework version 2.0, tous les fournisseurs de données .NET Framework peuvent servir dans les zones de confiance partielle. En outre, une nouvelle fonctionnalité de sécurité a été ajoutée pour les fournisseurs de données .NET Framework dans le .NET Framework version 1.1. Cette fonctionnalité vous permet de restreindre les chaînes de connexion qui peuvent être utilisées dans une zone de sécurité particulière. Vous pouvez également désactiver l'utilisation des mots de passe vides pour une zone de sécurité particulière. Pour plus d'informations, consultez [Code Access Security and ADO.NET](../../../../docs/framework/data/adonet/code-access-security.md).  
  
 Étant donné que chaque installation du .NET Framework possède un fichier Security.config distinct, il n’existe aucun problème de compatibilité avec les paramètres de sécurité. Toutefois, si votre application dépend des fonctionnalités de sécurité supplémentaires de ADO.NET incluse dans la version de .NET Framework 1.1 et ultérieures, vous ne pourrez pas distribuer à un système de la version 1.0.  
  
## <a name="sqlcommand-execution"></a>Exécution de SqlCommand  
 En commençant par le .NET Framework version 1.1, la façon qui <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A> exécute des commandes sur les données source a été modifiée.  
  
 Dans le .NET Framework version 1.0, <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A> exécutée toutes les commandes dans le contexte de la **sp_executesql** procédure stockée. Par conséquent, les commandes qui affectent l'état de la connexion (SET NOCOUNT ON, par exemple) ne s'appliquent qu'à l'exécution de la commande actuelle. L'état de la connexion n'est pas modifié pour les commandes suivantes qui sont exécutées pendant que la connexion est ouverte.  
  
 Dans le .NET Framework version 1.1 et ultérieure, <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A> s’exécute uniquement une commande dans le contexte de la **sp_executesql** procédure stockée si la commande contient des paramètres, ce qui permet un gain de performances. Par conséquent, si une commande affectant l'état de la connexion est incluse dans une commande non paramétrée, elle modifie l'état de la connexion pour toutes les commandes suivantes exécutées pendant que la connexion est ouverte.  
  
 Considérez le lot de commandes suivant exécuté dans un appel à <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A>.  
  
```sql
SET NOCOUNT ON;  
SELECT * FROM dbo.Customers;  
```  
  
 Dans le .NET Framework version 1.1 et ultérieure, NOCOUNT conserve la valeur ON pour toutes les commandes suivantes exécutées pendant que la connexion est ouverte. Dans le .NET Framework version 1.0, NOCOUNT n'on que pour l’exécution de la commande actuelle.  
  
 Cette modification peut affecter la compatibilité descendante et ascendante de votre application si vous dépendez du comportement de <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A> pour les deux versions du .NET Framework.  
  
 Pour les applications qui s’exécutent sur des versions antérieures ou ultérieures du .NET Framework, vous pouvez écrire votre code pour vous assurer que le comportement est le même quelle que soit la version en cours d’exécution sur. Si vous souhaitez vous assurer qu'une commande modifie l'état de la connexion pour toutes les commandes suivantes, nous vous recommandons d'exécuter votre commande à l'aide de la méthode <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery%2A>. Si vous souhaitez vous assurer qu'une commande ne modifie pas la connexion pour toutes les commandes suivantes, nous vous recommandons d'inclure les commandes qui rétablissent l'état de la connexion dans votre commande. Exemple :  
  
```sql
SET NOCOUNT ON;  
SELECT * FROM dbo.Customers;  
SET NOCOUNT OFF;  
```  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble d’ADO.NET](../../../../docs/framework/data/adonet/ado-net-overview.md)
- [Extraction et modification de données dans ADO.NET](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
