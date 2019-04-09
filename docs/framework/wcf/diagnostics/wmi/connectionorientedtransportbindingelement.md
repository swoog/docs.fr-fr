---
title: ConnectionOrientedTransportBindingElement
ms.date: 03/30/2017
ms.assetid: c1308313-f0e2-49e6-977d-6b4ce9ad35d1
ms.openlocfilehash: 04e6abc5941ec99769ff2c15d47881b60e81d2e0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59181569"
---
# <a name="connectionorientedtransportbindingelement"></a>ConnectionOrientedTransportBindingElement
ConnectionOrientedTransportBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ConnectionOrientedTransportBindingElement : TransportBindingElement  
{  
  datetime ChannelInitializationTimeout;  
  sint32 ConnectionBufferSize;  
  string HostNameComparisonMode;  
  sint32 MaxBufferSize;  
  datetime MaxOutputDelay;  
  sint32 MaxPendingAccepts;  
  sint32 MaxPendingConnections;  
  string TransferMode;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ConnectionOrientedTransportBindingElement ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe ConnectionOrientedTransportBindingElement a les propriétés suivantes :  
  
### <a name="channelinitializationtimeout"></a>ChannelInitializationTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Le timespan qui spécifie le délai d'initialisation du canal avant expiration.  
  
### <a name="connectionbuffersize"></a>ConnectionBufferSize  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Taille de la mémoire tampon utilisée pour transmettre une portion du message sérialisé sur le câble du client ou du service.  
  
### <a name="hostnamecomparisonmode"></a>HostNameComparisonMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur qui indique si le nom d'hôte est utilisé pour atteindre le service lors de la correspondance avec l'URI.  
  
### <a name="maxbuffersize"></a>MaxBufferSize  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Taille maximale autorisée de la mémoire tampon.  
  
### <a name="maxoutputdelay"></a>MaxOutputDelay  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Durée maximale pendant laquelle une portion d'un message ou un message complet peut rester en mémoire tampon avant d'être expédié.  
  
### <a name="maxpendingaccepts"></a>MaxPendingAccepts  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de threads d'acceptation asynchrones en attente qui sont disponibles pour traiter des connexions entrantes sur le service.  
  
### <a name="maxpendingconnections"></a>MaxPendingConnections  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de connexions en attente.  
  
### <a name="transfermode"></a>TransferMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur qui spécifie si les messages sont mis en mémoire tampon ou transmis en continu par le transport orienté connexion.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Channels.ConnectionOrientedTransportBindingElement>
