---
title: TcpConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 19acfba3-c057-4dbc-bac7-8674d7844d83
ms.openlocfilehash: f9e1c043579f632f16a7cf36bf34c2467a743e47
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50189561"
---
# <a name="tcpconnectionpoolsettings"></a>TcpConnectionPoolSettings
TcpConnectionPoolSettings  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class TcpConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe TcpConnectionPoolSettings ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe TcpConnectionPoolSettings a les propriétés suivantes :  
  
### <a name="groupname"></a>GroupName  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Nom de groupe du pool de connexions utilisé par l’élément de liaison.  
  
### <a name="idletimeout"></a>IdleTimeout  
 Type de données : datetime  
  
 Type d'accès : lecture seule  
  
 Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.  
  
### <a name="leasetimeout"></a>LeaseTimeout  
 Type de données : datetime  
  
 Type d'accès : lecture seule  
  
 Période maximale d'exécution de l'opération de bail avant expiration du délai d'attente.  
  
### <a name="maxoutboundconnectionsperendpoint"></a>MaxOutboundConnectionsPerEndpoint  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 Nombre maximal de connexions sortantes pour chaque point de terminaison.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.TcpConnectionPoolSettings>
