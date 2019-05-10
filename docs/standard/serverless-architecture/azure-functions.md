---
title: Azure Functions - applications sans serveur
description: Fonctions Azure offrent des fonctionnalités sans serveur dans plusieurs langues (C# JavaScript, Java) et plateformes pour fournir pilotée par événements instantanée mettre à l’échelle de code.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 4febcc01eebf3efce3fc1eb42e19c2ec6c0baa52
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64754233"
---
# <a name="azure-functions"></a>Azure Functions

Azure functions fournit une expérience de calcul sans serveur. Une fonction est appelée par un *déclencheur* (par exemple, l’accès à un point de terminaison HTTP ou un minuteur) et exécute un bloc de code ni la logique métier. Fonctions également la prise en charge spécialisée *liaisons* qui se connectent aux ressources telles que les files d’attente et de stockage.

![Logo de fonctions Azure](./media/azure-functions-logo.png)

Il existe deux versions de l’infrastructure Azure Functions. L’ancienne version prend en charge le .NET Framework complet et le nouveau runtime prend en charge les applications .NET Core multiplateforme. Langues supplémentaires en plus de C# tels que JavaScript, F#, et Java sont prises en charge. Fonctions créées dans le portail fournissent une syntaxe de script complexe. Fonctions créées en tant que projets autonomes peuvent être déployées avec des fonctionnalités et de support de plate-forme complet.

Pour plus d’informations, consultez [documentation Azure Functions](https://docs.microsoft.com/azure/azure-functions).

## <a name="functions-v1-vs-v2"></a>Fonctions des v1 et v2

Il existe deux versions du runtime Azure Functions : 1.x et 2.x. Version 1.x est généralement disponible (GA). Il prend en charge le développement de .NET à partir du portail ou les machines Windows et utilise le .NET Framework. 1.x prend en charge C#, JavaScript, et F#, avec prise en charge expérimentale pour Python, PHP, TypeScript, Batch, Bash et PowerShell.

[Version 2.x est également généralement disponible maintenant](https://azure.microsoft.com/blog/introducing-azure-functions-2-0/). Il s’appuie sur .NET Core et prend en charge le développement multiplateforme sur Windows, macOS et les machines Linux. 2.x ajoute la prise en charge de première classe pour Java, mais n’encore directement prend pas en charge les langages expérimentaux. Version 2.x utilise un nouveau modèle d’extensibilité de liaison qui permet des extensions tierces pour la plateforme, le contrôle de version indépendant de liaisons, et une plus rationalisé l’environnement d’exécution.

> **Il existe un problème connu dans la version 1.x avec [prise en charge de la redirection de liaison](https://github.com/Azure/azure-functions-host/issues/992).** Le problème est spécifique au développement .NET. Projets avec des dépendances sur les bibliothèques qui sont une version différente des bibliothèques incluses dans le runtime sont affectées. L’équipe de fonctions a validés dans progresse concrètes sur le problème. L’équipe traiteront des redirections de liaison dans la version 2.x avant sa mise en disponibilité générale. L’instruction officiel de l’équipe avec des suggestions de correction et les solutions de contournement est disponible ici : [Résolution d’assembly dans Azure Functions](https://github.com/Azure/azure-functions-host/wiki/Assembly-Resolution-in-Azure-Functions).

Pour plus d’informations, consultez [comparer 1.x et 2.x](https://docs.microsoft.com/azure/azure-functions/functions-versions).

## <a name="programming-language-support"></a>Prise en charge du langage de programmation

Les langues suivantes sont prises en charge soit en général à la disposition générale, afficher un aperçu, ou la version expérimentale.

|Langue      |1.x         |2.x      |
|--------------|------------|---------|
|**C#**        |GA          |Preview  |
|**JavaScript**|GA          |Preview  |
|**F#**        |GA          |         |
|**Java**      |            |Preview  |
|**Python**    |Expérimental|         |
|**PHP**       |Expérimental|         |
|**TypeScript**|Expérimental|         |
|**Batch**     |Expérimental|         |
|**Bash**      |Expérimental|         |
|**PowerShell**|Expérimental|         |

Pour plus d’informations, consultez [langues prises en charge](https://docs.microsoft.com/azure/azure-functions/supported-languages).

## <a name="app-service-plans"></a>Plans app service

Les fonctions sont soutenues par une *plan app service*. Le plan définit les ressources utilisées par l’application de fonctions. Vous pouvez affecter des plans à une région, déterminer la taille et le nombre de machines virtuelles qui sera utilisé et choisir un niveau tarifaire. Pour une approche sans serveur true, les applications de fonction peut utiliser le **consommation** plan. Le plan de consommation mettra à l’échelle le serveur principal automatiquement en fonction de charge.

Pour plus d’informations, consultez [plans App service](https://docs.microsoft.com/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview).

## <a name="create-your-first-function"></a>Créer votre première fonction

Il existe trois façons courantes que vous pouvez créer des applications de fonction.

* Fonctions de script dans le portail.
* Créer les ressources nécessaires à l’aide de l’Interface de ligne de commande Azure (CLI).
* Créer des fonctions localement à l’aide de votre IDE favori et publiez-les sur Azure.

Pour plus d’informations sur la création d’une fonction de script dans le portail, consultez [créer votre première fonction dans le portail Azure](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function).

Pour générer à partir de l’interface CLI, consultez [créer votre première fonction à l’aide de l’interface CLI](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function-azure-cli).

Pour créer une fonction à partir de Visual Studio, consultez [créer votre première fonction à l’aide de Visual Studio](https://docs.microsoft.com/azure/azure-functions/functions-create-your-first-function-visual-studio).

## <a name="understand-triggers-and-bindings"></a>Comprendre les déclencheurs et liaisons

Les fonctions sont appelées par un *déclencheur* et peut avoir exactement un. En plus d’appeler la fonction, certains déclencheurs servent également de liaisons. Vous pouvez également définir plusieurs liaisons en plus du déclencheur. *Liaisons* fournissent un moyen déclaratif pour connecter les données à votre code. Ils peuvent être passés d’entrée (in) ou recevoir des données (sortie). Déclencheurs et liaisons rendre fonctions facile à utiliser. Liaisons de supprimer la surcharge liée à la création manuelle de base de données ou un fichier connexions du système. Toutes les informations nécessaires pour les liaisons est contenue dans un spécial *functions.json* de fichiers pour les scripts ou déclarés avec les attributs dans le code.

Certains déclencheurs courants sont les suivantes :

* Stockage d’objets BLOB : appelez votre fonction lorsqu’un fichier ou dossier est chargé ou modifié dans le stockage.
* HTTP : appelle votre fonction comme une API REST.
* File d’attente : appelez votre fonction lorsqu’il existent des éléments dans une file d’attente.
* Minuteur : appelle votre fonction sur une cadence régulière.

Voici quelques exemples de liaisons :

* COSMOS DB : se connecter facilement à la base de données à charger ou enregistrer des fichiers.
* Stockage de table : utilisation du stockage de clé/valeur à partir de votre application de fonction.
* Stockage de file d’attente : facilement extraire des éléments à partir d’une file d’attente, ou placer de nouveaux éléments sur la file d’attente.

L’exemple suivant *functions.json* fichier définit un déclencheur et une liaison :

```json
{
  "bindings": [
    {
      "name": "myBlob",
      "type": "blobTrigger",
      "direction": "in",
      "path": "images/{name}",
      "connection": "AzureWebJobsStorage"
    },
    {
      "name": "$return",
      "type": "queue",
      "direction": "out",
      "queueName": "images",
      "connection": "AzureWebJobsStorage"
    }
  ],
  "disabled": false
}
```

Dans cet exemple, la fonction est déclenchée par une modification apportée à un stockage d’objets blob dans le `images` conteneur. Les informations pour le fichier sont transmises, donc le déclencheur agit également comme une liaison. Une autre liaison existe pour placer des informations sur une file d’attente nommée `images`.

Voici le script c# pour la fonction :

```csharp
public static string Run(Stream myBlob, string name, TraceWriter log)
{
    log.Info($"C# Blob trigger function Processed blob\n Name:{name} \n Size: {myBlob.Length} Bytes");
    return name;
}
```

L’exemple est une fonction simple qui prend le nom du fichier qui a été modifiée ou chargée dans un stockage d’objets blob et le place dans une file d’attente pour un traitement ultérieur.

Pour obtenir une liste complète des déclencheurs et liaisons, consultez [Azure Functions concepts des déclencheurs et liaisons](https://docs.microsoft.com/azure/azure-functions/functions-triggers-bindings).

## <a name="proxies"></a>Serveurs proxy

Proxys fournissent la fonctionnalité de redirection pour votre application. Proxys d’exposent un point de terminaison et mappent ce point de terminaison à une autre ressource. Avec les serveurs proxy, vous pouvez :

* Rediriger une demande entrante vers un autre point de terminaison.
* Modifier la requête entrante avant qu’il n’est transmise.
* Modifier ou fournir une réponse.

Proxys sont utilisés pour des scénarios tels que :

* Simplifier, raccourcir ou de modifier l’URL.
* En fournissant un préfixe d’API cohérent pour plusieurs services principaux.
* Simulation d’une réponse à un point de terminaison en cours de développement.
* En fournissant une réponse statique à un point de terminaison connu.
* Conservation d’un point de terminaison d’API cohérent tandis que le serveur principal a été déplacé ou migrée.

Serveurs proxy sont stockés en tant que définitions de JSON. Voici un exemple :

```json
{
  "$schema": "http://json.schemastore.org/proxies",
  "proxies": {
    "Domain Redirect": {
      "matchCondition": {
        "route": "/{shortUrl}"
      },
      "backendUri": "http://%WEBSITE_HOSTNAME%/api/UrlRedirect/{shortUrl}"
    },
    "Root": {
      "matchCondition": {
        "route": "/"
      },
      "responseOverrides": {
        "response.statusCode": "301",
        "response.statusReason": "Moved Permanently",
        "response.headers.location": "https://docs.microsoft.com/"
      }
    }
  }
}
```

Le `Domain Redirect` proxy prend un itinéraire abrégé et le mappe à la ressource de fonction plus de temps. La transformation de l’aspect suivant :

`https://--shorturl--/123` -> `https://--longurl--.azurewebsites.net/api/UrlRedirect/123`

Le `Root` proxy prend quoi que ce soit envoyé à l’URL racine (`https://--shorturl--/`) et la redirige vers le site de documentation.

Voici un exemple d’utilisation de proxys dans la vidéo [Azure : Importez votre application dans le cloud avec Azure Functions sans serveur](https://channel9.msdn.com/events/Connect/2017/E102). En temps réel, une application ASP.NET Core s’exécutant sur le serveur SQL Server local est migrée vers le Cloud Azure. Proxys sont utilisés pour aider à refactoriser un projet d’API Web traditionnel pour utiliser des fonctions.

Pour plus d’informations sur les proxys, consultez [fonctionne avec Azure Functions Proxies](https://docs.microsoft.com/azure/azure-functions/functions-proxies).

>[!div class="step-by-step"]
>[Précédent](azure-serverless-platform.md)
>[Suivant](application-insights.md)
