---
title: ServiceSecurityAuditBehavior
ms.date: 03/30/2017
ms.assetid: 2c5809e7-5364-44ce-bc71-848be4672e2a
ms.openlocfilehash: dc48b8742c60714720be3cf4b22ba672f73c720a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54570224"
---
# <a name="servicesecurityauditbehavior"></a>ServiceSecurityAuditBehavior
ServiceSecurityAuditBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp  
class ServiceSecurityAuditBehavior : Behavior  
{  
  string AuditLogLocation;  
  string MessageAuthenticationAuditLevel;  
  string ServiceAuthorizationAuditLevel;  
  boolean SuppressAuditFailure;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceSecurityAuditBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceSecurityAuditBehavior a les propriétés suivantes :  
  
### <a name="auditloglocation"></a>AuditLogLocation  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Emplacement du journal d'audit.  
  
### <a name="messageauthenticationauditlevel"></a>MessageAuthenticationAuditLevel  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Type de niveau d'authentification de message utilisé pour enregistrer des événements d'audit.  
  
### <a name="serviceauthorizationauditlevel"></a>ServiceAuthorizationAuditLevel  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Types d'événement d'autorisation enregistrés dans le journal d'audit.  
  
### <a name="suppressauditfailure"></a>SuppressAuditFailure  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur booléenne qui spécifie le comportement permettant de supprimer les erreurs d'écriture dans le journal d'audit.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
