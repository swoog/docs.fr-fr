---
title: Adoption de Windows Communication Foundation
ms.date: 03/30/2017
ms.assetid: 49ba71e2-9468-4082-84c5-cf8daf95e34a
ms.openlocfilehash: bcd6543e6cd47dc723b308acebec6f492fa14fb1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33489129"
---
# <a name="adopting-windows-communication-foundation"></a>Adoption de Windows Communication Foundation
Vous pouvez choisir d’utiliser Windows Communication Foundation (WCF) pour tout nouveau développement, tandis que continuant à gérer les applications existantes développées à l’aide d’ASP.NET. Étant donné que WCF est destinée à être le choix le plus adapté pour faciliter la communication avec les applications générées avec le .NET Framework dans n’importe quel scénario, il peut constituer un outil standard pour la résolution d’un large éventail de problèmes de communication du logiciel de façon qu’ASP.NET ne peut pas.  
  
 Nouvelles applications WCF peuvent être déployées sur les mêmes ordinateurs que les services Web ASP.NET existants. Si les services Web ASP.NET existants utilisent une version du .NET Framework antérieures à la version 2.0, vous pouvez utiliser l’outil ASP.NET IIS Registration pour déployer sélectivement le .NET Framework 2.0 dans les applications IIS dans lequel les nouvelles applications WCF doivent être hébergés. Cet outil est documenté à [ASP.NET IIS Registration Tool (Aspnet_regiis.exe)](http://go.microsoft.com/fwlink/?LinkId=94687), et a une interface utilisateur intégrée de la console de gestion IIS 6.0.  
  
 WCF peut être utilisé pour ajouter de nouvelles fonctionnalités aux services Web ASP.NET existants en ajoutant des services WCF configurés pour s’exécuter en mode de compatibilité ASP.NET pour les applications de service Web ASP.NET existant dans IIS. En raison du mode de compatibilité ASP.NET, le code pour les nouveaux services WCF peut accéder et mettre à jour les informations d’état application même que le code ASP.NET préexistant, à l’aide de la <xref:System.Web.HttpContext> classe. Les applications peuvent également partager les mêmes bibliothèques de classes.  
  
 Clients WCF peuvent utiliser les services Web ASP.NET. Les services WCF qui sont configurés avec la <xref:System.ServiceModel.BasicHttpBinding> peut être utilisé par les clients du service Web ASP.NET. Les services Web ASP.NET peuvent coexister avec les applications WCF et WCF peut même être utilisé pour ajouter des fonctionnalités aux services Web ASP.NET existants. Étant donné toutes les manières dans lequel les services WCF et ASP.NET Web peuvent être utilisés ensemble, vous voudrez migrer les services Web ASP.NET vers WCF uniquement si vous avez besoin des fonctionnalités fournies par les services WCF et pas ASP.NET Web.  
  
 Même les rares fois où cela est nécessaire, dites-vous bien qu'effectuer une migration de code d'une technologie à une autre est rarement la bonne solution. L’adoption d’une nouvelle technologie permet de satisfaire de nouvelles exigences qui ne peuvent pas être satisfaites avec la technologie antérieure, et dans ce cas, le mieux à faire est de concevoir une nouvelle solution qui satisfait l’ensemble des exigences récemment étendues. La nouvelle conception bénéficie de votre expérience avec le système existant et du savoir-faire acquis depuis que ce système a été conçu. La nouvelle conception peut également profiter de l'intégralité des possibilités offertes par les nouvelles technologies plutôt que de reproduire l'ancienne conception sur la nouvelle plate-forme. Après le prototypage des éléments clés de la nouvelle conception, il devient plus facile de réutiliser le code du système existant dans le nouveau.  
  
 Pour les rares cas où le portage d’applications de services Web ASP.NET vers WCF est la solution appropriée, la section suivante fournit quelques conseils sur la marche à suivre. Elle propose des conseils sur la manière de migrer des services et des clients.  
  
 Pour une analyse complète sur la façon de migrer des Services Web ASP.NET existants vers WCF, consultez [des Services Web ASP.NET et Windows Communication Foundation](http://go.microsoft.com/fwlink/?LinkID=71761). Cette section décrit comment implémenter un service WCF conforme à partir des métadonnées pour votre Service Web ASP.NET et comment migrer du code de service et le client Web ASP.NET vers WCF.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour récupérer des métadonnées et implémenter un service conforme](../../../../docs/framework/wcf/feature-details/how-to-retrieve-metadata-and-implement-a-compliant-service.md)  
 [Guide pratique pour migrer le code d’un service web ASP.NET vers Windows Communication Foundation](../../../../docs/framework/wcf/feature-details/migrate-asp-net-web-service-to-wcf.md)  
 [Guide pratique pour migrer le code client des services web ASP.NET vers Windows Communication Foundation](../../../../docs/framework/wcf/feature-details/migrate-asp-net-web-service-client-to-wcf.md)
