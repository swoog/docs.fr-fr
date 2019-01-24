---
title: 'Procédure : Utiliser le fournisseur d’appartenances ASP.NET'
ms.date: 03/30/2017
helpviewer_keywords:
- WCF and ASP.NET
- WCF, authorization
- WCF, security
ms.assetid: 322c56e0-938f-4f19-a981-7b6530045b90
ms.openlocfilehash: 4653a4b4ae90f391eac559210deb611e2a83d0f2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634504"
---
# <a name="how-to-use-the-aspnet-membership-provider"></a>Procédure : Utiliser le fournisseur d’appartenances ASP.NET
Le fournisseur d’appartenances [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] est une fonctionnalité qui permet aux développeurs [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] de créer des sites web permettant aux utilisateurs de créer des combinaisons uniques de nom d’utilisateur et de mot de passe. Grâce à cette fonctionnalité, les utilisateurs peuvent établir un compte avec le site et disposer d'un accès exclusif à celui-ci et à ses services. Cette approche diffère de la sécurité Windows, qui requiert que les utilisateurs disposent de comptes dans un domaine Windows. Au lieu de cela, l'utilisateur qui fournit ses informations d'identification (combinaison nom d'utilisateur/mot de passe) peut utiliser le site et ses services.  
  
 Pour un exemple d’application, consultez [Membership and Role Provider](../../../../docs/framework/wcf/samples/membership-and-role-provider.md). Pour plus d’informations sur l’utilisation de la [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] fonctionnalité du fournisseur de rôle, consultez [Comment : Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md).  
  
 La fonctionnalité d’appartenance requiert l’utilisation d’une base de données SQL Server pour stocker les informations utilisateur. La fonctionnalité inclut également des méthodes qui consistent à poser une question aux utilisateurs qui ont oublié leur mot de passe.  
  
 Les développeurs de Windows Communication Foundation (WCF) peuvent tirer parti de ces fonctionnalités pour des raisons de sécurité. Lorsqu’ils sont intégrés dans une application WCF, les utilisateurs doivent fournir une combinaison nom/mot de passe d’utilisateur à l’application de client WCF. Pour transférer les données au service WCF, utilisez une liaison qui prend en charge les informations d’identification de nom/mot de passe utilisateur, telles que la <xref:System.ServiceModel.WSHttpBinding> (dans la configuration, le [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md)) et définir le type d’informations d’identification à client`UserName`. Sur le service, sécurité WCF s’authentifie l’utilisateur en fonction du nom d’utilisateur et le mot de passe et assigne également le rôle spécifié par le [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] rôle.  
  
> [!NOTE]
>  WCF ne fournit pas de méthodes pour remplir la base de données avec des combinaisons nom/mot de passe d’utilisateur ou d’autres informations de l’utilisateur.  
  
### <a name="to-configure-the-membership-provider"></a>Pour configurer le fournisseur d'appartenances  
  
1.  Dans le fichier Web.config, sous le <`system.web`> élément, créer un <`membership`> élément.  
  
2.  Sous l'élément `<membership>`, créez un élément `<providers>`.  
  
3.  En tant qu’enfant à la <`providers`> élément, ajoutez un `<clear />` élément pour vider la collection de fournisseurs.  
  
4.  Sous le `<clear />` élément, créer un <`add`> élément avec les attributs suivants définis aux valeurs appropriées : `name`, `type`, `connectionStringName`, `applicationName`, `enablePasswordRetrieval`, `enablePasswordReset`, `requiresQuestionAndAnswer` , `requiresUniqueEmail`, et `passwordFormat`. L'attribut `name` est utilisé ultérieurement comme valeur dans le fichier de configuration. L'exemple suivant lui affecte la valeur `SqlMembershipProvider`.  
  
     L'exemple suivant présente la section de configuration.  
  
    ```xml  
    <!-- Configure the Sql Membership Provider -->  
    <membership defaultProvider="SqlMembershipProvider" userIsOnlineTimeWindow="15">  
      <providers>  
        <clear />  
          <add   
            name="SqlMembershipProvider"   
            type="System.Web.Security.SqlMembershipProvider"   
            connectionStringName="SqlConn"  
            applicationName="MembershipAndRoleProviderSample"  
            enablePasswordRetrieval="false"  
            enablePasswordReset="false"  
            requiresQuestionAndAnswer="false"  
            requiresUniqueEmail="true"  
            passwordFormat="Hashed" />  
      </providers>  
    </membership>  
    ```  
  
### <a name="to-configure-service-security-to-accept-the-user-namepassword-combination"></a>Pour configurer la sécurité de service afin d'accepter la combinaison nom d'utilisateur/mot de passe  
  
1.  Dans le fichier de configuration, sous le [ \<system.serviceModel >](../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) élément, ajoutez un [ \<liaisons >](../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md) élément.  
  
2.  Ajouter un [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) à la section des liaisons. Pour plus d’informations sur la création d’un élément de liaison WCF, consultez [Comment : Spécifier une liaison de Service dans la Configuration](../../../../docs/framework/wcf/how-to-specify-a-service-binding-in-configuration.md).  
  
3.  Affectez à l'attribut `mode` de l'élément `<security>` la valeur `Message`.  
  
4.  Définir le `clientCredentialType` attribut de la <`message`> élément à `UserName`. Cela spécifie qu'une paire nom d'utilisateur/mot de passe sera utilisée comme information d'identification du client.  
  
     L’exemple suivant présente le code de configuration de la liaison.  
  
    ```xml  
    <system.serviceModel>  
    <bindings>  
      <wsHttpBinding>  
      <!-- Set up a binding that uses UserName as the client credential type -->  
        <binding name="MembershipBinding">  
          <security mode ="Message">  
            <message clientCredentialType ="UserName"/>  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    </system.serviceModel>  
    ```  
  
### <a name="to-configure-a-service-to-use-the-membership-provider"></a>Pour configurer un service permettant d'utiliser le fournisseur d'appartenances  
  
1.  En tant qu’enfant à la `<system.serviceModel>` élément, ajoutez un [ \<comportements >](../../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) élément  
  
2.  Ajouter un [ \<serviceBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/servicebehaviors.md) à la <`behaviors`> élément.  
  
3.  Ajouter un [ \<comportement >](../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) et définir le `name` attribut une valeur appropriée.  
  
4.  Ajouter un [ \<serviceCredentials >](../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md) à la <`behavior`> élément.  
  
5.  Ajouter un [ \<userNameAuthentication >](../../../../docs/framework/configure-apps/file-schema/wcf/usernameauthentication.md) à la `<serviceCredentials>` élément.  
  
6.  Affectez à l'attribut `userNamePasswordValidationMode` la valeur `MembershipProvider`.  
  
    > [!IMPORTANT]
    >  Si le `userNamePasswordValidationMode` valeur n’est pas définie, WCF utilise l’authentification Windows au lieu du [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] fournisseur d’appartenances.  
  
7.  Affectez à l'attribut `membershipProviderName` le nom du fournisseur (spécifié lors de l'ajout du fournisseur dans la première procédure de cette rubrique). L'exemple suivant présente le fragment `<serviceCredentials>` à ce point.  
  
    ```xml  
    <behaviors>  
       <serviceBehaviors>  
          <behavior name="MyServiceBehavior">  
             <serviceCredentials>  
                <userNameAuthentication   
                userNamePasswordValidationMode="MembershipProvider"  
                membershipProviderName="SqlMembershipProvider" />  
             </serviceCredentials>  
          </behavior>  
       </serviceBehaviors>  
    </behaviors>  
    ```  
  
## <a name="example"></a>Exemple  
 Le code suivant montre la configuration d’un service qui utilise la fonctionnalité d’appartenance ASP.  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
  <system.serviceModel>  
    <services>  
      <service behaviorConfiguration="MyServiceBehavior" name="Microsoft.Samples.GettingStarted.CalculatorService">  
        <endpoint address="http://microsoft.com/WCFservices/Calculator"  
          binding="wsHttpBinding" bindingConfiguration="MembershipBinding"  
          name="ASPmemberUserName" contract="Microsoft.Samples.GettingStarted.ICalculator" />  
      </service>  
    </services>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="MyServiceBehavior">  
          <serviceCredentials>  
            <userNameAuthentication   
              userNamePasswordValidationMode="MembershipProvider"  
              membershipProviderName="SqlMembershipProvider" />  
          </serviceCredentials>  
        </behavior>  
          </serviceBehaviors>  
    </behaviors>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="MembershipBinding">  
          <security mode="Message">  
            <message clientCredentialType="UserName" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)
- [Fournisseur d’appartenances et de rôles](../../../../docs/framework/wcf/samples/membership-and-role-provider.md)
