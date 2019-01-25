---
title: Channel, classe
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: 3fbf398cca7ae9adbbecb9439bf3cbd32eb03969
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668390"
---
# <a name="channel-class"></a>Channel, classe
Canal  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class Channel  
{  
  string LocalAddress;  
  Endpoint ref;  
  string RemoteAddress;  
  string SessionId;  
  string Type;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe Channel ne définit aucune méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe Channel possède les propriétés suivantes.  
  
### <a name="localaddress"></a>LocalAddress  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Point de terminaison local du canal.  
  
### <a name="ref"></a>ref  
 Type de données : Point de terminaison  
  
 Type d’accès : Propriétés en lecture seule  
  
 Référence au point de terminaison auquel le canal se connecte.  
  
### <a name="remoteaddress"></a>RemoteAddress  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Adresse distante associée au canal.  
  
### <a name="sessionid"></a>SessionId  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Id de session actuel, le cas échéant.  
  
### <a name="type"></a>Type  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Type du canal.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.ChannelBase>
