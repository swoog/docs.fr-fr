---
title: Télémétrie des outils CLI .NET Core
description: Découvrez les fonctionnalités de télémétrie des outils .NET Core, qui collectent des informations d’utilisation à des fins d’analyse, les types de données collectées et comment désactiver la télémétrie.
author: richlander
ms.author: mairaw
ms.date: 08/04/2017
ms.openlocfilehash: 4c04867f5db512ef53c23ec41ea66db570a82021
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33216081"
---
# <a name="net-core-cli-tools-telemetry"></a><span data-ttu-id="76fb5-103">Télémétrie des outils CLI .NET Core</span><span class="sxs-lookup"><span data-stu-id="76fb5-103">.NET Core CLI Tools telemetry</span></span>

<span data-ttu-id="76fb5-104">Le [SDK .NET Core](index.md) inclut une [fonctionnalité de télémétrie](https://github.com/dotnet/cli/pull/2145) qui recueille des informations d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="76fb5-104">The [.NET Core SDK](index.md) includes a [telemetry feature](https://github.com/dotnet/cli/pull/2145) that collects usage information.</span></span> <span data-ttu-id="76fb5-105">Il est important pour l’équipe .NET de comprendre la façon dont les outils sont utilisés, afin de pouvoir les améliorer.</span><span class="sxs-lookup"><span data-stu-id="76fb5-105">It's important that the .NET Team understands how the tools are used so that we can improve them.</span></span> <span data-ttu-id="76fb5-106">Pour plus d’informations, consultez les [enseignements tirés de la fonctionnalité de télémétrie du SDK .NET Core](https://blogs.msdn.microsoft.com/dotnet/2017/07/21/what-weve-learned-from-net-core-sdk-telemetry/).</span><span class="sxs-lookup"><span data-stu-id="76fb5-106">For more information, see [What we've learned from .NET Core SDK Telemetry](https://blogs.msdn.microsoft.com/dotnet/2017/07/21/what-weve-learned-from-net-core-sdk-telemetry/).</span></span>

<span data-ttu-id="76fb5-107">Les données collectées sont anonymes et publiées sous forme regroupée en vue d’être utilisées par Microsoft et la communauté, sous la [licence Creative Commons Attribution](https://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="76fb5-107">The collected data is anonymous and published in an aggregated form for use by both Microsoft and the community under the [Creative Commons Attribution License](https://creativecommons.org/licenses/by/4.0/).</span></span> 

## <a name="scope"></a><span data-ttu-id="76fb5-108">Portée</span><span class="sxs-lookup"><span data-stu-id="76fb5-108">Scope</span></span>

<span data-ttu-id="76fb5-109">La commande `dotnet` permet de lancer des applications et l’interface CLI .NET Core.</span><span class="sxs-lookup"><span data-stu-id="76fb5-109">The `dotnet` command is used to launch both apps and the .NET Core CLI.</span></span> <span data-ttu-id="76fb5-110">La commande `dotnet` ne permet pas de collecter des données de télémétrie.</span><span class="sxs-lookup"><span data-stu-id="76fb5-110">The `dotnet` command itself doesn't collect telemetry.</span></span> <span data-ttu-id="76fb5-111">Les commandes de l’interface CLI .NET Core exécutées par la commande `dotnet` collectent les données de télémétrie.</span><span class="sxs-lookup"><span data-stu-id="76fb5-111">The .NET Core CLI commands run by the `dotnet` command collect the telemetry.</span></span>

<span data-ttu-id="76fb5-112">La télémétrie *n’est pas activée* quand vous utilisez la commande `dotnet` sans commande attachée :</span><span class="sxs-lookup"><span data-stu-id="76fb5-112">Telemetry *isn't enabled* when using the `dotnet` command itself, with no command attached:</span></span>

- `dotnet`
- `dotnet [path-to-app]`

<span data-ttu-id="76fb5-113">La télémétrie *est activée* quand vous utilisez les [commandes de l’interface CLI .NET Core](index.md), telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="76fb5-113">Telemetry *is enabled* when using the [.NET Core CLI commands](index.md), such as:</span></span>

- `dotnet build`
- `dotnet pack`
- `dotnet restore`
- `dotnet run`


## <a name="behavior"></a><span data-ttu-id="76fb5-114">Comportement</span><span class="sxs-lookup"><span data-stu-id="76fb5-114">Behavior</span></span>

<span data-ttu-id="76fb5-115">La fonctionnalité de télémétrie de l’interface CLI .NET Core est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="76fb5-115">The .NET Core CLI Tools telemetry feature is enabled by default.</span></span> <span data-ttu-id="76fb5-116">Pour ne pas l’utiliser, définissez la variable d’environnement `DOTNET_CLI_TELEMETRY_OPTOUT` sur `1` ou `true`.</span><span class="sxs-lookup"><span data-stu-id="76fb5-116">Opt-out of the telemetry feature by setting the `DOTNET_CLI_TELEMETRY_OPTOUT` environment variable to `1` or `true`.</span></span>

## <a name="data-points"></a><span data-ttu-id="76fb5-117">Points de données</span><span class="sxs-lookup"><span data-stu-id="76fb5-117">Data points</span></span>

<span data-ttu-id="76fb5-118">La fonctionnalité recueille les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="76fb5-118">The feature collects the following data:</span></span>

- <span data-ttu-id="76fb5-119">horodatage de l’appel&#8224;</span><span class="sxs-lookup"><span data-stu-id="76fb5-119">Timestamp of invocation&#8224;</span></span>
- <span data-ttu-id="76fb5-120">Commande appelée (par exemple, « build »)&#8224;</span><span class="sxs-lookup"><span data-stu-id="76fb5-120">Command invoked (for example, "build")&#8224;</span></span>
- <span data-ttu-id="76fb5-121">Adresse IP de trois octets utilisée pour déterminer l’emplacement géographique&#8224;</span><span class="sxs-lookup"><span data-stu-id="76fb5-121">Three octet IP address used to determine geographical location&#8224;</span></span>
- <span data-ttu-id="76fb5-122">`ExitCode` de la commande</span><span class="sxs-lookup"><span data-stu-id="76fb5-122">`ExitCode` of the command</span></span>
- <span data-ttu-id="76fb5-123">Exécuteur de tests (pour les projets de test)</span><span class="sxs-lookup"><span data-stu-id="76fb5-123">Test runner (for test projects)</span></span>
- <span data-ttu-id="76fb5-124">Système d’exploitation et version&#8224;</span><span class="sxs-lookup"><span data-stu-id="76fb5-124">Operating system and version&#8224;</span></span>
- <span data-ttu-id="76fb5-125">Si des ID d’exécution se trouvent sous le nœud runtimes</span><span class="sxs-lookup"><span data-stu-id="76fb5-125">Whether runtime IDs are present in the runtimes node</span></span>
- <span data-ttu-id="76fb5-126">Version du SDK .NET Core&#8224;</span><span class="sxs-lookup"><span data-stu-id="76fb5-126">.NET Core SDK version&#8224;</span></span>

<span data-ttu-id="76fb5-127">&#8224;Cette métrique est publiée.</span><span class="sxs-lookup"><span data-stu-id="76fb5-127">&#8224;This metric is published.</span></span>

<span data-ttu-id="76fb5-128">À compter du SDK .NET Core 2.0, de nouveaux points de données sont collectés :</span><span class="sxs-lookup"><span data-stu-id="76fb5-128">Starting with .NET Core SDK 2.0, new data points are collected:</span></span>

- <span data-ttu-id="76fb5-129">Arguments et options de la commande `dotnet` : seuls les arguments et options connus sont collectés (pas les chaînes arbitraires).</span><span class="sxs-lookup"><span data-stu-id="76fb5-129">`dotnet` command arguments and options: only known arguments and options are collected (not arbitrary strings).</span></span>
- <span data-ttu-id="76fb5-130">Si le SDK est en cours d’exécution dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="76fb5-130">Whether the SDK is running in a container.</span></span>
- <span data-ttu-id="76fb5-131">Frameworks cibles.</span><span class="sxs-lookup"><span data-stu-id="76fb5-131">Target frameworks.</span></span>
- <span data-ttu-id="76fb5-132">Adresse MAC hachée : ID unique et anonyme chiffré (SHA256) pour une machine.</span><span class="sxs-lookup"><span data-stu-id="76fb5-132">Hashed MAC address: a cryptographically (SHA256) anonymous and unique ID for a machine.</span></span> <span data-ttu-id="76fb5-133">Cette métrique n’est pas publiée.</span><span class="sxs-lookup"><span data-stu-id="76fb5-133">This metric is not published.</span></span>
- <span data-ttu-id="76fb5-134">Répertoire de travail actuel haché.</span><span class="sxs-lookup"><span data-stu-id="76fb5-134">Hashed current working directory.</span></span>

<span data-ttu-id="76fb5-135">La fonctionnalité ne collecte pas les informations personnelles, telles que les noms d’utilisateurs et les adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="76fb5-135">The feature doesn't collect personal data, such as usernames or email addresses.</span></span> <span data-ttu-id="76fb5-136">Elle n’analyse pas votre code et n’extrait pas de données sensibles au niveau du projet, telles que le nom, le dépôt ou l’auteur.</span><span class="sxs-lookup"><span data-stu-id="76fb5-136">It doesn't scan your code and doesn't extract sensitive project-level data, such as name, repo, or author.</span></span> <span data-ttu-id="76fb5-137">Les données sont envoyées en toute sécurité à des serveurs Microsoft à l’aide de la technologie [Microsoft Azure Application Insights](https://azure.microsoft.com/services/application-insights/), stockées à un emplacement dont l’accès est strictement limité et publiées conformément à des contrôles de sécurité stricts à partir de systèmes [Azure Storage](https://azure.microsoft.com/services/storage/) sécurisés.</span><span class="sxs-lookup"><span data-stu-id="76fb5-137">The data is sent securely to Microsoft servers using [Microsoft Azure Application Insights](https://azure.microsoft.com/services/application-insights/) technology, held under restricted access, and published under strict security controls from secure [Azure Storage](https://azure.microsoft.com/services/storage/) systems.</span></span>

<span data-ttu-id="76fb5-138">Nous souhaitons savoir comment vous utilisez les outils et s’ils fonctionnent correctement, et non ce que vous créez avec les outils.</span><span class="sxs-lookup"><span data-stu-id="76fb5-138">We want to know how the tools are used and if they're working well, not what you're building with the tools.</span></span> <span data-ttu-id="76fb5-139">Si vous pensez que la fonctionnalité de télémétrie collecte des données sensibles ou que nous gérons des données de manière non sécurisée ou incorrecte, [soumettez un problème dans la page des problèmes du dépôt dotnet/cli](https://github.com/dotnet/cli/issues) afin que nous effectuions un examen plus approfondi.</span><span class="sxs-lookup"><span data-stu-id="76fb5-139">If you suspect that the telemetry is collecting sensitive data or that we're insecurely or inappropriately handling data, [file an issue in the dotnet/cli repo issues](https://github.com/dotnet/cli/issues) for investigation.</span></span>

## <a name="published-data"></a><span data-ttu-id="76fb5-140">Données publiées</span><span class="sxs-lookup"><span data-stu-id="76fb5-140">Published data</span></span>

<span data-ttu-id="76fb5-141">Les données publiées sont disponibles tous les trimestres et sont répertoriées dans la page [.NET Core SDK Usage Data](https://github.com/dotnet/core/blob/master/release-notes/cli-usage-data.md) (Données d’utilisation du SDK .NET Core).</span><span class="sxs-lookup"><span data-stu-id="76fb5-141">Published data is available quarterly and are listed at [.NET Core SDK Usage Data](https://github.com/dotnet/core/blob/master/release-notes/cli-usage-data.md).</span></span> <span data-ttu-id="76fb5-142">Les colonnes d’un fichier de données sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="76fb5-142">The columns of a data file are:</span></span>
- <span data-ttu-id="76fb5-143">Horodateur</span><span class="sxs-lookup"><span data-stu-id="76fb5-143">Timestamp</span></span>
- <span data-ttu-id="76fb5-144">Occurrences&#8224;</span><span class="sxs-lookup"><span data-stu-id="76fb5-144">Occurrences&#8224;</span></span>
- <span data-ttu-id="76fb5-145">Commande</span><span class="sxs-lookup"><span data-stu-id="76fb5-145">Command</span></span>
- <span data-ttu-id="76fb5-146">Geography&#8225;</span><span class="sxs-lookup"><span data-stu-id="76fb5-146">Geography&#8225;</span></span>
- <span data-ttu-id="76fb5-147">OSFamily</span><span class="sxs-lookup"><span data-stu-id="76fb5-147">OSFamily</span></span>
- <span data-ttu-id="76fb5-148">RuntimeID</span><span class="sxs-lookup"><span data-stu-id="76fb5-148">RuntimeID</span></span>
- <span data-ttu-id="76fb5-149">OSVersion</span><span class="sxs-lookup"><span data-stu-id="76fb5-149">OSVersion</span></span>
- <span data-ttu-id="76fb5-150">SDKVersion</span><span class="sxs-lookup"><span data-stu-id="76fb5-150">SDKVersion</span></span>

<span data-ttu-id="76fb5-151">&#8224;La colonne *Occurrences* totalise le nombre d’utilisations de la commande concernée pour les métriques de la ligne donnée le jour indiqué.</span><span class="sxs-lookup"><span data-stu-id="76fb5-151">&#8224;The *Occurrences* column displays the aggregate count of that command's use for that row's metrics that day.</span></span> 

<span data-ttu-id="76fb5-152">&#8225;En règle générale, la colonne *Geography* affiche le nom d’un pays.</span><span class="sxs-lookup"><span data-stu-id="76fb5-152">&#8225;Typically, the *Geography* column displays the name of a country.</span></span> <span data-ttu-id="76fb5-153">Dans certains cas, le continent Antarctica (Antarctique) apparaît dans cette colonne si .NET Core est utilisé dans ce continent ou que les données de localisation sont incorrectes.</span><span class="sxs-lookup"><span data-stu-id="76fb5-153">In some cases, the continent of Antarctica appears in this column, either due to researchers using .NET Core in Antarctica or incorrect location data.</span></span>

### <a name="example"></a><span data-ttu-id="76fb5-154">Exemple</span><span class="sxs-lookup"><span data-stu-id="76fb5-154">Example</span></span>

| <span data-ttu-id="76fb5-155">Horodateur</span><span class="sxs-lookup"><span data-stu-id="76fb5-155">Timestamp</span></span>      | <span data-ttu-id="76fb5-156">Occurrences</span><span class="sxs-lookup"><span data-stu-id="76fb5-156">Occurrences</span></span> | <span data-ttu-id="76fb5-157">Commande</span><span class="sxs-lookup"><span data-stu-id="76fb5-157">Command</span></span> | <span data-ttu-id="76fb5-158">Geography</span><span class="sxs-lookup"><span data-stu-id="76fb5-158">Geography</span></span> | <span data-ttu-id="76fb5-159">OSFamily</span><span class="sxs-lookup"><span data-stu-id="76fb5-159">OSFamily</span></span> | <span data-ttu-id="76fb5-160">RuntimeID</span><span class="sxs-lookup"><span data-stu-id="76fb5-160">RuntimeID</span></span>     | <span data-ttu-id="76fb5-161">OSVersion</span><span class="sxs-lookup"><span data-stu-id="76fb5-161">OSVersion</span></span> | <span data-ttu-id="76fb5-162">SDKVersion</span><span class="sxs-lookup"><span data-stu-id="76fb5-162">SDKVersion</span></span> |
| -------------- | ----------- | ------- | --------- | -------- | ------------- | --------- | ---------- |
| <span data-ttu-id="76fb5-163">4/16/2017 0:00</span><span class="sxs-lookup"><span data-stu-id="76fb5-163">4/16/2017 0:00</span></span> | <span data-ttu-id="76fb5-164">8</span><span class="sxs-lookup"><span data-stu-id="76fb5-164">8</span></span>           | <span data-ttu-id="76fb5-165">run</span><span class="sxs-lookup"><span data-stu-id="76fb5-165">run</span></span>     | <span data-ttu-id="76fb5-166">Uganda</span><span class="sxs-lookup"><span data-stu-id="76fb5-166">Uganda</span></span>    | <span data-ttu-id="76fb5-167">Darwin</span><span class="sxs-lookup"><span data-stu-id="76fb5-167">Darwin</span></span>   | <span data-ttu-id="76fb5-168">osx.10.12-x64</span><span class="sxs-lookup"><span data-stu-id="76fb5-168">osx.10.12-x64</span></span> | <span data-ttu-id="76fb5-169">10.12</span><span class="sxs-lookup"><span data-stu-id="76fb5-169">10.12</span></span>     | <span data-ttu-id="76fb5-170">1.0.1</span><span class="sxs-lookup"><span data-stu-id="76fb5-170">1.0.1</span></span>      |

### <a name="datasets"></a><span data-ttu-id="76fb5-171">Groupes de données</span><span class="sxs-lookup"><span data-stu-id="76fb5-171">Datasets</span></span>

[<span data-ttu-id="76fb5-172">2016 - T3</span><span class="sxs-lookup"><span data-stu-id="76fb5-172">2016 - Q3</span></span>](https://dotnetcli.blob.core.windows.net/usagedata/dotnet-cli-usage-2016-q3.tsv)  
[<span data-ttu-id="76fb5-173">2016 - T4</span><span class="sxs-lookup"><span data-stu-id="76fb5-173">2016 - Q4</span></span>](https://dotnetcli.blob.core.windows.net/usagedata/dotnet-cli-usage-2016-q4.tsv)  
[<span data-ttu-id="76fb5-174">2017 - T1</span><span class="sxs-lookup"><span data-stu-id="76fb5-174">2017 - Q1</span></span>](https://dotnetcli.blob.core.windows.net/usagedata/dotnet-cli-usage-2017-q1.tsv)  
[<span data-ttu-id="76fb5-175">2017 - T2</span><span class="sxs-lookup"><span data-stu-id="76fb5-175">2017 - Q2</span></span>](https://dotnetcli.blob.core.windows.net/usagedata/dotnet-cli-usage-2017-q2.tsv)

<span data-ttu-id="76fb5-176">Des jeux de données supplémentaires sont publiés à l’aide d’un format d’URL standard.</span><span class="sxs-lookup"><span data-stu-id="76fb5-176">Additional datasets are posted using a standard URL format.</span></span> <span data-ttu-id="76fb5-177">Remplacez `<YEAR>` par l’année, et `<QUARTER>` par le trimestre de l’année (utilisez `1`, `2`, `3` ou `4`).</span><span class="sxs-lookup"><span data-stu-id="76fb5-177">Replace `<YEAR>` with the year and replace `<QUARTER>` with the quarter of the year (use `1`, `2`, `3`, or `4`).</span></span> <span data-ttu-id="76fb5-178">Les fichiers sont au format *TSV* (valeurs séparées par une tabulation).</span><span class="sxs-lookup"><span data-stu-id="76fb5-178">The files are in tab-separated values (*TSV*) format.</span></span> 

```
https://dotnetcli.blob.core.windows.net/usagedata/dotnet-cli-usage-<YEAR>-q<QUARTER>.tsv
```

## <a name="license"></a><span data-ttu-id="76fb5-179">Licence</span><span class="sxs-lookup"><span data-stu-id="76fb5-179">License</span></span>

<span data-ttu-id="76fb5-180">La distribution Microsoft de .NET Core est concédée sous licence avec le [CLUF de la BIBLIOTHÈQUE .NET MICROSOFT](https://aka.ms/dotnet-core-eula).</span><span class="sxs-lookup"><span data-stu-id="76fb5-180">The Microsoft distribution of .NET Core is licensed with the [MICROSOFT .NET LIBRARY EULA](https://aka.ms/dotnet-core-eula).</span></span> <span data-ttu-id="76fb5-181">Cette licence comprend la section « DATA » qui permet d’activer la télémétrie (ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="76fb5-181">This license includes the "DATA" section to enable telemetry (shown below).</span></span>

<span data-ttu-id="76fb5-182">Les [packages NuGet .NET](https://www.nuget.org/profiles/dotnetframework) utilisent la même licence, mais ne permettent pas la télémétrie (voir la section [Portée](#scope)).</span><span class="sxs-lookup"><span data-stu-id="76fb5-182">[.NET NuGet packages](https://www.nuget.org/profiles/dotnetframework) use the same license but don't enable telemetry (see [Scope](#scope)).</span></span>

> 2. <span data-ttu-id="76fb5-183">DONNÉES.</span><span class="sxs-lookup"><span data-stu-id="76fb5-183">DATA.</span></span> <span data-ttu-id="76fb5-184">Le logiciel peut collecter des informations sur vous et votre utilisation du logiciel et les envoyer à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="76fb5-184">The software may collect information about you and your use of the software, and send that to Microsoft.</span></span> <span data-ttu-id="76fb5-185">Microsoft peut utiliser ces informations pour améliorer ses produits et services.</span><span class="sxs-lookup"><span data-stu-id="76fb5-185">Microsoft may use this information to improve our products and services.</span></span> <span data-ttu-id="76fb5-186">Pour plus d’informations sur la collecte et l’utilisation des données, consultez la documentation d’aide et la déclaration de confidentialité à l’adresse http://go.microsoft.com/fwlink/?LinkId=528096.</span><span class="sxs-lookup"><span data-stu-id="76fb5-186">You can learn more about data collection and use in the help documentation and the privacy statement at http://go.microsoft.com/fwlink/?LinkId=528096.</span></span> <span data-ttu-id="76fb5-187">Votre utilisation du logiciel est considérée comme votre acceptation de ces pratiques.</span><span class="sxs-lookup"><span data-stu-id="76fb5-187">Your use of the software operates as your consent to these practices.</span></span>

## <a name="disclosure"></a><span data-ttu-id="76fb5-188">Divulgation d’informations</span><span class="sxs-lookup"><span data-stu-id="76fb5-188">Disclosure</span></span>

<span data-ttu-id="76fb5-189">Les outils CLI .NET Core affichent le texte suivant quand vous exécutez une commande pour la première fois (par exemple, `dotnet restore`).</span><span class="sxs-lookup"><span data-stu-id="76fb5-189">The .NET Core CLI Tools display the following text when you first run one of the commands (for example, `dotnet restore`).</span></span> <span data-ttu-id="76fb5-190">Le texte peut varier légèrement selon la version du SDK que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="76fb5-190">Text may vary slightly depending on the version of the SDK you're running.</span></span> <span data-ttu-id="76fb5-191">Lors de cette première exécution, Microsoft vous informe sur la collecte de données.</span><span class="sxs-lookup"><span data-stu-id="76fb5-191">This "first run" experience is how Microsoft notifies you about data collection.</span></span>

```console
Welcome to .NET Core!
---------------------
Learn more about .NET Core @ https://aka.ms/dotnet-docs. Use dotnet --help to see available commands or go to https://aka.ms/dotnet-cli-docs.
 
Telemetry
--------------
The .NET Core tools collect usage data in order to improve your experience. The data is anonymous and does not include command-line arguments. The data is collected by Microsoft and shared with the community.
You can opt out of telemetry by setting a DOTNET_CLI_TELEMETRY_OPTOUT environment variable to 1 using your favorite shell.
You can read more about .NET Core tools telemetry @ https://aka.ms/dotnet-cli-telemetry.
```

## <a name="see-also"></a><span data-ttu-id="76fb5-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76fb5-192">See also</span></span>

<span data-ttu-id="76fb5-193">[What we've learned from .NET Core SDK Telemetry](https://blogs.msdn.microsoft.com/dotnet/2017/07/21/what-weve-learned-from-net-core-sdk-telemetry/) (Enseignements tirés de la fonctionnalité de télémétrie du SDK .NET Core)</span><span class="sxs-lookup"><span data-stu-id="76fb5-193">[What we've learned from .NET Core SDK Telemetry](https://blogs.msdn.microsoft.com/dotnet/2017/07/21/what-weve-learned-from-net-core-sdk-telemetry/)</span></span>  
<span data-ttu-id="76fb5-194">[Source de référence de télémétrie (dotnet/cli repo ; branche release/2.0.0)](https://github.com/dotnet/cli/tree/release/2.0.0/src/dotnet/Telemetry) </span><span class="sxs-lookup"><span data-stu-id="76fb5-194">[Telemetry reference source (dotnet/cli repo; release/2.0.0 branch)](https://github.com/dotnet/cli/tree/release/2.0.0/src/dotnet/Telemetry) </span></span>  
<span data-ttu-id="76fb5-195">[.NET Core SDK Usage Data](https://github.com/dotnet/core/blob/master/release-notes/cli-usage-data.md) (Données d’utilisation du SDK .NET Core)</span><span class="sxs-lookup"><span data-stu-id="76fb5-195">[.NET Core SDK Usage Data](https://github.com/dotnet/core/blob/master/release-notes/cli-usage-data.md)</span></span>
