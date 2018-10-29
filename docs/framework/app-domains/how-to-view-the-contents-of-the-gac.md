---
title: Guide pratique pour visualiser le contenu du Global Assembly Cache
ms.date: 03/30/2017
helpviewer_keywords:
- assemblies [.NET Framework], global assembly cache
- global assembly cache, viewing contents
- viewing assemblies in global assembly cache
- Gacutil.exe
- strong-named assemblies, global assembly cache
- GAC (global assembly cache), viewing contents
- list of assemblies in global assembly cache
- Global Assembly Cache tool
ms.assetid: c5f786a0-969b-4f14-9f02-e77c3384d9af
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0375c835dea8984db34d3d1e24b2876fb9af8337
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181444"
---
# <a name="how-to-view-the-contents-of-the-global-assembly-cache"></a><span data-ttu-id="c0cd2-102">Guide pratique pour visualiser le contenu du Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="c0cd2-102">How to: View the contents of the global assembly cache</span></span>

<span data-ttu-id="c0cd2-103">Utilisez [l’outil Global Assembly Cache (Gacutil.exe)](../tools/gacutil-exe-gac-tool.md) pour visualiser le contenu du Global Assembly Cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="c0cd2-103">Use the [global assembly cache tool (gacutil.exe)](../tools/gacutil-exe-gac-tool.md) to view the contents of the global assembly cache (GAC).</span></span>

## <a name="view-the-assemblies-in-the-gac"></a><span data-ttu-id="c0cd2-104">Afficher les assemblys dans le GAC</span><span class="sxs-lookup"><span data-stu-id="c0cd2-104">View the assemblies in the GAC</span></span>

<span data-ttu-id="c0cd2-105">Pour afficher une liste des assemblys dans leGlobal Assembly Cache, ouvrez [l’invite de commandes développeur pour Visual Studio](../tools/developer-command-prompt-for-vs.md), puis entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c0cd2-105">To view a list of the assemblies in the global assembly cache, open [Developer Command Prompt for Visual Studio](../tools/developer-command-prompt-for-vs.md), and then enter the following command:</span></span>

```shell
gacutil -l
```

<span data-ttu-id="c0cd2-106">- ou -</span><span class="sxs-lookup"><span data-stu-id="c0cd2-106">-or-</span></span>

```shell
gacutil /l
```

> [!NOTE]
> <span data-ttu-id="c0cd2-107">Dans les versions antérieures du .NET Framework, l’extension du shell Windows [Shfusion.dll](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/34149zk3(v=vs.100)) vous permettait d’afficher le Global Assembly Cache dans l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c0cd2-107">In earlier versions of the .NET Framework, the [Shfusion.dll](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/34149zk3(v=vs.100)) Windows shell extension enabled you to view the global assembly cache in File Explorer.</span></span> <span data-ttu-id="c0cd2-108">À partir de [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], Shfusion.dll est obsolète.</span><span class="sxs-lookup"><span data-stu-id="c0cd2-108">Beginning with the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], Shfusion.dll is obsolete.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0cd2-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0cd2-109">See also</span></span>

- [<span data-ttu-id="c0cd2-110">Utilisation d’assemblys et du Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="c0cd2-110">Working with Assemblies and the Global Assembly Cache</span></span>](working-with-assemblies-and-the-gac.md)
- [<span data-ttu-id="c0cd2-111">Gacutil.exe (outil Global Assembly Cache)</span><span class="sxs-lookup"><span data-stu-id="c0cd2-111">Gacutil.exe (Global Assembly Cache Tool)</span></span>](../tools/gacutil-exe-gac-tool.md)