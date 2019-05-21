---
title: Conversion d'une application NetTcpBinding en une application de canal homologue
ms.date: 03/30/2017
ms.assetid: d4137292-a923-4b8f-8594-42276f2d3ce2
ms.openlocfilehash: 362945959a781fac360c42475148fee1e47a1183
ms.sourcegitcommit: ffd7dd79468a81bbb0d6449f6d65513e050c04c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2019
ms.locfileid: "65960134"
---
# <a name="converting-a-nettcpbinding-application-to-a-peer-channel-application"></a>Conversion d'une application NetTcpBinding en une application de canal homologue
Vous pouvez créer des connexions entre les clients à l’aide de la WinFX à l’aide de liaisons qui décrivent les paramètres de la connexion. Conversion d’une application .NET Framework à utiliser des connexions de peer-to-peer nécessite une liaison qui prend en charge cette technologie lors de l’établissement des connexions clientes. Le canal homologue fournit une liaison nommée <xref:System.ServiceModel.NetPeerTcpBinding>, que vous pouvez utiliser de manière semblable à <xref:System.ServiceModel.NetTcpBinding>. Les principales différences incluent la spécification d'un service de résolution et la définition de paramètres de sécurité.  
  
 Si une application utilise le programme de résolution et les paramètres de sécurité par défaut, la conversion d'une application normale client-serveur pour utiliser le canal homologue implique la modification du nom de la liaison de « NetTcpBinding » en « NetPeerTcpBinding » dans le fichier de configuration de l'application ; il n'est pas nécessaire de modifier la base de code de l'application.  
  
## <a name="see-also"></a>Voir aussi

- [Création d’une application de canal homologue](../../../../docs/framework/wcf/feature-details/building-a-peer-channel-application.md)
- [Liaisons fournies par le système](../../../../docs/framework/wcf/system-provided-bindings.md)
