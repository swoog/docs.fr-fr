---
title: Utiliser le pack de compatibilité Windows pour porter du code vers .NET Core
description: Découvrez le pack de compatibilité Windows et comment l’utiliser pour déplacer du code .NET Framework existant vers .NET Core
author: terrajobst
ms.date: 11/13/2017
ms.custom: seodec18
ms.openlocfilehash: 0a409c953ce38ed4c2959adaf4de9d3730ce37f4
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169935"
---
# <a name="use-the-windows-compatibility-pack-to-port-code-to-net-core"></a><span data-ttu-id="dd173-103">Utiliser le pack de compatibilité Windows pour porter du code vers .NET Core</span><span class="sxs-lookup"><span data-stu-id="dd173-103">Use the Windows Compatibility Pack to port code to .NET Core</span></span>

<span data-ttu-id="dd173-104">Certains des problèmes courants que l’on peut rencontrer en portant du code vers .NET Core sont des dépendances à des API et à des technologies propres à .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dd173-104">Some of the most common issues found when porting existing code to .NET Core are dependencies on APIs and technologies that are only found in the .NET Framework.</span></span> <span data-ttu-id="dd173-105">Le *pack de compatibilité Windows* comporte la plupart de ces technologies, ce qui facilite la création d’applications .NET Core et de bibliothèques .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="dd173-105">The *Windows Compatibility Pack* provides many of these technologies, so it's much easier to build .NET Core applications and .NET Standard libraries.</span></span>

<span data-ttu-id="dd173-106">Ce package est une [extension logique de.NET Standard 2.0](../whats-new/dotnet-core-2-0.md#api-changes-and-library-support) qui augmente considérablement l’ensemble d’API et le code existant est compilé sans presque aucune modification.</span><span class="sxs-lookup"><span data-stu-id="dd173-106">This package is a logical [extension of .NET Standard 2.0](../whats-new/dotnet-core-2-0.md#api-changes-and-library-support) that significantly increases API set and existing code compiles with almost no modifications.</span></span> <span data-ttu-id="dd173-107">Toutefois, pour respecter l’engagement de .NET Standard (« il s’agit de l’ensemble d’API fourni par toutes les implémentations .NET »), cela ne comprend pas les technologies qui ne peuvent pas fonctionner sur toutes les plateformes, telles que le Registre, WMI (Windows Management Instrumentation), ou les API d’émission de réflexion.</span><span class="sxs-lookup"><span data-stu-id="dd173-107">But in order to keep the promise of .NET Standard ("it is the set of APIs that all .NET implementations provide"), this didn't include technologies that can't work across all platforms, such as registry, Windows Management Instrumentation (WMI), or reflection emit APIs.</span></span>

<span data-ttu-id="dd173-108">Le *pack de compatibilité Windows* repose sur .NET Standard et permet d’accéder aux technologies Windows uniquement.</span><span class="sxs-lookup"><span data-stu-id="dd173-108">The *Windows Compatibility Pack* sits on top of .NET Standard and provides access to technologies that are Windows only.</span></span> <span data-ttu-id="dd173-109">Il est particulièrement utile pour les clients qui veulent passer à .NET Core, mais envisagent de rester sur Windows pour commencer.</span><span class="sxs-lookup"><span data-stu-id="dd173-109">It's especially useful for customers that want to move to .NET Core but plan to stay on Windows as a first step.</span></span> <span data-ttu-id="dd173-110">Dans ce scénario, le fait de ne pas pouvoir utiliser les technologies Windows uniquement est juste un obstacle à la migration sans aucun avantage en matière d’architecture.</span><span class="sxs-lookup"><span data-stu-id="dd173-110">In that scenario, not being able to use Windows-only technologies is only a migration hurdle with zero architectural benefits.</span></span>

## <a name="package-contents"></a><span data-ttu-id="dd173-111">Contenu du package</span><span class="sxs-lookup"><span data-stu-id="dd173-111">Package contents</span></span>

<span data-ttu-id="dd173-112">Le *pack de compatibilité Windows* est fourni via le package NuGet [Microsoft.Windows.Compatibility](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) et peut être référencé à partir de projets ciblant .NET Core ou .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="dd173-112">The *Windows Compatibility Pack* is provided via the NuGet Package [Microsoft.Windows.Compatibility](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) and can be referenced from projects targeting .NET Core or .NET Standard.</span></span>

<span data-ttu-id="dd173-113">Il fournit environ 20 000 API, dont des API Windows uniquement ainsi des API multiplateformes des domaines technologiques suivants :</span><span class="sxs-lookup"><span data-stu-id="dd173-113">It provides about 20,000 APIs, including Windows-only as well as cross-platform APIs from the following technology areas:</span></span>

* <span data-ttu-id="dd173-114">Pages de codes</span><span class="sxs-lookup"><span data-stu-id="dd173-114">Code Pages</span></span>
* <span data-ttu-id="dd173-115">CodeDom</span><span class="sxs-lookup"><span data-stu-id="dd173-115">CodeDom</span></span>
* <span data-ttu-id="dd173-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="dd173-116">Configuration</span></span>
* <span data-ttu-id="dd173-117">Services d'annuaire</span><span class="sxs-lookup"><span data-stu-id="dd173-117">Directory Services</span></span>
* <span data-ttu-id="dd173-118">Dessin</span><span class="sxs-lookup"><span data-stu-id="dd173-118">Drawing</span></span>
* <span data-ttu-id="dd173-119">ODBC</span><span class="sxs-lookup"><span data-stu-id="dd173-119">ODBC</span></span>
* <span data-ttu-id="dd173-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="dd173-120">Permissions</span></span>
* <span data-ttu-id="dd173-121">Ports</span><span class="sxs-lookup"><span data-stu-id="dd173-121">Ports</span></span>
* <span data-ttu-id="dd173-122">Listes de contrôle d’accès Windows</span><span class="sxs-lookup"><span data-stu-id="dd173-122">Windows Access Control Lists (ACL)</span></span>
* <span data-ttu-id="dd173-123">Windows Communication Foundation (WCF)</span><span class="sxs-lookup"><span data-stu-id="dd173-123">Windows Communication Foundation (WCF)</span></span>
* <span data-ttu-id="dd173-124">Chiffrement Windows</span><span class="sxs-lookup"><span data-stu-id="dd173-124">Windows Cryptography</span></span>
* <span data-ttu-id="dd173-125">Journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="dd173-125">Windows EventLog</span></span>
* <span data-ttu-id="dd173-126">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="dd173-126">Windows Management Instrumentation (WMI)</span></span>
* <span data-ttu-id="dd173-127">Compteurs de performances Windows</span><span class="sxs-lookup"><span data-stu-id="dd173-127">Windows Performance Counters</span></span>
* <span data-ttu-id="dd173-128">Registre Windows</span><span class="sxs-lookup"><span data-stu-id="dd173-128">Windows Registry</span></span>
* <span data-ttu-id="dd173-129">Mise en cache Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="dd173-129">Windows Runtime Caching</span></span>
* <span data-ttu-id="dd173-130">services Windows</span><span class="sxs-lookup"><span data-stu-id="dd173-130">Windows Services</span></span>

<span data-ttu-id="dd173-131">Pour plus d’informations, consultez la [spécification du pack de compatibilité](https://github.com/dotnet/designs/blob/master/accepted/compat-pack/compat-pack.md).</span><span class="sxs-lookup"><span data-stu-id="dd173-131">For more information, see the [spec of the compatibility pack](https://github.com/dotnet/designs/blob/master/accepted/compat-pack/compat-pack.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="dd173-132">Prise en main</span><span class="sxs-lookup"><span data-stu-id="dd173-132">Get started</span></span>

1. <span data-ttu-id="dd173-133">Avant le portage, veillez à examiner le [processus de portage](index.md).</span><span class="sxs-lookup"><span data-stu-id="dd173-133">Before porting, make sure to take a look at the [Porting Process](index.md).</span></span>

2. <span data-ttu-id="dd173-134">Lors du portage du code existant vers .NET Core ou .NET Standard, installez le package NuGet [Microsoft.Windows.Compatibility](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span><span class="sxs-lookup"><span data-stu-id="dd173-134">When porting existing code to .NET Core or .NET Standard, install the NuGet package [Microsoft.Windows.Compatibility](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

3. <span data-ttu-id="dd173-135">Si vous souhaitez rester sur Windows, vous êtes prêt.</span><span class="sxs-lookup"><span data-stu-id="dd173-135">If you want to stay on Windows, you're all set.</span></span>

4. <span data-ttu-id="dd173-136">Si vous souhaitez exécuter l’application .NET Core ou la bibliothèque .NET Standard sur Linux ou macOS, utilisez [l’analyseur d’API](https://blogs.msdn.microsoft.com/dotnet/2017/10/31/introducing-api-analyzer/) pour trouver l’usage des API qui ne fonctionnent pas sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="dd173-136">If you want to run the .NET Core application or .NET Standard library on Linux or macOS, use the [API Analyzer](https://blogs.msdn.microsoft.com/dotnet/2017/10/31/introducing-api-analyzer/) to find usage of APIs that won't work cross-platform.</span></span>

5. <span data-ttu-id="dd173-137">Supprimez les usages de ces API, remplacez-les par des alternatives multiplateformes ou protégez-les à l’aide d’une vérification de la plateforme, par exemple :</span><span class="sxs-lookup"><span data-stu-id="dd173-137">Either remove the usages of those APIs, replace them with cross-platform alternatives, or guard them using a platform check, like:</span></span>

    ```csharp
    private static string GetLoggingPath()
    {
        // Verify the code is running on Windows.
        if (RuntimeInformation.IsOSPlatform(OSPlatform.Windows))
        {
            using (var key = Registry.CurrentUser.OpenSubKey(@"Software\Fabrikam\AssetManagement"))
            {
                if (key?.GetValue("LoggingDirectoryPath") is string configuredPath)
                    return configuredPath;
            }
        }

        // This is either not running on Windows or no logging path was configured,
        // so just use the path for non-roaming user-specific data files.
        var appDataPath = Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData);
        return Path.Combine(appDataPath, "Fabrikam", "AssetManagement", "Logging");
    }
    ```

<span data-ttu-id="dd173-138">Pour obtenir une démonstration, regardez la [vidéo de Channel 9 sur le pack de compatibilité Windows](https://channel9.msdn.com/Events/Connect/2017/T123).</span><span class="sxs-lookup"><span data-stu-id="dd173-138">For a demo, check out the [Channel 9 video of the Windows Compatibility Pack](https://channel9.msdn.com/Events/Connect/2017/T123).</span></span>

