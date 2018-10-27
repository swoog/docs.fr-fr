---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 77d8403947d341ea2efcef98bbf166f94f75f31f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188727"
---
# <a name="namedpipeconnectionpoolsettings"></a>NamedPipeConnectionPoolSettings
NamedPipeConnectionPoolSettings  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe NamedPipeConnectionPoolSettings ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe NamedPipeConnectionPoolSettings a les propriétés suivantes :  
  
### <a name="groupname"></a>GroupName  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Nom de groupe du pool de connexions utilisé par l’élément de liaison.  
  
### <a name="idletimeout"></a>IdleTimeout  
 Type de données : datetime  
  
 Type d'accès : lecture seule  
  
 Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.  
  
### <a name="maxoutboundconnectionsperendpoint"></a>MaxOutboundConnectionsPerEndpoint  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 Nombre maximal de connexions sortantes pour chaque point de terminaison sur le client.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
