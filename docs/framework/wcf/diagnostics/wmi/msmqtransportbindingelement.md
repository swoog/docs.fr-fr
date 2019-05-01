---
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: 706cec5c414197ebabda7939728b95be32582e0f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61963304"
---
# <a name="msmqtransportbindingelement"></a>MsmqTransportBindingElement
MsmqTransportBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe MsmqTransportBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe MsmqTransportBindingElement a les propriétés suivantes :  
  
### <a name="maxpoolsize"></a>MaxPoolSize  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Taille maximale du pool contenant des objets de message MSMQ internes.  
  
### <a name="queuetransferprotocol"></a>QueueTransferProtocol  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur d'énumération qui indique le transport de canal de communication mis en file d'attente que cette liaison utilise.  
  
### <a name="useactivedirectory"></a>UseActiveDirectory  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Retourne une valeur Boolean qui indique si les adresses de file d'attente doivent être converties à l'aide d'Active Directory.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
