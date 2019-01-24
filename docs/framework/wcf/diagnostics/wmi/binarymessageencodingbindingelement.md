---
title: BinaryMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: e2bb3cdd-3bbd-4bb5-85fe-570457500a66
ms.openlocfilehash: 330496d5f0f80affcb6bc44a1f66f4321a635f00
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580588"
---
# <a name="binarymessageencodingbindingelement"></a>BinaryMessageEncodingBindingElement
BinaryMessageEncodingBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp  
class BinaryMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  sint32 MaxReadPoolSize;  
  sint32 MaxSessionSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe BinaryMessageEncodingBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe BinaryMessageEncodingBindingElement a les propriétés suivantes.  
  
## <a name="maxreadpoolsize"></a>MaxReadPoolSize  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Entier qui définit combien de messages peuvent être lus de manière simultanée sans allouer de nouveaux lecteurs.  
  
## <a name="maxsessionsize"></a>MaxSessionSize  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur qui spécifie la taille, en octets, de la mémoire tampon utilisée pour l'encodage.  
  
## <a name="maxwritepoolsize"></a>MaxWritePoolSize  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Entier qui définit combien de messages peuvent être envoyés simultanément sans allouer de nouveaux enregistreurs.  
  
## <a name="readerquotas"></a>ReaderQuotas  
 Type de données : XmlDictionaryReaderQuotas  
  
 Type d’accès : Propriétés en lecture seule  
  
 Quotas des lecteurs.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>
