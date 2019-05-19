---
title: Mécanismes de contrôle d'accès
ms.date: 03/30/2017
helpviewer_keywords:
- WCF security
- access control [WCF]
ms.assetid: 9d576122-3f55-4425-9acf-b23d0781e966
ms.openlocfilehash: 9ebd1489c35bb3b023ed73cd86fac1b6a352012b
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882171"
---
# <a name="access-control-mechanisms"></a>Mécanismes de contrôle d'accès
Vous pouvez contrôler l’accès de plusieurs façons avec Windows Communication Foundation (WCF). Cette rubrique présente brièvement les différents mécanismes et suggère quand utiliser chacun ; elle a pour objectif de vous aider à sélectionner le mécanisme approprié à utiliser. Les technologies d'accès sont répertoriées par ordre de complexité. La plus simple est le <xref:System.Security.Permissions.PrincipalPermissionAttribute> ; la plus complexe est le modèle d'identité.  
  
 En plus de ces mécanismes, l’emprunt d’identité et de délégation avec WCF sont expliqués dans [délégation et emprunt d’identité](../../../../docs/framework/wcf/feature-details/delegation-and-impersonation-with-wcf.md).  
  
## <a name="principalpermissionattribute"></a>PrincipalPermissionAttribute  
 <xref:System.Security.Permissions.PrincipalPermissionAttribute> permet de restreindre l'accès à une méthode de service. Lorsque l’attribut est appliqué à une méthode, il peut être utilisé pour demander l’identité d’un appelant spécifique ou l’appartenance à un groupe de Windows ou d’un rôle ASP.NET. Si le client est authentifié à l'aide d'un certificat X.509, il bénéficie d'une identité principale qui se compose du nom du sujet auquel s'ajoute l'empreinte numérique du certificat.  
  
 Utilisez l'attribut <xref:System.Security.Permissions.PrincipalPermissionAttribute> pour contrôler l'accès aux ressources sur l'ordinateur où le service s'exécute et pour contrôler si les utilisateurs du service feront toujours partie du même domaine Windows sur lequel le service s'exécute. Vous pouvez créer facilement des groupes Windows disposant de niveaux d'accès spécifiés (tels qu'aucun, lecture seule ou lecture et écriture).  
  
 Pour plus d’informations sur l’utilisation de l’attribut, consultez [Comment : Restreindre l’accès à la classe PrincipalPermissionAttribute](../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md). Pour plus d’informations sur l’identité, consultez [identité de Service et d’authentification](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).  
  
## <a name="aspnet-membership-provider"></a>Fournisseur d'appartenances ASP.NET  
 Une fonctionnalité d’ASP.NET est le fournisseur d’appartenances. Bien que le fournisseur d'appartenances ne soit pas techniquement un mécanisme de contrôle d'accès, il permet de contrôler l'accès au service en limitant le jeu d'identités possibles qui peuvent accéder au point de terminaison du service. La fonctionnalité d’appartenance inclut une base de données qui peut être remplie avec des associations nom d’utilisateur/mot de passe qui permettent aux utilisateurs d’un site Web d’établir des comptes avec le site. Pour accéder à un service qui utilise le fournisseur d'appartenances, un utilisateur doit se connecter avec son nom d'utilisateur et son mot de passe.  
  
> [!NOTE]
>  Vous devez tout d’abord remplir la base de données à l’aide de la fonctionnalité ASP.NET un service WCF pour pouvoir l’utiliser à des fins d’autorisation.  
  
 Vous pouvez également utiliser la fonctionnalité d’appartenance si vous disposez déjà d’une base de données d’appartenance d’un site Web ASP.NET existant et que vous souhaitez activer les utilisateurs d’utiliser votre service autorisé avec les mêmes noms d’utilisateur et mots de passe.  
  
 Pour plus d’informations sur l’utilisation de la fonctionnalité d’appartenance dans un service WCF, consultez [Comment : Utiliser le fournisseur d’appartenances ASP.NET](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-membership-provider.md).  
  
## <a name="aspnet-role-provider"></a>Fournisseur de rôle ASP.NET  
 Une autre fonctionnalité d’ASP.NET est la possibilité de gérer l’autorisation à l’aide de rôles. Le fournisseur de rôles ASP.NET permet à un développeur pour créer des rôles pour les utilisateurs et attribuer à chaque utilisateur à un rôle ou des rôles. Comme avec le fournisseur d’appartenances, les attributions de rôles sont stockées dans une base de données et peuvent être remplies à l’aide des outils fournis par une implémentation particulière du fournisseur de rôle ASP.NET. Comme avec la fonctionnalité d’appartenance, WCF les développeurs peuvent utiliser les informations dans la base de données pour autoriser des utilisateurs du service de rôles. Par exemple, ils peuvent utiliser le fournisseur de rôle en association avec le mécanisme de contrôle d'accès `PrincipalPermissionAttribute` décrit précédemment.  
  
 Vous pouvez également utiliser le fournisseur de rôles ASP.NET si vous disposez d’une base de données de fournisseur de rôle ASP.NET existante et que vous souhaitez utiliser le même ensemble de règles et d’assignations utilisateur dans votre service WCF.  
  
 Pour plus d’informations sur l’utilisation de la fonctionnalité de fournisseur de rôle, consultez [Comment : Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md).  
  
## <a name="authorization-manager"></a>Gestionnaire d'autorisations  
 Une autre fonctionnalité associe le Gestionnaire d’autorisations (AzMan) avec le fournisseur de rôles ASP.NET pour autoriser des clients. Lorsqu’ASP.NET héberge un service Web, AzMan peut être intégré dans l’application afin que l’autorisation au service s’effectue via AzMan. Gestionnaire de rôles ASP.NET fournit une API qui vous permet de gérer les rôles d’application, ajouter et supprimer des utilisateurs des rôles et vérifier l’appartenance au rôle, mais il n’autorise pas vous permettent d’interroger si un utilisateur est autorisé à effectuer une tâche nommée ou une opération. AzMan vous permet de définir des opérations individuelles et de les associer dans des tâches. Grâce à AZMan, outre les contrôles de rôle, vous pouvez également vérifier si un utilisateur peut effectuer une tâche. L’affectation des rôles et l’autorisation des tâches peuvent être configurées en dehors de l’application ou effectuées par programme au sein de l’application. Le composant logiciel enfichable Microsoft Management Console (MMC) d'administration AzMan permet aux administrateurs de modifier les tâches qu'un rôle peut effectuer au moment de l'exécution et de gérer l'appartenance aux rôles de chaque utilisateur.  
  
 Vous pouvez également utiliser AzMan et du fournisseur de rôle ASP.NET si vous avez accès à une installation AzMan existante déjà et que vous souhaitez autoriser vos utilisateurs de service en utilisant les fonctionnalités de la combinaison de fournisseur de rôle ou AzMan.  
  
 Pour plus d’informations sur AzMan et le fournisseur de rôles ASP.NET, consultez [How To : Utilisez le Gestionnaire d’autorisations (AzMan) avec ASP.NET 2.0](https://go.microsoft.com/fwlink/?LinkId=88951). Pour plus d’informations sur l’utilisation d’AzMan et du fournisseur de rôle pour les services WCF, consultez [Comment : Utiliser le fournisseur de rôles du Gestionnaire d’autorisations ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md).  
  
## <a name="identity-model"></a>Modèle d'identité  
 Le modèle d'identité est un ensemble d'API qui vous permettent de gérer des revendications et des stratégies pour autoriser des clients. Le modèle d'identité vous permet d'examiner chaque revendication incluse dans les informations d'identification que l'appelant a utilisée pour s'authentifier auprès du service, de comparer les revendications au jeu de stratégies pour le service et d'accorder ou de refuser l'accès en fonction de cette comparaison.  
  
 Utilisez le modèle d'identité si vous avez besoin d'un contrôle précis et de la capacité de définir des critères spécifiques avant d'accorder l'accès. Par exemple, lorsque vous utilisez <xref:System.Security.Permissions.PrincipalPermissionAttribute>, le critère est simplement que l'identité de l'utilisateur est authentifiée et que l'utilisateur appartient à un rôle spécifique. En revanche, le modèle d'identité vous permet de créer une stratégie stipulant que l'utilisateur doit être majeur et qu'il doit posséder un permis de conduire valide pour pouvoir être autorisé à consulter un document.  
  
 Par exemple, vous pouvez tirer parti du contrôle d'accès basé sur revendication du modèle d'identité lorsque vous utilisez des informations d'identification de fédération dans le scénario de jeton émis. Pour plus d’informations sur la fédération et jetons émis, consultez [fédération et jetons émis](../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).  
  
 Pour plus d’informations sur le modèle d’identité, consultez [la gestion des revendications et autorisation avec le modèle d’identité](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Security.Permissions.PrincipalPermissionAttribute>
- [Guide pratique pour Restreindre l’accès à la classe PrincipalPermissionAttribute](../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)
- [Guide pratique pour Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)
- [Guide pratique pour Utiliser le fournisseur de rôles du Gestionnaire d’autorisations ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md)
- [Gestion des revendications et autorisation avec le modèle d’identité](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
- [Délégation et emprunt d’identité](../../../../docs/framework/wcf/feature-details/delegation-and-impersonation-with-wcf.md)
