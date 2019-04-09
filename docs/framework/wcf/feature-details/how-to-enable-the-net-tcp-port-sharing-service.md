---
title: 'Procédure : activer le service de partage de ports Net.TCP'
ms.date: 03/30/2017
helpviewer_keywords:
- port sharing [WCF]
- activation services [WCF]
ms.assetid: c9175af4-c27c-4765-bf45-b8f7528a7282
ms.openlocfilehash: 77d1d983da87b37c6267cc38a16db446782797f1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59130648"
---
# <a name="how-to-enable-the-nettcp-port-sharing-service"></a>Procédure : activer le service de partage de ports Net.TCP
Windows Communication Foundation (WCF) utilise un service Windows appelé Service de partage de Port Net.TCP pour faciliter le partage de ports TCP entre plusieurs processus. Ce service est installé en tant que partie de WCF, mais le service n’est pas activé par défaut par mesure de sécurité et par conséquent, doit être activé manuellement avant la première utilisation. Cette rubrique décrit comment configurer le service de partage de ports Net.TCP à l'aide du composant logiciel enfichable Microsoft Management Console (MMC).  
  
 Après avoir activé le Service de partage de Port Net.TCP et que vous démarrez manuellement, consultez [Comment : Configurer un Service WCF pour utiliser le partage de ports](../../../../docs/framework/wcf/feature-details/how-to-configure-a-wcf-service-to-use-port-sharing.md) pour plus d’informations sur la configuration de votre service pour utiliser ce service.  
  
 Pour obtenir un exemple qui utilise le partage de ports net.tcp://, consultez le [Net.TCP Port Sharing, exemple](../../../../docs/framework/wcf/samples/net-tcp-port-sharing-sample.md).  
  
### <a name="to-enable-the-nettcp-port-sharing-service-using-mmc"></a>Pour activer le service de partage de ports Net.TCP à l'aide de MMC  
  
1.  Dans le menu Démarrer, ouvrez la Console de gestion de Services soit en ouvrant une fenêtre d’invite de commandes et en tapant `services.msc` ou en sélectionnant exécuter et en tapant `services.msc` dans la zone Ouvrir.  
  
2.  Dans le **nom** avec le bouton droit de la colonne de la liste des services, le **Service de partage de Port Net.Tcp**, puis sélectionnez **propriétés** dans le menu.  
  
3.  Pour activer la mise en route manuelle du service, dans le **propriétés** fenêtre Sélectionnez les **général** onglet, puis, dans le **type de démarrage** zone Sélectionnez manuel, puis cliquez sur **Appliquer**.  
  
4.  Pour démarrer le service, dans la zone d’état de Service, cliquez sur le **Démarrer** bouton. L'état du service doit maintenant afficher "Démarré".  
  
5.  Pour revenir à la liste des services, cliquez sur le **OK**et quittez la Console MMC.  
  
## <a name="example"></a>Exemple  
  
## <a name="see-also"></a>Voir aussi

- [Partage de ports Net.TCP](../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md)
- [Configuration du service de partage de ports Net.TCP](../../../../docs/framework/wcf/feature-details/configuring-the-net-tcp-port-sharing-service.md)
