---
title: Collecte des données de télémétrie par la CLI ML.NET
description: Découvrez les fonctionnalités de télémétrie de la CLI ML.NET, qui collectent des informations d’utilisation à des fins d’analyse, les types de données collectées et comment désactiver la télémétrie. En outre, vous trouverez des liens vers le contrat de licence de .NET et des informations sur la conformité de Microsoft au RGPD.
ms.topic: conceptual
ms.date: 05/05/2019
ms.custom: ''
ms.openlocfilehash: 49ebd6c9e1b77c85d891b8c9fb8cbd5c66b478a9
ms.sourcegitcommit: ca2ca60e6f5ea327f164be7ce26d9599e0f85fe4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65065542"
---
# <a name="telemetry-collection-by-the-mlnet-cli"></a>Collecte des données de télémétrie par la CLI ML.NET

La [CLI ML.NET](http://aka.ms/mlnet-cli) inclut une fonctionnalité de télémétrie qui collecte les données d’utilisation anonymes, qui sont agrégées en vue d’une utilisation par Microsoft.

## <a name="how-microsoft-uses-the-data"></a>Comment Microsoft utilise les données

L’équipe de produit utilise les données de télémétrie collectées par la CLI ML.NET pour essayer de comprendre comment améliorer les outils. Par exemple, si les clients utilisent rarement une tâche de machine learning spécifique, l’équipe de produit en analyse la raison, puis hiérarchise le développement des fonctionnalités à partir des conclusions qu’elle a tirées. En outre, les données de télémétrie collectées par la CLI ML.NET facilitent le débogage des problèmes tels que les plantages et les anomalies de code. 

Bien que l’équipe de produit apprécie cet insight, nous savons également que tout le monde n’est pas disposé à envoyer ces données. [Découvrez comment désactiver la télémétrie.](#opt-out-of-data-collection)

## <a name="scope"></a>Portée

La commande `mlnet` lance l’interface CLI ML.NET, mais ne collecte pas elle-même les données de télémétrie.

La télémétrie *n’est pas activée* quand vous exécutez la commande `mlnet` sans aucune autre commande attachée. Par exemple :

- `mlnet`
- `mlnet --help`

La télémétrie *est activée* quand vous exécutez une [commande CLI ML.NET](../reference/ml-net-cli-reference.md), telle que `mlnet auto-train`.

## <a name="opt-out-of-data-collection"></a>Refuser la collecte de données

La fonctionnalité de télémétrie de la CLI ML.NET est activée par défaut.

Pour la désactiver, affectez la valeur `1` ou `true` à la variable d’environnement `DOTNET_CLI_TELEMETRY_OPTOUT`. Cette variable d’environnement s’applique globalement à l’outil CLI .NET.

## <a name="data-points-collected"></a>Points de données collectés

La fonctionnalité recueille les données suivantes :

- Les commandes appelées, comme `auto-train`
- Adresse MAC hachée : ID unique et anonyme chiffré (SHA256) pour une machine
- Horodatage d’un appel
- Adresse IP de trois octets utilisée uniquement pour déterminer l’emplacement géographique
- Nom de tous les arguments/paramètres utilisés. Pas les valeurs du client, telles que des chaînes.
- Système d’exploitation et version
- Valeur du paramètre --ml-task : valeurs de catégorie, telles que `regression`, `binary-classification` et `multiclass-classification`
- Taille du fichier de jeu de données avec [arrondi logarithmique](https://en.wikipedia.org/wiki/Rounding#Rounding_to_a_specified_power) (puissance de 2 la plus proche)
- `ExitCode` de la commande

Les données sont envoyées de manière sécurisée à des serveurs Microsoft à l’aide de la technologie [Azure Application Insights](https://azure.microsoft.com/services/application-insights/), stockées à un emplacement dont l’accès est strictement limité et utilisées conformément à des contrôles de sécurité stricts à partir de systèmes [Stockage Azure](https://azure.microsoft.com/services/storage/) sécurisés.

### <a name="data-points-not-collected"></a>Points de données non collectés
La fonctionnalité de télémétrie *ne collecte pas* les données suivantes :
- Données personnelles, telles que les noms d’utilisateur
- Noms de fichier de jeu de données
- Données des fichiers de jeu de données

Si vous pensez que la fonctionnalité de télémétrie de la CLI ML.NET collecte des données sensibles ou que les données sont gérées de manière non sécurisée ou incorrecte, soumettez un problème dans le dépôt [ML.NET](https://github.com/dotnet/machinelearning) afin que nous investiguions.

## <a name="license"></a>Licence

La distribution Microsoft de la CLI ML.NET est concédée sous licence avec les [Termes du contrat de licence logicielle Microsoft : bibliothèque Microsoft .NET](https://aka.ms/dotnet-core-eula). Pour plus d’informations sur la collecte et le traitement de données, consultez la section intitulée « Données ».

## <a name="disclosure"></a>Divulgation d’informations

Quand vous exécutez pour la première fois une [commande de la CLI ML.NET](../reference/ml-net-cli-reference.md) telle que `mlnet auto-train`, l’outil CLI ML.NET affiche un texte de divulgation qui vous indique comment refuser la télémétrie. Le texte peut varier légèrement selon la version de la CLI que vous exécutez.

## <a name="see-also"></a>Voir aussi
- [Informations de référence sur l’interface de ligne de commande ML.NET](../reference/ml-net-cli-reference.md)
- [Termes du contrat de licence logiciel Microsoft : bibliothèque Microsoft .NET](https://aka.ms/dotnet-core-eula)
- [Confidentialité chez Microsoft](https://www.microsoft.com/en-us/trustcenter/privacy/)
- [Déclaration de confidentialité Microsoft](https://privacy.microsoft.com/en-us/privacystatement)
