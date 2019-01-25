---
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: d84184febd6db3f233aae6fe558b8e0f50a9cb82
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608834"
---
# <a name="onewaybindingelement"></a>OneWayBindingElement
OneWayBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe OneWayBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe OneWayBindingElement a les propriétés suivantes :  
  
### <a name="channelpoolsettings"></a>ChannelPoolSettings  
 Type de données : ChannelPoolSettings  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres du pool de canaux.  
  
### <a name="maxacceptedchannels"></a>MaxAcceptedChannels  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de canaux acceptés.  
  
### <a name="packetroutable"></a>PacketRoutable  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur qui indique si le paquet peut être routé.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.OneWayBindingElement>
