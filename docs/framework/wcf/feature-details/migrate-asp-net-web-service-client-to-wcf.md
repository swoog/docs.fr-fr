---
title: 'Comment : migrer le code client des services Web ASP.NET vers Windows Communication Foundation'
ms.date: 03/30/2017
ms.assetid: 2e0a22a7-e1d5-4718-8997-4319a7cd9027
ms.openlocfilehash: cb60f9cb2e8f35ee703b049eae9e3d99c1ec7d49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33491128"
---
# <a name="how-to-migrate-aspnet-web-service-client-code-to-the-windows-communication-foundation"></a>Comment : migrer le code client des services Web ASP.NET vers Windows Communication Foundation
La procédure suivante décrit les étapes générales à suivre pour migrer le code client de Service Web ASP.NET vers WCF.  
  
## <a name="procedure"></a>Procédure  
  
#### <a name="to-migrate-aspnet-web-service-client-code-to-wcf"></a>Pour migrer le code client des services Web ASP.NET vers WCF  
  
1.  Assurez-vous qu'un jeu complet de tests existe pour le client.  
  
2.  Utilisez Visual Studio 2005 pour mettre à niveau l'application cliente vers .NET 2.0. Exécutez l'ensemble des tests.  
  
3.  Supprimez le code client ASP.NET du projet client. Ce code se trouve dans les modules générés à l'aide de l'outil WSDL.exe.  
  
4.  Générer le code du client WCF à l’aide du [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md). Ajoutez ce code au projet client et fusionnez la sortie de la configuration dans le fichier de configuration existant du client.  
  
5.  Compilez l'application. Réparer les erreurs de compilation en remplaçant les références pour les types de clients anciens ASP.NET avec des références aux nouveaux types de client WCF.  
  
6.  Exécutez l'ensemble des tests.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour migrer le code d’un service web ASP.NET vers Windows Communication Foundation](../../../../docs/framework/wcf/feature-details/migrate-asp-net-web-service-to-wcf.md)
