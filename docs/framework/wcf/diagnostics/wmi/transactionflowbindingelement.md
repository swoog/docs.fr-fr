---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: d0311837ebb8112d9492fb548492bcd3e10230e7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514568"
---
# <a name="transactionflowbindingelement"></a>TransactionFlowBindingElement
TransactionFlowBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe TransactionFlowBindingElement ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe TransactionFlowBindingElement dispose des propriétés suivantes :  
  
### <a name="issuedtokens"></a>IssuedTokens  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Définit les exigences d’un en-tête de jetons de sécurité publié (IssuedTokens de WS-Trust).  
  
### <a name="transactionprotocol"></a>TransactionProtocol  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Protocole de transactions utilisé par le service pour transférer les transactions.  
  
### <a name="transactions"></a>Transactions  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique si la transaction entrante est prise en charge.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
