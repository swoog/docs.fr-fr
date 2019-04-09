---
title: Applications clientes de niveau intermédiaire
ms.date: 03/30/2017
ms.assetid: f9714a64-d0ae-4a98-bca0-5d370fdbd631
ms.openlocfilehash: 667cc98f46b131fe91e17f3b1b16af429dc597ee
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59174081"
---
# <a name="middle-tier-client-applications"></a>Applications clientes de niveau intermédiaire
Cette rubrique traite des différents problèmes spécifiques aux applications clientes de niveau intermédiaire qui utilisent Windows Communication Foundation (WCF).  
  
## <a name="increasing-middle-tier-client-performance"></a>Augmenter les performances du client de niveau intermédiaire  
 Par rapport aux précédentes technologies de communication, tels que les services Web à l’aide de [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], la création d’une instance de client WCF peut être plus complexe en raison de l’ensemble complet de fonctionnalités de WCF. Par exemple, lorsqu'un objet <xref:System.ServiceModel.ChannelFactory%601> est ouvert, il peut établir une session sécurisée avec le service, procédure qui augmente le temps de démarrage pour l'instance cliente. En règle générale, ces fonctionnalités supplémentaires n’affectent pas les applications clientes considérablement dans la mesure où le client WCF effectue plusieurs appels, puis se ferme.  
  
 Les applications clientes de niveau intermédiaire, cependant, peuvent créer rapidement de nombreux objets de client WCF et, par conséquent, rencontrer des initialisations accrue nécessaires. Il existe deux approches principales pour accroître les performances des applications de niveau intermédiaire lors d'un appel des services :  
  
-   Mettre en cache l’objet de client WCF et le réutiliser pour les appels suivants lorsque cela est possible.  
  
-   Créer un <xref:System.ServiceModel.ChannelFactory%601> objet, puis utiliser cet objet pour créer des objets de canal pour chaque appel client WCF.  
  
 Les problèmes à prendre en compte lors de l'utilisation de ces approches sont les suivants :  
  
-   Si le service maintient un état spécifique au client en utilisant une session, vous ne pouvez pas réutiliser le client WCF de couche intermédiaire avec les demandes de niveau de plusieurs clients, car l’état du service est liée à celle du client de niveau intermédiaire.  
  
-   Si le service doit s’authentifier sur une base par client, vous devez créer un nouveau client pour chaque demande entrante sur la couche intermédiaire au lieu de réutiliser le client WCF de niveau intermédiaire (ou un objet de canal de client WCF), car les informations d’identification de client de la couche intermédiaire ne peut pas être modifiée une fois le client WCF (ou <xref:System.ServiceModel.ChannelFactory%601>) a été créé.  
  
-   Si les canaux et les clients créés par les canaux sont thread-safe, ils peuvent ne pas prendre en charge l'écriture simultanée de plusieurs messages sur la transmission. Si vous envoyez des messages volumineux, notamment pour la diffusion en continu, l'opération d'envoi peut bloquer l'exécution d'une autre opération d'envoi. Cette situation entraîne deux types de problèmes : un manque d'accès concurrentiel et le risque d'interblocage si le flux de contrôle retourne au service par l'intermédiaire du canal (autrement dit, le client partagé appelle un service dont le chemin d'accès au code entraîne un rappel au client partagé). Cela est vrai quel que soit le type de client WCF que vous réutiliser.  
  
-   Vous devez traiter les canaux défaillants, que vous partagiez ou non le canal. Toutefois, lorsque les canaux sont réutilisés, un canal défaillant peut faire échouer plusieurs opérations de demande ou d'envoi en attente.  
  
 Pour obtenir un exemple qui illustre les meilleures pratiques pour réutiliser un client pour plusieurs requêtes, consultez [une liaison de données dans un Client ASP.NET](../../../../docs/framework/wcf/samples/data-binding-in-an-aspnet-client.md).  
  
 De plus, vous pouvez augmenter les performances de démarrage pour les clients qui utilisent des types de données sérialisables à l'aide de <xref:System.Xml.Serialization.XmlSerializer> pour générer et compiler le code de sérialisation pour ces types de données au moment de l'exécution qui peuvent ralentir les performances de démarrage. Le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) peut améliorer les performances de démarrage de ces applications en générant le code de sérialisation nécessaires à partir des assemblys compilés pour l’application. Pour plus d'informations, voir [Procédure : Améliorer le temps de démarrage de WCF Client Applications à l’aide de XmlSerializer](../../../../docs/framework/wcf/feature-details/startup-time-of-wcf-client-applications-using-the-xmlserializer.md).  
  
## <a name="see-also"></a>Voir aussi

- [Accès aux services à l'aide d'un client WCF](../../../../docs/framework/wcf/feature-details/accessing-services-using-a-client.md)
