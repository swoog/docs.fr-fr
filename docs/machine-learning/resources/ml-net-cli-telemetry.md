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
# <a name="telemetry-collection-by-the-mlnet-cli"></a><span data-ttu-id="414cd-104">Collecte des données de télémétrie par la CLI ML.NET</span><span class="sxs-lookup"><span data-stu-id="414cd-104">Telemetry collection by the ML.NET CLI</span></span>

<span data-ttu-id="414cd-105">La [CLI ML.NET](http://aka.ms/mlnet-cli) inclut une fonctionnalité de télémétrie qui collecte les données d’utilisation anonymes, qui sont agrégées en vue d’une utilisation par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="414cd-105">The [ML.NET CLI](http://aka.ms/mlnet-cli) includes a telemetry feature that collects anonymous usage data that is aggregated for use by Microsoft.</span></span>

## <a name="how-microsoft-uses-the-data"></a><span data-ttu-id="414cd-106">Comment Microsoft utilise les données</span><span class="sxs-lookup"><span data-stu-id="414cd-106">How Microsoft uses the data</span></span>

<span data-ttu-id="414cd-107">L’équipe de produit utilise les données de télémétrie collectées par la CLI ML.NET pour essayer de comprendre comment améliorer les outils.</span><span class="sxs-lookup"><span data-stu-id="414cd-107">The product team uses ML.NET CLI telemetry data to help understand how to improve the tools.</span></span> <span data-ttu-id="414cd-108">Par exemple, si les clients utilisent rarement une tâche de machine learning spécifique, l’équipe de produit en analyse la raison, puis hiérarchise le développement des fonctionnalités à partir des conclusions qu’elle a tirées.</span><span class="sxs-lookup"><span data-stu-id="414cd-108">For example, if customers infrequently use a particular machine learning task, the product team investigates why and uses findings to prioritize feature development.</span></span> <span data-ttu-id="414cd-109">En outre, les données de télémétrie collectées par la CLI ML.NET facilitent le débogage des problèmes tels que les plantages et les anomalies de code.</span><span class="sxs-lookup"><span data-stu-id="414cd-109">ML.NET CLI telemetry also helps with debugging of issues such as crashes and code anomalies.</span></span> 

<span data-ttu-id="414cd-110">Bien que l’équipe de produit apprécie cet insight, nous savons également que tout le monde n’est pas disposé à envoyer ces données.</span><span class="sxs-lookup"><span data-stu-id="414cd-110">While the product team appreciates this insight, we also know that not everyone wants to send this data.</span></span> [<span data-ttu-id="414cd-111">Découvrez comment désactiver la télémétrie.</span><span class="sxs-lookup"><span data-stu-id="414cd-111">Find out how to disable telemetry.</span></span>](#opt-out-of-data-collection)

## <a name="scope"></a><span data-ttu-id="414cd-112">Portée</span><span class="sxs-lookup"><span data-stu-id="414cd-112">Scope</span></span>

<span data-ttu-id="414cd-113">La commande `mlnet` lance l’interface CLI ML.NET, mais ne collecte pas elle-même les données de télémétrie.</span><span class="sxs-lookup"><span data-stu-id="414cd-113">The `mlnet` command launches the ML.NET CLI, but the command itself doesn't collect telemetry.</span></span>

<span data-ttu-id="414cd-114">La télémétrie *n’est pas activée* quand vous exécutez la commande `mlnet` sans aucune autre commande attachée.</span><span class="sxs-lookup"><span data-stu-id="414cd-114">Telemetry *isn't enabled* when you run the `mlnet` command with no other command attached.</span></span> <span data-ttu-id="414cd-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="414cd-115">For example:</span></span>

- `mlnet`
- `mlnet --help`

<span data-ttu-id="414cd-116">La télémétrie *est activée* quand vous exécutez une [commande CLI ML.NET](../reference/ml-net-cli-reference.md), telle que `mlnet auto-train`.</span><span class="sxs-lookup"><span data-stu-id="414cd-116">Telemetry *is enabled* when you run an [ML.NET CLI command](../reference/ml-net-cli-reference.md), such as `mlnet auto-train`.</span></span>

## <a name="opt-out-of-data-collection"></a><span data-ttu-id="414cd-117">Refuser la collecte de données</span><span class="sxs-lookup"><span data-stu-id="414cd-117">Opt out of data collection</span></span>

<span data-ttu-id="414cd-118">La fonctionnalité de télémétrie de la CLI ML.NET est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="414cd-118">The ML.NET CLI telemetry feature is enabled by default.</span></span>

<span data-ttu-id="414cd-119">Pour la désactiver, affectez la valeur `1` ou `true` à la variable d’environnement `DOTNET_CLI_TELEMETRY_OPTOUT`.</span><span class="sxs-lookup"><span data-stu-id="414cd-119">Opt out of the telemetry feature by setting the `DOTNET_CLI_TELEMETRY_OPTOUT` environment variable to `1` or `true`.</span></span> <span data-ttu-id="414cd-120">Cette variable d’environnement s’applique globalement à l’outil CLI .NET.</span><span class="sxs-lookup"><span data-stu-id="414cd-120">This environment variable applies globally to the .NET CLI tool.</span></span>

## <a name="data-points-collected"></a><span data-ttu-id="414cd-121">Points de données collectés</span><span class="sxs-lookup"><span data-stu-id="414cd-121">Data points collected</span></span>

<span data-ttu-id="414cd-122">La fonctionnalité recueille les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="414cd-122">The feature collects the following data:</span></span>

- <span data-ttu-id="414cd-123">Les commandes appelées, comme `auto-train`</span><span class="sxs-lookup"><span data-stu-id="414cd-123">Which commands are invoked, such as `auto-train`</span></span>
- <span data-ttu-id="414cd-124">Adresse MAC hachée : ID unique et anonyme chiffré (SHA256) pour une machine</span><span class="sxs-lookup"><span data-stu-id="414cd-124">Hashed MAC address: a cryptographically (SHA256) anonymous and unique ID for a machine</span></span>
- <span data-ttu-id="414cd-125">Horodatage d’un appel</span><span class="sxs-lookup"><span data-stu-id="414cd-125">Timestamp of an invocation</span></span>
- <span data-ttu-id="414cd-126">Adresse IP de trois octets utilisée uniquement pour déterminer l’emplacement géographique</span><span class="sxs-lookup"><span data-stu-id="414cd-126">Three octet IP address used only to determine geographical location</span></span>
- <span data-ttu-id="414cd-127">Nom de tous les arguments/paramètres utilisés.</span><span class="sxs-lookup"><span data-stu-id="414cd-127">Name of all arguments/parameters used.</span></span> <span data-ttu-id="414cd-128">Pas les valeurs du client, telles que des chaînes.</span><span class="sxs-lookup"><span data-stu-id="414cd-128">Not the customer's values, such as strings</span></span>
- <span data-ttu-id="414cd-129">Système d’exploitation et version</span><span class="sxs-lookup"><span data-stu-id="414cd-129">Operating system and version</span></span>
- <span data-ttu-id="414cd-130">Valeur du paramètre --ml-task : valeurs de catégorie, telles que `regression`, `binary-classification` et `multiclass-classification`</span><span class="sxs-lookup"><span data-stu-id="414cd-130">Value of --ml-task parameter: Categorical values, such as `regression`, `binary-classification`, and `multiclass-classification`</span></span>
- <span data-ttu-id="414cd-131">Taille du fichier de jeu de données avec [arrondi logarithmique](https://en.wikipedia.org/wiki/Rounding#Rounding_to_a_specified_power) (puissance de 2 la plus proche)</span><span class="sxs-lookup"><span data-stu-id="414cd-131">[Logarithmic rounded](https://en.wikipedia.org/wiki/Rounding#Rounding_to_a_specified_power) dataset file size (nearest power of 2)</span></span>
- <span data-ttu-id="414cd-132">`ExitCode` de la commande</span><span class="sxs-lookup"><span data-stu-id="414cd-132">`ExitCode` of the command</span></span>

<span data-ttu-id="414cd-133">Les données sont envoyées de manière sécurisée à des serveurs Microsoft à l’aide de la technologie [Azure Application Insights](https://azure.microsoft.com/services/application-insights/), stockées à un emplacement dont l’accès est strictement limité et utilisées conformément à des contrôles de sécurité stricts à partir de systèmes [Stockage Azure](https://azure.microsoft.com/services/storage/) sécurisés.</span><span class="sxs-lookup"><span data-stu-id="414cd-133">The data is sent securely to Microsoft servers using [Azure Application Insights](https://azure.microsoft.com/services/application-insights/) technology, held under restricted access, and used under strict security controls from secure [Azure Storage](https://azure.microsoft.com/services/storage/) systems.</span></span>

### <a name="data-points-not-collected"></a><span data-ttu-id="414cd-134">Points de données non collectés</span><span class="sxs-lookup"><span data-stu-id="414cd-134">Data points not collected</span></span>
<span data-ttu-id="414cd-135">La fonctionnalité de télémétrie *ne collecte pas* les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="414cd-135">The telemetry feature *doesn't* collect:</span></span>
- <span data-ttu-id="414cd-136">Données personnelles, telles que les noms d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="414cd-136">personal data, such as usernames</span></span>
- <span data-ttu-id="414cd-137">Noms de fichier de jeu de données</span><span class="sxs-lookup"><span data-stu-id="414cd-137">dataset filenames</span></span>
- <span data-ttu-id="414cd-138">Données des fichiers de jeu de données</span><span class="sxs-lookup"><span data-stu-id="414cd-138">data from dataset files</span></span>

<span data-ttu-id="414cd-139">Si vous pensez que la fonctionnalité de télémétrie de la CLI ML.NET collecte des données sensibles ou que les données sont gérées de manière non sécurisée ou incorrecte, soumettez un problème dans le dépôt [ML.NET](https://github.com/dotnet/machinelearning) afin que nous investiguions.</span><span class="sxs-lookup"><span data-stu-id="414cd-139">If you suspect that the ML.NET CLI telemetry is collecting sensitive data or that the data is being insecurely or inappropriately handled, file an issue in the [ML.NET](https://github.com/dotnet/machinelearning) repository for investigation.</span></span>

## <a name="license"></a><span data-ttu-id="414cd-140">Licence</span><span class="sxs-lookup"><span data-stu-id="414cd-140">License</span></span>

<span data-ttu-id="414cd-141">La distribution Microsoft de la CLI ML.NET est concédée sous licence avec les [Termes du contrat de licence logicielle Microsoft : bibliothèque Microsoft .NET](https://aka.ms/dotnet-core-eula).</span><span class="sxs-lookup"><span data-stu-id="414cd-141">The Microsoft distribution of ML.NET CLI is licensed with the [Microsoft Software License Terms: Microsoft .NET Library](https://aka.ms/dotnet-core-eula).</span></span> <span data-ttu-id="414cd-142">Pour plus d’informations sur la collecte et le traitement de données, consultez la section intitulée « Données ».</span><span class="sxs-lookup"><span data-stu-id="414cd-142">For details on data collection and processing, see the section entitled "Data."</span></span>

## <a name="disclosure"></a><span data-ttu-id="414cd-143">Divulgation d’informations</span><span class="sxs-lookup"><span data-stu-id="414cd-143">Disclosure</span></span>

<span data-ttu-id="414cd-144">Quand vous exécutez pour la première fois une [commande de la CLI ML.NET](../reference/ml-net-cli-reference.md) telle que `mlnet auto-train`, l’outil CLI ML.NET affiche un texte de divulgation qui vous indique comment refuser la télémétrie.</span><span class="sxs-lookup"><span data-stu-id="414cd-144">When you first run a [ML.NET CLI command](../reference/ml-net-cli-reference.md) such as `mlnet auto-train`, the ML.NET CLI tool displays disclosure text that tells you how to opt out of telemetry.</span></span> <span data-ttu-id="414cd-145">Le texte peut varier légèrement selon la version de la CLI que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="414cd-145">Text may vary slightly depending on the version of the CLI you're running.</span></span>

## <a name="see-also"></a><span data-ttu-id="414cd-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414cd-146">See also</span></span>
- [<span data-ttu-id="414cd-147">Informations de référence sur l’interface de ligne de commande ML.NET</span><span class="sxs-lookup"><span data-stu-id="414cd-147">ML.NET CLI reference</span></span>](../reference/ml-net-cli-reference.md)
- [<span data-ttu-id="414cd-148">Termes du contrat de licence logiciel Microsoft : bibliothèque Microsoft .NET</span><span class="sxs-lookup"><span data-stu-id="414cd-148">Microsoft Software License Terms: Microsoft .NET Library</span></span>](https://aka.ms/dotnet-core-eula)
- [<span data-ttu-id="414cd-149">Confidentialité chez Microsoft</span><span class="sxs-lookup"><span data-stu-id="414cd-149">Privacy at Microsoft</span></span>](https://www.microsoft.com/en-us/trustcenter/privacy/)
- [<span data-ttu-id="414cd-150">Déclaration de confidentialité Microsoft</span><span class="sxs-lookup"><span data-stu-id="414cd-150">Microsoft Privacy Statement</span></span>](https://privacy.microsoft.com/en-us/privacystatement)