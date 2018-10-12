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
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a>Guide pratique pour installer un assembly dans le Global Assembly Cache

Il existe deux façons d'installer un assembly avec nom fort dans le Global Assembly Cache (GAC).

> [!IMPORTANT]
> Seuls les assemblys avec noms forts peuvent être installés dans le GAC. Pour plus d’informations sur la façon de créer un assembly avec un nom fort, consultez [Guide pratique pour signer un assembly avec un nom fort](how-to-sign-an-assembly-with-a-strong-name.md).

## <a name="windows-installer"></a>Windows Installer

[Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache), le moteur d’installation de Windows, est la méthode recommandée pour ajouter des assemblys dans le Global Assembly Cache. Windows Installer fournit un décompte de références des assemblys dans le Global Assembly Cache, ainsi que d'autres avantages. Vous pouvez utiliser [l’extension WiX Toolset pour Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension) pour créer un package de programme d’installation pour Windows Installer.

## <a name="global-assembly-cache-tool"></a>Outil Global Assembly Cache

Vous pouvez utiliser [l’outil Global Assembly Cache (Gacutil.exe)](../tools/gacutil-exe-gac-tool.md) pour ajouter des assemblys avec nom fort au Global Assembly Cache et visualiser le contenu de ce cache.

   > [!NOTE]
   > Gacutil.exe ne sert qu'au développement. Il ne doit pas être utilisé pour installer des assemblys de production dans le Global Assembly Cache.

La syntaxe de gacutil est la suivante :

```shell
gacutil -i <assembly name>
```

Dans cette commande, *nom_assembly* est le nom de l’assembly à installer dans le Global Assembly Cache.

L'exemple suivant installe un assembly avec le nom de fichier `hello.dll` dans le Global Assembly Cache.

```shell
gacutil -i hello.dll
```

> [!NOTE]
> Dans les versions précédentes du .NET Framework, l'extension d'environnement Windows Shfusion.dll vous permettait de faire glisser des assemblys dans **l'Explorateur de fichiers** pour les installer. À partir de .NET Framework 4, Shfusion.dll est obsolète.

## <a name="see-also"></a>Voir aussi

- [Utilisation d’assemblys et du Global Assembly Cache](working-with-assemblies-and-the-gac.md)
- [Guide pratique pour supprimer un assembly du Global Assembly Cache](how-to-remove-an-assembly-from-the-gac.md)
- [Gacutil.exe (outil Global Assembly Cache)](../tools/gacutil-exe-gac-tool.md)
- [Comment : signer un assembly avec un nom fort](how-to-sign-an-assembly-with-a-strong-name.md)