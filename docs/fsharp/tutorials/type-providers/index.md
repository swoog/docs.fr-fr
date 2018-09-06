---
title: Fournisseurs de type
description: 'Découvrez comment un fournisseur de type F # est un composant qui fournit des types, propriétés et méthodes à utiliser dans vos programmes.'
ms.date: 04/02/2018
ms.openlocfilehash: 5fa9de229caa2ec3ba4a248ca5cd1c8aa5adb230
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43891666"
---
# <a name="type-providers"></a>Fournisseurs de type

Un fournisseur de type F# est un composant qui fournit des types, des propriétés et des méthodes à utiliser dans votre programme. Fournisseurs de type génèrent ce que l'on **Types fourni**, qui sont généré par le compilateur F # et sont basé sur une source de données externe.

Par exemple, un fournisseur de Type F # pour SQL peut générer des types représentant les tables et colonnes dans une base de données relationnelle. En fait, c’est ce que le [SQLProvider](https://fsprojects.github.io/SQLProvider/) fournisseur de Type ne.

Fourni que types dépendent des paramètres d’entrée à un fournisseur de Type. Entrée de ce genre peut être un exemple de source de données (par exemple, un fichier de schéma JSON), une URL qui pointe directement vers un service externe ou une chaîne de connexion à une source de données. Un fournisseur de Type peut également vous assurer que les groupes de types sont développés uniquement à la demande ; Autrement dit, ils sont développés si les types sont réellement référencés par votre programme. Cela permet l'intégration directe et à la demande d'espaces d'informations à grande échelle, tels que les marchés de données en ligne, de manière fortement typée.

## <a name="generative-and-erased-type-providers"></a>Fournisseurs de Type générative et effacé

Fournisseurs de type se présentent sous deux formes : générative et effacées.

Les fournisseurs de Type générative produisent des types qui peuvent être écrits en tant que types .NET dans l’assembly dans lequel ils sont générés. Cela leur permet d’être utilisé à partir du code dans d’autres assemblys. Cela signifie que la représentation typée de la source de données doit être généralement un est possible de représenter avec des types .NET.

Effacement des fournisseurs de Type produisent des types qui peuvent uniquement être utilisées dans l’assembly ou le projet, de qu'ils sont générés à partir. Les types sont éphémères ; Autrement dit, ils ne sont pas écrites dans un assembly et ne peut pas être consommés par le code dans d’autres assemblys. Elles peuvent contenir des *retardée* membres, vous permettant d’utiliser les types à partir d’un espace potentiellement infini d’informations. Elles sont utiles pour l’utilisation d’un petit sous-ensemble d’une source de données volumineux et interconnectées.

## <a name="commonly-used-type-providers"></a>Couramment utilisé des fournisseurs de Type

Les bibliothèques de largement utilisé suivantes contiennent des fournisseurs de Type pour différentes utilisations :

- [FSharp.Data](https://fsharp.github.io/FSharp.Data/) inclut les fournisseurs de Type pour les formats de document JSON, XML, CSV, HTML et ressources.
- [SQLProvider](https://fsprojects.github.io/SQLProvider/) fournit accès fortement typé aux bases de données de relation via LINQ F # et de mappage de l’objet de requêtes par rapport à ces sources de données.
- [FSharp.Data.SqlClient](https://fsprojects.github.io/FSharp.Data.SqlClient/) a un ensemble de fournisseurs de type pour le moment de la compilation vérifié l’incorporation de T-SQL en F #.
- [Fournisseur de Type de stockage Azure](https://fsprojects.github.io/AzureStorageTypeProvider/) fournit des types pour les objets BLOB Azure, les Tables et les files d’attente, ce qui vous permet d’accéder à ces ressources sans avoir à spécifier des noms de ressources sous forme de chaînes tout au long de votre programme.
- [FSharp.Data.GraphQL](https://fsprojects.github.io/FSharp.Data.GraphQL/index.html) contient le **GraphQLProvider**, qui fournit des types basés sur un serveur GraphQL spécifié par URL.

Lorsque cela est nécessaire, vous pouvez [créer vos propres fournisseurs de type personnalisé](creating-a-type-provider.md), ou référencer des fournisseurs de type qui ont été créés par d’autres utilisateurs. Par exemple, supposez que votre organisation dispose d'un service de données fournissant un nombre important et croissant de jeux de données nommées, chacun avec son propre schéma stable de données. Vous pouvez choisir de créer un fournisseur de type qui lit les schémas et présente les derniers groupes de données disponibles au programmeur de manière fortement typée.

## <a name="see-also"></a>Voir aussi

- [Didacticiel : Créer un fournisseur de Type](creating-a-type-provider.md)
- [Informations de référence du langage F#](../../language-reference/index.md)
- [Visual F#](../../index.md)
