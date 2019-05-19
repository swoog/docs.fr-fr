---
title: 'Procédure : utiliser le fournisseur de rôle ASP.NET avec un service'
ms.date: 03/30/2017
ms.assetid: 88d33a81-8ac7-48de-978c-5c5b1257951e
ms.openlocfilehash: f989252c7dd9b2ccdce8331e7cdd987042230ded
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880234"
---
# <a name="how-to-use-the-aspnet-role-provider-with-a-service"></a>Procédure : utiliser le fournisseur de rôle ASP.NET avec un service
Le fournisseur de rôles ASP.NET (conjointement avec le fournisseur d’appartenances ASP.NET) est une fonctionnalité qui permet aux développeurs ASP.NET créer des sites Web qui permettent aux utilisateurs de créer un compte avec un site et à affecter des rôles à des fins d’autorisation. Grâce à cette fonctionnalité, les utilisateurs peuvent établir un compte avec le site et disposer d’un accès exclusif à celui-ci et à ses services. Cette approche diffère de la sécurité Windows, qui requiert que les utilisateurs disposent de comptes dans un domaine Windows. Au lieu de cela, tout utilisateur qui fournit ses informations d'identification (combinaison nom d'utilisateur/mot de passe) peut utiliser le site et ses services.  
  
 Pour un exemple d’application, consultez [Membership and Role Provider](../../../../docs/framework/wcf/samples/membership-and-role-provider.md). Pour plus d’informations sur la fonctionnalité de fournisseur d’appartenance ASP.NET, consultez [Comment : Utiliser le fournisseur d’appartenances ASP.NET](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-membership-provider.md).  
  
 La fonctionnalité de fournisseur de rôle utilise une base de données SQL Server pour stocker des informations utilisateur. Les développeurs de Windows Communication Foundation (WCF) peuvent tirer parti de ces fonctionnalités pour des raisons de sécurité. Lorsque intégré à une application WCF, les utilisateurs doivent fournir une combinaison nom/mot de passe d’utilisateur à l’application de client WCF. Pour activer WCF à utiliser la base de données, vous devez créer une instance de la <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior> classe, définissez son <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior.PrincipalPermissionMode%2A> propriété <xref:System.ServiceModel.Description.PrincipalPermissionMode.UseAspNetRoles>et ajoutez l’instance à la collection de comportements pour le <xref:System.ServiceModel.ServiceHost> qui héberge le service.  
  
### <a name="to-configure-the-role-provider"></a>Pour configurer le fournisseur de rôle  
  
1. Dans le fichier Web.config, sous le <`system.web`> élément, ajouter un <`roleManager`> et affectez sa `enabled` attribut `true`.  
  
2. Affectez à l'attribut `defaultProvider` la valeur `SqlRoleProvider`.  
  
3. En tant qu’enfant à la <`roleManager`> élément, ajoutez un <`providers`> élément.  
  
4. En tant qu’enfant à la <`providers`> élément, ajoutez un <`add`> élément avec les attributs suivants définis aux valeurs appropriées : `name`, `type`, `connectionStringName`, et `applicationName`, comme illustré dans l’exemple suivant.  
  
    ```xml  
    <!-- Configure the Sql Role Provider. -->  
    <roleManager enabled ="true"   
     defaultProvider ="SqlRoleProvider" >  
       <providers>  
         <add name ="SqlRoleProvider"   
           type="System.Web.Security.SqlRoleProvider"   
           connectionStringName="SqlConn"   
           applicationName="MembershipAndRoleProviderSample"/>  
       </providers>  
    </roleManager>  
    ```  
  
### <a name="to-configure-the-service-to-use-the-role-provider"></a>Pour configurer le service pour utiliser le fournisseur de rôle  
  
1. Dans le fichier Web.config, ajoutez un [ \<system.serviceModel >](../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) élément.  
  
2. Ajouter un [ \<comportements >](../../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) élément à la <`system.ServiceModel`> élément.  
  
3. Ajouter un [ \<serviceBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/servicebehaviors.md) à la <`behaviors`> élément.  
  
4. Ajouter un [ \<comportement >](../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) élément et définissez la `name` attribut une valeur appropriée.  
  
5. Ajouter un [ \<serviceAuthorization >](../../../../docs/framework/configure-apps/file-schema/wcf/serviceauthorization-element.md) à la <`behavior`> élément.  
  
6. Affectez à l'attribut `principalPermissionMode` la valeur `UseAspNetRoles`.  
  
7. Affectez à l'attribut `roleProviderName` la valeur `SqlRoleProvider`. L'exemple suivant présente un fragment de la configuration.  
  
    ```xml  
    <behaviors>  
     <serviceBehaviors>  
      <behavior name="CalculatorServiceBehavior">  
       <serviceAuthorization principalPermissionMode ="UseAspNetRoles"  
                             roleProviderName ="SqlRoleProvider" />  
      </behavior>  
     </serviceBehaviors>  
    </behaviors>  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Fournisseur d’appartenances et de rôles](../../../../docs/framework/wcf/samples/membership-and-role-provider.md)
- [Guide pratique pour Utiliser le fournisseur d’appartenances ASP.NET](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-membership-provider.md)
