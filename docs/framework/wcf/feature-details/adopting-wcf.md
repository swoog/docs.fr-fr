---
title: Adoption de Windows Communication Foundation
ms.date: 03/30/2017
ms.assetid: 49ba71e2-9468-4082-84c5-cf8daf95e34a
ms.openlocfilehash: 58a51f7ea0db2297c7151a752de3f54307e0c5fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643349"
---
# <a name="adopting-windows-communication-foundation"></a>Adoption de Windows Communication Foundation

Vous pouvez choisir d’utiliser Windows Communication Foundation (WCF) pour tout nouveau développement, alors que continuant à gérer les applications existantes développées à l’aide de ASP.NET. Étant donné que WCF est destinée à être le meilleur choix pour faciliter la communication avec les applications générées avec le .NET Framework dans n’importe quel scénario, il peut constituer un outil standard pour résoudre un large éventail de problèmes de communication de logiciels de manière qu’ASP.NET ne peut pas.

Nouvelles applications WCF peuvent être déployées sur les mêmes machines en tant que services Web ASP.NET existants. Si les services Web ASP.NET existants utilisent une version du .NET Framework antérieures à la version 2.0, vous pouvez utiliser l’outil ASP.NET IIS Registration pour déployer sélectivement le .NET Framework 2.0 dans les applications IIS dans lequel les nouvelles applications WCF doivent être hébergés. Cet outil est décrit à l’adresse [outil ASP.NET IIS Registration (Aspnet_regiis.exe)](https://go.microsoft.com/fwlink/?LinkId=94687), et a une interface utilisateur intégrée de la console de gestion IIS 6.0.

WCF peut être utilisé pour ajouter de nouvelles fonctionnalités aux services Web ASP.NET existants en ajoutant des services WCF configurés pour s’exécuter en mode de compatibilité ASP.NET pour les applications de service Web ASP.NET existantes dans IIS. En raison du mode de compatibilité ASP.NET, le code pour les nouveaux services WCF permettre accéder et mettre à jour les informations d’état application même que le code ASP.NET préexistant, à l’aide de la <xref:System.Web.HttpContext> classe. Les applications peuvent également partager les mêmes bibliothèques de classes.

Les clients WCF peuvent utiliser les services Web ASP.NET. Les services WCF qui sont configurés avec le <xref:System.ServiceModel.BasicHttpBinding> peut être utilisé par les clients de service Web ASP.NET. Les services Web ASP.NET peuvent coexister avec les applications WCF et WCF peut même être utilisé pour ajouter des fonctionnalités aux services Web ASP.NET existants. Étant donné toutes les manières dans lequel les services WCF et ASP.NET Web peuvent être utilisés ensemble, voulez-vous migrer les services Web ASP.NET vers WCF uniquement si vous avez besoin des fonctionnalités fournies par les services WCF pas Web et ASP.NET.

Même dans les rares cas où il est nécessaire, migration de code à partir d’une seule technologie à l’autre est rarement l’approche correcte. L’adoption d’une nouvelle technologie permet de satisfaire de nouvelles exigences qui ne peuvent pas être satisfaites avec la technologie antérieure, et dans ce cas, le mieux à faire est de concevoir une nouvelle solution qui satisfait l’ensemble des exigences récemment étendues. La nouvelle conception bénéficie de votre expérience avec le système existant et du savoir-faire acquis depuis que ce système a été conçu. La nouvelle conception peut également profiter de l'intégralité des possibilités offertes par les nouvelles technologies plutôt que de reproduire l'ancienne conception sur la nouvelle plate-forme. Après le prototypage des éléments clés de la nouvelle conception, il devient plus facile de réutiliser le code du système existant dans le nouveau.

## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Récupérer les métadonnées et implémenter un Service conforme](../../../../docs/framework/wcf/feature-details/how-to-retrieve-metadata-and-implement-a-compliant-service.md)
