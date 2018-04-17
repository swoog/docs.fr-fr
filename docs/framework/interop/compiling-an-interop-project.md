---
title: Compilation d'un projet d'interopérabilité
ms.date: 03/30/2017
ms.prod: .net-framework
ms.technology:
- dotnet-clr
ms.topic: article
helpviewer_keywords:
- interoperation with unmanaged code, compiling
- COM interop, compiling
- exposing COM components to .NET Framework
- compiling interop projects
- interoperation with unmanaged code, exposing COM components
- COM interop, exposing COM components
ms.assetid: 6fcf6588-5e25-41af-b4ae-780974f2c3df
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: f64300e2f00eea788fcea9bd607af815cbea611d
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="compiling-an-interop-project"></a>Compilation d'un projet d'interopérabilité
Les projets de COM Interop qui référencent un ou plusieurs assemblys contenant des types COM importés sont compilés comme tout autre projet managé. Vous pouvez référencer des assemblys d’interopérabilité dans un environnement de développement tel que Visual Studio, ou vous pouvez les référencer quand vous utilisez un compilateur de ligne de commande. Dans les deux cas, l’assembly d’interopérabilité doit figurer dans le même répertoire que les autres fichiers projet pour que la compilation réussisse.  
  
 Il existe deux façons de référencer des assemblys d’interopérabilité :  
  
-   En utilisant des types interop incorporés : à compter de [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] et [!INCLUDE[vs_dev10_long](../../../includes/vs-dev10-long-md.md)], vous pouvez indiquer au compilateur d’incorporer les informations de type d’un assembly d’interopérabilité dans votre exécutable. Il s'agit de la technique recommandée.  
  
-   En déployant des assemblys d’interopérabilité : vous pouvez créer une référence standard à un assembly d’interopérabilité. Dans ce cas, l’assembly d’interopérabilité doit être déployé avec votre application.  
  
 Les différences entre ces deux techniques sont abordées de manière plus détaillée dans [Utilisation de types COM dans du code managé](https://msdn.microsoft.com/library/1a95a8ca-c8b8-4464-90b0-5ee1a1135b66(v=vs.100)).  
  
 L’incorporation des types interop avec Visual Studio est illustrée dans [Procédure pas à pas : incorporation d’informations de type provenant d’assemblys Microsoft Office](https://msdn.microsoft.com/library/85b55e05-bc5e-4665-b6ae-e1ada9299fd3(v=vs.100)) et [Procédure pas à pas : incorporation de types provenant d’assemblys managés](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21).  
  
 Pour référencer un assembly d’interopérabilité avec un compilateur de ligne de commande et pour incorporer des informations de type dans vos fichiers exécutables, utilisez le commutateur de compilateur [/link (Options du compilateur C#)](../../csharp/language-reference/compiler-options/link-compiler-option.md) ou [/link (Visual Basic)](../../visual-basic/reference/command-line-compiler/link.md) et spécifiez le nom de l’assembly d’interopérabilité.  
  
> [!NOTE]
>  Les applications Visual C++ ne peuvent pas incorporer d’informations de type, mais elles peuvent interagir avec des applications ou des compléments qui le font.  
  
 Pour compiler une application qui inclut un assembly PIA quand elle est déployée, utilisez le commutateur de compilateur **/reference** et spécifiez le nom de l’assembly d’interopérabilité.  
  
## <a name="see-also"></a>Voir aussi  
 [Exposition de composants COM au .NET Framework](exposing-com-components.md)  
 [Indépendance du langage et composants indépendants du langage](../../standard/language-independence-and-language-independent-components.md)  
 [Utilisation de Types COM en Code managé](https://msdn.microsoft.com/library/1a95a8ca-c8b8-4464-90b0-5ee1a1135b66(v=vs.100))  
 [Procédure pas à pas : incorporation d’informations de type provenant d’assemblys Microsoft Office](https://msdn.microsoft.com/library/85b55e05-bc5e-4665-b6ae-e1ada9299fd3(v=vs.100))  
 [Procédure pas à pas : incorporation de types provenant d’assemblys managés](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21)  
 [Importation d'une bibliothèque de types sous la forme d'un assembly](importing-a-type-library-as-an-assembly.md)
