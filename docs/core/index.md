---
title: Guide .NET Core
description: .NET Core est une implémentation modulaire à hautes performances de .NET pour la création d’applications Windows, Linux et Mac. Découvrez .NET Core pour démarrer.
author: richlander
ms.author: mairaw
ms.date: 08/01/2018
ms.custom: updateeachrelease
ms.openlocfilehash: cfa7c27871204b808c9d753a970d5abb907a183e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512839"
---
# <a name="net-core-guide"></a><span data-ttu-id="88681-104">Guide .NET Core</span><span class="sxs-lookup"><span data-stu-id="88681-104">.NET Core Guide</span></span>

<span data-ttu-id="88681-105">[.NET Core](about.md) est une plateforme de développement généraliste [open source](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT) qui est tenue à jour par Microsoft et la communauté .NET sur [GitHub](https://github.com/dotnet/core).</span><span class="sxs-lookup"><span data-stu-id="88681-105">[.NET Core](about.md) is an [open-source](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT) general-purpose development platform maintained by Microsoft and the .NET community on [GitHub](https://github.com/dotnet/core).</span></span> <span data-ttu-id="88681-106">Cette multiplateforme prend en charge Windows, macOS et Linux. Elle peut être utilisée dans des scénarios d’appareil, de cloud et d’applications IoT.</span><span class="sxs-lookup"><span data-stu-id="88681-106">It's cross-platform, supporting Windows, macOS and Linux, and can be used in device, cloud, and IoT applications.</span></span>

<span data-ttu-id="88681-107">Consultez [À propos de .NET Core](about.md) pour en savoir plus sur .NET Core, notamment ses caractéristiques, les langues et frameworks pris en charge et les API clés.</span><span class="sxs-lookup"><span data-stu-id="88681-107">See [About .NET Core](about.md) to learn more about .NET Core, including its characteristics, supported languages and frameworks, and key APIs.</span></span>

<span data-ttu-id="88681-108">Consultez les [Tutoriels .NET Core](tutorials/index.md) pour apprendre à créer une application .NET Core simple.</span><span class="sxs-lookup"><span data-stu-id="88681-108">Check out [.NET Core Tutorials](tutorials/index.md) to learn how to create a simple .NET Core application.</span></span> <span data-ttu-id="88681-109">Il suffit de quelques minutes pour créer votre première application et la rendre opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="88681-109">It only takes a few minutes to get your first app up and running.</span></span> <span data-ttu-id="88681-110">Si vous souhaitez tester .NET Core dans votre navigateur, consultez le démarrage rapide [Nombres en C#](https://docs.microsoft.com/dotnet/csharp/quick-starts/hello-world).</span><span class="sxs-lookup"><span data-stu-id="88681-110">If you want to try .NET Core in you browser, look at the [Numbers in C#](https://docs.microsoft.com/dotnet/csharp/quick-starts/hello-world) quickstart.</span></span>

## <a name="download-net-core-21"></a><span data-ttu-id="88681-111">Télécharger .NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="88681-111">Download .NET Core 2.1</span></span>

<span data-ttu-id="88681-112">Téléchargez le [SDK .NET Core 2.1](https://www.microsoft.com/net/download) pour tester .NET Core sur votre ordinateur Windows, macOS ou Linux.</span><span class="sxs-lookup"><span data-stu-id="88681-112">Download the [.NET Core  2.1 SDK](https://www.microsoft.com/net/download) to try .NET Core on your Windows, macOS, or Linux machine.</span></span> <span data-ttu-id="88681-113">Visitez [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) si vous préférez utiliser des conteneurs Docker.</span><span class="sxs-lookup"><span data-stu-id="88681-113">Visit [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) if you prefer to use Docker containers.</span></span>

<span data-ttu-id="88681-114">Toutes les versions de .NET Core sont disponibles sur [Téléchargements de .NET Core](https://www.microsoft.com/net/download/archives) si vous recherchez une autre version de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="88681-114">All .NET Core versions are available at [.NET Core Downloads](https://www.microsoft.com/net/download/archives) if you're looking for another .NET Core version.</span></span>

## <a name="net-core-21"></a><span data-ttu-id="88681-115">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="88681-115">.NET Core 2.1</span></span>

<span data-ttu-id="88681-116">La version la plus récente est [.NET Core 2.1](whats-new/dotnet-core-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="88681-116">The latest version is [.NET Core 2.1](whats-new/dotnet-core-2-1.md).</span></span> <span data-ttu-id="88681-117">Les nouvelles fonctionnalités incluent : outils généraux, API haute performance (comme <xref:System.Span%601?displayProperty=nameWithType>), compilation JIT à plusieurs niveaux, améliorations des performances de [génération](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) et du [runtime](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/), et prise en charge d’Alpine et d’ARM32.</span><span class="sxs-lookup"><span data-stu-id="88681-117">New features include: global tools, high-performance APIs (such as <xref:System.Span%601?displayProperty=nameWithType>), tiered JIT compilation, [build](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) and [runtime performance improvements](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/), and support for Alpine and ARM32.</span></span>

## <a name="create-your-first-application"></a><span data-ttu-id="88681-118">Créer votre première application</span><span class="sxs-lookup"><span data-stu-id="88681-118">Create your first application</span></span>

<span data-ttu-id="88681-119">Après avoir installé le SDK .NET Core, ouvrez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="88681-119">After installing the .NET Core SDK, open a command prompt.</span></span> <span data-ttu-id="88681-120">Tapez les commandes `dotnet` suivantes pour créer et exécuter une application C#.</span><span class="sxs-lookup"><span data-stu-id="88681-120">Type the following `dotnet` commands to create and run a C# application.</span></span>

```console
dotnet new console
dotnet run
```

<span data-ttu-id="88681-121">Vous devez voir la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="88681-121">You should see the following output:</span></span>

```console
Hello World!
```

## <a name="support"></a><span data-ttu-id="88681-122">Assistance</span><span class="sxs-lookup"><span data-stu-id="88681-122">Support</span></span>

<span data-ttu-id="88681-123">.NET Core est [pris en charge par Microsoft](https://www.microsoft.com/net/support/policy) sur Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="88681-123">.NET Core is [supported by Microsoft](https://www.microsoft.com/net/support/policy), on Windows, macOS and Linux.</span></span> <span data-ttu-id="88681-124">La sécurité et la qualité sont mises à jour plusieurs fois par an, en général, tous les mois.</span><span class="sxs-lookup"><span data-stu-id="88681-124">It's updated for security and quality several times a year, typically monthly.</span></span>

<span data-ttu-id="88681-125">Les distributions binaires .NET Core sont générées et testées sur des serveurs managés par Microsoft dans Azure et elles sont prises en charge comme tous les produits Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88681-125">.NET Core binary distributions are built and tested on Microsoft-maintained servers in Azure and supported just like any Microsoft product.</span></span>

<span data-ttu-id="88681-126">[Red Hat prend en charge .NET Core](http://redhatloves.net/) sur Red Hat Enterprise Linux (RHEL).</span><span class="sxs-lookup"><span data-stu-id="88681-126">[Red Hat supports .NET Core](http://redhatloves.net/) on Red Hat Enterprise Linux (RHEL).</span></span> <span data-ttu-id="88681-127">Red Hat génère .NET Core à partir de la source et le rend disponible dans les [collections logicielles Red Hat](https://developers.redhat.com/products/softwarecollections/overview/).</span><span class="sxs-lookup"><span data-stu-id="88681-127">Red Hat builds .NET Core from source and makes it available in the [Red Hat Software Collections](https://developers.redhat.com/products/softwarecollections/overview/).</span></span> <span data-ttu-id="88681-128">Red Hat et Microsoft collaborent pour s’assurer que .NET Core fonctionne correctement sur RHEL.</span><span class="sxs-lookup"><span data-stu-id="88681-128">Red Hat and Microsoft collaborate to ensure that .NET Core works well on RHEL.</span></span>