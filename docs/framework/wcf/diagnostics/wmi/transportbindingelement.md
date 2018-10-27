---
title: TransportBindingElement
ms.date: 03/30/2017
ms.assetid: 54ecfbee-53c0-410c-a7fa-a98f2e40c545
ms.openlocfilehash: 79d8b1f4a5127ca36eb57954cff6ee6a97e55e41
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50182656"
---
# <a name="transportbindingelement"></a>TransportBindingElement
TransportBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class TransportBindingElement : BindingElement  
{  
  boolean ManualAddressing;  
  sint64 MaxBufferPoolSize;  
  sint64 MaxReceivedMessageSize;  
  string Scheme;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe TransportBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe TransportBindingElement a les propriétés suivantes :  
  
### <a name="manualaddressing"></a>ManualAddressing  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Valeur booléenne qui spécifie si l'utilisateur souhaite prendre le contrôle de l'adressage des messages.  
  
### <a name="maxbufferpoolsize"></a>MaxBufferPoolSize  
 Type de données : sint64  
  
 Type d'accès : lecture seule  
  
 Taille maximale du pool de mémoires tampons pour la liaison.  
  
### <a name="maxreceivedmessagesize"></a>MaxReceivedMessageSize  
 Type de données : sint64  
  
 Type d'accès : lecture seule  
  
 Taille maximale d'un message traité par cette liaison.  
  
### <a name="scheme"></a>Scheme  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Schéma d'URI pour le transport.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.TransportBindingElement>
