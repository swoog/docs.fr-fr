---
title: Sécurité de l'intégration du CLR dans SQL Server
ms.date: 03/30/2017
ms.assetid: 489fe096-fd1d-42de-8438-bf7aed46aea2
ms.openlocfilehash: 8df8a19850e9cce28b1f09e80908dafb8bfedaf6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361000"
---
# <a name="clr-integration-security-in-sql-server"></a>Sécurité de l'intégration du CLR dans SQL Server
Microsoft SQL Server introduit le composant Common Language Runtime (CLR) du .NET Framework. L'intégration du CLR vous permet d'écrire des procédures stockées, des déclencheurs, des types définis par l'utilisateur, des fonctions définies par l'utilisateur, des agrégats définis par l'utilisateur et des fonctions de flux évaluées par une table, en utilisant tout langage .NET Framework, tel que Microsoft Visual Basic .NET ou Microsoft Visual C#.  
  
 Le CLR prend en charge un modèle de sécurité appelé sécurité d'accès du code (CAS) pour le code managé. Dans ce modèle, les autorisations sont accordées aux assemblys en fonction de la preuve fournie par le code dans les métadonnées. SQL Server intègre le modèle de sécurité de SQL Server, basé sur l'utilisateur avec le modèle de sécurité du CLR, basé sur l'accès du code.  
  
## <a name="external-resources"></a>Ressources externes  
 Pour plus d'informations sur l'intégration du CLR avec SQL Server, voir les ressources répertoriées ci-dessous.  
  
|Ressource|Description|  
|--------------|-----------------|  
|[Sécurité d’accès du code](http://msdn.microsoft.com/library/23a20143-241d-4fe5-9d9f-3933fd594c03)|Contient des rubriques qui décrivent la sécurité d'accès du code dans le .NET Framework.|  
|[Sécurité d’intégration du CLR](http://go.microsoft.com/fwlink/?LinkId=59998)|Présente le modèle de sécurité pour le code managé qui s'exécute au sein de SQL Server.|  
  
## <a name="see-also"></a>Voir aussi  
 [Sécurisation des applications ADO.NET](../../../../../docs/framework/data/adonet/securing-ado-net-applications.md)  
 [Scénarios de sécurité des applications dans SQL Server](../../../../../docs/framework/data/adonet/sql/application-security-scenarios-in-sql-server.md)  
 [Intégration CLR SQL Server](../../../../../docs/framework/data/adonet/sql/sql-server-common-language-runtime-integration.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](http://go.microsoft.com/fwlink/?LinkId=217917)
