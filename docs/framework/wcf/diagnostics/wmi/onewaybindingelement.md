---
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: ee7cfed20234175ba54dd25dbbbab4615c1ed7af
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485741"
---
# <a name="onewaybindingelement"></a>OneWayBindingElement
OneWayBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe OneWayBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe OneWayBindingElement a les propriétés suivantes :  
  
### <a name="channelpoolsettings"></a>ChannelPoolSettings  
 Type de données : ChannelPoolSettings  
  
 Type d'accès : lecture seule  
  
 Paramètres du pool de canaux.  
  
### <a name="maxacceptedchannels"></a>MaxAcceptedChannels  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 Nombre maximal de canaux acceptés.  
  
### <a name="packetroutable"></a>PacketRoutable  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Valeur qui indique si le paquet peut être routé.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.OneWayBindingElement>
