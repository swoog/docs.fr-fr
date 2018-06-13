---
title: Autorisations web et socket
ms.date: 03/30/2017
helpviewer_keywords:
- Networking
- positions [.NET Framework], accepting
- sockets, permissions
- network, permissions
- Internet, permissions
- Network Resources
- SocketPermission class, about SocketPermission class
- positions [.NET Framework], connecting
- WebPermission class, about WebPermission class
- permissions [.NET Framework], sockets
- security [.NET Framework], Internet
- positions [.NET Framework], granting
ms.assetid: d51ad8cb-03ae-4a51-bfcd-cfcf6b98afa9
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 4353f029d2e82460ab413bc8ccc248577a505504
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33394931"
---
# <a name="web-and-socket-permissions"></a>Autorisations web et socket
La sécurité Internet pour les applications utilisant l’espace de noms <xref:System.Net> est apportée par les classes <xref:System.Net.WebPermission> et <xref:System.Net.SocketPermission>. La classe **WebPermission** détermine si une application est autorisée à demander des données à partir d’un URI ou d’utiliser un URI sur Internet. La classe **SocketPermission** détermine si une application est autorisée à utiliser un <xref:System.Net.Sockets.Socket> pour accepter des données sur un port local ou pour communiquer avec des appareils distants utilisant un protocole de transport à une autre adresse, en fonction de l’hôte, du numéro de port et du protocole de transport du socket.  
  
 La classe d’autorisation à utiliser dépend du type de votre application. Les applications qui utilisent <xref:System.Net.WebRequest> et ses descendants doivent utiliser la classe **WebPermission** pour gérer les autorisations. Les applications qui utilisent un accès de niveau socket doivent utiliser la classe **SocketPermission** pour gérer les autorisations.  
  
 **WebPermission** et **SocketPermission** définissent deux autorisations : Accept et Connect. Accept autorise l’application à répondre à une connexion entrante à partir d’une autre partie. Connect l’autorise à démarrer une connexion à une autre partie.  
  
 Pour les instances **SocketPermission**, Accept signifie qu’une application peut accepter des connexions entrantes sur une adresse de transport locale et Connect signifie qu’une application peut se connecter à une adresse de transport distante (ou locale).  
  
 Pour les instances **WebPermission**, Accept signifie qu’une application peut exporter l’URI contrôlé par **WebPermission** sur Internet et Connect signifie qu’une application peut accéder à cet URI (distant ou local).  
  
## <a name="see-also"></a>Voir aussi  
 [Sécurité](../../../docs/standard/security/index.md)  
 [Sécurité dans la programmation réseau](../../../docs/framework/network-programming/security-in-network-programming.md)
