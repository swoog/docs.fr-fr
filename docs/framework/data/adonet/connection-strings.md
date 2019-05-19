---
title: Chaînes de connexion dans ADO.NET
ms.date: 10/10/2018
ms.assetid: 745c5f95-2f02-4674-b378-6d51a7ec2490
ms.openlocfilehash: 3b7cb0ab061da8364a9fecc3868ba9aaf7501577
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65881160"
---
# <a name="connection-strings-in-adonet"></a>Chaînes de connexion dans ADO.NET

Une chaîne de connexion contient des informations d'initialisation qui sont passées en tant que paramètre d'un fournisseur de données à une source de données. Le fournisseur de données reçoit la chaîne de connexion en tant que la valeur de la <xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType> propriété. Le fournisseur analyse la chaîne de connexion et vérifie que la syntaxe est correcte et que les mots clés sont pris en charge. Le <xref:System.Data.Common.DbConnection.Open?displayProperty=nameWithType> méthode passe les paramètres de connexion analysée à la source de données. La source de données effectue une validation supplémentaire et établit une connexion.

## <a name="connection-string-syntax"></a>Syntaxe de chaîne de connexion

Une chaîne de connexion est une liste délimitée par des points-virgules de paires clé/valeur de paramètre :

```
keyword1=value; keyword2=value;
```

Mots clés ne respectent pas la casse. Valeurs, toutefois, peuvent être la casse, en fonction de la source de données. Peuvent contenir des mots clés et valeurs [blancs](https://en.wikipedia.org/wiki/Whitespace_character#Unicode). Espaces de début et de fin est ignoré dans les mots clés et guillemets valeurs.

Si une valeur contient le point-virgule, [caractères de contrôle Unicode](https://en.wikipedia.org/wiki/Unicode_control_characters), ou à gauche ou un espace blanc, elle doit figurer entre guillemets simples ou doubles. Exemple :

```
Keyword=" whitespace  ";
Keyword='special;character';
```

Le caractère englobant n’a pas peut se produire au sein de la valeur qu’elle comprend. Par conséquent, une valeur contenant des guillemets simples peut être placées entre uniquement dans des guillemets doubles et vice versa :

```
Keyword='double"quotation;mark';
Keyword="single'quotation;mark";
```

Les guillemets eux-mêmes, ainsi que le signe égal, ne nécessite pas d’échappement, par conséquent, les chaînes de connexion suivantes sont valides :

```
Keyword=no "escaping" 'required';
Keyword=a=b=c
```

Dans la mesure où chaque valeur est lue jusqu'à ce que le point-virgule suivant ou à la fin de chaîne, la valeur dans l’exemple de ce dernier est `a=b=c`, et le point-virgule final est facultatif.

Toutes les chaînes de connexion partagent la même syntaxe de base décrite ci-dessus. L’ensemble des mots clés reconnus varie selon le fournisseur, toutefois et a évolué au fil des années à partir d’API antérieures telles que *ODBC*. Le *.NET Framework* fournisseur de données pour *SQL Server* (`SqlClient`) prend en charge de nombreux mots clés à partir d’une API plus anciennes, mais se montre généralement plus souple et accepte des synonymes pour la plupart de la chaîne de connexion courantes mots clés.

Fautes de frappe peut provoquer des erreurs. Par exemple, `Integrated Security=true` est valide, mais `IntegratedSecurity=true` provoque une erreur.

Chaînes de connexion générées manuellement en cours d’exécution à partir de l’entrée utilisateur non validée sont vulnérables aux attaques par injection de chaîne et mettre en péril la sécurité au niveau de la source de données. Pour résoudre ces problèmes, *ADO.NET* 2.0 a introduit [générateurs de chaînes de connexion](../../../../docs/framework/data/adonet/connection-string-builders.md) pour chaque *.NET Framework* fournisseur de données. Ces générateurs de chaînes de connexion exposent des paramètres en tant que propriétés fortement typées et le rendent possible de valider la chaîne de connexion avant d’être envoyée à la source de données.

## <a name="in-this-section"></a>Dans cette section

[Générateurs de chaînes de connexion](../../../../docs/framework/data/adonet/connection-string-builders.md)\
Montre comment utiliser les classes `ConnectionStringBuilder` pour générer des chaînes de connexion valides au moment de l'exécution.

[Chaînes de connexion et les fichiers de Configuration](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md)\
Montre comment stocker et extraire des chaînes de connexion dans des fichiers de configuration.

[Syntaxe de chaîne de connexion](../../../../docs/framework/data/adonet/connection-string-syntax.md)\
Décrit comment configurer des chaînes de connexion spécifiques au fournisseur pour `SqlClient`, `OracleClient`, `OleDb` et `Odbc`.

[Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md)\
Montre des techniques pour la protection des informations utilisées pour la connexion à une source de données.

## <a name="see-also"></a>Voir aussi

- [Connexion à une source de données](/cpp/data/odbc/connecting-to-a-data-source)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
