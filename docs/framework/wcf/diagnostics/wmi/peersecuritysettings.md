---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: 1c33e1ce710fea3b1698a6dab47a199e40388f5a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59217885"
---
# <a name="peersecuritysettings"></a>PeerSecuritySettings
PeerSecuritySettings  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe PeerSecuritySettings ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe PeerSecuritySettings a les propriétés suivantes :  
  
### <a name="mode"></a>Mode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Utilisation ou non d'une sécurité au niveau du message et au niveau du transport par un point de terminaison configuré avec la liaison.  
  
### <a name="transport"></a>Transport  
 Type de données : PeerTransportSecuritySettings  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres de sécurité du transport.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.PeerSecuritySettings>
