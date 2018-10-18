---
title: Azure Functions - applications sans serveur
description: Fonctions Azure offrent des fonctionnalités sans serveur dans plusieurs langues (C# JavaScript, Java) et plateformes pour fournir pilotée par événements instantanée mettre à l’échelle de code.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: f08ba20b485197acd3bb5cdfe5699cd6be991d7c
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "49369952"
---
# <a name="azure-functions"></a><span data-ttu-id="ddde7-103">Azure Functions</span><span class="sxs-lookup"><span data-stu-id="ddde7-103">Azure Functions</span></span>

<span data-ttu-id="ddde7-104">Azure functions fournit une expérience de calcul sans serveur.</span><span class="sxs-lookup"><span data-stu-id="ddde7-104">Azure functions provide a serverless compute experience.</span></span> <span data-ttu-id="ddde7-105">Une fonction est appelée par un *déclencheur* (par exemple, l’accès à un point de terminaison HTTP ou un minuteur) et exécute un bloc de code ni la logique métier.</span><span class="sxs-lookup"><span data-stu-id="ddde7-105">A function is invoked by a *trigger* (such as access to an HTTP endpoint or a timer) and executes a block of code or business logic.</span></span> <span data-ttu-id="ddde7-106">Fonctions également la prise en charge spécialisée *liaisons* qui se connectent aux ressources telles que les files d’attente et de stockage.</span><span class="sxs-lookup"><span data-stu-id="ddde7-106">Functions also support specialized *bindings* that connect to resources like storage and queues.</span></span>

![Logo de fonctions Azure](./media/azure-functions-logo.png)

<span data-ttu-id="ddde7-108">Il existe deux versions de l’infrastructure Azure Functions.</span><span class="sxs-lookup"><span data-stu-id="ddde7-108">There are two versions of the Azure Functions framework.</span></span> <span data-ttu-id="ddde7-109">L’ancienne version prend en charge le .NET Framework complet et le nouveau runtime prend en charge les applications .NET Core multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="ddde7-109">The legacy version supports the full .NET Framework and the new runtime supports cross-platform .NET Core applications.</span></span> <span data-ttu-id="ddde7-110">Des langues supplémentaires en plus de c#, tels que JavaScript, F # et Java sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ddde7-110">Additional languages besides C# such as JavaScript, F#, and Java are supported.</span></span> <span data-ttu-id="ddde7-111">Fonctions créées dans le portail fournissent une syntaxe de script complexe.</span><span class="sxs-lookup"><span data-stu-id="ddde7-111">Functions created in the portal provide a rich scripting syntax.</span></span> <span data-ttu-id="ddde7-112">Fonctions créées en tant que projets autonomes peuvent être déployées avec des fonctionnalités et de support de plate-forme complet.</span><span class="sxs-lookup"><span data-stu-id="ddde7-112">Functions created as standalone projects can be deployed with full platform support and capabilities.</span></span>

<span data-ttu-id="ddde7-113">Pour plus d’informations, consultez [documentation Azure Functions](https://docs.microsoft.com/azure/azure-functions).</span><span class="sxs-lookup"><span data-stu-id="ddde7-113">For more information, see [Azure Functions documentation](https://docs.microsoft.com/azure/azure-functions).</span></span>

## <a name="functions-v1-vs-v2"></a><span data-ttu-id="ddde7-114">Fonctions des v1 et v2</span><span class="sxs-lookup"><span data-stu-id="ddde7-114">Functions v1 vs. v2</span></span>

<span data-ttu-id="ddde7-115">Il existe deux versions du runtime Azure Functions : 1.x et 2.x.</span><span class="sxs-lookup"><span data-stu-id="ddde7-115">There are two versions of the Azure Functions runtime: 1.x and 2.x.</span></span> <span data-ttu-id="ddde7-116">Version 1.x est généralement disponible (GA).</span><span class="sxs-lookup"><span data-stu-id="ddde7-116">Version 1.x is generally available (GA).</span></span> <span data-ttu-id="ddde7-117">Il prend en charge le développement de .NET à partir du portail ou les machines Windows et utilise le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ddde7-117">It supports .NET development from the portal or Windows machines and uses the .NET Framework.</span></span> <span data-ttu-id="ddde7-118">1.x prend en charge c#, JavaScript et F #, avec prise en charge expérimentale pour Python, PHP, TypeScript, Batch, Bash et PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddde7-118">1.x supports C#, JavaScript, and F#, with experimental support for Python, PHP, TypeScript, Batch, Bash, and PowerShell.</span></span>

<span data-ttu-id="ddde7-119">Version 2.x est en version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="ddde7-119">Version 2.x is in preview.</span></span> <span data-ttu-id="ddde7-120">Il s’appuie sur .NET Core et prend en charge le développement multiplateforme sur Windows, macOS et les machines Linux.</span><span class="sxs-lookup"><span data-stu-id="ddde7-120">It leverages .NET Core and supports cross-platform development on Windows, macOS, and Linux machines.</span></span> <span data-ttu-id="ddde7-121">2.x ajoute la prise en charge de première classe pour Java, mais n’encore directement prend pas en charge les langages expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="ddde7-121">2.x adds first-class support for Java but doesn't yet directly support any of the experimental languages.</span></span> <span data-ttu-id="ddde7-122">Version 2.x utilise un nouveau modèle d’extensibilité de liaison qui permet des extensions tierces pour la plateforme, le contrôle de version indépendant de liaisons, et une plus rationalisé l’environnement d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ddde7-122">Version 2.x uses a new binding extensibility model that enables third-party extensions to the platform, independent versioning of bindings, and a more streamlined execution environment.</span></span>

> <span data-ttu-id="ddde7-123">**Il existe un problème connu dans la version 1.x avec [prise en charge de la redirection de liaison](https://github.com/Azure/azure-functions-host/issues/992).**</span><span class="sxs-lookup"><span data-stu-id="ddde7-123">**There is a known issue in 1.x with [binding redirect support](https://github.com/Azure/azure-functions-host/issues/992).**</span></span> <span data-ttu-id="ddde7-124">Le problème est spécifique au développement .NET.</span><span class="sxs-lookup"><span data-stu-id="ddde7-124">The issue is specific to .NET development.</span></span> <span data-ttu-id="ddde7-125">Projets avec des dépendances sur les bibliothèques qui sont une version différente des bibliothèques incluses dans le runtime sont affectées.</span><span class="sxs-lookup"><span data-stu-id="ddde7-125">Projects with dependencies on libraries that are a different version from the libraries included in the runtime are impacted.</span></span> <span data-ttu-id="ddde7-126">L’équipe de fonctions a validés dans progresse concrètes sur le problème.</span><span class="sxs-lookup"><span data-stu-id="ddde7-126">The functions team has committed to making concrete progress on the problem.</span></span> <span data-ttu-id="ddde7-127">L’équipe traiteront des redirections de liaison dans la version 2.x avant sa mise en disponibilité générale.</span><span class="sxs-lookup"><span data-stu-id="ddde7-127">The team will address binding redirects in 2.x before it goes into general availability.</span></span> <span data-ttu-id="ddde7-128">L’instruction officiel de l’équipe avec des suggestions de correction et les solutions de contournement est disponible ici : [résolution d’Assembly dans Azure Functions](https://github.com/Azure/azure-functions-host/wiki/Assembly-Resolution-in-Azure-Functions).</span><span class="sxs-lookup"><span data-stu-id="ddde7-128">The official team statement with suggested fixes and workarounds is available here: [Assembly resolution in Azure Functions](https://github.com/Azure/azure-functions-host/wiki/Assembly-Resolution-in-Azure-Functions).</span></span>

<span data-ttu-id="ddde7-129">Pour plus d’informations, consultez [comparer 1.x et 2.x](https://docs.microsoft.com/azure/azure-functions/functions-versions).</span><span class="sxs-lookup"><span data-stu-id="ddde7-129">For more information, see [Compare 1.x and 2.x](https://docs.microsoft.com/azure/azure-functions/functions-versions).</span></span>

## <a name="programming-language-support"></a><span data-ttu-id="ddde7-130">Prise en charge du langage de programmation</span><span class="sxs-lookup"><span data-stu-id="ddde7-130">Programming language support</span></span>

<span data-ttu-id="ddde7-131">Les langues suivantes sont prises en charge soit en général à la disposition générale, afficher un aperçu, ou la version expérimentale.</span><span class="sxs-lookup"><span data-stu-id="ddde7-131">The following languages are supported either in general availability (GA), preview, or experimental.</span></span>

|<span data-ttu-id="ddde7-132">Langue</span><span class="sxs-lookup"><span data-stu-id="ddde7-132">Language</span></span>      |<span data-ttu-id="ddde7-133">1.x</span><span class="sxs-lookup"><span data-stu-id="ddde7-133">1.x</span></span>         |<span data-ttu-id="ddde7-134">2.x</span><span class="sxs-lookup"><span data-stu-id="ddde7-134">2.x</span></span>      |
|--------------|------------|---------|
|<span data-ttu-id="ddde7-135">**C#**</span><span class="sxs-lookup"><span data-stu-id="ddde7-135">**C#**</span></span>        |<span data-ttu-id="ddde7-136">DISPONIBILITÉ GÉNÉRALE</span><span class="sxs-lookup"><span data-stu-id="ddde7-136">GA</span></span>          |<span data-ttu-id="ddde7-137">Preview</span><span class="sxs-lookup"><span data-stu-id="ddde7-137">Preview</span></span>  |
|<span data-ttu-id="ddde7-138">**JavaScript**</span><span class="sxs-lookup"><span data-stu-id="ddde7-138">**JavaScript**</span></span>|<span data-ttu-id="ddde7-139">DISPONIBILITÉ GÉNÉRALE</span><span class="sxs-lookup"><span data-stu-id="ddde7-139">GA</span></span>          |<span data-ttu-id="ddde7-140">Preview</span><span class="sxs-lookup"><span data-stu-id="ddde7-140">Preview</span></span>  |
|<span data-ttu-id="ddde7-141">**F#**</span><span class="sxs-lookup"><span data-stu-id="ddde7-141">**F#**</span></span>        |<span data-ttu-id="ddde7-142">DISPONIBILITÉ GÉNÉRALE</span><span class="sxs-lookup"><span data-stu-id="ddde7-142">GA</span></span>          |         |
|<span data-ttu-id="ddde7-143">**Java**</span><span class="sxs-lookup"><span data-stu-id="ddde7-143">**Java**</span></span>      |            |<span data-ttu-id="ddde7-144">Preview</span><span class="sxs-lookup"><span data-stu-id="ddde7-144">Preview</span></span>  |
|<span data-ttu-id="ddde7-145">**Python**</span><span class="sxs-lookup"><span data-stu-id="ddde7-145">**Python**</span></span>    |<span data-ttu-id="ddde7-146">Expérimental</span><span class="sxs-lookup"><span data-stu-id="ddde7-146">Experimental</span></span>|         |
|<span data-ttu-id="ddde7-147">**PHP**</span><span class="sxs-lookup"><span data-stu-id="ddde7-147">**PHP**</span></span>       |<span data-ttu-id="ddde7-148">Expérimental</span><span class="sxs-lookup"><span data-stu-id="ddde7-148">Experimental</span></span>|         |
|<span data-ttu-id="ddde7-149">**TypeScript**</span><span class="sxs-lookup"><span data-stu-id="ddde7-149">**TypeScript**</span></span>|<span data-ttu-id="ddde7-150">Expérimental</span><span class="sxs-lookup"><span data-stu-id="ddde7-150">Experimental</span></span>|         |
|<span data-ttu-id="ddde7-151">**Batch**</span><span class="sxs-lookup"><span data-stu-id="ddde7-151">**Batch**</span></span>     |<span data-ttu-id="ddde7-152">Expérimental</span><span class="sxs-lookup"><span data-stu-id="ddde7-152">Experimental</span></span>|         |
|<span data-ttu-id="ddde7-153">**Bash**</span><span class="sxs-lookup"><span data-stu-id="ddde7-153">**Bash**</span></span>      |<span data-ttu-id="ddde7-154">Expérimental</span><span class="sxs-lookup"><span data-stu-id="ddde7-154">Experimental</span></span>|         |
|<span data-ttu-id="ddde7-155">**PowerShell**</span><span class="sxs-lookup"><span data-stu-id="ddde7-155">**PowerShell**</span></span>|<span data-ttu-id="ddde7-156">Expérimental</span><span class="sxs-lookup"><span data-stu-id="ddde7-156">Experimental</span></span>|         |

<span data-ttu-id="ddde7-157">Pour plus d’informations, consultez [langues prises en charge](https://docs.microsoft.com/azure/azure-functions/supported-languages).</span><span class="sxs-lookup"><span data-stu-id="ddde7-157">For more information, see [Supported languages](https://docs.microsoft.com/azure/azure-functions/supported-languages).</span></span>

## <a name="app-service-plans"></a><span data-ttu-id="ddde7-158">Plans app service</span><span class="sxs-lookup"><span data-stu-id="ddde7-158">App service plans</span></span>

<span data-ttu-id="ddde7-159">Les fonctions sont soutenues par une *plan app service*.</span><span class="sxs-lookup"><span data-stu-id="ddde7-159">Functions are backed by an *app service plan*.</span></span> <span data-ttu-id="ddde7-160">Le plan définit les ressources utilisées par l’application de fonctions.</span><span class="sxs-lookup"><span data-stu-id="ddde7-160">The plan defines the resources used by the functions app.</span></span> <span data-ttu-id="ddde7-161">Vous pouvez affecter des plans à une région, déterminer la taille et le nombre de machines virtuelles qui sera utilisé et choisir un niveau tarifaire.</span><span class="sxs-lookup"><span data-stu-id="ddde7-161">You can assign plans to a region, determine the size and number of virtual machines that will be used, and pick a pricing tier.</span></span> <span data-ttu-id="ddde7-162">Pour une approche sans serveur true, les applications de fonction peut utiliser le **consommation** plan.</span><span class="sxs-lookup"><span data-stu-id="ddde7-162">For a true serverless approach, function apps may use the **consumption** plan.</span></span> <span data-ttu-id="ddde7-163">Le plan de consommation mettra à l’échelle le serveur principal automatiquement en fonction de charge.</span><span class="sxs-lookup"><span data-stu-id="ddde7-163">The consumption plan will scale the back end automatically based on load.</span></span>

<span data-ttu-id="ddde7-164">Pour plus d’informations, consultez [plans App service](https://docs.microsoft.com/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview).</span><span class="sxs-lookup"><span data-stu-id="ddde7-164">For more information, see [App service plans](https://docs.microsoft.com/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview).</span></span>

## <a name="create-your-first-function"></a><span data-ttu-id="ddde7-165">Créer votre première fonction</span><span class="sxs-lookup"><span data-stu-id="ddde7-165">Create your first function</span></span>

<span data-ttu-id="ddde7-166">Il existe trois façons courantes que vous pouvez créer des applications de fonction.</span><span class="sxs-lookup"><span data-stu-id="ddde7-166">There are three common ways you can create function apps.</span></span>

* <span data-ttu-id="ddde7-167">Fonctions de script dans le portail.</span><span class="sxs-lookup"><span data-stu-id="ddde7-167">Script functions in the portal.</span></span>
* <span data-ttu-id="ddde7-168">Créer les ressources nécessaires à l’aide de l’Interface de ligne de commande Azure (CLI).</span><span class="sxs-lookup"><span data-stu-id="ddde7-168">Create the necessary resources using the Azure Command Line Interface (CLI).</span></span>
* <span data-ttu-id="ddde7-169">Créer des fonctions localement à l’aide de votre IDE favori et publiez-les sur Azure.</span><span class="sxs-lookup"><span data-stu-id="ddde7-169">Build functions locally using your favorite IDE and publish them to Azure.</span></span>

<span data-ttu-id="ddde7-170">Pour plus d’informations sur la création d’une fonction de script dans le portail, consultez [créer votre première fonction dans le portail Azure](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function).</span><span class="sxs-lookup"><span data-stu-id="ddde7-170">For more information on creating a scripted function in the portal, see [Create your first function in the Azure portal](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function).</span></span>

<span data-ttu-id="ddde7-171">Pour générer à partir de l’interface CLI, consultez [créer votre première fonction à l’aide de l’interface CLI](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function-azure-cli).</span><span class="sxs-lookup"><span data-stu-id="ddde7-171">To build from the Azure CLI, see [Create your first function using the Azure CLI](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function-azure-cli).</span></span>

<span data-ttu-id="ddde7-172">Pour créer une fonction à partir de Visual Studio, consultez [créer votre première fonction à l’aide de Visual Studio](https://docs.microsoft.com/azure/azure-functions/functions-create-your-first-function-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="ddde7-172">To create a function from Visual Studio, see [Create your first function using Visual Studio](https://docs.microsoft.com/azure/azure-functions/functions-create-your-first-function-visual-studio).</span></span>

## <a name="understand-triggers-and-bindings"></a><span data-ttu-id="ddde7-173">Comprendre les déclencheurs et liaisons</span><span class="sxs-lookup"><span data-stu-id="ddde7-173">Understand triggers and bindings</span></span>

<span data-ttu-id="ddde7-174">Les fonctions sont appelées par un *déclencheur* et peut avoir exactement un.</span><span class="sxs-lookup"><span data-stu-id="ddde7-174">Functions are invoked by a *trigger* and can have exactly one.</span></span> <span data-ttu-id="ddde7-175">En plus d’appeler la fonction, certains déclencheurs servent également de liaisons.</span><span class="sxs-lookup"><span data-stu-id="ddde7-175">In addition to invoking the function, certain triggers also serve as bindings.</span></span> <span data-ttu-id="ddde7-176">Vous pouvez également définir plusieurs liaisons en plus du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="ddde7-176">You may also define multiple bindings in addition to the trigger.</span></span> <span data-ttu-id="ddde7-177">*Liaisons* fournissent un moyen déclaratif pour connecter les données à votre code.</span><span class="sxs-lookup"><span data-stu-id="ddde7-177">*Bindings* provide a declarative way to connect data to your code.</span></span> <span data-ttu-id="ddde7-178">Ils peuvent être passés d’entrée (in) ou recevoir des données (sortie).</span><span class="sxs-lookup"><span data-stu-id="ddde7-178">They can be passed in (input) or receive data (output).</span></span> <span data-ttu-id="ddde7-179">Déclencheurs et liaisons rendre fonctions facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ddde7-179">Triggers and bindings make functions easy to work with.</span></span> <span data-ttu-id="ddde7-180">Liaisons de supprimer la surcharge liée à la création manuelle de base de données ou un fichier connexions du système.</span><span class="sxs-lookup"><span data-stu-id="ddde7-180">Bindings remove the overhead of manually creating database or file system connections.</span></span> <span data-ttu-id="ddde7-181">Toutes les informations nécessaires pour les liaisons est contenue dans un spécial *functions.json* de fichiers pour les scripts ou déclarés avec les attributs dans le code.</span><span class="sxs-lookup"><span data-stu-id="ddde7-181">All of the information needed for the bindings is contained in a special *functions.json* file for scripts or declared with attributes in code.</span></span>

<span data-ttu-id="ddde7-182">Certains déclencheurs courants sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddde7-182">Some common triggers include:</span></span>

* <span data-ttu-id="ddde7-183">Stockage d’objets BLOB : appelez votre fonction lorsqu’un fichier ou dossier est chargé ou modifié dans le stockage.</span><span class="sxs-lookup"><span data-stu-id="ddde7-183">Blob Storage: invoke your function when a file or folder is uploaded or changed in storage.</span></span>
* <span data-ttu-id="ddde7-184">HTTP : appelle votre fonction comme une API REST.</span><span class="sxs-lookup"><span data-stu-id="ddde7-184">HTTP: invoke your function like a REST API.</span></span>
* <span data-ttu-id="ddde7-185">File d’attente : appelez votre fonction lorsqu’il existent des éléments dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ddde7-185">Queue: invoke your function when items exist in a queue.</span></span>
* <span data-ttu-id="ddde7-186">Minuteur : appelle votre fonction sur une cadence régulière.</span><span class="sxs-lookup"><span data-stu-id="ddde7-186">Timer: invoke your function on a regular cadence.</span></span>

<span data-ttu-id="ddde7-187">Voici quelques exemples de liaisons :</span><span class="sxs-lookup"><span data-stu-id="ddde7-187">Examples of bindings include:</span></span>

* <span data-ttu-id="ddde7-188">COSMOS DB : se connecter facilement à la base de données à charger ou enregistrer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="ddde7-188">CosmosDB: easily connect to the database to load or save files.</span></span>
* <span data-ttu-id="ddde7-189">Stockage de table : utilisation du stockage de clé/valeur à partir de votre application de fonction.</span><span class="sxs-lookup"><span data-stu-id="ddde7-189">Table Storage: work with key/value storage from your function app.</span></span>
* <span data-ttu-id="ddde7-190">Stockage de file d’attente : facilement extraire des éléments à partir d’une file d’attente, ou placer de nouveaux éléments sur la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ddde7-190">Queue Storage: easily retrieve items from a queue, or place new items on the queue.</span></span>

<span data-ttu-id="ddde7-191">L’exemple suivant *functions.json* fichier définit un déclencheur et une liaison :</span><span class="sxs-lookup"><span data-stu-id="ddde7-191">The following example *functions.json* file defines a trigger and a binding:</span></span>

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

<span data-ttu-id="ddde7-192">Dans cet exemple, la fonction est déclenchée par une modification apportée à un stockage d’objets blob dans le `images` conteneur.</span><span class="sxs-lookup"><span data-stu-id="ddde7-192">In this example, the function is triggered by a change to blob storage in the `images` container.</span></span> <span data-ttu-id="ddde7-193">Les informations pour le fichier sont transmises, donc le déclencheur agit également comme une liaison.</span><span class="sxs-lookup"><span data-stu-id="ddde7-193">The information for the file is passed in, so the trigger also acts as a binding.</span></span> <span data-ttu-id="ddde7-194">Une autre liaison existe pour placer des informations sur une file d’attente nommée `images`.</span><span class="sxs-lookup"><span data-stu-id="ddde7-194">Another binding exists to put information onto a queue named `images`.</span></span>

<span data-ttu-id="ddde7-195">Voici le script c# pour la fonction :</span><span class="sxs-lookup"><span data-stu-id="ddde7-195">Here is the C# script for the function:</span></span>

```csharp
public static string Run(Stream myBlob, string name, TraceWriter log)
{
    log.Info($"C# Blob trigger function Processed blob\n Name:{name} \n Size: {myBlob.Length} Bytes");
    return name;
}
```

<span data-ttu-id="ddde7-196">L’exemple est une fonction simple qui prend le nom du fichier qui a été modifiée ou chargée dans un stockage d’objets blob et le place dans une file d’attente pour un traitement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="ddde7-196">The example is a simple function that takes the name of the file that was modified or uploaded to blob storage, and places it on a queue for later processing.</span></span>

<span data-ttu-id="ddde7-197">Pour obtenir une liste complète des déclencheurs et liaisons, consultez [Azure Functions concepts des déclencheurs et liaisons](https://docs.microsoft.com/azure/azure-functions/functions-triggers-bindings).</span><span class="sxs-lookup"><span data-stu-id="ddde7-197">For a full list of triggers and bindings, see [Azure Functions triggers and bindings concepts](https://docs.microsoft.com/azure/azure-functions/functions-triggers-bindings).</span></span>

## <a name="proxies"></a><span data-ttu-id="ddde7-198">Serveurs proxy</span><span class="sxs-lookup"><span data-stu-id="ddde7-198">Proxies</span></span>

<span data-ttu-id="ddde7-199">Proxys fournissent la fonctionnalité de redirection pour votre application.</span><span class="sxs-lookup"><span data-stu-id="ddde7-199">Proxies provide redirect functionality for your application.</span></span> <span data-ttu-id="ddde7-200">Proxys d’exposent un point de terminaison et mappent ce point de terminaison à une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="ddde7-200">Proxies expose an endpoint and map that endpoint to another resource.</span></span> <span data-ttu-id="ddde7-201">Avec les serveurs proxy, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="ddde7-201">With proxies, you can:</span></span>

* <span data-ttu-id="ddde7-202">Rediriger une demande entrante vers un autre point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ddde7-202">Reroute an incoming request to another endpoint.</span></span>
* <span data-ttu-id="ddde7-203">Modifier la requête entrante avant qu’il n’est transmise.</span><span class="sxs-lookup"><span data-stu-id="ddde7-203">Modify the incoming request before it's passed along.</span></span>
* <span data-ttu-id="ddde7-204">Modifier ou fournir une réponse.</span><span class="sxs-lookup"><span data-stu-id="ddde7-204">Modify or provide a response.</span></span>

<span data-ttu-id="ddde7-205">Proxys sont utilisés pour des scénarios tels que :</span><span class="sxs-lookup"><span data-stu-id="ddde7-205">Proxies are used for scenarios such as:</span></span>

* <span data-ttu-id="ddde7-206">Simplifier, raccourcir ou de modifier l’URL.</span><span class="sxs-lookup"><span data-stu-id="ddde7-206">Simplifying, shortening, or changing the URL.</span></span>
* <span data-ttu-id="ddde7-207">En fournissant un préfixe d’API cohérent pour plusieurs services principaux.</span><span class="sxs-lookup"><span data-stu-id="ddde7-207">Providing a consistent API prefix to multiple back-end services.</span></span>
* <span data-ttu-id="ddde7-208">Simulation d’une réponse à un point de terminaison en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="ddde7-208">Mocking a response to an endpoint being developed.</span></span>
* <span data-ttu-id="ddde7-209">En fournissant une réponse statique à un point de terminaison connu.</span><span class="sxs-lookup"><span data-stu-id="ddde7-209">Providing a static response to a well-known endpoint.</span></span>
* <span data-ttu-id="ddde7-210">Conservation d’un point de terminaison d’API cohérent tandis que le serveur principal a été déplacé ou migrée.</span><span class="sxs-lookup"><span data-stu-id="ddde7-210">Keeping an API endpoint consistent while the back end is moved or migrated.</span></span>

<span data-ttu-id="ddde7-211">Serveurs proxy sont stockés en tant que définitions de JSON.</span><span class="sxs-lookup"><span data-stu-id="ddde7-211">Proxies are stored as JSON definitions.</span></span> <span data-ttu-id="ddde7-212">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="ddde7-212">Here is an example:</span></span>

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

<span data-ttu-id="ddde7-213">Le `Domain Redirect` proxy prend un itinéraire abrégé et le mappe à la ressource de fonction plus de temps.</span><span class="sxs-lookup"><span data-stu-id="ddde7-213">The `Domain Redirect` proxy takes a shortened route and maps it to the longer function resource.</span></span> <span data-ttu-id="ddde7-214">La transformation de l’aspect suivant :</span><span class="sxs-lookup"><span data-stu-id="ddde7-214">The transformation looks like:</span></span>

`https://--shorturl--/123` -> `https://--longurl--.azurewebsites.net/api/UrlRedirect/123`

<span data-ttu-id="ddde7-215">Le `Root` proxy prend quoi que ce soit envoyé à l’URL racine (`https://--shorturl--/`) et la redirige vers le site de documentation.</span><span class="sxs-lookup"><span data-stu-id="ddde7-215">The `Root` proxy takes anything sent to the root URL (`https://--shorturl--/`) and redirects it to the documentation site.</span></span>

<span data-ttu-id="ddde7-216">Voici un exemple d’utilisation de proxys dans la vidéo [Azure : importez votre application dans le cloud avec Azure Functions sans serveur](https://channel9.msdn.com/events/Connect/2017/E102).</span><span class="sxs-lookup"><span data-stu-id="ddde7-216">An example of using proxies is shown in the video [Azure: Bring your app to the cloud with serverless Azure Functions](https://channel9.msdn.com/events/Connect/2017/E102).</span></span> <span data-ttu-id="ddde7-217">En temps réel, une application ASP.NET Core s’exécutant sur le serveur SQL Server local est migrée vers le Cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="ddde7-217">In real time, an ASP.NET Core application running on local SQL Server is migrated to the Azure Cloud.</span></span> <span data-ttu-id="ddde7-218">Proxys sont utilisés pour aider à refactoriser un projet d’API Web traditionnel pour utiliser des fonctions.</span><span class="sxs-lookup"><span data-stu-id="ddde7-218">Proxies are used to help refactor a traditional Web API project to use functions.</span></span>

<span data-ttu-id="ddde7-219">Pour plus d’informations sur les proxys, consultez [fonctionne avec Azure Functions Proxies](https://docs.microsoft.com/azure/azure-functions/functions-proxies).</span><span class="sxs-lookup"><span data-stu-id="ddde7-219">For more information about Proxies, see [Work with Azure Functions Proxies](https://docs.microsoft.com/azure/azure-functions/functions-proxies).</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="ddde7-220">[Précédent](azure-serverless-platform.md)
[Suivant](application-insights.md)</span><span class="sxs-lookup"><span data-stu-id="ddde7-220">[Previous](azure-serverless-platform.md)
[Next](application-insights.md)</span></span>