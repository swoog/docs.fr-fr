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
ms.openlocfilehash: 3650de934cb3d2940d0e8e971d03aff856bddfd7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43394463"
---
# <a name="how-to-view-the-contents-of-the-global-assembly-cache"></a>Guide pratique pour visualiser le contenu du Global Assembly Cache
Utilisez l’[outil Global Assembly Cache (Gacutil.exe)](../../../docs/framework/tools/gacutil-exe-gac-tool.md) pour visualiser le contenu du Global Assembly Cache.  
  
### <a name="to-view-a-list-of-the-assemblies-in-the-global-assembly-cache"></a>Pour visualiser une liste des assemblys dans le Global Assembly Cache  
  
1.  À l’[invite de commandes Visual Studio](../../../docs/framework/tools/developer-command-prompt-for-vs.md), tapez la commande suivante :  
  
     **gacutil -l**   
     - ou -  
    **gacutil /l**  
  
 Dans les versions antérieures du .NET Framework, l’extension du shell Windows [Shfusion.dll](https://msdn.microsoft.com/library/0d9464cf-ddba-4ca9-bbec-f678fb58f380) vous permettait d’afficher le Global Assembly Cache dans l’Explorateur de fichiers. À partir de [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], Shfusion.dll est obsolète.  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation d’assemblys et du Global Assembly Cache](../../../docs/framework/app-domains/working-with-assemblies-and-the-gac.md)  
 [Gacutil.exe (outil Global Assembly Cache)](../../../docs/framework/tools/gacutil-exe-gac-tool.md)
