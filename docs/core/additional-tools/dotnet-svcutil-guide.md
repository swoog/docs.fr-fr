---
title: Outil dotnet-svcutil Microsoft WCF
description: Vue d’ensemble de l’outil dotnet-svcutil Microsoft WCF, qui ajoute des fonctionnalités pour les projets .NET Core et ASP.NET Core, de manière similaire à l’outil svcutil WCF pour les projets .NET Framework.
author: mlacouture
ms.author: jralexander
ms.date: 06/04/2018
ms.openlocfilehash: c40dd9b437afe7381244b944228b6b2efe046eb2
ms.sourcegitcommit: d8bf4976eafe3289275be3811e7cb721bfff7e1e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34753420"
---
# <a name="microsoft-wcf-dotnet-svcutil-tool"></a><span data-ttu-id="69a06-103">Outil dotnet-svcutil Microsoft WCF</span><span class="sxs-lookup"><span data-stu-id="69a06-103">Microsoft WCF dotnet-svcutil tool</span></span>

<span data-ttu-id="69a06-104">L’outil **dotnet-svcutil** Windows Communication Foundation (WCF) est un outil CLI .NET Core qui récupère les métadonnées d’un service web sur un emplacement réseau ou dans un fichier WSDL, puis génère une classe WCF contenant des méthodes de proxy clientes pour accéder aux opérations du service web.</span><span class="sxs-lookup"><span data-stu-id="69a06-104">The Windows Communication Foundation (WCF) **dotnet-svcutil** tool is a .NET Core CLI tool that retrieves metadata from a web service on a network location or from a WSDL file, and generates a WCF class containing client proxy methods that access the web service operations.</span></span>

<span data-ttu-id="69a06-105">Comme l’outil [**Métadonnées de modèle de service - svcutil**](../../framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour les projets .NET Framework, **dotnet-svcutil** est un outil en ligne de commande pour générer une référence de service web compatible avec les projets .NET Core et .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="69a06-105">Similar to the [**Service Model Metadata - svcutil**](../../framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool for .NET Framework projects, the **dotnet-svcutil** is a command-line tool for generating a web service reference compatible with .NET Core and .NET Standard projects.</span></span>

<span data-ttu-id="69a06-106">L’outil **dotnet-svcutil** est une option alternative au fournisseur de services connectés Visual Studio [**WCF Web Service Reference**](wcf-web-service-reference-guide.md) inclus dans Visual Studio 2017 v15.5.</span><span class="sxs-lookup"><span data-stu-id="69a06-106">The **dotnet-svcutil** tool is an alternative option to the [**WCF Web Service Reference**](wcf-web-service-reference-guide.md) Visual Studio connected service provider that first shipped with Visual Studio 2017 v15.5.</span></span> <span data-ttu-id="69a06-107">L’outil **dotnet-svcutil**, en tant qu’outil CLI .NET Core, est disponible sur les plateformes Linux, macOS et Windows.</span><span class="sxs-lookup"><span data-stu-id="69a06-107">The **dotnet-svcutil** tool as a .NET Core CLI tool, is available cross-platform on Linux, macOS, and Windows.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69a06-108">Vous devez référencer des services uniquement à partir d’une source approuvée.</span><span class="sxs-lookup"><span data-stu-id="69a06-108">You should only reference services from a trusted source.</span></span> <span data-ttu-id="69a06-109">L’ajout de références à partir d’une source non fiable peut compromettre la sécurité.</span><span class="sxs-lookup"><span data-stu-id="69a06-109">Adding references from an untrusted source may compromise security.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="69a06-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="69a06-110">Prerequisites</span></span>

* <span data-ttu-id="69a06-111">[Kit SDK .NET Core](https://www.microsoft.com/net/download) 1.0.4 ou versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="69a06-111">[.NET Core SDK](https://www.microsoft.com/net/download) v1.0.4 or later versions</span></span>
* <span data-ttu-id="69a06-112">Votre éditeur de code favori</span><span class="sxs-lookup"><span data-stu-id="69a06-112">Your favorite code editor</span></span>

## <a name="getting-started"></a><span data-ttu-id="69a06-113">Bien démarrer</span><span class="sxs-lookup"><span data-stu-id="69a06-113">Getting started</span></span>

<span data-ttu-id="69a06-114">L’exemple suivant vous guide à travers les étapes requises pour ajouter une référence de service web à un projet de console .NET Core et pour appeler le service.</span><span class="sxs-lookup"><span data-stu-id="69a06-114">The following example walks you through the steps required to add a web service reference to a .NET Core console project and invoke the service.</span></span> <span data-ttu-id="69a06-115">Vous allez créer une application console .NET Core nommée _HelloSvcutil_ et ajouter une référence à un service web qui implémente le contrat suivant :</span><span class="sxs-lookup"><span data-stu-id="69a06-115">You will create a .NET Core console application named _HelloSvcutil_ and will add a reference to a web service that implements the following contract:</span></span>

```csharp
[ServiceContract]
public interface ISayHello
{
    [OperationContract]
    string Hello(string name);
}
```

<span data-ttu-id="69a06-116">Pour cet exemple, le service web est supposé être hébergé à l’adresse suivante : `http://contoso.com/SayHello.svc`</span><span class="sxs-lookup"><span data-stu-id="69a06-116">For this example, the web service will be assumed to be hosted at the following address: `http://contoso.com/SayHello.svc`</span></span>

<span data-ttu-id="69a06-117">À partir d’une fenêtre de commande Windows, macOS ou Linux, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-117">From a Windows, macOS, or Linux command window perform the following steps:</span></span>

1. <span data-ttu-id="69a06-118">Créez un répertoire nommé _HelloSvcutil_ pour votre projet et faites-en votre répertoire actuel, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="69a06-118">Create a directory named _HelloSvcutil_ for your project and make it your current directory, as in the following example:</span></span>

```console
mkdir HelloSvcutil
cd HelloSvcutil
```

2. <span data-ttu-id="69a06-119">Créez un nouveau projet console C# dans ce répertoire à l’aide de la commande [`dotnet new`](../tools/dotnet-new.md), comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-119">Create a new C# console project in that directory using the [`dotnet new`](../tools/dotnet-new.md) command as follows:</span></span>

```console
dotnet new console
```

3. <span data-ttu-id="69a06-120">Ouvrez le fichier projet `HelloSvcutil.csproj` dans l’éditeur de votre projet, modifiez l’élément `Project` et ajoutez le [`dotnet-svcutil` package NuGet](https://nuget.org/packages/dotnet-svcutil) comme référence d’outil CLI à l’aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="69a06-120">Open the `HelloSvcutil.csproj` project file in your editor, edit the `Project` element, and add the [`dotnet-svcutil` NuGet package](https://nuget.org/packages/dotnet-svcutil) as a CLI tool reference, using the following code:</span></span>

```xml
<ItemGroup>
  <DotNetCliToolReference Include="dotnet-svcutil" Version="1.0.0" />
</ItemGroup>
```

4. <span data-ttu-id="69a06-121">Restaurez le package _-dotnet svcutil_ à l’aide de la commande [`dotnet restore`](../tools/dotnet-restore.md), comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-121">Restore the _dotnet-svcutil_ package using the [`dotnet restore`](../tools/dotnet-restore.md) command as follows:</span></span>

```console
dotnet restore
```

5. <span data-ttu-id="69a06-122">Exécutez _dotnet_ avec la commande _svcutil_ pour générer le fichier de référence de service web, comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-122">Run _dotnet_ with the _svcutil_ command to generate the web service reference file as follows:</span></span>

```console
dotnet svcutil http://contoso.com/SayHello.svc
```
<span data-ttu-id="69a06-123">Le fichier généré est enregistré en tant que _HelloSvcutil/ServiceReference1/Reference.cs_.</span><span class="sxs-lookup"><span data-stu-id="69a06-123">The generated file is saved as _HelloSvcutil/ServiceReference1/Reference.cs_.</span></span> <span data-ttu-id="69a06-124">L’outil _dotnet_svcutil_ ajoute également au projet les packages WCF appropriés requis par le code proxy en tant que références de package.</span><span class="sxs-lookup"><span data-stu-id="69a06-124">The _dotnet_svcutil_ tool also adds to the project the appropriate WCF packages required by the proxy code as package references.</span></span>

6. <span data-ttu-id="69a06-125">Restaurez les packages WCF à l’aide de la commande [`dotnet restore`](../tools/dotnet-restore.md), comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-125">Restore the WCF packages using the [`dotnet restore`](../tools/dotnet-restore.md) command as follows:</span></span>

```console
dotnet restore
```

7. <span data-ttu-id="69a06-126">Ouvrez le fichier `Program.cs` dans votre éditeur, modifiez la méthode `Main()`, puis remplacez le code généré automatiquement par le code suivant pour appeler le service web :</span><span class="sxs-lookup"><span data-stu-id="69a06-126">Open the `Program.cs` file in your editor, edit the `Main()` method, and replace the auto-generated code with the following code to invoke the web service:</span></span>

```csharp
static void Main(string[] args)
{
    var client = new SayHelloClient();
    Console.WriteLine(client.HelloAsync("dotnet-svcutil").Result);
}
```

8. <span data-ttu-id="69a06-127">Exécutez l’application en utilisant la commande [`dotnet run`](../tools/dotnet-run.md), comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-127">Run the application using the [`dotnet run`](../tools/dotnet-run.md) command as follows:</span></span>

```console
dotnet run
```
<span data-ttu-id="69a06-128">La sortie suivante devrait s'afficher : « Hello dotnet-svcutil! »</span><span class="sxs-lookup"><span data-stu-id="69a06-128">You should see the following output: "Hello dotnet-svcutil!"</span></span>

<span data-ttu-id="69a06-129">Pour obtenir une description détaillée des paramètres de l’outil `dotnet-svcutil`, appelez l’outil en passant le paramètre d’aide comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a06-129">For a detailed description of the `dotnet-svcutil` tool parameters, invoke the tool passing the help parameter as follows:</span></span>

```console
dotnet svcutil --help
```

## <a name="next-steps"></a><span data-ttu-id="69a06-130">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="69a06-130">Next steps</span></span>

### <a name="feedback--questions"></a><span data-ttu-id="69a06-131">Commentaires et questions</span><span class="sxs-lookup"><span data-stu-id="69a06-131">Feedback & questions</span></span>

<span data-ttu-id="69a06-132">Si vous avez des questions ou des commentaires, [ouvrez un problème sur GitHub](https://github.com/dotnet/wcf/issues/new).</span><span class="sxs-lookup"><span data-stu-id="69a06-132">If you have any questions or feedback, [open an issue on GitHub](https://github.com/dotnet/wcf/issues/new).</span></span> <span data-ttu-id="69a06-133">Vous pouvez également consulter les questions ou problèmes existants dans le [dépôt WCF sur GitHub](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling).</span><span class="sxs-lookup"><span data-stu-id="69a06-133">You can also review any existing questions or issues [at the WCF repo on GitHub](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling).</span></span>

### <a name="release-notes"></a><span data-ttu-id="69a06-134">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="69a06-134">Release notes</span></span>

* <span data-ttu-id="69a06-135">Pour obtenir des informations à jour sur les versions, notamment les problèmes connus, consultez les [Notes de publication](https://github.com/dotnet/wcf/blob/master/release-notes/dotnet-svcutil-notes.md).</span><span class="sxs-lookup"><span data-stu-id="69a06-135">Refer to the [Release notes](https://github.com/dotnet/wcf/blob/master/release-notes/dotnet-svcutil-notes.md) for updated release information, including known issues.</span></span>

### <a name="information"></a><span data-ttu-id="69a06-136">Information</span><span class="sxs-lookup"><span data-stu-id="69a06-136">Information</span></span>

* [<span data-ttu-id="69a06-137">Package NuGet dotnet-svcutil</span><span class="sxs-lookup"><span data-stu-id="69a06-137">dotnet-svcutil NuGet Package</span></span>](https://nuget.org/packages/dotnet-svcutil)
