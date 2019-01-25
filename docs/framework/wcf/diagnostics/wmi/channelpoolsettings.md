---
title: ChannelPoolSettings
ms.date: 03/30/2017
ms.assetid: d3f475bd-f780-4bbe-b291-339387322964
ms.openlocfilehash: 4a3e45140765f99f4a30b77fc9d02b167601b50b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591475"
---
# <a name="channelpoolsettings"></a>ChannelPoolSettings
ChannelPoolSettings  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ChannelPoolSettings  
{  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundChannelsPerEndpoint;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ChannelPoolSettings ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe ChannelPoolSettings a les propriétés suivantes :  
  
### <a name="idletimeout"></a>IdleTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.  
  
### <a name="leasetimeout"></a>LeaseTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Période maximale d'exécution d'une opération de bail avant expiration du délai d'attente.  
  
### <a name="maxoutboundchannelsperendpoint"></a>MaxOutboundChannelsPerEndpoint  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de canaux sortants pour chaque point de terminaison.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
