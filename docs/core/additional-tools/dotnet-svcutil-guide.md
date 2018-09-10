---
title: Outil dotnet-svcutil Microsoft WCF
description: Vue d’ensemble de l’outil dotnet-svcutil Microsoft WCF, qui ajoute des fonctionnalités pour les projets .NET Core et ASP.NET Core, de manière similaire à l’outil svcutil WCF pour les projets .NET Framework.
author: mlacouture
ms.author: jralexander
ms.date: 08/20/2018
ms.openlocfilehash: bb4d8e5f3997318b720535b0f1e07fc33d13338a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511884"
---
# <a name="microsoft-wcf-dotnet-svcutil-tool"></a>Outil dotnet-svcutil Microsoft WCF

L’outil **dotnet-svcutil** Windows Communication Foundation (WCF) est un outil CLI .NET Core qui récupère les métadonnées d’un service web sur un emplacement réseau ou dans un fichier WSDL, puis génère une classe WCF contenant des méthodes de proxy clientes pour accéder aux opérations du service web.

Comme l’outil [**Métadonnées de modèle de service - svcutil**](../../framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour les projets .NET Framework, **dotnet-svcutil** est un outil en ligne de commande pour générer une référence de service web compatible avec les projets .NET Core et .NET Standard.

L’outil **dotnet-svcutil** est une option alternative au fournisseur de services connectés Visual Studio [**WCF Web Service Reference**](wcf-web-service-reference-guide.md) inclus dans Visual Studio 2017 v15.5. L’outil **dotnet-svcutil**, en tant qu’outil CLI .NET Core, est disponible sur les plateformes Linux, macOS et Windows.

> [!IMPORTANT]
> Vous devez référencer des services uniquement à partir d’une source approuvée. L’ajout de références à partir d’une source non fiable peut compromettre la sécurité.

## <a name="prerequisites"></a>Prérequis

* [Kit SDK .NET Core](https://www.microsoft.com/net/download) 1.0.4 ou versions ultérieures
* Votre éditeur de code favori

## <a name="getting-started"></a>Bien démarrer

L’exemple suivant vous guide à travers les étapes requises pour ajouter une référence de service web à un projet de console .NET Core et pour appeler le service. Vous allez créer une application console .NET Core nommée _HelloSvcutil_ et ajouter une référence à un service web qui implémente le contrat suivant :

```csharp
[ServiceContract]
public interface ISayHello
{
    [OperationContract]
    string Hello(string name);
}
```

Pour cet exemple, le service web est supposé être hébergé à l’adresse suivante : `http://contoso.com/SayHello.svc`

À partir d’une fenêtre de commande Windows, macOS ou Linux, procédez comme suit :

1. Créez un répertoire nommé _HelloSvcutil_ pour votre projet et faites-en votre répertoire actuel, comme dans l’exemple suivant :

```console
mkdir HelloSvcutil
cd HelloSvcutil
```

2. Créez un nouveau projet console C# dans ce répertoire à l’aide de la commande [`dotnet new`](../tools/dotnet-new.md), comme suit :

```console
dotnet new console
```

3. Ouvrez le fichier projet `HelloSvcutil.csproj` dans l’éditeur de votre projet, modifiez l’élément `Project` et ajoutez le [`dotnet-svcutil` package NuGet](https://nuget.org/packages/dotnet-svcutil) comme référence d’outil CLI à l’aide du code suivant :

```xml
<ItemGroup>
  <DotNetCliToolReference Include="dotnet-svcutil" Version="1.0.*" />
</ItemGroup>
```

4. Restaurez le package _-dotnet svcutil_ à l’aide de la commande [`dotnet restore`](../tools/dotnet-restore.md), comme suit :

```console
dotnet restore
```

5. Exécutez _dotnet_ avec la commande _svcutil_ pour générer le fichier de référence de service web, comme suit :

```console
dotnet svcutil http://contoso.com/SayHello.svc
```
Le fichier généré est enregistré en tant que _HelloSvcutil/ServiceReference1/Reference.cs_. L’outil _dotnet_svcutil_ ajoute également au projet les packages WCF appropriés requis par le code proxy en tant que références de package.

6. Restaurez les packages WCF à l’aide de la commande [`dotnet restore`](../tools/dotnet-restore.md), comme suit :

```console
dotnet restore
```

7. Ouvrez le fichier `Program.cs` dans votre éditeur, modifiez la méthode `Main()`, puis remplacez le code généré automatiquement par le code suivant pour appeler le service web :

```csharp
static void Main(string[] args)
{
    var client = new SayHelloClient();
    Console.WriteLine(client.HelloAsync("dotnet-svcutil").Result);
}
```

8. Exécutez l’application en utilisant la commande [`dotnet run`](../tools/dotnet-run.md), comme suit :

```console
dotnet run
```
La sortie suivante devrait s'afficher : « Hello dotnet-svcutil! »

Pour obtenir une description détaillée des paramètres de l’outil `dotnet-svcutil`, appelez l’outil en passant le paramètre d’aide comme suit :

```console
dotnet svcutil --help
```

## <a name="next-steps"></a>Étapes suivantes

### <a name="feedback--questions"></a>Commentaires et questions

Si vous avez des questions ou des commentaires, [ouvrez un problème sur GitHub](https://github.com/dotnet/wcf/issues/new). Vous pouvez également consulter les questions ou problèmes existants dans le [dépôt WCF sur GitHub](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling).

### <a name="release-notes"></a>Notes de publication

* Pour obtenir des informations à jour sur les versions, notamment les problèmes connus, consultez les [Notes de publication](https://github.com/dotnet/wcf/blob/master/release-notes/dotnet-svcutil-notes.md).

### <a name="information"></a>Information

* [Package NuGet dotnet-svcutil](https://nuget.org/packages/dotnet-svcutil)
