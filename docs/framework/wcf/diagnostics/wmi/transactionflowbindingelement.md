---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: c2fb32c4c693cbfc487ce89b36f013398cbdb703
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="transactionflowbindingelement"></a>TransactionFlowBindingElement
TransactionFlowBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe TransactionFlowBindingElement ne définit pas de méthodes.  
  
## <a name="properties"></a>Propriétés  
 La classe TransactionFlowBindingElement dispose des propriétés suivantes :  
  
### <a name="issuedtokens"></a>IssuedTokens  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Définit les exigences d’un en-tête de jetons de sécurité publié (IssuedTokens de WS-Trust).  
  
### <a name="transactionprotocol"></a>TransactionProtocol  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Protocole de transactions utilisé par le service pour transférer les transactions.  
  
### <a name="transactions"></a>Transactions  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Indique si la transaction entrante est prise en charge.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
