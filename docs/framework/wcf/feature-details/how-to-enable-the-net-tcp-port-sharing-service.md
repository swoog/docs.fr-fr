---
title: 'Comment : activer le service de partage de ports Net.TCP'
ms.date: 03/30/2017
helpviewer_keywords:
- port sharing [WCF]
- activation services [WCF]
ms.assetid: c9175af4-c27c-4765-bf45-b8f7528a7282
ms.openlocfilehash: 4b5a18e11d9fc15f23b5353883a63d838face58a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-enable-the-nettcp-port-sharing-service"></a>Comment : activer le service de partage de ports Net.TCP
Windows Communication Foundation (WCF) utilise un service Windows appelé le Service de partage de ports Net.TCP pour faciliter le partage de ports TCP entre plusieurs processus. Ce service est installé en tant que partie de WCF, mais le service n’est pas activé par défaut pour des raisons de sécurité et par conséquent, doit être activé manuellement avant la première utilisation. Cette rubrique décrit comment configurer le service de partage de ports Net.TCP à l'aide du composant logiciel enfichable Microsoft Management Console (MMC).  
  
 Après avoir activé le Service de partage de ports Net.TCP et que vous démarrez manuellement, consultez [Comment : configurer un Service WCF à utiliser le partage de Port](../../../../docs/framework/wcf/feature-details/how-to-configure-a-wcf-service-to-use-port-sharing.md) pour plus d’informations sur la façon de configurer votre service pour utiliser ce service.  
  
 Pour voir un exemple qui utilise le partage de ports net.tcp://, le [Net.TCP Port Sharing, exemple](../../../../docs/framework/wcf/samples/net-tcp-port-sharing-sample.md).  
  
### <a name="to-enable-the-nettcp-port-sharing-service-using-mmc"></a>Pour activer le service de partage de ports Net.TCP à l'aide de MMC  
  
1.  Dans le menu Démarrer, ouvrez la Console de gestion de Services soit en ouvrant une fenêtre d’invite de commandes et en tapant `services.msc` ou en sélectionnant exécuter et en tapant `services.msc` dans la zone Ouvrir.  
  
2.  Dans le **nom** avec le bouton droit de la colonne de la liste des services, le **Service de partage de Port Net.Tcp**, puis sélectionnez **propriétés** à partir du menu.  
  
3.  Pour permettre le démarrage manuel du service, dans le **propriétés** fenêtre Sélectionner le **général** onglet et dans le **type de démarrage** zone Sélectionnez manuel, puis cliquez sur **Appliquer**.  
  
4.  Pour démarrer le service, dans la zone d’état de Service, cliquez sur le **Démarrer** bouton. L'état du service doit maintenant afficher "Démarré".  
  
5.  Pour revenir à la liste des services, cliquez sur le **OK**, quittez la Console MMC.  
  
## <a name="example"></a>Exemple  
  
## <a name="see-also"></a>Voir aussi  
 [Partage de ports Net.TCP](../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md)  
 [Configuration du service de partage de ports Net.TCP](../../../../docs/framework/wcf/feature-details/configuring-the-net-tcp-port-sharing-service.md)
