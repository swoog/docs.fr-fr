---
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: 0ca3d198ce225221348ac7b405ea91ad215cd298
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59190897"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a>System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
Le taux de réception entrant des messages est trop élevé.  
  
## <a name="description"></a>Description  
 Ce suivi se produit lors de la tentative de traitement des messages entrants. Un message n'a pas pu être transmis à un voisin spécifique en raison du dépassement du quota défini pour ce voisin. Ce cas se produit lorsqu’un voisin qui ne répond pas ne peut pas effacer un backlog avec messages en attente pour ce voisin.  
  
## <a name="troubleshooting"></a>Résolution des problèmes  
 Réduisez le taux auquel les messages sont envoyés dans la maille.  
  
## <a name="see-also"></a>Voir aussi

- [Traçage](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
