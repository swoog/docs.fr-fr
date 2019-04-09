---
title: 'Procédure : Auditer les événements de sécurité Windows Communication Foundation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- security [WCF], auditing events
ms.assetid: e71e9587-3336-46a2-9a9e-d72a1743ecec
ms.openlocfilehash: 0dd025b8b7adc97420699eb2f5099ab1ee75b820
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125757"
---
# <a name="how-to-audit-windows-communication-foundation-security-events"></a>Procédure : Auditer les événements de sécurité Windows Communication Foundation
Windows Communication Foundation (WCF) vous permet de consigner les événements de sécurité pour le journal des événements Windows, qui peut être affiché à l’aide de l’Observateur d’événements Windows. Cette rubrique explique comment installer une application afin qu'elle enregistre des événements de sécurité. Pour plus d’informations sur l’audit de WCF, consultez [audit](../../../../docs/framework/wcf/feature-details/auditing-security-events.md).  
  
### <a name="to-audit-security-events-in-code"></a>Pour auditer des événements de sécurité dans le code  
  
1.  Spécifiez l'emplacement du journal d'audit. Pour cela, affectez à la propriété <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior.AuditLogLocation%2A> de la classe <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> l'une des valeurs d'énumération <xref:System.ServiceModel.AuditLogLocation>, tel qu'indiqué dans le code suivant.  
  
     [!code-csharp[AuditingSecurityEvents#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/auditingsecurityevents/cs/auditingsecurityevents.cs#2)]
     [!code-vb[AuditingSecurityEvents#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/auditingsecurityevents/vb/auditingsecurityevents.vb#2)]  
  
     Le <xref:System.ServiceModel.AuditLogLocation> énumération a trois valeurs : `Application`, `Security`, ou `Default`. La valeur spécifie l'un des journaux visibles dans l'Observateur d'événements, le journal de sécurité ou le journal des applications. Si vous utilisez la valeur `Default`, le journal réel dépend du système d'exploitation sur lequel l'application s'exécute. Si l'audit est activé et que l'emplacement du journal n'est pas spécifié, la valeur par défaut est le journal `Security` pour les plateformes qui prennent en charge l'écriture dans le journal de sécurité ; sinon, les événements sont consignés dans le journal `Application`. Seuls [!INCLUDE[ws2003](../../../../includes/ws2003-md.md)] et [!INCLUDE[wv](../../../../includes/wv-md.md)] prennent en charge l'écriture dans le journal de sécurité par défaut.  
  
2.  Installez les types d'événements à auditer. Vous pouvez auditer simultanément des événements au niveau du service ou des événements d'autorisation au niveau du message. Pour cela, affectez à la propriété <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior.ServiceAuthorizationAuditLevel%2A> ou <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior.MessageAuthenticationAuditLevel%2A> l'une des valeurs d'énumération <xref:System.ServiceModel.AuditLevel>, tel qu'indiqué dans le code suivant.  
  
     [!code-csharp[AuditingSecurityEvents#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/auditingsecurityevents/cs/auditingsecurityevents.cs#3)]
     [!code-vb[AuditingSecurityEvents#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/auditingsecurityevents/vb/auditingsecurityevents.vb#3)]  
  
3.  Spécifiez s'il convient de supprimer ou d'exposer les défaillances de l'application concernant des événements d'audit de journal. Affectez à la propriété <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior.SuppressAuditFailure%2A> la valeur `true` ou `false`, tel qu'indiqué dans le code suivant.  
  
     [!code-csharp[AuditingSecurityEvents#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/auditingsecurityevents/cs/auditingsecurityevents.cs#4)]
     [!code-vb[AuditingSecurityEvents#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/auditingsecurityevents/vb/auditingsecurityevents.vb#4)]  
  
     La propriété `SuppressAuditFailure` par défaut a la valeur `true`, afin que l'échec de l'audit n'affecte pas l'application. Sinon, une exception est levée. Tout audit exécuté avec succès entraîne l'écriture d'un suivi de détails d'information. Tout échec d'audit entraîne l'écriture d'un suivi au niveau d'erreur.  
  
4.  Supprimez le <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> existant de la collection de comportements située dans la description d’un <xref:System.ServiceModel.ServiceHost>. La collection de comportements est accessible par le biais de la propriété <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A>, qui elle-même est accessible à partir de la propriété <xref:System.ServiceModel.ServiceHostBase.Description%2A>. Puis, ajoutez le nouveau <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> à la même collection, tel qu’indiqué dans le code suivant.  
  
     [!code-csharp[AuditingSecurityEvents#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/auditingsecurityevents/cs/auditingsecurityevents.cs#5)]
     [!code-vb[AuditingSecurityEvents#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/auditingsecurityevents/vb/auditingsecurityevents.vb#5)]  
  
### <a name="to-set-up-auditing-in-configuration"></a>Pour installer l'audit dans la configuration  
  
1.  Pour configurer l’audit dans la configuration, ajoutez un [ \<comportement >](../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) élément à la [ \<comportements >](../../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) section du fichier web.config. Ajoutez ensuite une [ \<serviceSecurityAudit >](../../../../docs/framework/configure-apps/file-schema/wcf/servicesecurityaudit.md) élément et définissez les différents attributs, comme indiqué dans l’exemple suivant.  
  
    ```xml  
    <behaviors>  
       <behavior name="myAuditBehavior">  
          <serviceSecurityAudit auditLogLocation="Application"  
                suppressAuditFailure="false"   
                serviceAuthorizationAuditLevel="None"   
                messageAuthenticationAuditLevel="SuccessOrFailure" />  
          </behavior>  
    </behaviors>  
    ```  
  
2.  Vous devez spécifier le comportement du service, tel qu'indiqué dans l'exemple suivant.  
  
    ```xml  
    <services>  
        <service type="WCS.Samples.Service.Echo"   
        behaviorConfiguration=" myAuditBehavior">  
           <endpoint address=""  
                    binding="wsHttpBinding"  
                    bindingConfiguration="CertificateDefault"   
                    contract="WCS.Samples.Service.IEcho" />  
        </service>  
    </services>  
    ```  
  
## <a name="example"></a>Exemple  
 Le code suivant crée une instance de la classe <xref:System.ServiceModel.ServiceHost> et ajoute un nouveau <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> à sa collection de comportements.  
  
 [!code-csharp[AuditingSecurityEvents#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/auditingsecurityevents/cs/auditingsecurityevents.cs#1)]
 [!code-vb[AuditingSecurityEvents#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/auditingsecurityevents/vb/auditingsecurityevents.vb#1)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Affecter à la propriété <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior.SuppressAuditFailure%2A> la valeur `true` supprime toute impossibilité de générer des audits de sécurité (si la propriété a la valeur `false`, une exception est levée). Toutefois, si vous activez le Windows suivant **paramètre de sécurité locale** propriété, tout échec de génération des événements d’audit entraîne Windows arrêter immédiatement :  
  
 **Audit : Arrêter le système immédiatement s’il est impossible d’enregistrer les audits de sécurité**  
  
 Pour définir la propriété, ouvrez le **paramètres de sécurité locaux** boîte de dialogue. Sous **paramètres de sécurité**, cliquez sur **stratégies locales**. Puis cliquez sur **Options de sécurité**.  
  
 Si le <xref:System.ServiceModel.AuditLogLocation> propriété est définie sur <xref:System.ServiceModel.AuditLogLocation.Security> et **auditer l’accès aux objets** n’est pas définie le **stratégie de sécurité locale**, événements d’audit ne seront pas écrites dans le journal de sécurité. Notez qu'aucun échec n'est retourné, mais que les entrées d'audit ne sont pas écrites dans le journal de sécurité.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior.AuditLogLocation%2A>
- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
- <xref:System.ServiceModel.AuditLogLocation>
- [Audit](../../../../docs/framework/wcf/feature-details/auditing-security-events.md)
