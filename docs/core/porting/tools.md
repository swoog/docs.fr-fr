---
title: Outils de portage vers .NET Core
description: Découvrez certains des outils que vous pouvez utiliser pour effectuer un portage vers .NET Core
author: cartermp
ms.author: mairaw
ms.date: 12/07/2018
ms.openlocfilehash: 88e3edb0442b3326a77323fe4b6396f3eb1ca767
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904869"
---
# <a name="tools-to-help-with-porting-to-net-core"></a><span data-ttu-id="bed20-103">Outils facilitant le portage vers .NET Core</span><span class="sxs-lookup"><span data-stu-id="bed20-103">Tools to help with porting to .NET Core</span></span>

<span data-ttu-id="bed20-104">Les outils présentés dans cet article peuvent vous être utiles dans le cadre d’un portage :</span><span class="sxs-lookup"><span data-stu-id="bed20-104">You may find the tools listed in this article helpful when porting:</span></span>

* <span data-ttu-id="bed20-105">[.NET Portability Analyzer](../../standard/analyzers/portability-analyzer.md) : chaîne d’outils capable de générer un rapport sur la portabilité de votre code entre .NET Framework et .NET Core :  En tant qu’[outil en ligne de commande](https://github.com/Microsoft/dotnet-apiport/releases) En tant qu’[extension Visual Studio](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b)</span><span class="sxs-lookup"><span data-stu-id="bed20-105">[.NET Portability Analyzer](../../standard/analyzers/portability-analyzer.md), a toolchain that can generate a report of how portable your code is between .NET Framework and .NET Core:  As a [command line tool](https://github.com/Microsoft/dotnet-apiport/releases) As a [Visual Studio Extension](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b)</span></span>
* <span data-ttu-id="bed20-106">[.NET API Analyzer](../../standard/analyzers/api-analyzer.md) : analyseur Roslyn qui découvre les risques potentiels liés à la compatibilité des API C# sur différentes plateformes et détecte les appels aux API dépréciées.</span><span class="sxs-lookup"><span data-stu-id="bed20-106">[.NET API analyzer](../../standard/analyzers/api-analyzer.md) - A Roslyn analyzer that discovers potential compatibility risks for C# APIs on different platforms and detects calls to deprecated APIs.</span></span>

<span data-ttu-id="bed20-107">En outre, vous pouvez essayer de porter des solutions plus petites ou des projets individuels au format de fichier de projet .NET Core avec l’outil [CsprojToVs2017](https://github.com/hvanbakel/CsprojToVs2017).</span><span class="sxs-lookup"><span data-stu-id="bed20-107">Additionally, you can attempt to port smaller solutions or individual projects to the .NET Core project file format with the [CsprojToVs2017](https://github.com/hvanbakel/CsprojToVs2017) tool.</span></span>

> [!WARNING] 
> <span data-ttu-id="bed20-108">CsprojToVs2017 est un outil tiers.</span><span class="sxs-lookup"><span data-stu-id="bed20-108">CsprojToVs2017 is a third-party tool.</span></span> <span data-ttu-id="bed20-109">Il n’existe aucune garantie que cet outil fonctionne pour tous vos projets, et il peut entraîner de légères modifications du comportement dont vous dépendez.</span><span class="sxs-lookup"><span data-stu-id="bed20-109">There is no guarantee that it will work for all of your projects, and it may cause subtle changes in behavior that you depend on.</span></span> <span data-ttu-id="bed20-110">CsprojToVs2017 doit être utilisé comme un _point de départ_ qui automatise les tâches de base pouvant être automatisées.</span><span class="sxs-lookup"><span data-stu-id="bed20-110">CsprojToVs2017 should be used as a _starting point_ that automates the basic things that can be automated.</span></span> <span data-ttu-id="bed20-111">Ce n’est pas une solution garantie pour la migration de formats de fichiers projet.</span><span class="sxs-lookup"><span data-stu-id="bed20-111">It is not a guaranteed solution to migrating project file formats.</span></span>