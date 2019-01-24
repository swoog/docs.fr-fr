---
title: TcpTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 33bbc1e5-44e4-4ee3-b7b5-801dc78956e4
ms.openlocfilehash: 0d5dc5c9b9bf2313d18c9fadb1a2adb87c1b11b1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610784"
---
# <a name="tcptransportbindingelement"></a>TcpTransportBindingElement
TcpTransportBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class TcpTransportBindingElement : ConnectionOrientedTransportBindingElement  
{  
  TcpConnectionPoolSettings ConnectionPoolSettings;  
  sint32 ListenBacklog;  
  boolean PortSharingEnabled;  
  boolean TeredoEnabled;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe TcpTransportBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe TcpTransportBindingElement a les propriétés suivantes :  
  
### <a name="connectionpoolsettings"></a>ConnectionPoolSettings  
 Type de données : TcpConnectionPoolSettings  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres de pool de connexions.  
  
### <a name="listenbacklog"></a>ListenBacklog  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de demandes de connexion en file d'attente pouvant être en attente.  
  
### <a name="portsharingenabled"></a>PortSharingEnabled  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur booléenne qui spécifie si le partage de port TCP est activé pour cette connexion.  
  
### <a name="teredoenabled"></a>TeredoEnabled  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur booléenne qui spécifie si Teredo (technologie d'adressage de clients placés derrière des pare-feu) est activé.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.TcpTransportBindingElement>
