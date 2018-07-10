---
title: Microservices hébergés dans Docker - C#
description: Apprenez à créer des services principaux ASP.NET qui s’exécutent dans des conteneurs Docker
ms.date: 06/08/2017
ms.assetid: 87e93838-a363-4813-b859-7356023d98ed
ms.openlocfilehash: 1f4b38243beb1210b1374bd701fac66b2fa72cc5
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106348"
---
# <a name="microservices-hosted-in-docker"></a>Microservices hébergés dans Docker

Ce didacticiel détaille les tâches nécessaires pour générer et déployer un microservice ASP.NET Core dans un conteneur Docker. Au cours de ce didacticiel, vous apprendrez à :

* Générer une application ASP.NET Core.
* Créer un environnement de développement Docker.
* Créer une image Docker basée sur une image existante.
* Déployer votre service dans un conteneur Docker.

Au passage, vous verrez également certaines fonctionnalités du langage C# :

* Conversion des objets C# en charges utiles JSON.
* Création d’objets de transfert de données immuables
* Traitement des requêtes HTTP entrantes et création de la réponse HTTP
* Utilisation des types valeur Nullable

Vous pouvez [afficher ou télécharger l’exemple d’application](https://github.com/dotnet/samples/tree/master/csharp/getting-started/WeatherMicroservice) de cette rubrique. Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).

## <a name="why-docker"></a>Pourquoi Docker ?

Docker facilite la création d’images de machine standard pour héberger vos services dans un centre de données ou dans le cloud public. Docker vous permet de configurer l’image et de la répliquer en fonction des besoins pour mettre à l’échelle l’installation de votre application.

Tout le code de ce didacticiel fonctionne dans n’importe quel environnement .NET Core.
Les tâches supplémentaires pour une installation Docker fonctionneront pour une application ASP.NET Core. 

## <a name="prerequisites"></a>Prérequis

Vous devez configurer votre ordinateur pour exécuter .NET Core. Vous trouverez les instructions d’installation sur la page de [.NET Core](https://www.microsoft.com/net/core).
Vous pouvez exécuter cette application sur Windows, Linux, Mac OS ou dans un conteneur Docker.
Vous devez installer l’éditeur de code de votre choix. Les descriptions ci-dessous utilisent [Visual Studio Code](https://code.visualstudio.com/), un éditeur open source et multiplateforme. Cependant, vous pouvez utiliser les outils avec lesquels vous êtes le plus à l’aise.

Vous devez également installer le moteur Docker. Consultez la [page d’installation de Docker](http://www.docker.com/products/docker) pour obtenir des instructions pour votre plateforme.
Docker peut être installé dans de nombreuses distributions Linux, Mac OS ou Windows. La page mentionnée ci-dessus contient des sections pour chacune des installations disponibles.

## <a name="create-the-application"></a>Création de l’application

Maintenant que vous avez installé tous les outils, créez une application ASP.NET Core dans un répertoire appelé « WeatherMicroservice » en exécutant la commande suivante dans votre interpréteur de commandes préféré :

```console
dotnet new web -o WeatherMicroservice
```

La commande `dotnet` exécute les outils nécessaires pour le développement .NET. Chaque verbe exécute une commande différente.

La commande `dotnet new` sert à créer des projets .NET Core.

L’option `-o WeatherMicroservice` après la commande `dotnet new` est utilisée pour indiquer l’emplacement où créer l’application ASP.NET Core.

Pour ce microservice, nous souhaitons que l’application web soit la plus simple et la plus légère possible. Nous avons donc utilisé le modèle « ASP.NET Core vide », en spécifiant son nom court, `web`.

Le modèle crée quatre fichiers pour vous :

* Un fichier Startup.cs. Cela contient la base de l’application.
* Un fichier Program.cs. Cela contient le point d’entrée de l’application.
* Un fichier WeatherMicroservice.csproj. Il s’agit du fichier de génération de l’application.
* Un fichier Properties/launchSettings.json. Il contient les paramètres de débogage utilisés par l’EDI.

Vous pouvez maintenant exécuter l’application générée par le modèle :

```console
dotnet run
```

Cette commande restaure tout d’abord les dépendances requises pour générer l’application, puis elle génère l’application.

La configuration par défaut écoute le port `http://localhost:5000`. Vous pouvez ouvrir un navigateur et accéder à cette page pour voir un « Hello World! » « Operation Not Found! ».

Quand vous avez terminé, vous pouvez arrêter l’application en appuyant sur <kbd>Ctrl</kbd>+<kbd>C</kbd>.

### <a name="anatomy-of-an-aspnet-core-application"></a>Anatomie d’une application ASP.NET Core

Maintenant que vous avez créé l’application, nous allons voir comment cette fonctionnalité est implémentée. Deux des fichiers générés sont particulièrement intéressants à ce stade : WeatherMicroservice.csproj et Startup.cs. 

Le fichier .csproj contient des informations sur le projet.
Les deux nœuds les plus intéressants sont `<TargetFramework>` et `<PackageReference>`.

Le nœud `<TargetFramework>` spécifie la version de .NET qui exécutera cette application.

Chaque nœud `<PackageReference>` sert à spécifier un package qui est nécessaire pour cette application.

L’application est implémentée dans Startup.cs. Ce fichier contient la classe de démarrage.

Les deux méthodes sont appelées par l’infrastructure ASP.NET Core pour configurer et exécuter l’application. La méthode `ConfigureServices` décrit les services qui sont nécessaires pour cette application. Vous créez un microservice épuré, vous n’avez donc pas besoin de configurer de dépendances. La méthode `Configure` configure les gestionnaires pour les requêtes HTTP entrantes. Le modèle génère un gestionnaire simple qui répond à une demande dont le texte est « Hello World! ».

## <a name="build-a-microservice"></a>Créer un microservice

Le service que vous vous apprêtez à générer fournira des rapports météorologiques depuis n’importe où dans le monde. Dans une application de production, vous appelleriez un service pour récupérer des données météorologiques. Pour notre exemple, nous allons générer des prévisions météorologiques aléatoires. 

Il existe un certain nombre de tâches que vous devez effectuer pour implémenter notre service météo aléatoire :

* Analyser la requête entrante pour lire la latitude et la longitude.
* Générer des données de prévision aléatoires.
* Convertir ces données de prévision aléatoires d’objets C# en paquets JSON.
* Définir l’en-tête de réponse pour indiquer que votre service renvoie JSON.
* Écrivez la réponse.

Les sections suivantes décrivent chacune de ces étapes.

### <a name="parsing-the-query-string"></a>Analyse de la chaîne de requête

Vous commencerez par analyser la chaîne de requête. Le service acceptera les arguments 'lat' et 'longs' sur la chaîne de requête dans ce formulaire :

```
http://localhost:5000/?lat=-35.55&long=-12.35
```

Toutes les modifications que vous devez apporter se trouvent dans l’expression lambda définie comme argument de `app.Run` dans votre classe de démarrage.

L’argument de l’expression lambda est le `HttpContext` pour la demande. Une de ses propriétés est l’objet `Request`. L’objet `Request` a une propriété `Query` qui contient un dictionnaire de toutes les valeurs dans la chaîne de requête pour la demande. La première addition consiste à rechercher les valeurs de latitude et longitude :

[!code-csharp[ReadQueryString](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#ReadQueryString "read variables from the query string")]

Les valeurs du dictionnaire `Query` sont de type `StringValue`. Ce type peut contenir une collection de chaînes. Pour votre service météo, chaque valeur est une chaîne unique. C’est pourquoi il y a un appel à `FirstOrDefault()` dans le code ci-dessus. 

Ensuite, vous devez convertir les chaînes en valeurs de type double. La méthode que vous allez utiliser pour convertir la chaîne en double est `double.TryParse()` :

```csharp
bool TryParse(string s, out double result);
```

Cette méthode s’appuie sur les paramètres de sortie de C# pour indiquer si la chaîne d’entrée peut être convertie en double. Si la chaîne constitue une représentation valide pour un double, la méthode retourne true et l’argument `result` contient la valeur. Si la chaîne ne représente pas une valeur double valide, la méthode retourne false.

Vous pouvez adapter cette API à l’aide d’une *méthode d’extension* qui renvoie un *double Nullable*. Un *type de valeur Nullable* est un type qui représente un type de valeur et peut également contenir un une valeur manquante ou Null. Un type Nullable est représenté en ajoutant le caractère `?` à la déclaration de type. 

Les méthodes d’extension sont des méthodes qui sont définies comme des méthodes statiques mais qui, en ajoutant le modificateur `this` sur le premier paramètre, peuvent être appelées comme si elles étaient des membres de cette classe. Les méthodes d’extension peuvent être définies uniquement dans les classes statiques. Voici la définition de la classe contenant la méthode d’extension pour l’analyse :

[!code-csharp[TryParseExtension](../../../samples/csharp/getting-started/WeatherMicroservice/Extensions.cs#TryParseExtension "try parse to a nullable")]

Avant d’appeler la méthode d’extension, changez la culture actuelle pour qu’elle soit invariante :

[!code-csharp[SetCulture](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#SetCulture "set current culture to invariant")]

Cela permet de s’assurer que votre application analyse les nombres de la même façon sur tous les serveurs, quel que soit sa culture par défaut.

Vous pouvez maintenant utiliser la méthode d’extension pour convertir les arguments de chaîne de requête en type double :

[!code-csharp[UseTryParse](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#UseTryParse "Use the try parse extension method")]

Pour tester facilement le code d’analyse, mettez à jour la réponse pour inclure les valeurs des arguments :

[!code-csharp[WriteResponse](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#WriteResponse "Write the output response")]

À ce stade, vous pouvez exécuter l’application web et voir si votre code d’analyse fonctionne. Ajoutez des valeurs à la requête web dans un navigateur, et vous devriez voir les résultats de la mise à jour.

### <a name="build-a-random-weather-forecast"></a>Générer des prévisions météorologiques aléatoires

La tâche suivante consiste à créer des prévisions météorologiques aléatoires. Commençons avec un conteneur de données qui contient les valeurs que vous souhaiteriez pour les prévisions météorologiques :

```csharp
public class WeatherReport
{
    private static readonly string[] PossibleConditions =
    {
        "Sunny",
        "Mostly Sunny",
        "Partly Sunny",
        "Partly Cloudy",
        "Mostly Cloudy",
        "Rain"
    };

    public int HighTemperatureFahrenheit { get; }
    public int LowTemperatureFahrenheit { get; }
    public int AverageWindSpeedMph { get; }
    public string Condition { get; }
}
```

Ensuite, générez un constructeur qui définit de façon aléatoire ces valeurs. Ce constructeur utilise les valeurs de latitude et de longitude pour amorcer le générateur de nombres `Random`. Cela signifie que la prévision pour un même emplacement est la même. Si vous changez les arguments de latitude et de longitude, vous obtiendrez une prévision différente (car vous démarrez avec une valeur initiale différente).

[!code-csharp[WeatherReportConstructor](../../../samples/csharp/getting-started/WeatherMicroservice/WeatherReport.cs#WeatherReportConstructor "Weather Report Constructor")]

Vous pouvez maintenant générer des prévisions sur 5 jours dans votre méthode de réponse :

```csharp
if (latitude.HasValue && longitude.HasValue)
{
    var forecast = new List<WeatherReport>();
    for (var days = 1; days <= 5; days++)
    {
        forecast.Add(new WeatherReport(latitude.Value, longitude.Value, days));
    }
}
```

### <a name="build-the-json-response"></a>Générer la réponse JSON

La tâche de code finale sur le serveur consiste à convertir la liste `WeatherReport` en document JSON, et à renvoyer cela au client. Commençons par créer le document JSON. Vous allez ajouter le sérialiseur JSON Newtonsoft à la liste des dépendances. Vous pouvez pour cela utiliser la commande `dotnet` suivante :

```console
dotnet add package Newtonsoft.Json
```

Ensuite, vous pouvez utiliser la classe `JsonConvert` pour écrire l’objet dans une chaîne :

[!code-csharp[ConvertToJson](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#ConvertToJSON "Convert objects to JSON")]

Le code ci-dessus convertit l’objet de prévision (une liste d’objets `WeatherForecast`) en document JSON. Une fois que vous avez construit le document de réponse, vous définissez le type de contenu `application/json` et écrivez la chaîne.

Maintenant, l’application s’exécute et renvoie des prévisions aléatoires.

## <a name="build-a-docker-image"></a>Créer une image Docker

La dernière tâche consiste à exécuter l’application dans Docker. Nous allons créer un conteneur Docker qui exécute une image Docker qui représente l’application.

Une ***image Docker*** est un fichier qui définit l’environnement d’exécution de l’application.

Un ***conteneur Docker*** représente une instance en cours d’exécution d’une image Docker.

Par analogie, vous pouvez considérer *l’Image Docker* comme une *classe* et le *conteneur Docker* comme un objet ou une instance de cette classe.  

Le Dockerfile suivant correspond à nos besoins :

```
FROM microsoft/dotnet:2.1-sdk AS build
WORKDIR /app

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY . ./
RUN dotnet publish -c Release -o out

# Build runtime image
FROM microsoft/dotnet:2.1-aspnetcore-runtime
WORKDIR /app
COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "WeatherMicroservice.dll"]
```

Attardons-nous sur son contenu.

La première ligne spécifie l’image source utilisée pour générer l’application :

```
FROM microsoft/dotnet:2.1-sdk AS build
```

Docker vous permet de configurer une image d’ordinateur basée sur un modèle source. Cela signifie que vous n’êtes pas obligé de fournir tous les paramètres de la machine lorsque vous démarrez. Il vous suffit de fournir les modifications éventuelles. Les modifications apportées ici serviront à inclure notre application.

Dans cet exemple, nous allons utiliser la version `2.1-sdk` de l’image `dotnet`. Il s’agit du moyen le plus simple de créer un environnement Docker. Cette image inclut le runtime .NET Core et le kit SDK .NET Core.
Cela simplifie la prise en main et la génération initiale, mais crée une image plus grande. Nous allons donc utiliser cette image pour générer l’application et une image différente pour l’exécuter.

Les lignes suivantes configurent et génèrent votre application :

```
WORKDIR /app

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY . ./
RUN dotnet publish -c Release -o out
```

Cela copie le fichier projet du répertoire actif sur la machine virtuelle Docker et restaure tous les packages. L’utilisation de l’interface de ligne de commande dotnet signifie que l’image Docker doit inclure le kit de développement logiciel .NET Core. Après cela, le reste de votre application est copié et la commande `dotnet
publish` génère et crée un package de votre application.

Pour finir, nous allons créer une deuxième image Docker qui exécute l’application :

```
# Build runtime image
FROM microsoft/dotnet:2.1-aspnetcore-runtime
WORKDIR /app
COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "WeatherMicroservice.dll"]
```

Cette image utilise la version `2.1-aspnetcore-runtime` de l’image `dotnet`, qui contient tous les éléments nécessaires pour exécuter des applications ASP.NET Core, mais n’inclut pas le kit SDK .NET Core. Cela signifie que nous ne pouvons pas utiliser cette image pour créer des applications .NET Core, mais par contre cela limite la taille de l’image finale.

Nous allons copier l’application générée de la première image vers la deuxième.

La commande `ENTRYPOINT` indique à Docker quelle commande démarre le service.

## <a name="building-and-running-the-image-in-a-container"></a>Génération et exécution de l’image dans un conteneur

Nous allons créer une image et exécuter le service à l’intérieur d’un conteneur Docker. Nous ne voulons pas que tous les fichiers de votre répertoire local soient copiés dans l’image. Au lieu de cela, nous allons développer l’application dans le conteneur. Vous allez créer un fichier `.dockerignore` pour spécifier les répertoires qui ne sont pas copiés dans l’image. Nous ne souhaitons copier aucune des ressources build. Spécifiez les répertoires build et publish dans le fichier `.dockerignore` :

```
bin/*
obj/*
out/*
```

Vous générez l’image avec la commande `docker build`. Exécutez la commande suivante à partir du répertoire qui contient votre code.

```console
docker build -t weather-microservice .
```

Cette commande génère l’image de conteneur sur la base de toutes les informations de votre fichier Docker. L’argument `-t` fournit une balise ou un nom pour cette image de conteneur. Dans la ligne de commande ci-dessus, la balise utilisée pour le conteneur Docker est `weather-microservice`. Lorsque cette commande est terminée, vous disposez d’un conteneur prêt à exécuter votre nouveau service. 

Exécutez la commande suivante pour démarrer le conteneur et lancer votre service :

```console
docker run -d -p 80:80 --name hello-docker weather-microservice
```

L’option `-d` consiste à exécuter le conteneur de façon détachée du terminal actuel. Cela signifie que vous ne verrez pas le résultat de la commande dans votre terminal. L’option `-p` indique le mappage de port entre le service et la machine hôte. Ici, elle indique que toute requête entrante sur le port 80 doit être transférée vers le port 80 sur le conteneur. Le fait de spécifier 80 permet d’établir une correspondance avec le port sur lequel votre service écoute, qui est le port par défaut pour les applications de production. L’argument `--name` nomme votre conteneur en cours d’exécution. Il s’agit d’un nom convivial que vous pouvez utiliser pour travailler avec ce conteneur.

Vous pouvez voir si l’image est en cours d’exécution avec la commande :

```console
docker ps
```

Si votre conteneur est en cours d’exécution, vous verrez une ligne qui répertorie les processus en cours d’exécution. (Il peut s’agir du seul processus.)

Vous pouvez tester votre service en ouvrant un navigateur et en accédant à localhost et en spécifiant une latitude et une longitude :

```
http://localhost/?lat=35.5&long=40.75
```

## <a name="attaching-to-a-running-container"></a>Attachement à un conteneur en cours d’exécution

Quand vous avez exécuté votre service dans une fenêtre de commande, vous avez pu voir les informations de diagnostic imprimées pour chaque requête. Ces informations ne s’affichent pas lorsque votre conteneur s’exécute en mode détaché. La commande attach de Docker vous permet de vous attacher à un conteneur en cours d’exécution afin de voir les informations du journal.  Exécutez cette commande à partir d’une fenêtre de commande :

```console
docker attach --sig-proxy=false hello-docker
```

L’argument `--sig-proxy=false` signifie que les commandes <kbd>Ctrl</kbd>+<kbd>C</kbd> ne sont pas envoyées au processus de conteneur, mais arrêtent plutôt la commande `docker attach`. Le dernier argument est le nom donné au conteneur dans la commande `docker run`. 

> [!NOTE]
> Vous pouvez également utiliser l’ID de conteneur assigné au Docker pour faire référence à un conteneur. Si vous n’avez pas spécifié de nom pour votre conteneur dans `docker run`, vous devez utiliser l’ID de conteneur.

Ouvrez un navigateur et accédez à votre service. Vous verrez les messages de diagnostic dans la fenêtre de commande à partir du conteneur en cours d’exécution attaché.

Appuyez sur <kbd>Ctrl</kbd>+<kbd>C</kbd> pour arrêter le processus d’attachement.

Lorsque vous avez terminé de manipuler votre conteneur, vous pouvez l’arrêter :

```console
docker stop hello-docker
```

Le conteneur et l’image sont toujours disponibles pour vous permettre de redémarrer.  Si vous souhaitez supprimer le conteneur de votre machine, utilisez cette commande :

```console
docker rm hello-docker
```

Si vous souhaitez supprimer des images inutilisées dans votre machine, utilisez cette commande :

```console
docker rmi weather-microservice
```

## <a name="conclusion"></a>Conclusion 

Dans ce didacticiel, vous avez créé un microservice ASP.NET Core, auquel vous avez ensuite ajouté quelques fonctionnalités simples.

Vous avez créé une image conteneur Docker pour ce service et exécuté ce conteneur sur votre machine. Vous avez attaché une fenêtre de terminal au service et vu les messages de diagnostic à partir de votre service.

En chemin, vous avez vu plusieurs fonctionnalités du langage C# en action.
