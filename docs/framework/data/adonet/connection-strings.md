---
title: Chaînes de connexion dans ADO.NET
ms.date: 03/30/2017
ms.assetid: 745c5f95-2f02-4674-b378-6d51a7ec2490
ms.openlocfilehash: 1e6e2b6870195c99279639e1f4576a30b7126d4d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583685"
---
# <a name="connection-strings-in-adonet"></a>Chaînes de connexion dans ADO.NET
Le .NET Framework 2.0 a introduit de nouvelles fonctionnalités permettant d'utiliser des chaînes de connexion, y compris l'intégration de nouveaux mots clés aux classes de générateur de chaînes de connexion, qui facilitent la création de chaînes de connexion valides au moment de l'exécution.  
  
Une chaîne de connexion contient des informations d'initialisation qui sont passées en tant que paramètre d'un fournisseur de données à une source de données. La syntaxe dépend du fournisseur de données et la chaîne de connexion est analysée lors de la tentative d'ouverture d'une connexion. Des erreurs de syntaxe génèrent une exception runtime mais d'autres erreurs ne se produisent qu'après que la source de données a reçu des informations de connexion. Une fois validée, la source de données applique les options spécifiées dans la chaîne de connexion et ouvre la connexion.
  
Le format d'une chaîne de connexion est une liste délimitée par des points-virgules de paires de paramètres clé/valeur :
  
    keyword1=value; keyword2=value;
  
Mots clés ne respectent pas la casse. Valeurs, toutefois, peuvent être la casse, en fonction de la source de données. Peuvent contenir des mots clés et valeurs [blancs](https://en.wikipedia.org/wiki/Whitespace_character#Unicode), bien que le début et de fin d’un espace blanc sont ignoré dans les mots clés et guillemets valeurs.

Si une valeur contient le point-virgule, [caractères de contrôle Unicode](https://en.wikipedia.org/wiki/Unicode_control_characters), début ou de fin d’un espace blanc elle doit figurer entre guillemets simples ou doubles, par exemple :

    Keyword=" whitespace  ";
    Keyword='special;character';

Le caractère englobant n’a pas peut se produire au sein de la valeur qu’elle comprend. Par conséquent, une valeur contenant des guillemets simples peut être placées entre uniquement dans des guillemets doubles et vice versa :

    Keyword='double"quotation;mark';
    Keyword="single'quotation;mark";

Les guillemets eux-mêmes, ainsi que le signe égal, ne nécessite pas d’échappement, par conséquent, les chaînes de connexion suivantes sont valides :

    Keyword=no "escaping" 'required';
    Keyword=a=b=c

Dans la mesure où chaque valeur est lue jusqu'à ce que le point-virgule suivant ou à la fin de chaîne, la valeur dans l’exemple de ce dernier est `a=b=c`, et le point-virgule final est facultatif.

La syntaxe de chaîne de connexion valide dépend du fournisseur et a évolué au fil des ans, par rapport aux premières API, telles qu'ODBC. Le fournisseur de données .NET Framework pour SQL Server (SqlClient) incorpore de nombreux éléments d'une syntaxe plus ancienne et se montre généralement plus souple avec une syntaxe de chaîne de connexion ordinaire. Des synonymes tout aussi valides d'éléments de syntaxe de chaîne de connexion se rencontrent fréquemment, mais certaines erreurs de syntaxe et d'orthographe peuvent poser des problèmes. Par exemple, "`Integrated Security=true`" est valide, tandis que "`IntegratedSecurity=true`" provoque une erreur. Par ailleurs, les chaînes de connexion générées au moment de l'exécution à partir d'une entrée utilisateur non validée peuvent entraîner des attaques par injection de chaîne, ce qui compromet la sécurité au niveau de la source de données.
  
Pour résoudre ces problèmes, ADO.NET 2.0 a introduit de nouveaux générateurs de chaînes de connexion pour chaque fournisseur de données .NET Framework. Les mots clés son exposés en tant que propriétés, ce qui permet de valider la syntaxe de chaîne de connexion avant de la soumettre à la source de données.
  
## <a name="in-this-section"></a>Dans cette section  
 [Générateurs de chaînes de connexion](../../../../docs/framework/data/adonet/connection-string-builders.md)  
 Montre comment utiliser les classes `ConnectionStringBuilder` pour générer des chaînes de connexion valides au moment de l'exécution.
  
 [Chaînes de connexion et fichiers de configuration](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md)  
 Montre comment stocker et extraire des chaînes de connexion dans des fichiers de configuration.
  
 [Syntaxe des chaînes de connexion](../../../../docs/framework/data/adonet/connection-string-syntax.md)  
 Décrit comment configurer des chaînes de connexion spécifiques au fournisseur pour `SqlClient`, `OracleClient`, `OleDb` et `Odbc`.
  
 [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md)  
 Montre des techniques pour la protection des informations utilisées pour la connexion à une source de données.
  
## <a name="see-also"></a>Voir aussi  
 [Connexion à une source de données](/cpp/data/odbc/connecting-to-a-data-source)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
