---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: 79601308c66abe43dd5a7f72bd2a05b9d2346c2b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59975154"
---
# <a name="operationbehaviorattribute"></a>OperationBehaviorAttribute
OperationBehaviorAttribute  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe OperationBehaviorAttribute ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe OperationBehaviorAttribute a les propriétés suivantes :  
  
### <a name="autodisposeparameters"></a>AutoDisposeParameters  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 État de la fonctionnalité d’élimination automatique pour les paramètres.  
  
### <a name="impersonation"></a>Emprunt d'identité  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique le niveau d'emprunt d'identité de l'appelant pris en charge par l'opération.  
  
### <a name="releaseinstancemode"></a>ReleaseInstanceMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique à quel moment il convient de recycler l'objet lors de l'appel d'une opération.  
  
### <a name="transactionautocomplete"></a>TransactionAutoComplete  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique s’il convient de valider automatiquement la transaction actuelle si aucune exception non traitée ne se produit.  
  
### <a name="transactionscoperequired"></a>TransactionScopeRequired  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique si l’opération nécessite une transaction.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.OperationBehaviorAttribute>
