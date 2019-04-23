---
title: 'Procédure : Spécifiez les informations d’identification du Client pour un Service de données demandent (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing requests
ms.assetid: 1632f9af-e45f-4363-9222-03823daa8e28
ms.openlocfilehash: ca2ed1fcf113e06535c8900e5836eb64f9b23958
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59518134"
---
# <a name="how-to-specify-client-credentials-for-a-data-service-request-wcf-data-services"></a>Procédure : Spécifiez les informations d’identification du Client pour un Service de données demandent (WCF Data Services)
Par défaut, la bibliothèque cliente ne fournit aucune information d'identification lors de l'envoi d'une demande à un service [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)]. Toutefois, vous pouvez spécifier que les informations d'identification soient transmises aux demandes authentifiées sur le service de données en fournissant un <xref:System.Net.NetworkCredential> pour la propriété <xref:System.Data.Services.Client.DataServiceContext.Credentials%2A> du <xref:System.Data.Services.Client.DataServiceContext>. Pour plus d'informations, consultez [Securing WCF Data Services](../../../../docs/framework/data/wcf/securing-wcf-data-services.md). L'exemple de cette rubrique décrit comment fournir explicitement des informations d'identification utilisées par le client [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] lors d'une demande de données au service de données.  
  
 L'exemple dans cette rubrique utilise l'exemple de service de données Northwind et des classes de service de données clientes générées automatiquement. Ce service et les classes de données client sont créés lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md). Vous pouvez également utiliser le [service de données exemple Northwind](https://go.microsoft.com/fwlink/?LinkId=187426) qui est publié sur le [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] site Web ; cet exemple de données service est en lecture seule et essayez d’enregistrer les modifications retourne une erreur. Les exemples de données des services sur le [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] site Web autoriser une authentification anonyme.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant provient de la page code-behind pour un fichier d’Extensible Application Markup Language (XAML) qui est la page principale de l’application Windows Presentation Framework. Cet exemple affiche une instance `LoginWindow` pour collecter les informations d'authentification de l'utilisateur, puis les utilise pour la création d'une demande au service de données.  
  
 [!code-csharp[Astoria Northwind Client#ClientCredentials](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/clientcredentials.xaml.cs#clientcredentials)]  
 [!code-vb[Astoria Northwind Client#ClientCredentials](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/clientcredentials.xaml.vb#clientcredentials)]
  
## <a name="example"></a>Exemple  
 Vous trouverez ci-après le code XAML qui définit la page principale de l'application WPF.  
  
 [!code-xaml[Astoria Northwind Client#ClientCredentialsXaml](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/clientcredentials.xaml#clientcredentialsxaml)]  
  
## <a name="example"></a>Exemple  
 L'exemple suivant provient de la page code-behind de la fenêtre utilisée pour collecter les informations d'authentification de l'utilisateur avant une demande au service de données.  
  
 [!code-csharp[Astoria Northwind Client#ClientCredentialsLogin](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/clientcredentialslogin.xaml.cs#clientcredentialslogin)]  
 [!code-vb[Astoria Northwind Client#ClientCredentialsLogin](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/clientcredentialslogin.xaml.vb#clientcredentialslogin)]
  
## <a name="example"></a>Exemple  
 Vous trouverez ci-après le code XAML qui définit la connexion de l'application WPF.  
  
 [!code-xaml[Astoria Northwind Client#ClientCredentialsLoginXaml](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/clientcredentialslogin.xaml#clientcredentialsloginxaml)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Les considérations sur la sécurité suivantes s'appliquent à l'exemple de cette rubrique :  
  
-   Pour vérifier que les informations d'identification fournies dans cet exemple fonctionnent, le service de données Northwind doit utiliser un schéma d'authentification autre que l'accès anonyme. Autrement, le site web qui héberge le service de données ne demandera aucune information d’identification.  
  
-   Les informations d'identification de l'utilisateur ne doivent être demandées que pendant l'exécution et ne doivent pas être mises en cache. Les informations d'identification doivent toujours être stockées de manière sécurisée.  
  
-   Les données transmises avec une authentification de base et Digest ne sont pas chiffrées, par conséquent les données sont visibles par tous. De plus, les informations d'authentification de base (nom d'utilisateur et mot de passe) sont envoyées en texte clair et peuvent être interceptées.  
  
 Pour plus d'informations, consultez [Securing WCF Data Services](../../../../docs/framework/data/wcf/securing-wcf-data-services.md).  
  
## <a name="see-also"></a>Voir aussi

- [Sécurisation de WCF Data Services](../../../../docs/framework/data/wcf/securing-wcf-data-services.md)
- [Bibliothèque cliente WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
