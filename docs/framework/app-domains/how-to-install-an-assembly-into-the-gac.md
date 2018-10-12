---
title: Installer un assembly dans le GAC
ms.date: 09/20/2018
helpviewer_keywords:
- assemblies [.NET Framework], global assembly cache
- Gacutil.exe
- strong-named assemblies, global assembly cache
- global assembly cache, installing assemblies
- Global Assembly Cache tool
- windows installer, global assembly cache
ms.assetid: a7e6f091-d02c-49ba-b736-7295cb0eb743
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d365ac77fe6cd7fc4fca36705729ec12b06d6830
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46584579"
---
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a><span data-ttu-id="09e05-102">Guide pratique pour installer un assembly dans le Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="09e05-102">How to: Install an assembly into the global assembly cache</span></span>

<span data-ttu-id="09e05-103">Il existe deux façons d'installer un assembly avec nom fort dans le Global Assembly Cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="09e05-103">There are two ways to install a strong-named assembly into the global assembly cache (GAC).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09e05-104">Seuls les assemblys avec noms forts peuvent être installés dans le GAC.</span><span class="sxs-lookup"><span data-stu-id="09e05-104">Only strong-named assemblies can be installed into the GAC.</span></span> <span data-ttu-id="09e05-105">Pour plus d’informations sur la façon de créer un assembly avec un nom fort, consultez [Guide pratique pour signer un assembly avec un nom fort](how-to-sign-an-assembly-with-a-strong-name.md).</span><span class="sxs-lookup"><span data-stu-id="09e05-105">For information about how to create a strong-named assembly, see [How to: Sign an Assembly with a Strong Name](how-to-sign-an-assembly-with-a-strong-name.md).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="09e05-106">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="09e05-106">Windows Installer</span></span>

<span data-ttu-id="09e05-107">[Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache), le moteur d’installation de Windows, est la méthode recommandée pour ajouter des assemblys dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="09e05-107">[Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache), the Windows installation engine, is the recommended way to add assemblies to the global assembly cache.</span></span> <span data-ttu-id="09e05-108">Windows Installer fournit un décompte de références des assemblys dans le Global Assembly Cache, ainsi que d'autres avantages.</span><span class="sxs-lookup"><span data-stu-id="09e05-108">Windows Installer provides reference counting of assemblies in the global assembly cache and other benefits.</span></span> <span data-ttu-id="09e05-109">Vous pouvez utiliser [l’extension WiX Toolset pour Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension) pour créer un package de programme d’installation pour Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="09e05-109">You can use the [WiX Toolset extension for Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension) to create an installer package for Windows Installer.</span></span>

## <a name="global-assembly-cache-tool"></a><span data-ttu-id="09e05-110">Outil Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="09e05-110">Global assembly cache tool</span></span>

<span data-ttu-id="09e05-111">Vous pouvez utiliser [l’outil Global Assembly Cache (Gacutil.exe)](../tools/gacutil-exe-gac-tool.md) pour ajouter des assemblys avec nom fort au Global Assembly Cache et visualiser le contenu de ce cache.</span><span class="sxs-lookup"><span data-stu-id="09e05-111">You can use the [Global assembly cache tool (gacutil.exe)](../tools/gacutil-exe-gac-tool.md) to add strong-named assemblies to the global assembly cache and to view the contents of the global assembly cache.</span></span>

   > [!NOTE]
   > <span data-ttu-id="09e05-112">Gacutil.exe ne sert qu'au développement. Il ne doit pas être utilisé pour installer des assemblys de production dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="09e05-112">Gacutil.exe is only for development purposes and should not be used to install production assemblies into the global assembly cache.</span></span>

<span data-ttu-id="09e05-113">La syntaxe de gacutil est la suivante :</span><span class="sxs-lookup"><span data-stu-id="09e05-113">The syntax for gacutil is as follows:</span></span>

```shell
gacutil -i <assembly name>
```

<span data-ttu-id="09e05-114">Dans cette commande, *nom_assembly* est le nom de l’assembly à installer dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="09e05-114">In this command, *assembly name* is the name of the assembly to install in the global assembly cache.</span></span>

<span data-ttu-id="09e05-115">L'exemple suivant installe un assembly avec le nom de fichier `hello.dll` dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="09e05-115">The following example installs an assembly with the file name `hello.dll` into the global assembly cache.</span></span>

```shell
gacutil -i hello.dll
```

> [!NOTE]
> <span data-ttu-id="09e05-116">Dans les versions précédentes du .NET Framework, l'extension d'environnement Windows Shfusion.dll vous permettait de faire glisser des assemblys dans **l'Explorateur de fichiers** pour les installer.</span><span class="sxs-lookup"><span data-stu-id="09e05-116">In earlier versions of the .NET Framework, the Shfusion.dll Windows shell extension enabled you to install assemblies by dragging them in **File Explorer**.</span></span> <span data-ttu-id="09e05-117">À partir de .NET Framework 4, Shfusion.dll est obsolète.</span><span class="sxs-lookup"><span data-stu-id="09e05-117">Beginning with the .NET Framework 4, Shfusion.dll is obsolete.</span></span>

## <a name="see-also"></a><span data-ttu-id="09e05-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09e05-118">See also</span></span>

- [<span data-ttu-id="09e05-119">Utilisation d’assemblys et du Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="09e05-119">Working with Assemblies and the Global Assembly Cache</span></span>](working-with-assemblies-and-the-gac.md)
- [<span data-ttu-id="09e05-120">Guide pratique pour supprimer un assembly du Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="09e05-120">How to: Remove an Assembly from the Global Assembly Cache</span></span>](how-to-remove-an-assembly-from-the-gac.md)
- [<span data-ttu-id="09e05-121">Gacutil.exe (outil Global Assembly Cache)</span><span class="sxs-lookup"><span data-stu-id="09e05-121">Gacutil.exe (Global Assembly Cache Tool)</span></span>](../tools/gacutil-exe-gac-tool.md)
- [<span data-ttu-id="09e05-122">Comment : signer un assembly avec un nom fort</span><span class="sxs-lookup"><span data-stu-id="09e05-122">How to: Sign an Assembly with a Strong Name</span></span>](how-to-sign-an-assembly-with-a-strong-name.md)