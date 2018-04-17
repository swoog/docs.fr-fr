---
title: Fournisseurs de type
description: 'Découvrez comment un fournisseur de type F # est un composant qui fournit des types, propriétés et méthodes à utiliser dans vos programmes.'
author: cartermp
ms.author: phcart
ms.date: 04/02/2018
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 25697ef6-465e-4248-9de5-1d199d4a8b59
ms.openlocfilehash: 248fb2db2364cdad53e701603fd2cada33498701
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="type-providers"></a>Fournisseurs de type

Un fournisseur de type F# est un composant qui fournit des types, des propriétés et des méthodes à utiliser dans votre programme. Fournisseurs de type génèrent ce que l'on appelle **fourni des Types**, qui sont généré par le compilateur F # et sont basé sur une source de données externe.

Par exemple, un fournisseur de Type F # pour SQL peut générer des types représentant les tables et colonnes dans une base de données relationnelle. En fait, c’est ce que le [SQLProvider](https://fsprojects.github.io/SQLProvider/) fournisseur de Type ne.

Fourni que types dépendent des paramètres d’entrée à un fournisseur de Type. Cette entrée peut être un exemple de source de données (par exemple, un fichier de schéma JSON), une URL qui pointe directement vers un service externe ou une chaîne de connexion à une source de données. Un fournisseur de Type garantit également que les groupes de types sont développés uniquement à la demande ; Autrement dit, ils sont développés si les types sont réellement référencés par votre programme. Cela permet l'intégration directe et à la demande d'espaces d'informations à grande échelle, tels que les marchés de données en ligne, de manière fortement typée.

## <a name="generative-and-erased-type-providers"></a>Fournisseurs de Type générative et effacées

Fournisseurs de type se présentent sous deux formes : générative et effacées.

Fournisseurs de Type générative produisent des types qui peuvent être écrits en tant que types .NET dans l’assembly dans lequel ils sont générés. Cela leur permet à être consommés à partir du code dans d’autres assemblys. Cela signifie que la représentation sous forme de type de la source de données doit être généralement un qui n’est possible de représenter avec les types .NET.

Effacement des fournisseurs de Type produisent des types qui ne peuvent être utilisés dans l’assembly ou le projet qu’ils sont générés à partir de. Les types sont éphémères ; Autrement dit, ils ne sont pas écrites dans un assembly et ne peut pas être consommés par le code dans d’autres assemblys. Elles peuvent contenir des *retardée* membres, vous permettant de types d’utilisation à partir d’un espace d’informations potentiellement infini. Ils sont utiles pour l’utilisation d’un petit sous-ensemble d’une source de données volumineux et interconnectés.

## <a name="commonly-used-type-providers"></a>Fournisseurs de Type communément utilisés

Les bibliothèques suivantes largement utilisé contiennent des fournisseurs de Type pour différentes utilisations :

- [FSharp.Data](https://fsharp.github.io/FSharp.Data/) inclut les fournisseurs de Type JSON, XML, CSV et HTML de ressources et les formats de document.
- [SQLProvider](https://fsprojects.github.io/SQLProvider/) fournit un accès fortement typé aux bases de données de relation via LINQ F # et de mappage d’objet de requêtes par rapport à ces sources de données.
- [FSharp.Data.SqlClient](https://fsprojects.github.io/FSharp.Data.SqlClient/) a un ensemble de fournisseurs de type pour le moment de la compilation vérifié l’incorporation de T-SQL en F #.
- [Le fournisseur de Type de stockage Azure](https://fsprojects.github.io/AzureStorageTypeProvider/) fournit des types pour les objets BLOB Azure, les Tables et les files d’attente, ce qui vous permet d’accéder à ces ressources sans avoir à spécifier des noms de ressources sous forme de chaînes dans l’ensemble de votre programme.
- [FSharp.Data.GraphQL](https://fsprojects.github.io/FSharp.Data.GraphQL/index.html) contient le **GraphQLProvider**, qui fournit les types basés sur un serveur GraphQL spécifié par l’URL.

Le cas échéant, vous pouvez [créer vos propres fournisseurs de type personnalisé](creating-a-type-provider.md), ou référencer des fournisseurs de type qui ont été créés par d’autres. Par exemple, supposez que votre organisation dispose d'un service de données fournissant un nombre important et croissant de jeux de données nommées, chacun avec son propre schéma stable de données. Vous pouvez choisir de créer un fournisseur de type qui lit les schémas et présente les derniers groupes de données disponibles au programmeur de manière fortement typée.

## <a name="see-also"></a>Voir aussi
[Didacticiel : Créer un fournisseur de Type](creating-a-type-provider.md)

[Informations de référence du langage F#](../../language-reference/index.md)

[Visual F#](../../index.md)
