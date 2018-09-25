---
title: "Comment : verrouiller des points de terminaison dans l'entreprise"
ms.date: 03/30/2017
ms.assetid: 1b7eaab7-da60-4cf7-9d6a-ec02709cf75d
ms.openlocfilehash: 032b69c1fae38576b0374b329f1ab6fe90e2b1a0
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075514"
---
# <a name="how-to-lock-down-endpoints-in-the-enterprise"></a>Comment : verrouiller des points de terminaison dans l'entreprise
Les entreprises de grande taille exigent souvent que les applications soient développées conformément à leurs stratégies de sécurité. La rubrique suivante explique comment développer et installer un validateur de point de terminaison client qui peut être utilisé pour valider toutes les applications clientes de Windows Communication Foundation (WCF) installées sur les ordinateurs.  
  
 Dans ce cas, le validateur est un validateur client car ce comportement de point de terminaison est ajouté au client [ \<commonBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/commonbehaviors.md) section dans le fichier machine.config. WCF charge des comportements de point de terminaison commun uniquement pour les applications clientes et des comportements de service communs uniquement pour les applications de service. Pour installer ce même validateur pour les applications de service, le validateur doit être un comportement de service. Pour plus d’informations, consultez le [ \<commonBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/commonbehaviors.md) section.  
  
> [!IMPORTANT]
>  Comportements de service ou de point de terminaison non marqués avec le <xref:System.Security.AllowPartiallyTrustedCallersAttribute> attribut (APTCA) qui sont ajoutés à la [ \<commonBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/commonbehaviors.md) section d’un fichier de configuration ne sont pas exécutés lorsque l’application s’exécute dans une confiance partielle environnement et aucune exception n’est levée lorsque cela se produit. Pour appliquer l'exécution des comportements courants tels que les validateurs, vous devez effectuer l'une des actions suivantes :  
>   
>  -- Marquez votre comportement courant avec l'attribut <xref:System.Security.AllowPartiallyTrustedCallersAttribute> afin qu'il soit exécuté lorsqu'il est déployé comme une application de confiance partielle. Notez qu'une entrée de Registre peut être définie sur l'ordinateur pour interdire l'exécution des assemblys marqués avec l'attribut APTCA.  
>   
>  -- Si l'application est déployée comme une application de confiance partielle, vérifiez que les utilisateurs ne peuvent pas modifier les paramètres de sécurité d'accès du code pour exécuter l'application dans un environnement de confiance partielle. S'ils peuvent le faire, le validateur personnalisé ne s'exécute pas et aucune exception n'est levée. Pour savoir comment garantir cette configuration, consultez le `levelfinal` option à l’aide de [Code Access Security Policy Tool (Caspol.exe)](https://go.microsoft.com/fwlink/?LinkId=248222).  
>   
>  Pour plus d’informations, consultez [Partial Trust Best Practices](../../../../docs/framework/wcf/feature-details/partial-trust-best-practices.md) et [pris en charge les scénarios de déploiement](../../../../docs/framework/wcf/feature-details/supported-deployment-scenarios.md).  
  
### <a name="to-create-the-endpoint-validator"></a>Pour créer le validateur de point de terminaison  
  
1.  Créez un objet <xref:System.ServiceModel.Description.IEndpointBehavior> avec les étapes de validation souhaitées dans la méthode <xref:System.ServiceModel.Description.IEndpointBehavior.Validate%2A>. Le code suivant fournit un exemple. (Le `InternetClientValidatorBehavior` provient de la [Validation de la sécurité](../../../../docs/framework/wcf/samples/security-validation.md) exemple.)  
  
     [!code-csharp[LockdownValidation#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/lockdownvalidation/cs/internetclientvalidatorbehavior.cs#2)]  
  
2.  Créez un objet <xref:System.ServiceModel.Configuration.BehaviorExtensionElement> qui enregistre le validateur de point de terminaison créé à l'étape 1. L'exemple de code suivant illustre ce point. (Le code d’origine pour cet exemple se trouve dans le [Validation de la sécurité](../../../../docs/framework/wcf/samples/security-validation.md) exemple.)  
  
     [!code-csharp[LockdownValidation#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/lockdownvalidation/cs/internetclientvalidatorelement.cs#3)]  
  
3.  Assurez-vous que l'assembly compilé est signé avec un nom fort. Pour plus d’informations, consultez le [Strong Name Tool (SN. (EXE)](https://go.microsoft.com/fwlink/?LinkId=248217) et les commandes du compilateur pour votre langue.  
  
### <a name="to-install-the-validator-into-the-target-computer"></a>Pour installer le validateur dans l'ordinateur cible  
  
1.  Installez le validateur de point de terminaison à l'aide du mécanisme approprié. Dans une entreprise, cela peut s'effectuer en utilisant la stratégie de groupe ou SMS (Systems Management Server).  
  
2.  Installer l’assembly avec nom fort dans le global assembly cache en utilisant le [Gacutil.exe (outil Global Assembly Cache)](https://msdn.microsoft.com/library/ex0ss12c\(v=vs.110\).aspx).  
  
3.  Utilisez les types d'espaces de noms <xref:System.Configuration?displayProperty=nameWithType> pour :  
  
    1.  Ajoutez l’extension à la [ \<behaviorExtensions >](../../../../docs/framework/configure-apps/file-schema/wcf/behaviorextensions.md) section à l’aide d’un nom de type qualifié complet et verrouillez l’élément.  
  
         [!code-csharp[LockdownValidation#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/lockdownvalidation/cs/hostapplication.cs#5)]  
  
    2.  Ajoutez l’élément de comportement à la `EndpointBehaviors` propriété de la [ \<commonBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/commonbehaviors.md) section et verrouillez l’élément. (Pour installer le validateur sur le service, le validateur doit être un <xref:System.ServiceModel.Description.IServiceBehavior> et être ajouté à la propriété `ServiceBehaviors`.) L'exemple de code suivant illustre la configuration appropriée après les étapes a. et b., à la seule exception qu'il n'y a pas de nom fort.  
  
         [!code-csharp[LockdownValidation#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/lockdownvalidation/cs/hostapplication.cs#6)]  
  
    3.  Enregistrez le fichier machine.config. L’exemple de code suivant exécute l’ensemble des tâches dans l’étape 3, mais enregistre une copie du fichier machine.config modifié localement.  
  
         [!code-csharp[LockdownValidation#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/lockdownvalidation/cs/hostapplication.cs#7)]  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant indique comment ajouter un comportement commun au fichier machine.config et enregistrer une copie sur le disque. Le `InternetClientValidatorBehavior` provient de la [Validation de la sécurité](../../../../docs/framework/wcf/samples/security-validation.md) exemple.  
  
 [!code-csharp[LockdownValidation#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/lockdownvalidation/cs/hostapplication.cs#1)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Vous pouvez également chiffrer les éléments du fichier de configuration. Pour plus d'informations, consultez la section Voir aussi.  
  
## <a name="see-also"></a>Voir aussi  
 [Chiffrement des éléments de fichier de configuration à l’aide de DPAPI](https://go.microsoft.com/fwlink/?LinkId=94954)  
 [Chiffrement des éléments de fichier de configuration à l’aide de RSA](https://go.microsoft.com/fwlink/?LinkId=94955)
