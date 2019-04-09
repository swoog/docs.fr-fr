---
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: ba9031dad96f12c7c48b03f1da4af1b3adc6dd4f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59194061"
---
# <a name="peertransportbindingelement"></a>PeerTransportBindingElement
PeerTransportBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe PeerTransportBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe PeerTransportBindingElement a les propriétés suivantes :  
  
### <a name="listenipaddress"></a>ListenIPAddress  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Adresse IP sur laquelle le nœud homologue écoute les messages.  
  
### <a name="port"></a>Port  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Port d’interface de réseau sur lequel la liaison traite les messages de canaux homologues.  
  
### <a name="security"></a>Sécurité  
 Type de données : PeerSecuritySettings  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres de sécurité de transport de l'homologue.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
