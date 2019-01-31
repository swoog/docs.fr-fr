---
title: Opérations de canal dans le .NET Framework
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- pipes [.NET Framework]
- pipe operations [.NET Framework]
- interprocess communication [.NET Framework], pipes
- I/O [.NET Framework], pipes
ms.assetid: 7b964ebd-7a4f-4d28-8194-7841f9e4c702
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 919d4606e4ba72f07ba382244f8508975beffec9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741239"
---
# <a name="pipe-operations-in-the-net-framework"></a>Opérations de canal dans le .NET Framework
Les canaux sont un moyen de communication entre processus. Il existe deux types de canaux :  
  
-   Canaux anonymes.  
  
     Les canaux anonymes fournissent une communication entre processus sur un ordinateur local. Les canaux anonymes nécessitent moins de traitement que les canaux nommés, mais ils offrent des services limités. Ils sont unidirectionnels et ne peuvent pas être utilisés sur un réseau. Ils prennent seulement en charge une instance de serveur. Les canaux anonymes sont utiles pour la communication entre threads, ou entre processus parents et enfants où les handles de canaux peuvent être facilement passés au processus enfant durant sa création.  
  
     Dans .NET Framework, l’implémentation des canaux anonymes s’effectue à l’aide des classes <xref:System.IO.Pipes.AnonymousPipeServerStream> et <xref:System.IO.Pipes.AnonymousPipeClientStream>.  
  
     Voir [Guide pratique pour utiliser des canaux anonymes pour la communication entre processus en local](../../../docs/standard/io/how-to-use-anonymous-pipes-for-local-interprocess-communication.md).  
  
-   Canaux nommés.  
  
     Les canaux nommés fournissent la communication entre un serveur de canaux et un ou plusieurs clients de canaux. Ils peuvent être unidirectionnels ou en duplex. Ils prennent en charge la communication basée sur les messages et permettent à plusieurs clients de se connecter simultanément au processus serveur à l’aide du même nom de canal. Les canaux nommés prennent également en charge l’emprunt d’identité, ce qui permet aux processus de connexion d’utiliser leurs propres autorisations sur des serveurs distants.  
  
     Dans .NET Framework, l’implémentation des canaux nommés s’effectue à l’aide des classes <xref:System.IO.Pipes.NamedPipeServerStream> et <xref:System.IO.Pipes.NamedPipeClientStream>.  
  
     Voir [Guide pratique pour utiliser des canaux nommés pour la communication entre processus en réseau](../../../docs/standard/io/how-to-use-named-pipes-for-network-interprocess-communication.md).  
  
## <a name="see-also"></a>Voir aussi

- [Fichier et flux de données E/S](../../../docs/standard/io/index.md)
- [Guide pratique pour utiliser des canaux anonymes pour la communication entre processus en local](../../../docs/standard/io/how-to-use-anonymous-pipes-for-local-interprocess-communication.md)
- [Guide pratique pour utiliser des canaux nommés pour la communication entre processus en réseau](../../../docs/standard/io/how-to-use-named-pipes-for-network-interprocess-communication.md)
