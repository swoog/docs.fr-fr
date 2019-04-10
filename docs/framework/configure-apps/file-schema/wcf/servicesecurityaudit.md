---
title: <serviceSecurityAudit>
ms.date: 03/30/2017
ms.assetid: ba517369-a034-4f8e-a2c4-66517716062b
ms.openlocfilehash: 384a1cdb6d39f4d6ecd2353a15c0da7c6d2e82bd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59224080"
---
# <a name="servicesecurityaudit"></a>\<serviceSecurityAudit>
Spécifie des paramètres qui activent l'audit d'événements de sécurité pendant des opérations de service.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceSecurityAudit>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<serviceSecurityAudit auditLogLocation="Default/Application/Security"
                      messageAuthenticationAuditLevel="None/Success/Failure/SuccessOrFailure"
                      serviceAuthorizationAuditLevel="None/Success/Failure/SuccessOrFailure"
                      suppressAuditFailure="Boolean" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|auditLogLocation|Spécifie l'emplacement du journal d'audit. Les valeurs valides sont les suivantes :<br /><br /> -Valeur par défaut : Événements de sécurité sont écrits dans le journal des applications sur Windows XP et dans le journal des événements sur Windows Server 2003 et Windows Vista.<br />-Application : Événements d’audit sont écrits dans le journal des événements.<br />-Sécurité : Événements d’audit sont écrits dans le journal des événements de sécurité.<br /><br /> La valeur par défaut est Default. Pour plus d'informations, consultez <xref:System.ServiceModel.AuditLogLocation>.|  
|suppressAuditFailure|Valeur booléenne qui spécifie le comportement permettant de supprimer les erreurs d'écriture dans le journal d'audit.<br /><br /> Les applications doivent être averties des erreurs d'écriture dans le journal d'audit. Si votre application n'est pas conçue pour gérer les erreurs d'audit, vous devez utiliser cet attribut pour supprimer les erreurs d'écriture dans le journal d'audit.<br /><br /> Si cet attribut a pour valeur `true`, les exceptions autres qu'OutOfMemoryException, StackOverFlowException, ThreadAbortException et ArgumentException qui résultent de tentatives d'écriture d'événements d'audit sont contrôlées par le système et ne sont pas propagées dans l'application. Si cet attribut a pour valeur `false`, toutes les exceptions qui résultent de tentatives d'écriture d'événements d'audit sont passées à l'application.<br /><br /> La valeur par défaut est `true`.|  
|serviceAuthorizationAuditLevel|Spécifie les types d'événements d'autorisation enregistrés dans le journal d'audit. Les valeurs valides sont les suivantes :<br /><br /> -None : Aucun audit d’événements d’autorisation de service n’est effectuée.<br />-Réussite : Seuls les événements d’autorisation service réussis sont audités.<br />-Échec : Seuls les événements d’autorisation de service échec sont audités.<br />-SuccessOrFailure : Événements d’autorisation du service réussite et d’échec sont audités.<br /><br /> La valeur par défaut est None. Pour plus d'informations, consultez <xref:System.ServiceModel.AuditLevel>.|  
|messageAuthenticationAuditLevel|Spécifie le type d'événements d'audit d'authentification de message enregistrés. Les valeurs valides sont les suivantes :<br /><br /> -None : Aucun événement d’audit n’est générées.<br />-Réussite : Seuls les événements de (validation complète, y compris la validation des signatures de message, le chiffrement et validation du jeton) sécurité réussis sont enregistrés.<br />-Échec : Seuls les événements d’échec sont enregistrés.<br />-SuccessOrFailure : Événements de réussite et d’échec sont enregistrés.<br /><br /> La valeur par défaut est None. Pour plus d'informations, consultez <xref:System.ServiceModel.AuditLevel>.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Spécifie un élément de comportement.|  
  
## <a name="remarks"></a>Notes  
 Cet élément de configuration est utilisé pour auditer les événements de l’authentification Windows Communication Foundation (WCF). Lorsque l'audit est activé, il est possible de réaliser l'audit des tentatives d'authentification réussies ou échouées (ou les deux). Les événements sont écrits dans l'un des trois journaux des événements : application, sécurité ou journal par défaut de la version du système d'exploitation. Les journaux des événements peuvent être consultés à l'aide de l'Observateur d'événements Windows.  
  
 Pour obtenir un exemple détaillé de l’utilisation de cet élément de configuration, consultez [le comportement de l’audit Service](../../../../../docs/framework/wcf/samples/service-auditing-behavior.md).  
  
 Par défaut, sur Windows XP, les événements d’audit peuvent être consultés dans le journal des applications, tandis que sur Windows Server 2003 et Windows Vista, ils peuvent être consultés dans le journal de sécurité. L'emplacement des événements d'audit peut être spécifié en affectant la valeur 'Application' ou 'Security' à l'attribut `auditLogLocation`. Pour plus d'informations, voir [Procédure : Auditer les événements de sécurité](../../../../../docs/framework/wcf/feature-details/how-to-audit-wcf-security-events.md). Si les événements sont écrits dans le journal de sécurité, LocalSecurityPolicy -> Enable Object Access doit être définie pour « Success » et « Failure ».  
  
 Lors de la consultation du journal des événements, la source des événements d'audit est « ServiceModel Audit 3.0.0.0 ». Les enregistrements de l'audit d'authentification du message portent la catégorie « MessageAuthentication », tandis que les enregistrements de l'audit d'autorisation du service portent la catégorie « ServiceAuthorization ».  
  
 Les événements de l'audit d'authentification du message permettent de savoir si le message a été falsifié, s'il a expiré et si le client peut s'authentifier auprès du service. Ils fournissent des informations sur la réussite ou l'échec de l'authentification, l'identité du client, le point de terminaison auquel le message a été envoyé et l'action associée au message.  
  
 Les événements de l'audit d'autorisation du service permettent de connaître la décision d'autorisation prise par un gestionnaire d'autorisation du service. Ils fournissent des informations sur indique si l’autorisation a réussi ou échoué, ainsi que l’identité du client, le point de terminaison le message a été envoyé, l’action associée au message, l’identificateur du contexte d’autorisation qui a été généré à partir de la message entrant et le type du Gestionnaire d’autorisation qui a pris la décision d’accès.  
  
## <a name="example"></a>Exemple  
  
```xml  
<system.serviceModel>
  <behaviors>
    <serviceBehaviors>
      <behavior name="NewBehavior">
        <serviceSecurityAudit auditLogLocation="Application"
                              suppressAuditFailure="true"
                              serviceAuthorizationAuditLevel="Success"
                              messageAuthenticationAuditLevel="Success" />
      </behavior>
    </serviceBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.ServiceSecurityAuditElement>
- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Audit](../../../../../docs/framework/wcf/feature-details/auditing-security-events.md)
- [Procédure : auditer des événements de sécurité](../../../../../docs/framework/wcf/feature-details/how-to-audit-wcf-security-events.md)
- [Service Auditing Behavior](../../../../../docs/framework/wcf/samples/service-auditing-behavior.md)
